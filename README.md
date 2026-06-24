# 网络安全科研 AI 工作流 Skills

本仓库是《网络安全科研AI工作流完整指导书》配套的统一 Skills 集合。涵盖从选题到投稿的全流程科研支持。

## 安装

```bash
# 克隆到 Claude Code 用户级 Skills 目录
git clone git@github.com:pamisu/research-workflow-skills.git ~/.claude/skills/
```

## 配套文档

| 文档 | 说明 |
|------|------|
| [docs/网络安全科研AI工作流完整指导书.md](docs/网络安全科研AI工作流完整指导书.md) | 七阶段科研工作流详细指导 |
| [docs/网络安全科研AI工作流速查表.md](docs/网络安全科研AI工作流速查表.md) | 阶段-Skill-操作速查索引 |
| [docs/示例：基于图的预训练加密流量分类研究全流程.md](docs/示例：基于图的预训练加密流量分类研究全流程.md) | 全流程实操案例演示 |

## Skills 清单

### 🔵 核心科研流程（全程使用）

| Skill | 用途 | 指导书阶段 |
|-------|------|-----------|
| `academic-research-suite` | 科研主干：/ars-plan 选题、/ars-lit-review 文献综述、/ars-review 模拟审稿、写作逻辑校验 | 全阶段 |
| `planning-with-files` | 跨会话项目计划持久化 | 全阶段 |
| `neat-freak` | `/neat` 阶段收尾文档归档 | 每阶段收尾 |
| `unslop` | 去 AI 写作痕迹，5 级强度可调，保留代码/URL/表格 | 阶段六 |
| `research-codex` | 结构化深度文献调研（两阶段：纲要→深度展开） | 阶段二 |

### 🟢 论文写作与出版

| Skill | 用途 |
|-------|------|
| `nature-figure` | 顶会图表规范校验与生成 |
| `nature-writing` | 论文章节写作优化 |
| `nature-polishing` | 语言抛光与学术表达优化 |
| `nature-citation` | 引用格式规范化 |
| `nature-reviewer` | 模拟审稿辅助 |
| `nature-data` | 实验数据展示规范 |
| `nature-paper2ppt` | 论文转演示文稿 |
| `nature-response` | 审稿意见回复辅助 |
| `nature-reader` | 论文深度阅读与总结 |

### 🟡 威胁情报与威胁建模

| Skill | 用途 |
|-------|------|
| `threat-actor-ttps-mitre` | MITRE ATT&CK 威胁行为体 TTPs 分析 |
| `threat-navigator-mitre` | MITRE Navigator 攻击路径可视化与映射 |
| `apt-group-analysis` | APT 组织画像与攻击模式分析 |
| `threat-landscape-misp` | MISP 威胁情报平台威胁态势分析 |
| `threat-intel-feeds` | 威胁情报源结构化分析 |
| `threat-intel-splunk` | Splunk 威胁情报富化与关联 |
| `threat-hunt-framework` | 威胁狩猎假设框架构建 |
| `cyber-risk-assessment` | NIST 800-30 网络安全风险评估 |
| `threat-modeling` | 通用威胁建模方法论 |

### 🟠 网络流量分析与威胁狩猎

| Skill | 用途 |
|-------|------|
| `network-traffic-incidents` | 网络流量安全事件分析 |
| `malware-traffic-analysis` | 恶意软件网络流量特征分析 |
| `packet-analysis-scapy` | Scapy 数据包级深度分析 |
| `network-flow-analysis` | NetFlow/IPFIX 流数据分析 |
| `dns-exfiltration-analysis` | DNS 隧道与数据外泄检测 |
| `network-anomaly-zeek` | Zeek 网络异常检测 |
| `tls-certificate-analysis` | TLS 证书透明度日志审计 |
| `ransomware-network-analysis` | 勒索软件网络指标分析 |
| `covert-channels-malware` | 恶意软件隐蔽信道分析 |
| `security-logs-splunk` | Splunk 安全日志分析 |
| `detection-rule-splunk` | Splunk SPL 检测规则编写 |

### 🔴 代码安全与检测工程

| Skill | 用途 | 适用条件 |
|-------|------|----------|
| `yara-authoring` | YARA 规则编写 | 恶意软件/Indicator 检测 |
| `semgrep-rules` | Semgrep 代码扫描规则 | 静态代码分析 |
| `semgrep-variants` | Semgrep 规则变体生成 | 规则覆盖增强 |
| `static-analysis-semgrep` | 基于 Semgrep 的静态分析 | 通用代码审计 |
| `static-analysis-codeql` | 基于 CodeQL 的静态分析 | 深度代码审计 |
| `sarif-analysis` | SARIF 格式分析结果处理 | 多工具集成 |
| `code-audit` | AI Agent 行为审计 | 实验代码审查 |
| `mutation-testing` | 变异测试 | 测试质量评估 |
| `fp-check` | 误报验证 | 检测规则优化 |
| `differential-review` | 差异代码审查 | Code review |

### 🟣 检测工程与 SOC 运营

| Skill | 用途 |
|-------|------|
| `siem-detection` | SIEM 检测规则工程 |
| `finding-triage` | 安全告警分诊与优先级排序 |
| `breach-patterns` | 入侵模式识别与分析 |
| `prompt-injection` | LLM 提示注入检测 |
| `soc-operations` | SOC 运营流程 |
| `briiirussell-threat-hunting` | 威胁狩猎方法论 |
| `masriyan-threat-hunting` | 威胁狩猎操作指南 |
| `log-analysis` | 日志分析模板与方法 |
| `network-security` | 网络安全基础 |
| `incident-response` | 应急响应流程 |
| `blue-team-defense` | 蓝队防御策略 |

## 使用方式

Skills 安装后无需"启动"，在 Claude Code 会话中直接调用即可：

```
/academic-research-suite: 针对「基于GNN的加密流量分类」做文献综述...
/neat
用 threat-intel-feeds 技能分析当前的威胁情报...
用 nature-figure 技能检查图表规范...
用 unslop 润色这段论文内容，强度等级 3...
```

不调用不占上下文（仅元数据 ~80 tokens/skill，55 个 Skills ≈ 4400 tokens）。

## 维护与进化

```bash
# 添加新 Skill
cp -r /path/to/new-skill ~/program/research-workflow-skills/

# 更新 Skill
cd ~/program/research-workflow-skills/new-skill
# 修改 SKILL.md 或替换整个目录



# 移除不需要的 Skill
rm -rf ~/program/research-workflow-skills/unused-skill

# 提交变更
git add -A && git commit -m "调整 Skills 配置"

# 重启 Claude Code 即可生效
```

## 参考

- [网络安全科研AI工作流完整指导书](https://github.com/...)
- [示例：基于图的预训练加密流量分类研究全流程](https://github.com/...)
