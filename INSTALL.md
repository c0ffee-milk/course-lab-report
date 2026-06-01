# Installation

Only the nested folder `skills/course-lab-report/` is the installable skill.

Do **not** install the repository root, because it also contains repository documentation such as `README.md` and `INSTALL.md`.

## Installable files

```text
skills/course-lab-report/
├── SKILL.md
└── REPORT_ANCHORS.md
```

## Claude Code

From the repository root:

```bash
cp -R skills/course-lab-report ~/.claude/skills/course-lab-report
```

Restart or reload Claude Code so it can discover the skill.

## Codex

From the repository root:

```bash
cp -R skills/course-lab-report ~/.codex/skills/course-lab-report
```

Restart or reload Codex so it can discover the skill.

## Other agents

Copy `skills/course-lab-report/` into the target agent's skills directory:

```bash
cp -R skills/course-lab-report <target-skills-dir>/course-lab-report
```
