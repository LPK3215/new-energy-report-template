# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个 LaTeX 学术报告项目，主题为"新能源取代化石燃料成为能源主流的时间进程与条件分析"。文档采用中英文双语格式，包含图表、表格和参考文献。

## 编译命令

### 主要编译方式

```bash
cd src/single-file
latexmk -pdf complete-document.tex
```

### 手动编译（如果需要）

```bash
cd src/single-file
pdflatex complete-document.tex
pdflatex complete-document.tex  # 第二次编译以更新交叉引用
```

### 清理辅助文件

```bash
cd src/single-file
latexmk -c  # 清理辅助文件但保留 PDF
latexmk -C  # 清理所有生成文件包括 PDF
```

## 文档结构

### 文档类与布局
- 使用 `ctexart` 文档类，支持中文排版
- 双栏布局 (`twocolumn`)，A4 纸张，10pt 字号
- 页边距：上下左右均为 2.5cm，栏间距 2em
- 无页眉页脚 (`\pagestyle{empty}`)

### 通栏区域
文档开头使用 `\twocolumn[...]` 环境创建通栏区域，包含：
- 中文标题、作者、单位
- 中文摘要和关键词
- 英文标题、作者、单位
- 英文摘要和关键词
- 分隔线

### 正文章节结构
1. 全球能源结构与能源主流格局现状
2. 新能源替代化石能源的客观驱动因素
3. 新能源取代化石能源的时间进程分析
4. 新能源成为能源主流面临的主要约束条件
5. 结论
6. 参考文献

### 图表系统
- 使用 `tikz` 和 `pgfplots` 绘制数据图表
- 使用 `bicaption` 包实现中英文双语图表标题
- 图表编号格式：图 1 / Fig. 1，表 1 / Table 1
- 所有图表数据均为实际统计数据（来源：IEA、IRENA、Ember 等）

## 关键 LaTeX 包

- **中文支持**: `ctexart` 文档类
- **字体**: `times`, `mathptmx` (Times New Roman 风格)
- **数学**: `amsmath`, `amsfonts`, `amssymb`, `bm`
- **图形**: `graphicx`, `tikz`, `pgfplots`
- **表格**: `booktabs`, `multirow`
- **标题**: `titlesec` (自定义章节格式), `caption`, `bicaption`
- **布局**: `geometry`, `stfloats` (双栏底部浮动)
- **缩进**: `indentfirst` (强制首段缩进)

## 字体要求

文档依赖 Windows 中文字体：
- 微软雅黑 (msyh.ttc)
- 仿宋 (simfang.ttf)
- 黑体 (simhei.ttf)
- 宋体 (simsun.ttc)

在非 Windows 系统上编译可能需要安装相应字体或修改字体配置。

## 修改建议

### 添加新章节
在正文区域按照现有格式添加 `\section{}` 和 `\subsection{}`。

### 添加图表
- 图表使用 `figure` 或 `table` 环境
- 使用 `\bicaption{中文标题}{English Title}` 设置双语标题
- 使用 `\label{fig:xxx}` 或 `\label{tab:xxx}` 设置引用标签

### 修改页面布局
在文档开头的 `\geometry{}` 命令中调整页边距和其他布局参数。
