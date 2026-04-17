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

PRB、RE 与 Cell-RS 的对应关系（含多天线下 DTX 分布）

<div style="display:flex; gap:2px; align-items:flex-start; flex-wrap:wrap;">
  <div style="flex:1; min-width:280px;">
    <img src="images/CableFree-LTE-RS-RE-Distribution.png"  style="width:100%; max-width:620px; height:auto;" />    
  </div>
  <div style="flex:1; min-width:280px;">
    <img src="images/CableFree-LTE-OFDMA-Channel-RSRP.png"  style="width:100%; max-width:620px; height:auto;" />   
  </div>
</div>


### 2.2 RSRQ 是什么

`RSRQ`（Reference Signal Received Quality）定义为：

`RSRQ = N * RSRP / RSSI = RSRP / (RSSI/N)`

其中 `N` 是 RSSI 测量带宽内的 RB 数。`RSSI/N` 可以理解为“每个 RB 的平均总接收功率”，所以 `RSRQ = RSRP/(RSSI/N)` 的写法更利于直觉理解。  
关键点是：**分子与分母必须在同一测量带宽、同一 RB 集上得到**。

为什么定义成 `N*RSRP/RSSI`，而不是 `(12*N)*RSRP/RSSI`？

- 这个指标的目标是“工程可用”，不是做最细粒度 RE 物理对齐；
- `N`（RB 数）对应带宽与调度尺度，跨场景更稳定、可比较性更好；
- 若强行引入 `12` 去做 RE 级归一化，会更依赖 RE 级细节（端口映射、参考信号位置、DTX 等），工程上反而不够稳；
- LTE 调度最小单位是 PRB，因此按 PRB 维度归一化更符合网优和移动性决策使用方式。

你在规范映射表里的观察非常重要：`RSRQ` 的上报上限可到 `-3 dB`，明显高于很多资料常提到的 `-10.8 dB`。  
这两者并不矛盾，原因是它们对应的场景不同：

- `-10.8 dB`（即 `10*log10(1/12)`）来自一种常见简化模型：把系统近似成“满载、等功率分布”时得到的参考点；
- 规范上报上限到 `-3 dB` 反映的是更一般的可测场景（例如低负载、低干扰时，分母 `RSSI` 下降，`RSRQ` 可更接近 0 dB）；
- 因此，`-10.8 dB` 更适合作为“典型满载直觉值”，而 `-3 dB` 才是规范映射层面的上边界。

>[!tips] 工程直觉小结（便于记忆）：
>  `RSRP` 更像“我离基站有多近”（覆盖/强度）；
   `RSRQ` 更像“这条路有多堵”（质量，受负载与干扰共同影响）。
   当 `RSRP` 很好（例如 `-70 dBm`）但 `RSRQ` 很差（例如 `-15 dB`）时，常见含义是：覆盖没问题，但质量环境较差（可能小区较忙或干扰较高），因此实际速率未必高。
>>[!note] 补充边界：
>> `RSRQ` 不是纯“负载指标”，它反映的是参考信号相对总背景功率（含负载相关发射、干扰、噪声）的质量；
>> `RSRP` 与距离强相关，但也会受天线方向、遮挡、频段和站点参数影响。
>
>>[!example] 典型场景下的计算:
>>1. 单天线下，一个PRB上所有的RE都在传输数据，而且每个 RE 上的功率都相同: `RSRQ = N/12N = -10.8db`
>>2. 双天线下，继承1的假设，CRS 不会叠加，其他的RE能量会叠加，于是就是 `(12 - 4) * 2 = 16` 个 RE 的能量，然后叠加 4个cell-rs的能量，总共就是20个RE能量的总和. `RSRQ = N/20N = -13db`
>>3. 完全空载的情况下，单天线就是 `RSRQ = N / 2N = -3db`
>>4. 完全空载的情况下，双天线就是 `RSRQ = N / 4N = -6db`
### 2.3 RSSI 是什么

`RSSI`（Received Signal Strength Indicator）是总接收功率统计量，包含服务小区功率、其他小区干扰以及热噪声等（按规范规定的符号和带宽条件统计）。

统计口径上，`RSSI` 不是“一个 slot（0.5ms）里所有 RE 的简单总和”，也不是只取某一个 symbol。  
根据 `36.214`，`RSSI` 的统计口径是“默认规则 + 高层可配置规则”：

| 场景 | RSSI 统计符号范围 |
|---|---|
| 默认（未被高层特别指示） | 仅统计包含参考信号（antenna port 0 RS）的 OFDM symbols |
| 高层指示 `all OFDM symbols for performing RSRQ measurements` | 统计测量子帧下行部分的所有 OFDM symbols |
| 高层指示特定子帧/发现信号测量场景 | 按指示的子帧或 discovery signal occasions 统计对应下行 OFDM symbols |

无论采用哪种符号范围，`RSSI` 的统计逻辑都是：
- 在每个被选中的 OFDM symbol 上，先对测量带宽内（`N` 个 PRB）的接收功率做总和；
- 再在这些被选中的 OFDM symbols 维度上做线性平均。

速记一句话：`RSSI` 是“PRB 维度求和 + symbol 维度线性平均”，且 symbol 选择可由高层配置改变。

常见直觉表达可以写成：

`RSSI = wideband power = noise + serving cell power + interference power`

这个表达用于理解 RSSI 的组成是正确的。  
`RSSI` 是总接收功率，包括有用信号（RSRP）、噪声（noise）和干扰（interference）；所以如果没有噪声和干扰，而且整个带宽都在传输数据，`RSSI` 和 `RSRP` 的关系可近似写为：`RSSI ~= 12*N*RSRP`。

可把它理解为两种统计视角：
- `RSRP` 更像“点状统计”（单个参考信号 RE 的平均功率）；
- `RSSI` 更像“面状统计”（测量带宽内相关 RE 的总功率）。

其中 `N` 为测量带宽内的 PRB 数。  
注意：这不是所有场景都严格成立的恒等式，真实网络中会受负载、端口配置、功率分配与干扰环境影响。

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

## 4. SINR 与 RSRP/RSRQ 的关系（补充）

`SINR`（Signal to Interference plus Noise Ratio）可写为：

`SINR = S / (I + N)`

其中 `S` 是有用信号功率，`I` 是干扰功率，`N` 是噪声功率。

学习时可这样区分：

- `RSRP` 更偏“信号强度”；
- `RSRQ` 更偏“信号质量（参考信号相对总背景功率）”；
- `SINR` 更直接反映“当前链路可解调条件”，与吞吐和调制编码阶数关系更紧密。

三者关系可直觉化理解为：

- `RSRP` 高，不代表 `SINR` 一定高（可能干扰也高）；
- `RSRP` 高但 `RSRQ` 差时，`SINR` 往往也不理想；
- `RSRQ` 常被当作工程上的“质量代理量”，但它不等于严格意义的 `SINR`。

> [!note] 口径提醒
> `RSRP/RSRQ` 的定义与上报在 3GPP 中有明确测量口径；`SINR` 更常用于链路性能分析与仿真。三者相关但不可直接互相替代。

---

## 5. SNR 是什么（以及与 RSRP 的关系）

`SNR`（Signal to Noise Ratio）定义为：

`SNR = S / N`

其中 `S` 是有用信号功率，`N` 是噪声功率。与 `SINR` 不同，`SNR` 不包含外部干扰项 `I`。

在原网页里常见一句：“under full load and high SNR”。这里 `high SNR` 是**前提条件**，不是公式变量。  
它的作用是说明：当噪声影响较小、系统接近理想化时，下面这个近似更容易成立：

`RSRP(dBm) ~= RSSI(dBm) - 10*log10(12*N)`

>[!tips] 工程直觉小结（便于记忆）：
> `SNR` 更像“底噪有多干净”；
> `SINR` 更像“底噪 + 外部干扰合起来有多干净”。
> 所以同样 `RSRP` 下，`SNR` 好不代表 `SINR` 一定好（可能干扰很高）。

>>[!note] 补充边界：
>> `high SNR` 只是该近似式的适用背景，不是协议里的固定门限；
>> 真实网络还会受负载、干扰、端口配置和调度行为影响，不能只靠单一近似式判断链路质量。

>>[!example] 典型理解方式：
>>1. 当噪声和干扰都较低时，`RSRP` 与体验通常同向变好，近似式更有参考价值。
>>2. 当噪声低但干扰高时，`SNR` 可能不差，但 `SINR/RSRQ` 依然可能很差，速率不一定高。
>>3. 当噪声本身较高时（低 `SNR`），近似式误差通常增大，应优先看实测与全量指标。

---

## 6. 公式怎么学才不容易混乱

在理想化前提下（高 SNR、满负载、功率分布均匀），常见近似关系为：

`RSRP(dBm) ~= RSSI(dBm) - 10*log10(12*N)`

这个式子适合建立“量级直觉”，但不要机械套用到所有场景。  
一旦进入参数设计或问题定位，应优先依据规范定义和实测数据。

另外，单位一定要分清：

- `RSRP`、`RSSI` 常用 `dBm`（绝对功率）；
- `RSRQ` 常用 `dB`（比值）。

---

## 7. 学习中最常见的 5 个误区

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

## 8. 继续深入时的规范阅读顺序

如果你下一步要进入更严谨的网优或参数配置，建议按下面顺序看规范：

- `TS 36.214`：测量定义与口径（RSRP/RSRQ/RSSI 的核心出处）。
- `TS 36.133`：上报范围、精度、性能要求。
- `TS 36.331`：测量配置、触发事件（A1~A5）、上报机制。
- `TS 36.211`：CRS 与物理资源映射细节。

---

## 9. 复习速记

- `RSRP`：有用信号强度（覆盖）。
- `RSRQ`：有用信号质量（受干扰和噪声影响）。
- `RSSI`：总功率背景。
- 切换实践：先看 `RSRP`，再用 `RSRQ` 修正判断。
- 工程落地：经验值可参考，规范和实测才是最终依据。

---

## 图片来源

- https://www.cablefree.net/wirelesstechnology/4glte/rsrp-rsrq-measurement-lte/
- https://arimas.com/2016/04/04/78-rsrp-and-rsrq-measurement-in-lte/

