# 新能源课程报告

## 项目简介

本项目为《新能源取代化石燃料成为能源主流的时间进程与条件分析》课程报告的 LaTeX 源代码及编译文件。

## 报告主题

分析在全球减排目标和能源转型背景下，新能源（风电、光伏等）何时以及在何种条件下能够取代化石燃料成为能源主流。报告基于 IEA、IRENA 等权威机构的公开数据，从电力结构、成本变化、装机规模等多个维度进行系统分析。

## 项目结构

```
.
├── src/
│   └── single-file/
│       ├── complete-document.tex    # LaTeX 源文件
│       ├── complete-document.pdf    # 编译生成的 PDF
│       └── *.aux, *.log, *.fls...  # LaTeX 编译辅助文件
├── README.md                        # 项目说明文档
└── .gitignore                       # Git 忽略文件配置
```

## 报告内容概要

### 主要章节

1. **全球能源结构与能源主流格局现状**
   - 能源主流格局的基本界定
   - 全球电力结构中新能源与化石能源占比变化
   - 不同能源形态下"主流地位"的差异

2. **新能源替代化石能源的客观驱动因素**
   - 新能源发电成本变化趋势（LCOE 分析）
   - 新能源装机规模与发电量增长特征
   - 技术进步与产业规模效应对能源结构的影响

3. **新能源取代化石能源的时间进程分析**
   - 不同能源领域中新能源替代节奏的差异
   - 国际机构能源转型情景下的时间尺度判断
   - 新能源成为能源主流的阶段性特征分析

4. **新能源成为能源主流面临的主要约束条件**
   - 能源系统运行与消纳能力约束
   - 区域资源禀赋与基础设施差异
   - 能源转型过程中面临的不确定性因素

5. **结论**

### 数据可视化

报告包含多个数据图表：
- 全球电力结构变化趋势（2000-2024）
- 新能源发电成本（LCOE）变化趋势（2010-2024）
- 全球可再生能源新增装机容量变化
- 不同地区新能源发电成本结构对比

## 编译说明

### 环境要求

- LaTeX 发行版：TeX Live 或 MiKTeX
- 编译引擎：XeLaTeX 或 pdfLaTeX
- 必需宏包：ctex, geometry, tikz, pgfplots, booktabs, bicaption 等

### 编译命令

```bash
cd src/single-file
xelatex complete-document.tex
xelatex complete-document.tex  # 二次编译以生成正确的交叉引用
```

或使用 latexmk 自动编译：

```bash
latexmk -xelatex complete-document.tex
```

## 作者信息

- 作者：刘培宽
- 单位：上海工程技术大学 电子电气工程学院

## 参考文献

报告主要参考以下权威机构的数据和报告：
- IEA (International Energy Agency) - World Energy Outlook 2024
- IRENA (International Renewable Energy Agency) - Renewable Power Generation Costs in 2024
- Energy Institute - Statistical Review of World Energy 2025
- Ember - Global Electricity Review

## 许可证

本项目仅用于学术交流和课程作业，未经授权不得用于商业用途。
