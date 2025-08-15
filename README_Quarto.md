# R语言基础教程 - Quarto版本

## 概述

本项目已将原有的R Markdown (Rmd) 幻灯片转换为 Quarto (Qmd) 格式。

## 文件说明

- `R-fundamentals.qmd` - 转换后的Quarto演示文稿
- `R-fundamentals.Rmd` - 原始的R Markdown文件（保留作为参考）
- `resources/` - 图片和资源文件夹
- `zh-CN.css` 和 `customize.css` - 样式文件

## 主要转换内容

### YAML头部更改
- 从 `xaringan::moon_reader` 改为 `revealjs` 格式
- 添加了Quarto特有的配置选项，如幻灯片编号、黑板功能等
- 保持了原有的CSS样式文件引用

### 语法转换
- 将xaringan的类选择器（如 `class: inverse, center, middle`）转换为Quarto的类语法（如 `{.inverse .center .middle}`）
- 将 `--` 分隔符改为 `. . .` 用于渐进显示
- 更新了代码块选项语法（从 `{r option=value}` 改为 `#| option: value`）
- 将图片语法从HTML格式改为Markdown格式
- 使用 `::: {.columns}` 和 `::: {.column}` 替代 `.pull-left` 和 `.pull-right`

### 功能增强
- 添加了幻灯片导航功能
- 启用了代码行号显示
- 添加了预览链接功能
- 集成了黑板功能用于演示

## 如何使用

### 前提条件
确保已安装：
- R (>= 4.0.0)
- Quarto CLI
- 必要的R包：tidyverse, leaflet, DT等

### 渲染幻灯片
```bash
quarto render R-fundamentals.qmd
```

或在RStudio中打开qmd文件并点击"Render"按钮。

### 预览幻灯片
```bash
quarto preview R-fundamentals.qmd
```

## 主要特性

- **响应式设计**：适配不同屏幕尺寸
- **交互式元素**：支持代码执行和图表显示
- **现代化界面**：使用Reveal.js提供流畅的演示体验
- **多格式输出**：可导出为HTML、PDF等多种格式
- **中文支持**：保持了原有的中文字体和样式

## 注意事项

1. 确保所有资源文件（图片、CSS等）的路径正确
2. 某些xaringan特有的功能可能需要手动调整
3. 建议在渲染前检查所有代码块是否正常运行

## 技术支持

如有问题，请参考：
- [Quarto官方文档](https://quarto.org/)
- [Quarto演示文稿指南](https://quarto.org/docs/presentations/)