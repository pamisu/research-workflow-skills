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

### 🔵 核心科研流程（6 个）

| Skill | 用途 | 指导书阶段 |
|-------|------|-----------|
| `academic-research-suite` | /ars-plan 选题、/ars-lit-review 文献综述、/ars-review 模拟审稿、写作逻辑校验 | 全阶段 |
| `planning-with-files` | 跨会话项目计划持久化 | 全阶段 |
| `neat-freak` | `/neat` 阶段收尾文档归档 | 每阶段收尾 |
| `unslop` | 去 AI 写作痕迹，5 级强度可调 | 阶段六 |
| `unslop-file` | Markdown 文件人性化 | 辅助 |
| `research-codex` | 结构化深度文献调研（research → deep → report） | 阶段二 |

### 🟢 论文写作（7 个）

| Skill | 用途 |
|-------|------|
| `nature-figure` | 顶会图表规范校验与生成 |
| `nature-writing` | 论文章节写作优化 |
| `nature-polishing` | 语言抛光与学术表达优化 |
| `nature-citation` | 引用格式规范化 |
| `nature-data` | 实验数据展示规范 |
| `nature-paper2ppt` | 论文转演示文稿 |
| `nature-response` | 审稿意见回复辅助 |

## 使用方式

```
/academic-research-suite: 针对「基于GNN的加密流量分类」做文献综述...
/neat
用 nature-figure 技能检查图表规范...
用 unslop 润色这段论文内容，强度等级 3...
```

**上下文成本**：15 个 Skills，仅元数据 ~4,100 tokens。不调用不加载 body。

## 精简历程

| 阶段 | 技能数 | 上下文 | 移除了什么 |
|------|--------|--------|-----------|
| 初始 | 63 | ~12,600 | — |
| 第一轮 | 40 | ~8,800 | 重叠/niche/SOC/通用模板/非科研工具 |
| 第二轮 | 31 | ~7,500 | 辅助 skill、功能重叠、Splunk 合并 |
| 第三轮 | 22 | ~5,900 | 网络流量（实验数据处理用 AI 原生能力）、代码安全（小项目人工审查） |
| 最终 | **15** | **~4,100** | 威胁情报（加密流量分类方向不涉及攻击者行为分析） |
| **累计** | **-76%** | **-67%** | |
