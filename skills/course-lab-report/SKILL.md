---
name: course-lab-report
description: Write Chinese computer-related university lab reports and course reports in the user's established style, including universal structure, subject-specific adaptation, evidence analysis, and Word formatting. Use when the user asks to write, rewrite, expand, polish, structure, or format a 课程实验报告、实验报告、课程报告、实验设计报告, or similar computer-course document.
---

# Course Lab Report

## Quick start

When asked to write a course/lab report:

1. Treat it as a **general computer-course report**, not as a fixed course-category template.
2. Infer the concrete subject from the assignment: concepts, tools, environment, tasks, code, screenshots, logs, measurements, or expected outputs.
3. Start from the universal structure below, then adapt section names, order, and depth to the assignment and any provided school template.
4. Use the user's stable style: formal Chinese, purpose → principle → process → result → analysis → reflection, with screenshot/table/code evidence.
5. For `.docx`, also invoke `docx-editor-cn` and apply the formatting anchors in [REPORT_ANCHORS.md](REPORT_ANCHORS.md).

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

## Style rules

- Body sections use objective narration; 心得/个人体会 may use first person.
- Prefer transitions: “首先…随后…接着…配置完成后…结果显示…说明…”.
- Keep paragraphs concrete: include tools, commands, files, modules, signals, metrics, IPs, test cases, or screenshots.
- Security labs must be framed as authorized course-lab work and include defensive implications.
- Code/design labs should explain function, interface, key logic, and verification rather than dumping code.

## Word output

When producing `.docx`:

- Use A4 and Chinese academic formatting unless a template differs.
- Match the provided cover/template.
- Include TOC for medium/long reports.
- Put figure captions below images and table captions above tables.
- Use one caption numbering style consistently.
- Use clean centered data tables; prefer three-line tables for formal academic data tables unless the template requires full-grid tables.

## Final checklist

- [ ] The report follows any provided school template.
- [ ] The structure is adapted to the specific subject, not copied from a fixed course category.
- [ ] Purpose, principle, environment, process, result, analysis, and reflection are present where appropriate.
- [ ] Every major task/module/experiment has evidence and analysis.
- [ ] Captions, tables, and result explanations are consistent.
- [ ] The final reflection is specific and technical.
