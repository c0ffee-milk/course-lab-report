# Report Anchors Extracted from Reference Reports

These anchors come from the user's past computer-related course reports. They are not course-category templates. Use them as a general writing and formatting framework, then adapt the structure to the concrete subject, assignment requirements, and any provided school template.

## 1. Universal report logic

Across the reference reports, the stable logic is:

1. **基本信息先行**: school/college, course name, experiment/report title, major/class, student ID, name, teacher, date.
2. **任务目标明确**: explain what the experiment asks the student to understand, implement, configure, verify, or analyze.
3. **原理服务过程**: introduce only the concepts needed for the later steps, and immediately connect them to the concrete experiment.
4. **环境交代清楚**: tools, platforms, devices, IPs, code files, datasets, hardware boards, software versions, or test targets.
5. **过程可复现**: steps are ordered and concrete; include commands, configurations, code paths, module names, or UI operations.
6. **证据支撑结论**: screenshots, tables, code snippets, command outputs, waveforms, hardware displays, flags/keys, or test results prove each important claim.
7. **结果必须分析**: after each result, state what it proves and how it satisfies the requirement.
8. **问题体现思考**: include symptoms, causes, solutions, verification, and lessons.
9. **心得回到能力提升**: first-person reflection should name specific technical understanding, debugging method, engineering practice, or security awareness.

## 2. General front matter anchors

### Standard cover fields

Use the fields required by the assignment or school template. Common fields from the reference reports:

```text
武汉大学国家网络安全学院
[课程实验/设计/实践报告标题]
题目/实验名称：[实验题目]
课程名称：[课程名称]
专业(班)/专业名称：[专业班级]
学号：[学号]
姓名：[姓名]
任课教师/指导老师：[教师]
日期：[日期]
```

### Optional front matter

Add only when appropriate:

- **郑重声明**: for formal long reports or provided templates.
- **摘要 + 关键词**: for comprehensive reports, course designs, multi-task reports, or reports with substantial implementation.
- **目录**: for medium/long reports or when the output is `.docx`.
- **评分标准/教师评语评分**: only when the course template includes it.

### Abstract pattern

```text
本次实验围绕[主题/对象]展开，实验目的是[核心目标]。实验过程主要包括[方法/任务链/模块设计/验证流程]。通过[工具/平台/测试方法]完成了[主要结果]。实验结果表明[结论]，同时说明[工程意义/安全启示/理论联系实践]。
```

Keywords should be concrete: tools, protocols, algorithms, modules, mechanisms, or methods.

## 3. Universal body skeleton

Start from this skeleton and adapt it:

```md
# 一、实验目的与要求
# 二、实验原理与相关知识
# 三、实验环境与工具
# 四、实验内容与实施过程
# 五、实验结果与分析
# 六、问题、解决方法与思考
# 七、实验总结与心得
```

Possible renamings based on the assignment:

- “实验目的与要求” may become “实验目的和意义” or “实验目的及实验内容”.
- “实验原理与相关知识” may become “实验原理” or be merged into “实验内容”.
- “实验内容与实施过程” may become “实验步骤及内容”, “概要设计/详细设计”, “任务一/任务二”, or table cells in a fixed template.
- “实验结果与分析” may become “测试及结果分析”, “实验关键过程及其分析”, or “实验结果”.
- “问题、解决方法与思考” may become “出现的问题及解决方法” or “问题及思考”.
- “实验总结与心得” may become “实验心得”, “实验总结”, or “个人实验贡献与体会”.

Do not treat these as categories; they are structural options chosen according to the assignment.

## 4. How to adapt structure to a subject

Before writing, reason through these questions:

### 4.1 What is the experiment's main object?

- **A configuration or deployment**: emphasize topology/environment, parameter planning, configuration steps, state verification, troubleshooting.
- **A tool-based procedure**: emphasize task objective, tool parameters, operation sequence, observed output, and risk/defense or usage reflection.
- **A program/module/system implementation**: emphasize design goal, architecture, module responsibilities, interfaces, key logic, test cases, and output verification.
- **A mechanism analysis**: emphasize concept chain, source/code path, data/control flow, key structures, and evidence from screenshots or code.
- **A measurement or comparison**: emphasize metrics, test setup, baseline, result table, analysis, and limitations.

### 4.2 What is the best internal structure?

Choose one or combine them:

- **Task blocks** when the assignment has multiple independent tasks:
  ```md
  ## 任务一 [名称]
  ### 任务描述
  ### 实验目标
  ### 实验工具/环境
  ### 操作过程
  ### 结果与分析
  ```
- **Module/design blocks** when building software/hardware/system components:
  ```md
  ## [模块/组件名称]
  ### 功能描述
  ### 接口/输入输出/关键参数
  ### 关键逻辑
  ### 验证方法与结果
  ```
- **Procedure blocks** when following a lab manual:
  ```md
  ## [步骤名称]
  [操作目的] → [具体操作] → [截图/命令/代码] → [结果说明]
  ```
- **Question-answer blocks** when the assignment asks conceptual questions:
  ```md
  ## [问题]
  [概念解释] + [结合实验/代码/截图分析] + [结论]
  ```
- **Fixed table template** when the school provides a table: keep the table and fill each row/cell using purpose, process, result, analysis, and reflection.

### 4.3 What should be emphasized?

Adapt emphasis without changing the universal logic:

- Protocol/network-like work: address planning, topology, device roles, commands, state tables, connectivity tests.
- Security-like work: authorization context, target identification, tool parameters, exploitation/verification chain, final flag/key/result, defensive implications.
- Code/software work: source files, functions/classes, algorithm flow, inputs/outputs, tests, edge cases, logs.
- OS/system mechanism work: hardware/software event chain, interrupt/syscall path, buffers, kernel functions, process/state transitions.
- Hardware/FPGA work: modules, signals, state machines, timing, constraints, simulation, board verification, resource/performance reports.
- Database/data/ML work: schema/dataset, preprocessing, query/model logic, metrics, result tables/figures, error analysis.

These are emphasis guides, not separate report categories.

## 5. Section-writing patterns

### 实验目的与要求

```text
本实验旨在通过[操作/实现/验证]，掌握[知识点1]、理解[知识点2]，并能够使用[工具/平台/方法]完成[具体任务]。实验要求包括：
1. ...
2. ...
```

### 实验原理与相关知识

```text
[概念]用于[作用]。在本实验中，[对象/工具/模块/设备]通过[具体方法]实现[目标]。需要注意的是，[约束/易错点]，否则可能导致[失败现象]。
```

### 实验环境与工具

```text
本实验在[平台/环境]中完成，主要使用[工具/设备/代码文件]。其中，[工具/模块A]用于[作用]，[工具/模块B]用于[作用]。
```

Use tables when there are many parameters:

```md
| 项目 | 取值 | 说明 |
|---|---|---|
```

### 实验内容与实施过程

```text
首先，[操作]，用于[目的]。随后，[操作]，完成[配置/实现/测试]。配置/实现完成后，通过[命令/截图/测试]查看结果。
```

For each important step, include:

1. action,
2. reason,
3. evidence,
4. interpretation.

### 实验结果与分析

```text
在[工具/设备/模块]上执行[验证操作]后，可以看到[关键输出/现象]。该结果说明[配置/实现/机制]已经生效，并且[实验要求]得到满足。
```

If multiple results exist, group by verification target instead of dumping screenshots.

### 问题、解决方法与思考

```text
**[问题名]。** 实验中出现[现象]。造成该问题的原因是[原因]。解决时应[具体操作]，并通过[验证方法]确认结果。该问题说明[经验/原则]。
```

### 实验总结与心得

```text
通过本次实验，我对[核心主题]有了更直观/深入的理解。实验过程中，[具体机制/问题/调试过程]让我认识到[技术认识]。在后续处理类似任务时，应按照[检查顺序/方法]逐项验证。该实验不仅帮助我掌握了[工具/方法]，也提升了[工程能力/安全意识/系统思维]。
```

## 6. Evidence and caption rules

### Figures

- Figures should be centered in `.docx` and followed by a centered caption.
- Use one numbering style consistently: `图 1 描述` or `图 章-序 描述`.
- Before or after each figure, explain what it proves.
- Good figure uses: topology, physical connection, configuration screen, command output, code path, waveform, hardware display, final result.

Example:

```md
完成参数配置后，执行测试命令查看运行状态，结果如图 3 所示。

![图 3 状态查看结果](images/status.png)

图 3 状态查看结果

结果显示[关键字段]，说明[结论]。
```

### Tables

- Use tables for address planning, environment/tool lists, module interfaces, parameters, test cases, result comparisons, or scoring rubrics.
- Data tables should have a short introduction and a short analysis.
- Academic-style data tables should use three-line formatting in Word unless the course template requires full-grid tables.

### Code, commands, and logs

- Keep snippets close to their explanation.
- Do not paste huge code unless required; summarize function, key logic, and verification.
- Commands should be reproducible and followed by result interpretation.
- Logs/output should be reduced to the lines that prove the point.

## 7. Formatting anchors

### Word (`.docx`)

Use `docx-editor-cn` and follow:

- A4 page; margins 2.5 cm unless a provided template differs.
- Chinese body font: 宋体; headings: 黑体; English/code: Cambria Math or Times New Roman.
- Body size: 小四 / 12 pt; first-line indent 2 Chinese characters.
- **All text color defaults to black (RGB 0,0,0). Do not use colored text unless the template or user explicitly requires it.**
- Heading hierarchy should be clean and numbered.
- Long reports include TOC.
- Figure captions below figures; table captions above tables.
- Captions are centered and consistently numbered.
- Cover/template tables may use full borders and centered cells.
- Data tables should be clean and centered; use three-line tables for formal academic data tables.

### Markdown (`.md`)

- Use GitHub-flavored Markdown.
- Headings: `#` for title, `##` for major sections, `###` for subsections.
- **All text is plain black by default. Do not use colored text or HTML color tags unless the user explicitly requires it.**
- Images: `![图 n 描述](relative/path.png)` with a caption line below.
- Tables: use alignment columns; keep cell content concise.
- Code: fenced blocks with language identifier (` ```bash `, ` ```c `, etc.).
- Place screenshots and figures in a `figures/` subdirectory alongside the `.md` file.

### LaTeX → PDF

- Use `ctexart` or `ctexrep` document class with `UTF8` option for Chinese support.
- Page geometry: A4, margins 2.5 cm (`\usepackage[a4paper, margin=2.5cm]{geometry}`).
- **All text color defaults to black. Do not use `\textcolor` or `\color` commands unless the template or user explicitly requires it.**
- Fonts: `ctex` handles 宋体/黑体 automatically; use `\ttfamily` or `listings`/`minted` for code.
- Body: 12 pt, first-line indent 2 characters (`\setlength{\parindent}{2em}`).
- Headings: `\section`, `\subsection`, `\subsubsection` with automatic numbering.
- Figures: `figure` environment with `\centering`, `\includegraphics`, `\caption`.
- Tables: `table` environment with `booktabs` (`\toprule`, `\midrule`, `\bottomrule`) for three-line style.
- Code listings: `listings` package with `\lstset{basicstyle=\ttfamily, breaklines=true}`; set `literate` for Chinese if needed.
- Bibliography: `biblatex` with `biber` backend, or `natbib` with `thebiblivironment`.
- Build: `latexmk -xelatex -interaction=nonstopmode main.tex` or two passes of `xelatex`.
- Project structure:

```text
report/
├── main.tex
├── figures/
│   ├── fig01.png
│   └── ...
├── references.bib
└── Makefile          # optional, wraps latexmk
```

## 8. Reference report handling

When the user provides reference reports (e.g., past reports, sample reports, template reports):

### What to ask

Before drafting, ask the user which elements to reference. Present these options:

| Element | What it covers |
|---------|---------------|
| 章节结构 | Heading hierarchy, section order, section naming conventions |
| 排版格式 | Page layout, fonts, spacing, margins, table style, caption format |
| 写作风格 | Tone, sentence patterns, transition phrases, paragraph structure |
| 证据呈现 | How screenshots, tables, code, and logs are introduced, captioned, and analyzed |
| 内容深度 | Level of detail in principles, process descriptions, result analysis, and reflection |
| 特定章节 | Specific sections to model (e.g., replicate the reference's 心得 or 问题思考 style) |

### How to apply

- **Only use what the user explicitly selects.** Do not copy structure, style, or content from reference reports by default.
- **When elements are selected, follow them strictly.** For example, if the user selects "章节结构" and the reference uses `实验目的 → 实验原理 → 实验环境 → 实验步骤 → 实验结果 → 心得体会`, use that exact order and naming.
- If the user says "参考全部" or equivalent, apply all dimensions from the reference report(s).
- If the user provides multiple reference reports with conflicting patterns, ask which report takes priority for each element.

## 9. Quality bar

A strong report should:

- Match the provided assignment/template instead of forcing a canned category.
- Be complete enough to reproduce the experiment.
- Explain why each step matters.
- Show key evidence instead of only describing it.
- Analyze every major result.
- Include realistic problems, causes, and solutions.
- Tie the final reflection to specific technical gains.
- Avoid generic filler and unsupported claims.
