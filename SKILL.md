---
name: timeline-docx
description: "Create professional Word documents that organize content into clear items, each with a concise timeline summary. Use when the user wants a structured .docx report, summary, or catalog with chronological timelines for projects, skills, events, products, or topics."
type: workflow
lifecycle: active
---

# Timeline Docx — Structured Documents with Per-Item Timelines

Generate clean, professional .docx files that present multiple items (projects, skills, milestones, products, news topics, etc.), each accompanied by a focused timeline summary.

## When to Use
- User asks for a Word document / doc / 文档 / 报告 that organizes multiple items with timelines.
- Requests for “时间线总结”, chronological summary, or structured catalog in .docx format.
- Open-source skill style deliverables that need a polished document output.

## Core Workflow

1. **Clarify items** (if not already provided)
   - Identify the list of items (e.g., skills, projects, events).
   - For each item, gather or research key dates and milestones.

2. **Structure the document**
   - Title + short introduction
   - For every item:
     - Heading 1 or 2: Item name
     - 1–3 sentence overview
     - **Timeline Summary** subsection (table or clean bullet list)
   - Optional: overall summary or comparison table at the end

3. **Generate with docx-js**
   - Ensure `npm install -g docx` is available (or use existing installation).
   - Use US Letter page size (12240 × 15840 DXA), Arial font, proper heading styles with outlineLevel.
   - Prefer tables for timelines when there are 3+ dated events.
   - Use `ShadingType.CLEAR` for table backgrounds.
   - Always set both table `width`/`columnWidths` and cell widths in DXA.

4. **Validate and deliver**
   - Run validation if available (`python scripts/office/validate.py`).
   - Save the final .docx to the working directory / artifacts.
   - Offer the file for download.

## Timeline Format Recommendations

**Table style (preferred for 3+ events):**

| Date | Milestone | Notes |
|------|-----------|-------|
| 2024-01 | Initial release | Open-sourced on GitHub |
| 2024-06 | Major update | Added plugin support |

**Bullet style (for shorter timelines):**

- **2024-01**: Initial release — open-sourced
- **2024-06**: Major update — added plugin support

## Document Styling Defaults

- Font: Arial
- Title: Heading 1, bold, 16pt+
- Item headings: Heading 2
- Timeline headings: Heading 3 or bold paragraph
- Margins: 1 inch
- Page size: US Letter
- Colors: Professional, high-contrast (black text, light gray table headers if needed)

## Example Prompt Triggers
- “帮我整理一个doc，每一项都有时间线总结”
- “Create a Word document catalog of open-source skills with timelines”
- “生成一份带时间线的项目总结文档”

## Notes
- This skill focuses on structure and timeline clarity, not deep research (research can be done with other tools first).
- Keep timelines factual and concise.
- If content is missing, ask for the list of items or use web search / connected tools to gather accurate dates.
- Compatible with Codex, Claude Code, Grok, and other agents that support the open Agent Skills format.
