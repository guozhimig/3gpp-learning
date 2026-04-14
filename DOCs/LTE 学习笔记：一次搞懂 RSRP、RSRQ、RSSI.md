在 LTE 中，终端（UE）做小区重选和切换时，最核心的无线测量量就是 `RSRP` 和 `RSRQ`。这篇笔记按“先理解，再会用”的顺序，带你把 `RSRP`、`RSRQ`、`RSSI` 一次理顺，并避免常见误区。

---

## 1. 先建立整体认知

你可以先把三个量理解成三种不同视角：

- `RSRP`：看“有用信号强不强”（覆盖视角）。
- `RSRQ`：看“有用信号在当前干扰环境下质量如何”（质量视角）。
- `RSSI`：看“总接收功率背景有多高”（环境视角，包含干扰与噪声）。

一句话记忆：**RSRP 偏覆盖，RSRQ 偏质量，RSSI 是背景。**

---

## 2. 三个量的定义与关系

### 2.1 RSRP 是什么

`RSRP`（Reference Signal Received Power）是：  
在测量带宽内，对承载小区参考信号（CRS）的资源元素（RE）功率做线性平均（结果常以 dBm 表示）。

所以它不是“整带宽总功率”，而是“参考信号 RE 的平均功率”。

图组（同一主题）：PRB、RE 与 Cell-RS 的对应关系（含多天线下 DTX 分布）  
<div style="display:flex; gap:12px; align-items:flex-start; flex-wrap:wrap;">
  <div style="flex:1; min-width:280px;">
    <img src="images/CableFree-LTE-RS-RE-Distribution.png" alt="图1 PRB与RE网格中Cell-RS的位置及多天线下DTX交织分布" style="width:100%; max-width:420px; height:auto;" />
    <p>图1 PRB 与 RE 网格中 Cell-RS 的位置及多天线下 DTX 交织分布</p>
  </div>
  <div style="flex:1; min-width:280px;">
    <img src="images/CableFree-LTE-OFDMA-Channel-RSRP.png" alt="图2 从OFDMA信道估计视角补充展示PRB和RE上的Cell-RS采样位置" style="width:100%; max-width:420px; height:auto;" />
    <p>图2 从 OFDMA 信道估计视角补充展示 PRB/RE 上的 Cell-RS 采样位置</p>
  </div>
</div>

### 2.2 RSRQ 是什么

`RSRQ`（Reference Signal Received Quality）定义为：

`RSRQ = N * RSRP / RSSI`

其中 `N` 是 RSSI 测量带宽内的 RB 数。  
关键点是：**分子与分母必须在同一测量带宽、同一 RB 集上得到**。

### 2.3 RSSI 是什么

`RSSI`（Received Signal Strength Indicator）是总接收功率统计量，包含服务小区功率、其他小区干扰以及热噪声等（按规范规定的符号和带宽条件统计）。

---

## 3. 为什么切换/重选要同时看 RSRP 和 RSRQ

只看 `RSRP`，可以判断覆盖是否足够；但当干扰升高时，`RSRP` 可能还可以，业务质量却已经变差。  
这时 `RSRQ` 能补上“质量信息”，帮助识别“信号不弱但质量差”的场景。

工程上常见思路：

- 用 `RSRP` 做候选小区强度排序；
- 用 `RSRQ` 作为质量补充判据；
- 最终由 RRC 事件参数（如 A3/A5）控制上报与触发。

图3 切换中覆盖与质量的分工（示意）  
![[images/CableFree-LTE_Network_little.png]]

---

## 4. 公式怎么学才不容易混乱

在理想化前提下（高 SNR、满负载、功率分布均匀），常见近似关系为：

`RSRP(dBm) ~= RSSI(dBm) - 10*log10(12*N)`

这个式子适合建立“量级直觉”，但不要机械套用到所有场景。  
一旦进入参数设计或问题定位，应优先依据规范定义和实测数据。

另外，单位一定要分清：

- `RSRP`、`RSSI` 常用 `dBm`（绝对功率）；
- `RSRQ` 常用 `dB`（比值）。

---

## 5. 学习中最常见的 5 个误区

1. **把 RSRP 当成整带宽总功率**  
   纠正：RSRP 是参考信号 RE 平均功率，不是全带宽总功率。

2. **把经验阈值当成规范阈值**  
   纠正：网页中的固定门限常是经验值，不是通用 3GPP 硬门限。

3. **把特定推导结果泛化到所有场景**  
   纠正：许多结论依赖前提（负载、天线、功率分配等），前提变了结论也会变。

4. **忽略“同一 RB 集测量”约束**  
   纠正：`RSRQ = N*RSRP/RSSI` 的前提是同一测量集合。

5. **把天线影响当成唯一因果**  
   纠正：天线配置会影响统计结果，但定义本身仍是 `N*RSRP/RSSI`。

图4 RSRQ 报告范围示意（辅助记忆）  
![[images/CableFree-LTE-RSRQ-reporting-range.png]]

---

## 6. 继续深入时的规范阅读顺序

如果你下一步要进入更严谨的网优或参数配置，建议按下面顺序看规范：

- `TS 36.214`：测量定义与口径（RSRP/RSRQ/RSSI 的核心出处）。
- `TS 36.133`：上报范围、精度、性能要求。
- `TS 36.331`：测量配置、触发事件（A1~A5）、上报机制。
- `TS 36.211`：CRS 与物理资源映射细节。

---

## 7. 复习速记

- `RSRP`：有用信号强度（覆盖）。
- `RSRQ`：有用信号质量（受干扰和噪声影响）。
- `RSSI`：总功率背景。
- 切换实践：先看 `RSRP`，再用 `RSRQ` 修正判断。
- 工程落地：经验值可参考，规范和实测才是最终依据。

---

## 图片来源

- https://www.cablefree.net/wirelesstechnology/4glte/rsrp-rsrq-measurement-lte/
- https://arimas.com/2016/04/04/78-rsrp-and-rsrq-measurement-in-lte/

