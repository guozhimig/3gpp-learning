# 3GPP Learning Project

## 项目概述

本项目旨在为通信领域工作者提供3GPP 36系列（LTE）和38系列（5G NR）无线通信协议的完整学习资源和技术参考。

## 当前实现版本

- **LTE实现**: Release 12 (R12) 系列
- **5G NR实现**: Release 17 (R17) 系列，支持RedC<mark style="background: #FF5582A6;">ap技术</mark>

## 项目结构

```
3GPP learning/
├── 3GPP_无线通信协议_参考手册.mdc    # 主要参考手册
├── DOCs/                           # 文档库
│   ├── 3GPP_R12/                   # LTE R12文档索引
│   │   └── LTE_R12_文档索引.md
│   ├── 3GPP_R17/                   # 5G NR R17文档索引
│   │   └── NR_R17_文档索引.md
│   └── README.md                   # 文档库总览
├── .gitignore                      # Git忽略文件
└── README.md                       # 项目说明
```

## 主要特性

### 📚 完整的协议文档索引
- **LTE R12**: 113个TS文档的完整索引
- **5G NR R17**: 125个TS文档的完整索引
- **RedCap支持**: 完整的R17 RedCap技术文档

### 🔗 Cursor Docs集成
- 自动索引3GPP官方FTP文档
- 实时访问最新Release版本
- 支持精准的协议条款引用

### 📖 学习资源
- 详细的技术概念说明
- 协议栈层次结构图
- 关键术语对照表
- 学习路径建议

## 快速开始

### 1. 克隆项目
```bash
git clone https://github.com/your-username/3gpp-learning.git
cd 3gpp-learning
```

### 2. 使用Cursor Docs
1. 在Cursor中打开项目
2. 进入Settings > Indexing & Docs
3. 添加以下文档源：
   - LTE R12: `https://www.3gpp.org/ftp/Specs/latest/Rel-12/36_series/`
   - 5G NR R17: `https://www.3gpp.org/ftp/Specs/latest/Rel-17/38_series/`

### 3. 开始学习
- 阅读 `3GPP_无线通信协议_参考手册.mdc`
- 查看 `DOCs/` 目录下的详细文档索引
- 使用Cursor的AI助手进行技术讨论

## 技术优势

### 🚀 高效学习
- 结构化的学习路径
- 完整的技术对比
- 实时更新的官方文档

### 🎯 精准引用
- 准确的协议条款引用
- 详细的技术参数说明
- 完整的实现要求

### 🔄 持续更新
- 跟随3GPP Release演进
- 自动同步最新文档
- 支持新特性学习

## 贡献指南

欢迎提交Issue和Pull Request来改进这个项目：

1. Fork本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建Pull Request

## 许可证

本项目采用MIT许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 联系方式

- 项目链接: [https://github.com/your-username/3gpp-learning](https://github.com/your-username/3gpp-learning)
- 问题反馈: [Issues](https://github.com/your-username/3gpp-learning/issues)

---

*本项目旨在促进3GPP无线通信协议的学习和技术交流*
