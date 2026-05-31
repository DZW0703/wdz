# wdz

[English](README.md) | [简体中文](README_ZH.md)

`wdz` 是一个 Codex skill，用来封装 WDZ 偏好的科研、编码、实验和论文写作协作风格。

当任务涉及 LLM、VLM、Agent、VLN、CV、RL、数据挖掘、ML/DL、医学 AI 等快速变化的 CS 研究方向，或需要遵循“方向调研 -> 复现 -> 创意 -> 实验 -> 结果 -> 论文”的论文导向流程时，使用该 skill。短期硬件条件可以影响执行计划，但不应主导 skill 的身份定位。

## 技能路由

该 skill 会在执行前优先判断是否应调用更专门的技能：

- PPT、presentation、slides，或任意文档转演示文稿 -> 使用 **ppt-master**。
- Word / `.docx` 创建、编辑、检查、润色或转换 -> 使用 **docx**。
- 调研、深度调研、文献综述、论文检索、来源筛选或 benchmark 梳理 -> 使用 **Academic Research** 的 deep-research，并结合相关 **nature-skills**。
- 混合任务选择最小但足够的技能组合，并按顺序执行。

## 安装

将 skill 文件夹复制到 Codex skills 目录：

```powershell
Copy-Item -Recurse -Force .\wdz C:\Users\Administrator\.codex\skills\wdz
```

如果 slash menu 或 skill 列表没有立刻刷新，重启 Codex。

## 结构

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

## 调用示例

```text
$wdz 帮我调研 VLN 方向，形成论文导向的研究计划。
$wdz 按我的风格阅读这个 repo，找最快可复现实验路径。
$wdz 基于当前结果写一个 paper-shaped outline 和实验表。
$wdz 把这个文档做成 PPT。
$wdz 帮我编辑这个 Word 文档。
```

## 维护

- 编辑 `wdz/SKILL.md` 来维护 Codex 加载的精简行为策略。
- 编辑 `wdz/references/` 下的文件来维护详细风格上下文和模板。
- `WDZ_RESEARCH_STYLE.md` 是英文权威源。
- `WDZ_RESEARCH_STYLE_ZH.md` 是简体中文参考源。
- 保持 `README.md` 与 `README_ZH.md` 同步。
- 除非 Codex skill 打包规则变化，不要把 README 放入已安装的 skill 文件夹。
