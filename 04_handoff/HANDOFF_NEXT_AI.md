# HANDOFF_NEXT_AI

> 最后更新：2026-03-28 21:22
> 更新者：Antigravity (Gemini)

---

## 你是谁、你在哪

项目：**local-memory-governance**
路径：`D:\AgentTeam-Workspace\local-memory-governance`

## ⚠️ 重大纠偏声明

**之前按文件类型直接归位的思路已暂停，改为先做项目归属审计。**

核心发现：之前"可自动执行"的 55 项中，43 项实际属于具体项目的上下文文档。按类型送到中央 `Dev\notes\` 会破坏项目上下文完整性。

**现行规则优先级**：
1. `HIGH_RISK_NO_MOVE_RULES.md` — 高风险不动
2. `PROJECT_OWNERSHIP_RULES.md` — 先按项目归属判
3. `DROP_RULES.md` — 再按类型判（仅适用于真正散落的）

## 接手必读

1. 本文件
2. `04_handoff\EXECUTION_LOG.md`
3. `03_registry\ERROR_PATTERNS.md`（8 个已知模式）
4. `03_registry\HIGH_RISK_NO_MOVE_RULES.md`
5. `03_registry\PROJECT_OWNERSHIP_RULES.md` — **新增**
6. `03_registry\DROP_RULES.md`

## 当前状态

### 已完成
- [x] 全盘扫描 + 工作区地图 + 三份判决
- [x] 批次 1 清理（23 项，948 MB）
- [x] 三区分类 + HTML 仪表盘
- [x] 交接体系 + 8 个错误模式
- [x] DROP_RULES + 高风险纠偏（51 条）
- [x] 低风险清单（69 项）+ 预检（55 通过）
- [x] **项目归属审计**：69 项重分类（43 属于项目 + 7 散落 + 8 不明 + 11 其他）

### 本轮说明
本轮（Round 10）完成了项目归属审计。**没有执行任何移动。** 之前的 `APPROVED_BATCH1.csv` 已暂停。

### 未完成
- [ ] **新批次**：43 项项目归属文档归入各自项目 + 7 项散落归 Archive（需重新预检）
- [ ] B 组 8 项人工确认项目归属
- [ ] HOME 根脚本依赖审计
- [ ] Downloads 安装包清理
- [ ] opencode / my_projects 审计

## 已写死的决策

| 决策 | 来源 |
|------|------|
| 高风险不动 | HIGH_RISK_NO_MOVE_RULES.md |
| 项目文档跟项目走 | PROJECT_OWNERSHIP_RULES.md |
| 只有散落的才进中央 | PROJECT_OWNERSHIP_RULES.md |
| APPROVED_BATCH1 已暂停 | LOW_RISK_BATCH1_REVISED.md |

## 永久规则

每轮结束更新 4 文件：HANDOFF / EXECUTION_LOG / ERROR_LOG / ERROR_PATTERNS
