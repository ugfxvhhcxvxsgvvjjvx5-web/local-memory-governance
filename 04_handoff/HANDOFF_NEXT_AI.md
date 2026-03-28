# HANDOFF_NEXT_AI

> 最后更新：2026-03-28 19:56
> 更新者：Antigravity (Gemini)
> 适用于：任何 AI 接手此项目的第一步

---

## 你是谁、你在哪

你正在接手 **local-memory-governance** 项目。
路径：`D:\AgentTeam-Workspace\local-memory-governance`
GitHub：https://github.com/ugfxvhhcxvxsgvvjjvx5-web/local-memory-governance

这个项目的目标是：**搞清楚这台 Windows 电脑上到底有什么，解决文件散落、工作区重叠、只收不判的混乱问题。**

## 接手必读（按顺序）

1. **本文件** — 你正在读的这个
2. `04_handoff\EXECUTION_LOG.md` — 完整执行流水账，看已经做了什么
3. `03_registry\ERROR_PATTERNS.md` — 已知错误模式，避免重复踩坑
4. `03_registry\DROP_RULES.md` — **新增** — 归位规则，新内容该放哪
5. `03_registry\WORKSPACE_DECISION.md` — 已写死的工作区判决
6. `03_registry\PRIMARY_VAULT_DECISION.md` — 已写死的 Vault 判决
7. `03_registry\PRIMARY_MEMORY_SYSTEM_DECISION.md` — 已写死的记忆系统判决

## 当前项目状态

### 已完成
- [x] 全盘扫描（C 盘 HOME / 桌面 / 下载 / D 盘全部工作区）
- [x] 工作区地图绘制（7 个互相重叠的工作区已识别）
- [x] 三份正式判决写死（主工作区 / 主 Vault / 主记忆系统）
- [x] 批次 1 超保守清理（23 项，释放 948 MB）
- [x] 三区分类方案（HOME 根 / 桌面 / AgentTeam-Workspace）
- [x] HTML 可视化仪表盘
- [x] PATH_REGISTRY.csv + ACTIVE_ASSET_REGISTRY.csv
- [x] 交接与错误追踪体系（4 文件）
- [x] 6 个已知错误模式沉淀
- [x] **DROP_RULES 归位规则体系**（12 节规则 + 18 个示例）

### 未完成
- [ ] 批次 2 清理（Downloads 旧安装包 ~2.5 GB）
- [ ] HOME 根目录文件实际归位（飞书 20 个 + 视频自动化 19 个 .md → Archive 或 Dev/notes）
- [ ] 桌面安装包和解压残留移出
- [ ] AgentTeam-Workspace 一级目录分层（建 _archive/ 收纳冻结任务）
- [ ] 审计 opencode (29.7 GB) / my_projects (16.8 GB) 内容
- [ ] HTML 仪表盘双语版（专业版 + 洗脚城大爷版）

## 已写死的决策（不可推翻）

| 决策 | 结论 | 来源文件 |
|------|------|----------|
| 唯一现役主工作区 | `D:\AgentTeam-Workspace` | WORKSPACE_DECISION.md |
| 唯一现役核心项目区 | `D:\AgentTeam-Workspace\Dev` | WORKSPACE_DECISION.md |
| 主 Vault | `iCloudDrive\iCloud~md~obsidian` | PRIMARY_VAULT_DECISION.md |
| 主记忆系统 | `C:\Users\Administrator\memory-v2` | PRIMARY_MEMORY_SYSTEM_DECISION.md |
| 新内容归位规则 | 见 DROP_RULES.md 12 节 | DROP_RULES.md |

## 永久规则

### 新内容产生时
任何 AI 在此项目里新增文件、脚本、研究、截图、导出、安装包、任务目录之前，**必须先遵循** `03_registry\DROP_RULES.md`

### 每轮任务结束时
必须同步更新以下 4 个文件，否则任务不算完成：

1. `04_handoff\HANDOFF_NEXT_AI.md` — 覆盖更新，保持永远最新
2. `04_handoff\EXECUTION_LOG.md` — 追加写入
3. `04_handoff\ERROR_LOG.md` — 追加写入（无错误也要写"本轮无新错误"）
4. `03_registry\ERROR_PATTERNS.md` — 发现重复错误时更新

## 禁止做的事

* 不删除 Dev
* 不删除正式 Obsidian Vault
* 不做大迁移
* 不在别的地方新开主工作区
* 不删除 opencode / my_projects / new idea（未审计）
* 不盲删非空目录
* 不把新内容散落在 HOME 根（见 DROP_RULES）

## 已知冲突

本轮未发现已有分类和已有判决之间的冲突。
