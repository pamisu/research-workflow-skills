---
name: ars-suite
description: >
  Claude-native Academic Research Skills suite — 4 integrated skills covering the full
  research-to-publication pipeline: deep-research (13-agent literature research, 8 modes),
  academic-paper (12-agent paper writing, 11 modes), academic-paper-reviewer (5-reviewer
  simulation), and academic-pipeline (10-stage orchestrator). Use when the user asks for
  deep research, literature review, systematic review, paper writing, peer review simulation,
  full research-to-paper workflow, or related academic tasks. Triggers include: research,
  deep research, write paper, review paper, academic pipeline, 研究, 深度研究, 写论文,
  文献综述, 审稿, 学术流水线.
version: "2.11.0"
upstream: "https://github.com/Imbad0202/academic-research-skills"
license: "CC-BY-NC 4.0"
---

# ARS Suite — Academic Research Skills for Claude Code

This is a **stripped, zh-CN+en-only** packaging of the [academic-research-skills](https://github.com/Imbad0202/academic-research-skills) Claude Code plugin by Cheng-I Wu. Licensed under CC-BY-NC 4.0.

## Sub-Skills

| Skill | Version | Description |
|-------|---------|-------------|
| [deep-research](deep-research/SKILL.md) | 2.11.0 | 13-agent literature research: 8 modes including systematic review, meta-analysis, fact-check |
| [academic-paper](academic-paper/SKILL.md) | 3.2.0 | 12-agent paper writing: 11 modes, 5 citation formats (APA/Chicago/MLA/IEEE/Vancouver) |
| [academic-paper-reviewer](academic-paper-reviewer/SKILL.md) | 1.10.0 | Multi-perspective peer review: EIC + 3 reviewers + Devil's Advocate |
| [academic-pipeline](academic-pipeline/SKILL.md) | 3.13.0 | Full-pipeline orchestrator: research → write → review → revise → finalize |

## Shared Infrastructure

The `shared/` directory contains agents, contracts, templates, and references used across all 4 sub-skills. Do not load `shared/` wholesale — each sub-skill's `SKILL.md` loads only what it needs.

## Stripped Content

- Removed: zh-TW, ja-JP, ko-KR translations (zh-CN + en only)
- Removed: Python scripts (CI, tests, verification tools)
- Removed: Plugin infrastructure (hooks, commands, .github workflows)
- Removed: Evaluation harnesses, test fixtures, migration scripts
- Kept: All agent definitions, contracts, templates, references, examples

## License

CC-BY-NC 4.0 — Attribution-NonCommercial. See [LICENSE](LICENSE).
