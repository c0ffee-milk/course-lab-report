# Course Lab Report Skill

A Claude/Codex skill for writing Chinese computer-related university lab reports and course reports.

This skill is designed for general computer-course reporting rather than a fixed subject category. It starts from a universal report structure, then guides the agent to adapt the report to the concrete assignment, evidence, course template, and subject matter.

## What it does

`course-lab-report` helps an agent write, rewrite, expand, polish, structure, or format:

- 课程实验报告
- 实验报告
- 课程报告
- 实验设计报告
- Computer-related course deliverables with screenshots, tables, code, logs, results, or analysis

It is especially useful when a report needs to preserve a formal Chinese academic style while still adapting to different computer-science subjects.

## Core approach

The skill follows a reusable logic extracted from real course reports:

1. Basic information and cover fields first
2. Clear experiment goals and requirements
3. Principles connected directly to the experiment
4. Concrete environment and tools
5. Reproducible process
6. Evidence-backed results
7. Result analysis rather than bare success claims
8. Problems, causes, fixes, and lessons
9. Specific technical reflection

Instead of classifying reports into rigid categories, the skill asks the agent to reason about:

- What is being configured, built, verified, measured, or analyzed?
- What evidence proves the result?
- Should the report use task blocks, module/design blocks, step blocks, Q&A blocks, or a fixed school table?
- What subject-specific details should be emphasized?

## Repository structure

```text
course-lab-report/
├── README.md
├── INSTALL.md
└── skills/
    └── course-lab-report/
        ├── SKILL.md            # Main skill instructions and trigger description
        └── REPORT_ANCHORS.md   # Detailed structure, writing, evidence, and formatting anchors
```

Only `skills/course-lab-report/` is the installable skill folder. Do not install the repository root.

## Installation

### Claude Code

Copy the skill folder into your Claude Code skills directory:

```bash
cp -R skills/course-lab-report ~/.claude/skills/course-lab-report
```

Restart or reload Claude Code so it can discover the skill.

### Codex

Copy the skill folder into your Codex skills directory:

```bash
cp -R skills/course-lab-report ~/.codex/skills/course-lab-report
```

Restart or reload Codex so it can discover the skill.

### Other agents

If your agent supports the same skill format, copy `skills/course-lab-report/` into that agent's skills directory. Keep `SKILL.md` and `REPORT_ANCHORS.md` together because the main skill references the anchor file.

## Usage examples

Ask your agent something like:

```text
帮我根据这些截图和实验要求写一份课程实验报告。
```

```text
把这个实验过程整理成正式的 Word 实验报告，保持中文课程报告风格。
```

```text
根据这份实验指导书和我的运行结果，补全实验原理、过程、结果分析和心得。
```

```text
润色这份计算机课程报告，让结构更完整，图表说明更规范。
```

The agent should load `course-lab-report` when the task involves Chinese computer-course lab reports or similar deliverables.

## What the skill emphasizes

### Universal report structure

The default structure is:

```text
封面/基本信息
摘要（长报告或课程设计需要）
目录（中长报告需要）
一、实验目的与要求
二、实验原理与相关知识
三、实验环境与工具
四、实验内容与实施过程
五、实验结果与分析
六、问题、解决方法与思考
七、实验总结与心得
参考文献/附录/教师评语评分（如模板要求）
```

The skill does not force every section. If a school or course template is provided, it preserves that template and maps the universal logic into it.

### Evidence handling

Reports should not simply list screenshots. Each figure, table, command, code snippet, log, waveform, metric, or result should be introduced and interpreted:

```text
配置完成后，执行 [命令/操作] 查看 [对象] 的状态，结果如图 n 所示。

图 n 描述

结果显示 [关键现象]，说明 [配置/实现/实验要求] 已经满足。
```

### Subject adaptation

The skill guides the agent to adapt content for different computer-course tasks, such as:

- configuration and deployment experiments
- tool-based procedures
- program, module, or system implementation
- operating-system or mechanism analysis
- measurement or comparison experiments
- database, data, or machine-learning reports
- security labs in authorized course environments
- hardware/FPGA/module-design reports

These are emphasis patterns, not rigid categories.

## Notes

- The skill is written for Chinese report generation.
- For `.docx` output, use it together with a Word/document-generation skill or tool.
- For security-lab reports, the skill instructs the agent to frame offensive steps as authorized course-lab work and include defensive implications.
- For code/design reports, the skill favors function/interface/key-logic/verification explanations over dumping large code blocks.

## License

No license has been added yet. Add one if you want to define reuse terms explicitly.
