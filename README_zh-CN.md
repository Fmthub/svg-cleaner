# SVG Cleaner - Web 端 SVG 批量修复与优化终极方案

[![Next.js](https://img.shields.io/badge/Next.js-16.1.1-black)](https://nextjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38bdf8)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/license-MIT-green)]()

[🇺🇸 English](./README.md) | [🇨🇳 简体中文](./README_zh-CN.md)

**SVG Cleaner** (by FMThub) 是 Web 开发工作流中缺失的一环。它连接了设计工具（Figma, Sketch）与前端实现（Iconfont, React 组件），解决了设计师导出的 SVG 在开发中常常遇到的“显示异常”、“无法变色”、“Iconfont 上传报错”等痛点。

---

## 🌟 为什么需要 SVG Cleaner?

### 痛点 (The Problem)

- **Figma/Sketch 导出问题**: 设计工具导出的 SVG 往往包含复杂的 `<defs>`, `clip-path` 和 `stroke` 属性，直接用于 Web 开发时经常出错。
- **Iconfont 上传失败**: 将带有描边（stroke）的 SVG 上传到 Iconfont 经常会失败，或者图标变成纯黑、不可见。
- **代码冗余**: 标准 SVG 充满了元数据和冗余代码，导致体积肿胀。

### 解决方案 (The Solution)

**SVG Cleaner** 不仅仅是一个压缩工具，它是一个**结构修复器**：

1.  **描边转填充 (Stroke to Fill)**: 自动将描边转换为填充，合并为单一路径。
2.  **结构清理 (Structure Clean)**: 扁平化分组，移除不可见元素，统一路径数据。
3.  **SVGO 优化 (Optimize)**: 内置 SVGO，在不损失画质的前提下极限压缩体积。

> "上传 Iconfont 或用于 React/Vue 组件前的完美预处理工具。"

---

## ⚔️ 竞品对比

| 功能特性          | **SVG Cleaner (本项目)** | **SVGOMG / SVGO** | **Iconfont** | **Figma / Sketch** |
| :---------------- | :----------------------: | :---------------: | :----------: | :----------------: |
| **描边转填充**    |     ✅ **完美支持**      |     ❌ 不支持     |  ❌ 不支持   |    ❌ 部分支持     |
| **体积优化**      |       ✅ **支持**        |    ✅ **支持**    |  ❌ 不支持   |     ❌ 不支持      |
| **批量处理**      |       ✅ **支持**        |    ❌ 仅单文件    |  ❌ 需手动   |     ✅ 仅导出      |
| **视觉结构修复**  |       ✅ **支持**        |     ❌ 不支持     |  ❌ 不支持   |     ❌ 不支持      |
| **Iconfont 兼容** |     ✅ **100% 就绪**     |      ⚠️ 未必      | ⚠️ 经常失败  |    ⚠️ 经常失败     |

- **vs SVGOMG**: SVGOMG 是极好的压缩工具，但它保留了原始结构（如 stroke）。如果你的目标是修复图标结构以用于 Icon Font 或 CSS 样式，SVGOMG 是不够的。
- **vs Iconfont**: Iconfont 是托管服务，不是修复工具。它拒绝无效的 SVG。**SVG Cleaner** 将您的 SVG 预处理为 Iconfont 完美接受的格式。
- **vs Figma**: Figma 导出的是你绘制的内容。**SVG Cleaner** 将你绘制的内容转换为浏览器/代码实际需要的格式。

---

## ✨ 核心功能

- **🎨 智能修复 (Intelligent Fix)**:
  - 自动识别混合颜色和描边。
  - 将 `stroke`（描边）转换为 `fill`（填充/轮廓），同时保留视觉保真度。
  - 处理通常会破坏其他工具的复杂形状。
- **🚀 深度优化 (Deep Optimization)**:
  - 内置 **SVGO** 集成。
  - 多重扫描压缩，精度控制，移除元数据。
- **🌈 色彩还原 (Color Reconstruction)**:
  - 在修复过程中保留原始颜色、透明度和填充规则。
- **👁️ 实时预览 (Real-time Preview)**:
  - 即时前后对比。
  - 在深色/浅色/网格背景下检查图标细节。
- **📦 批量处理 (Batch Processing)**:
  - 拖拽上传多个文件。
  - 一键下载修复后的 ZIP 包。

---

## 🤝 反馈与支持

虽然我们已经努力处理各种复杂的 SVG case，但仍可能存在部分边缘情况（如极复杂的路径嵌套或特殊的遮罩）。

如果您遇到**无法修复**或**修复后显示异常**的 SVG 文件，欢迎提交 Issue：

1.  访问 [GitHub Issues](https://github.com/fmthub/svg-cleaner/issues)
2.  创建一个新 Issue
3.  **请务必附上原始的 SVG 文件**（或代码）以及修复后的截图/描述

我们会尽快分析并优化核心算法。

---
