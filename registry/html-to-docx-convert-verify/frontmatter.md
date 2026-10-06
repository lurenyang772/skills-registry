---
name: html-to-docx-convert-verify
description: 在 Windows 上把 HTML 交付稿转换为高保真 .docx 并做结构级验收。当需要交付 Word（研报/方案/文档）、复用 tencent-docx 插件流水线的 Stage 3（doc-converter / html-to-docx）、或怀疑「目录丢失 / 页码页脚失效 / 章节未分节」时使用。含环境自建（官方脚本在 Windows 失效的绕法）、引擎硬契约（目录必须用 ol、章节首块不能是占位符）、以及 7 项缺一不可的 docx 验收口径。
category: capability
agent_created: true
version: "1.1"
tags: [docx, html-to-docx, tencent-docx, windows, verification, toc, sections]
---
