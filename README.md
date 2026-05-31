# wdz

[English](README.md) | [简体中文](README_ZH.md)

`wdz` is a Codex skill that packages WDZ's preferred research, coding, experiment, and paper-writing collaboration style.

Use it when working on fast-moving CS research topics such as LLM, VLM, Agents, VLN, CV, RL, Data Mining, ML/DL, Medical AI, or when the task should follow WDZ's paper-oriented workflow: topic survey -> reproduction -> idea -> experiment -> results -> paper. Temporary hardware limits can inform execution planning, but they should not dominate the skill's identity.

## Skill Routing

The skill now explicitly routes specialized document and research tasks before execution:

- PPT, presentation, slides, or document-to-deck tasks -> use **ppt-master**.
- Word / `.docx` creation, editing, inspection, polishing, or conversion -> use **docx**.
- Research, survey, deep research, literature review, paper search, or benchmark mapping -> use **Academic Research** deep-research plus relevant **nature-skills**.
- For mixed tasks, choose the smallest effective skill combination and execute in that order.

## Install

Copy the skill folder into Codex skills:

```powershell
Copy-Item -Recurse -Force .\wdz C:\Users\Administrator\.codex\skills\wdz
```

Restart Codex if the slash menu or skill list does not refresh immediately.

## Structure

```text
wdz/
  SKILL.md
  agents/
    openai.yaml
  references/
    WDZ_RESEARCH_STYLE.md
    WDZ_RESEARCH_STYLE_ZH.md
    compact-profile.md
    research-output-template.md
```

## Invocation

Examples:

```text
$wdz 帮我调研 VLN 方向，形成论文导向的研究计划。
$wdz 按我的风格阅读这个 repo，找最快可复现实验路径。
$wdz 基于当前结果写一个 paper-shaped outline 和实验表。
$wdz 把这个文档做成 PPT。
$wdz 帮我编辑这个 Word 文档。
```

## Maintenance

- Edit `wdz/SKILL.md` for the concise behavior policy loaded by Codex.
- Edit files under `wdz/references/` for detailed style context and templates.
- Keep `WDZ_RESEARCH_STYLE.md` as the authoritative English source.
- Keep `WDZ_RESEARCH_STYLE_ZH.md` as the Simplified Chinese reference source.
- Keep `README.md` and `README_ZH.md` synchronized.
- Do not place this README inside the installed skill folder unless Codex skill packaging rules change.
