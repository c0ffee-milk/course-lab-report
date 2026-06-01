---
name: course-lab-report
description: Write Chinese computer-related university lab reports and course reports in the user's established style, including universal structure, subject-specific adaptation, evidence analysis, and Word formatting. Use when the user asks to write, rewrite, expand, polish, structure, or format a 课程实验报告、实验报告、课程报告、实验设计报告, or similar computer-course document.
---

# Course Lab Report

## Quick start

When asked to write a course/lab report, follow these steps **in order**. Do NOT start drafting until steps 1–3 are complete.

### Step 1 — Check for reference reports (MANDATORY GATE)

**Before doing anything else**, check whether the user provided any reference reports, sample reports, or past reports (as files, links, or mentions).

- **If reference reports exist**: STOP and ask the user which elements to reference. Present these options explicitly:
  1. 章节结构（heading order and section naming）
  2. 排版格式（layout, fonts, spacing, table style）
  3. 写作风格（tone, transitions, paragraph patterns）
  4. 证据呈现（how screenshots/tables/code are introduced and analyzed）
  5. 内容深度（detail level in principles, process, results）
  6. 特定章节（specific sections to model after）
  7. 以上全部（reference all elements）

  **Wait for the user's answer before proceeding.** Do not guess, do not assume "参考全部", do not start writing. Once the user answers, follow their selected elements strictly throughout the report.

- **If no reference reports exist**: skip this step and continue.

### Step 2 — Analyze the assignment

1. Treat it as a **general computer-course report**, not as a fixed course-category template.
2. Infer the concrete subject from the assignment: concepts, tools, environment, tasks, code, screenshots, logs, measurements, or expected outputs.
3. Start from the universal structure below, then adapt section names, order, and depth to the assignment and any provided school template.
4. Use the user's stable style: formal Chinese, purpose → principle → process → result → analysis → reflection, with screenshot/table/code evidence.
5. Ask the user for output format (`.docx`, `.md`, or LaTeX/PDF) if not specified. Apply the corresponding formatting anchors in [REPORT_ANCHORS.md](REPORT_ANCHORS.md).

## Universal skeleton

Default structure:

```md
# 封面/基本信息
# 摘要（长报告或课程设计需要）
关键词：...
# 目录（中长报告需要）
# 一、实验目的与要求
# 二、实验原理与相关知识
# 三、实验环境与工具
# 四、实验内容与实施过程
# 五、实验结果与分析
# 六、问题、解决方法与思考
# 七、实验总结与心得
# 参考文献/附录/教师评语评分（如模板要求）
```

Do not force every report to include every section. If a school template is provided, preserve it and map the universal logic into that template.

## Subject adaptation loop

Before drafting, decide:

1. **Main object**: configuration, tool procedure, program/module, hardware system, algorithm, OS mechanism, database/data experiment, measurement, or conceptual analysis.
2. **Evidence form**: screenshot, command output, code snippet, topology, table, waveform, hardware display, log, flag/key, test case, metric, or UI result.
3. **Best internal shape**:
   - multiple tasks → use task blocks;
   - system/program design → use module/design blocks;
   - lab-manual procedure → use step blocks;
   - conceptual questions → use question-answer blocks;
   - fixed school table → keep the table and fill it with the universal logic.
4. **Subject emphasis**: protocols/addresses, security authorization and defense, source files and algorithms, hardware signals, OS call chains, datasets/metrics, or performance comparisons.

See [REPORT_ANCHORS.md](REPORT_ANCHORS.md) for detailed adaptation patterns and formatting anchors.

## Writing rules

- **实验目的**: convert assignment bullets into measurable goals using 掌握、理解、实现、验证、分析.
- **实验原理**: explain only concepts used later; connect each concept to the actual experiment.
- **实验环境**: include platforms, tools, versions, devices, files, datasets, boards, IPs, or dependencies.
- **实验过程**: write reproducible action → reason → evidence → interpretation chains.
- **实验结果**: avoid bare “成功”; state what output proves and which requirement it satisfies.
- **问题思考**: describe symptom, cause, fix, verification, and lesson.
- **心得**: use first person, but keep it specific to the subject and technical gains.

## Evidence pattern

Use this pattern around screenshots/tables/code/results:

```md
配置完成后，执行 [命令/操作] 查看 [对象] 的状态，结果如图 n 所示。

![图 n 描述](path/to/image.png)

图 n 描述

结果显示 [关键现象]，说明 [配置/实现/实验要求] 已经满足。
```

For tables, introduce why the table exists, then analyze key rows after it.

## Role and perspective

**You are the student.** Write the report as if you personally conducted the experiment, observed the results, and composed the submission. The report is a natural student deliverable — not a response to a user's instructions.

- Never mention the user's instructions, chat dialogue, or meta-writing process in the report. Phrases like “根据用户要求”, “用户提供了”, “按照指示” must not appear.
- Do not reference AI tools, agents, or the writing process itself.
- Think from the student's perspective: what would a real student include after doing this experiment? What would they leave out?
- The user's input (screenshot files, assignment text, lab manual, code) is **raw material** — absorb it and re-express it as the student's own work, not as quoted instructions.
- If the user's input contains meta-language (e.g., “帮我写”, “补全这部分”), filter it out and focus on the technical content only.

## Style rules

- Body sections use objective narration; 心得/个人体会 may use first person.
- Prefer transitions: “首先…随后…接着…配置完成后…结果显示…说明…”.
- Keep paragraphs concrete: include tools, commands, files, modules, signals, metrics, IPs, test cases, or screenshots.
- Security labs must be framed as authorized course-lab work and include defensive implications.
- Code/design labs should explain function, interface, key logic, and verification rather than dumping code.

## Output formats

The user may request `.docx`, `.md`, or LaTeX/PDF. If not specified, ask. See [REPORT_ANCHORS.md](REPORT_ANCHORS.md) for detailed formatting anchors per format.

### Word (`.docx`)

- Invoke `docx-editor-cn` for formatting.
- A4, Chinese academic style, three-line tables, consistent caption numbering.

### Markdown (`.md`)

- GitHub-flavored Markdown; relative image paths; fenced code blocks with language tags.

### LaTeX → PDF

- Check local TeX environment (`which xelatex`); if missing, tell the user to install TeX Live/MacTeX.
- Build a complete project: `main.tex` (`ctexart`/`ctexrep`), `figures/`, `references.bib`, optional `Makefile`.
- After writing, compile with `latexmk -xelatex`; if it fails, read the `.log`, fix, and retry. Deliver the PDF to the user.

## Final checklist

- [ ] The report follows any provided school template.
- [ ] The structure is adapted to the specific subject, not copied from a fixed course category.
- [ ] If reference reports were provided, the user-selected elements are strictly followed.
- [ ] All text color defaults to black (no colored text unless the template or user requires it).
- [ ] The report reads as a natural student submission — no traces of user instructions, chat context, or AI involvement.
- [ ] Purpose, principle, environment, process, result, analysis, and reflection are present where appropriate.
- [ ] Every major task/module/experiment has evidence and analysis.
- [ ] Captions, tables, and result explanations are consistent.
- [ ] The final reflection is specific and technical.
