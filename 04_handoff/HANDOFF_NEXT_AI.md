# HANDOFF_NEXT_AI

> 最后更新：2026-03-28 20:13
> 更新者：Antigravity (Gemini)
> 适用于：任何 AI 接手此项目的第一步

---

## 你是谁、你在哪

你正在接手 **local-memory-governance** 项目。
路径：`D:\AgentTeam-Workspace\local-memory-governance`
GitHub：https://github.com/ugfxvhhcxvxsgvvjjvx5-web/local-memory-governance

这个项目的目标是：**搞清楚这台 Windows 电脑上到底有什么，解决文件散落、工作区重叠、只收不判的混乱问题。**

## ⚠️ 高风险纠偏声明

**之前任何涉及 exe / 解压目录 / 配置文件 / 高风险运行资产迁移的想法，全部暂停，先审计再说。**

HIGH_RISK_NO_MOVE_RULES.md 优先级 **高于** DROP_RULES.md。对于 exe、解压目录、便携软件、配置文件、脚本等高风险资产：**不移动、不删除、不归档、不改名**，直到完成依赖审计。

## 接手必读（按顺序）

1. **本文件** — 你正在读的这个
2. `04_handoff\EXECUTION_LOG.md` — 完整执行流水账
3. `03_registry\ERROR_PATTERNS.md` — 已知错误模式
4. `03_registry\HIGH_RISK_NO_MOVE_RULES.md` — **高风险纠偏规则（优先级最高）**
5. `03_registry\DROP_RULES.md` — 普通内容归位规则
6. `03_registry\WORKSPACE_DECISION.md` — 工作区判决
7. `03_registry\PRIMARY_VAULT_DECISION.md` — Vault 判决
8. `03_registry\PRIMARY_MEMORY_SYSTEM_DECISION.md` — 记忆系统判决

## 当前项目状态

### 已完成
- [x] 全盘扫描（C / D 盘全部工作区）
- [x] 工作区地图（7 个重叠工作区）
- [x] 三份正式判决（主工作区 / 主 Vault / 主记忆系统）
- [x] 批次 1 清理（23 项，948 MB）
- [x] 三区分类方案（HOME / 桌面 / AgentTeam）
- [x] HTML 仪表盘
- [x] 交接与错误追踪体系（4 文件）
- [x] 6 个错误模式沉淀
- [x] DROP_RULES 归位规则（12 节 + 18 示例）
- [x] **高风险纠偏**：HIGH_RISK_NO_MOVE_RULES + 51 条高风险资产盘点 + 桌面高风险报告 + 7 种依赖风险说明

### 未完成
- [ ] 批次 2 清理（Downloads 安装包，但现在受 HIGH_RISK_NO_MOVE_RULES 约束，需先逐个确认）
- [ ] HOME 根目录 .md 文件归位（这些是普通文档，可按 DROP_RULES 处理）
- [ ] AgentTeam 分层（建 _archive/）
- [ ] 审计 opencode (29.7 GB) / my_projects (16.8 GB)
- [ ] 审计 HOME 根脚本的依赖关系（gmn-proxy / codex-watchdog 等）
- [ ] HTML 仪表盘双语版

## 已写死的决策

| 决策 | 结论 | 来源 |
|------|------|------|
| 唯一现役主工作区 | `D:\AgentTeam-Workspace` | WORKSPACE_DECISION.md |
| 唯一核心项目区 | `D:\AgentTeam-Workspace\Dev` | WORKSPACE_DECISION.md |
| 主 Vault | `iCloudDrive\iCloud~md~obsidian` | PRIMARY_VAULT_DECISION.md |
| 主记忆系统 | `memory-v2` | PRIMARY_MEMORY_SYSTEM_DECISION.md |
| 普通内容归位规则 | 见 12 节 | DROP_RULES.md |
| 高风险资产纠偏 | 不动不删不归档 | HIGH_RISK_NO_MOVE_RULES.md |

## 永久规则

### 新内容产生时
先遵循 `DROP_RULES.md`，但如果涉及高风险资产则遵循 `HIGH_RISK_NO_MOVE_RULES.md`

### 每轮任务结束时
必须更新 4 个文件：HANDOFF_NEXT_AI / EXECUTION_LOG / ERROR_LOG / ERROR_PATTERNS

## 禁止做的事

* 不删 Dev / 不删 Vault / 不大迁移 / 不新开工作区
* 不删 opencode / my_projects / new idea
* 不盲删非空目录
* **不移动任何高风险运行资产（exe/解压目录/配置/脚本/dll）直到完成依赖审计**
