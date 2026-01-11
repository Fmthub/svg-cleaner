# SVG Cleaner - Ultimate SVG Cleaner & Optimizer for Web

[![Next.js](https://img.shields.io/badge/Next.js-16.1.1-black)](https://nextjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38bdf8)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/license-MIT-green)]()

[🇺🇸 English](./README.md) | [🇨🇳 简体中文](./README_zh-CN.md)

**SVG Cleaner** (by FMThub) is the missing link in your web development workflow. It bridges the gap between design tools (Figma, Sketch, Illustrator) and development implementation (Iconfont, React Components, Web Fonts).

It solves common pain points like "display errors," "unable to change color," and "Iconfont upload failures" often caused by dirty SVG exports.

---

## 🌟 Why SVG Cleaner?

### The Problem

- **Figma/Sketch Exports**: Design tools often export "dirty" SVGs with complex `<defs>`, `clip-path`, and `stroke` attributes that break in web usage.
- **Iconfont Rejection**: Uploading SVGs with strokes to Iconfont often fails or results in invisible icons.
- **Messy Code**: Standard SVGs are full of metadata and redundancy, bloating your bundle size.

### The Solution

**SVG Cleaner** is not just a compressor. It is a **structure fixer**:

1.  **Stroke to Fill**: Automatically converts strokes to fills path-by-path.
2.  **Structure Clean**: Flattens groups, removes hidden elements, and unifies paths.
3.  **SVGO Optimization**: Compresses file size without losing visual quality.

> "The perfect pre-processor before uploading to Iconfont or using in React/Vue."

---

## ⚔️ Comparison

| Feature                    | **SVG Cleaner (This Tool)** | **SVGOMG / SVGO** |  **Iconfont**  | **Figma / Sketch** |
| :------------------------- | :-------------------------: | :---------------: | :------------: | :----------------: |
| **Convert Stroke to Fill** |       ✅ **Perfect**        |   ❌ No support   | ❌ No support  | ❌ Partial support |
| **Optimize File Size**     |         ✅ **Yes**          |    ✅ **Yes**     |     ❌ No      |       ❌ No        |
| **Batch Processing**       |         ✅ **Yes**          |  ❌ Single file   |   ❌ Manual    |   ✅ Export only   |
| **Visual Structure Fix**   |         ✅ **Yes**          |       ❌ No       |     ❌ No      |       ❌ No        |
| **Iconfont Compatible**    |      ✅ **100% Ready**      |     ⚠️ Maybe      | ⚠️ Often Fails |   ⚠️ Often Fails   |

- **vs SVGOMG**: SVGOMG is great for compression, but it preserves the original structure (e.g., strokes). If your goal is to _fix_ the icon structure for icon fonts or CSS styling, SVGOMG is not enough.
- **vs Iconfont**: Iconfont is a hosting service, not a fixer. It rejects invalid SVGs. **SVG Cleaner** prepares your SVGs so Iconfont accepts them perfectly.
- **vs Figma**: Figma exports what you draw. **SVG Cleaner** transforms what you drew into what browsers/code actually need.

---

## ✨ Key Features

- **🎨 Intelligent Fix**:
  - Automatically identifies mixed colors and strokes.
  - Converts `stroke` to `fill` (outline) while preserving visual fidelity.
  - Handles complex shapes that usually break other tools.
- **🚀 Deep Optimization**:
  - Built-in **SVGO** integration.
  - Multipass compression, precision control, and metadata removal.
- **🌈 Color Reconstruction**:
  - Preserves original colors, opacity, and fill-rules during the fixing process.
- **👁️ Real-time Preview**:
  - Instant before/after comparison.
  - Test icons against dark/light/grid backgrounds.
- **📦 Batch Processing**:
  - Drag & drop multiple files.
  - One-click ZIP download.

---

## 🤝 Feedback & Support

We strive to handle all edge cases, but complex path nestings or masks can sometimes be tricky.

If you encounter an SVG that **cannot be fixed** or **looks wrong** after processing, please submit an Issue:

1.  Visit [GitHub Issues](https://github.com/fmthub/svg-cleaner/issues)
2.  Create a new Issue
3.  **Please attach the original SVG file** (or code) and a screenshot/description of the issue.

We will analyze it and improve our core algorithm.

---
