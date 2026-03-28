# HANDOFF_NEXT_AI

> 最后更新：2026-03-28 20:42
> 更新者：Antigravity (Gemini)
> 适用于：任何 AI 接手此项目的第一步

---

## 你是谁、你在哪

你正在接手 **local-memory-governance** 项目。
路径：`D:\AgentTeam-Workspace\local-memory-governance`
GitHub：https://github.com/ugfxvhhcxvxsgvvjjvx5-web/local-memory-governance

目标：**搞清楚这台机器上到底有什么，解决文件散落、工作区重叠、只收不判的问题。**

## ⚠️ 高风险纠偏声明

**之前任何涉及 exe / 解压目录 / 配置文件 / 高风险运行资产迁移的想法，全部暂停，先审计再说。**

HIGH_RISK_NO_MOVE_RULES.md 优先级 **高于** DROP_RULES.md。

## 接手必读（按顺序）

1. **本文件**
2. `04_handoff\EXECUTION_LOG.md` — 完整执行流水账
3. `03_registry\ERROR_PATTERNS.md` — 7 个已知错误模式
4. `03_registry\HIGH_RISK_NO_MOVE_RULES.md` — 高风险纠偏（优先级最高）
5. `03_registry\DROP_RULES.md` — 普通内容归位规则
6. `02_reports\LOW_RISK_REHOME_RULES.md` — 低风险清单准入标准
7. `03_registry\WORKSPACE_DECISION.md` / `PRIMARY_VAULT_DECISION.md` / `PRIMARY_MEMORY_SYSTEM_DECISION.md`

## 当前项目状态

### 已完成
- [x] 全盘扫描 + 工作区地图
- [x] 三份正式判决（主工作区 / 主 Vault / 主记忆系统）
- [x] 批次 1 清理（23 项，948 MB）
- [x] 三区分类方案（HOME / 桌面 / AgentTeam）
- [x] HTML 仪表盘
- [x] 交接与错误追踪体系（4 文件）+ 7 个错误模式
- [x] DROP_RULES 归位规则（12 节 + 18 示例）
- [x] 高风险纠偏：51 条高风险资产 + 依赖风险说明
- [x] **批次 3A：低风险拟归位清单**（69 个候选对象，只列清单未执行）

### 未完成
- [ ] **批次 3B：执行低风险归位**（69 项中 58 项可自动执行，11 项需人工确认）
- [ ] HOME 根脚本依赖审计（gmn-proxy / codex-watchdog 等）
- [ ] 批次 2 清理（Downloads 安装包，受 HIGH_RISK 约束需逐个确认）
- [ ] AgentTeam 分层（建 _archive/）
- [ ] 审计 opencode (29.7 GB) / my_projects (16.8 GB)
- [ ] HTML 仪表盘双语版

### 本轮说明
本轮（Round 8）只做了"拟归位清单"，**没有实际移动任何文件**。清单中 69 个对象全部只是候选，等待下一步批准后执行。

## 已写死的决策

| 决策 | 结论 | 来源 |
|------|------|------|
| 唯一现役主工作区 | `D:\AgentTeam-Workspace` | WORKSPACE_DECISION.md |
| 唯一核心项目区 | `Dev` | WORKSPACE_DECISION.md |
| 主 Vault | iCloud 同步版 | PRIMARY_VAULT_DECISION.md |
| 主记忆系统 | memory-v2 | PRIMARY_MEMORY_SYSTEM_DECISION.md |
| 普通内容归位 | DROP_RULES.md | 12 节规则 |
| 高风险资产 | 不动不删不归档 | HIGH_RISK_NO_MOVE_RULES.md |
| 低风险清单准入 | LOW_RISK_REHOME_RULES.md | 严格类型过滤 |

## 永久规则

### 新内容产生时
先查 HIGH_RISK_NO_MOVE_RULES → 再查 DROP_RULES

### 每轮结束
更新 4 文件：HANDOFF / EXECUTION_LOG / ERROR_LOG / ERROR_PATTERNS
