# 网络安全科研 AI 工作流 Skills

配套《网络安全科研AI工作流完整指导书》的 Skills 集合。聚焦科研核心流程，仅保留全程使用的通用技能。

## 安装

```bash
git clone git@github.com:pamisu/research-workflow-skills.git ~/.claude/skills/
```

## 配套文档

| 文档 | 说明 |
|------|------|
| [docs/网络安全科研AI工作流完整指导书.md](docs/网络安全科研AI工作流完整指导书.md) | 七阶段科研工作流详细指导 |
| [docs/网络安全科研AI工作流速查表.md](docs/网络安全科研AI工作流速查表.md) | 阶段-Skill-操作速查索引 |
| [docs/示例：基于图的预训练加密流量分类研究全流程.md](docs/示例：基于图的预训练加密流量分类研究全流程.md) | 全流程实操案例演示 |

## Skills 清单（15 个）

### 🔵 学术研究套件（4 个子技能，CC-BY-NC 4.0）

`ars-suite/` 来自 [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)，精简为 zh-CN + en。

| 子技能 | 版本 | 用途 |
|--------|------|------|
| `deep-research` | v2.11.0 | 13-agent 深度文献调研，8 模式（系统综述/Meta分析/事实核查等） |
| `academic-paper` | v3.2.0 | 12-agent 论文写作，11 模式，5 引用格式（含 IEEE） |
| `academic-paper-reviewer` | v1.10.0 | 5 审稿人模拟（EIC+3 peer+Devil's Advocate） |
| `academic-pipeline` | v3.13.0 | 10 阶段全流程编排器（研究→写作→审查→修改→定稿） |

### 🟢 论文写作（7 个）

| Skill | 用途 |
|-------|------|
| `academic-figure` | 顶会图表规范校验与生成 |
| `paper-writing` | 论文章节写作优化 |
| `paper-polishing` | 语言抛光与学术表达优化 |
| `targeted-citation` | CS/安全顶会定向引用 |
| `data-availability` | 实验数据可用性声明 |
| `paper2ppt` | 论文转演示文稿 |
| `reviewer-response` | 审稿意见回复辅助 |

### ⚪ 核心工作流（4 个）

| Skill | 用途 |
|-------|------|
| `planning-with-files` | 跨会话项目计划持久化 |
| `neat-freak` | `/neat` 阶段收尾文档归档 |
| `unslop` | 去 AI 写作痕迹，5 级强度可调 |
| `unslop-file` | Markdown 文件人性化 |

## 使用方式

```
用 deep-research 对「基于GNN的加密流量分类」做系统综述...
用 academic-paper 写论文，引用格式选 IEEE...
/neat
用 academic-figure 技能检查图表规范...
用 unslop 润色这段论文内容，强度等级 3...
```

**上下文成本**：15 个 Skills，仅元数据 ~4,100 tokens。不调用不加载 body。

## 精简历程

| 阶段 | 技能数 | 上下文 | 移除了什么 |
|------|--------|--------|-----------|
| 初始 | 63 | ~12,600 | — |
| v1 | 40 | ~8,800 | 重叠/niche/SOC/通用模板/非科研工具 |
| v2 | 31 | ~7,500 | 辅助 skill、功能重叠 |
| v3 | 22 | ~5,900 | 网络流量、代码安全 |
| v4 | 15 | ~4,100 | 威胁情报、nature-*品牌化 |
| v5 | **15** | **~4,100** | nature-*→通用化、Codex ARS→Claude ARS、清除多语言冗余 |
| **累计** | **-76%** | **-67%** | |
