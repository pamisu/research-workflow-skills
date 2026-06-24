# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

A **Claude Code Skills collection** for academic cybersecurity research — 15 curated skills + a 7-stage methodology guidebook in `docs/`.

## Context Cost

15 skills, ~4,100 tokens constant context (frontmatter only). Bodies load on demand.

## Directory Structure

```
skill-name/
├── SKILL.md          # Required: YAML frontmatter + Markdown body
├── LICENSE           # Optional
├── manifest.yaml     # Optional (nature-* skills)
├── README.md         # Optional (nature-* skills)
└── assets/           # Optional
```

## Skill Inventory

### Core Research (6)
`academic-research-suite`, `planning-with-files`, `neat-freak`, `unslop`, `unslop-file`, `research-codex/*` (3 sub-skills: research, research-deep, research-report)

### Paper Writing (7)
`nature-figure`, `nature-writing`, `nature-polishing`, `nature-citation`, `nature-data`, `nature-paper2ppt`, `nature-response`

### Removed Categories
Network traffic, code security, threat intel, SOC operations, and all niche/overlapping skills were removed as they don't apply to ML-focused traffic classification research. Experimental data processing, code auditing, and threat modeling are handled by Claude's native capabilities or aren't needed for this research direction.

## Documentation System

| File | Role |
|------|------|
| `docs/网络安全科研AI工作流完整指导书.md` | Full 7-stage methodology |
| `docs/网络安全科研AI工作流速查表.md` | Stage → skill → operation quick lookup |
| `docs/示例：基于图的预训练加密流量分类研究全流程.md` | Complete TIGraphCL worked example |

Guidebook references skills by source repo, so individual skill changes usually don't require guidebook updates. Keep §1.1/§1.2 source URLs accurate.

## Common Operations

```bash
# Add a skill
cp -r /path/to/new-skill . && git add -A && git commit -m "add: <name>"

# Remove a skill
git rm -r <skill-name> && git commit -m "remove: <name>"

# Check context cost
total=0; count=0
for f in $(find . -name "SKILL.md" -not -path "./.git/*"); do
  chars=$(awk '/^---$/{if(++c==2)exit;next} c==1{print}' "$f" | wc -c)
  total=$((total + chars)); count=$((count + 1))
done
echo "$count skills | $total chars FM | ~$((total * 10 / 35)) tokens"
```

## Key Conventions

- **Skill identity = directory name**, not the `name:` field in frontmatter
- **`description` field = trigger** — concise but specific enough for Claude Code to auto-invoke
- **Guidebook ↔ skills consistency** — keep docs in sync with installed skills
- **"按需启用"** — removed skills can be restored via git history or from source repos
