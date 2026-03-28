# LOW_RISK_BATCH1_REVISED

> 修订时间：2026-03-28
> 原因：项目归属审计发现之前"按文件类型归入中央目录"会破坏项目上下文
> 状态：**之前的 APPROVED_BATCH1.csv (55 项) 已暂停**

---

## 从原自动批次中移出的对象

### 移出 1：飞书项目文档（20 个 .md + 9 个 .html = 29 项）

**为什么移出**：这 29 个文件全部属于飞书集成项目（`2026-03-09_openclaw-feishu-setup`）。之前建议送到 `Dev\notes\feishu-research\`，但这会把项目核心上下文文档从项目中拆出来。正确做法是归入项目自己的 `docs/` 目录。

**正确目标**：
- 20 个 .md → `D:\AgentTeam-Workspace\2026-03-09_openclaw-feishu-setup\docs\`
- 9 个 .html → `D:\AgentTeam-Workspace\2026-03-09_openclaw-feishu-setup\captures\`（已有此目录）

### 移出 2：视频自动化文档（14 个 .md = 14 项）

**为什么移出**：这 14 个文件属于视频自动化项目（`bilibili-video-absorber`）。之前建议送到 `Dev\notes\video-automation-research\`，但拆出去会破坏研究链条。

**正确目标**：`D:\AgentTeam-Workspace\bilibili-video-absorber\docs\research\`

### 移出 3：桌面 HTML（1 项）

**为什么移出**：`ai-os-automation-flowchart.html` 项目归属不明确，升级为候审。

---

## 仍然适合进入第一批的对象（7 项）

这些是经过项目归属审计后，确认"不属于任何项目"的真正散落研究：

| # | 文件 | 目标 |
|---|------|------|
| 1 | temp-bing-h5support.html | D:\Archive\web-captures\ |
| 2 | temp-bing.html | D:\Archive\web-captures\ |
| 3 | adobe-davinci-automation-capabilities.json | D:\Archive\research-data-2026\ |
| 4 | ai-video-api-top30.json | D:\Archive\research-data-2026\ |
| 5 | video-editing-tools-scan.json | D:\Archive\research-data-2026\ |
| 6 | video-editing-tools-scan.raw.json | D:\Archive\research-data-2026\ |
| 7 | video-plugins-scan.json | D:\Archive\research-data-2026\ |

---

## 第一批是否建议执行？

**建议暂不执行**。理由：

1. 7 项体量太小（仅 2 个 HTML + 5 个 JSON），单独执行一个批次投入产出比低
2. 更重要的是先把 43 项"项目归属文档"归入各自项目内
3. 建议把 43 项项目归属 + 7 项散落研究合并为一个新的"完整归位批次"
4. 那个批次再做预检（确认项目内 docs/ 目录存在性、同名冲突等）后执行

---

## 数据对比

| 指标 | 之前 (Round 9) | 现在 (Round 10) |
|------|---------------|-----------------|
| "可自动执行"数量 | 55 | 7 (散落) + 43 (项目归属) = 50 (目标不同) |
| 目标路径类型 | 全部送中央 notes/archive | 43 送项目内 + 7 送中央 |
| Dev\notes\ 使用 | 39 项 | 0 项（不再使用中央 notes 吞并项目文档） |
| 需人工确认 | 10 | 19 (含新增的 8 个项目不明确 + 原有的 10 个 + 1 个升级候审) |

---

## Batch1 CSV 状态

`LOW_RISK_MOVE_APPROVED_BATCH1.csv` 状态：**已暂停**，被本文件取代。

后续执行应基于 `OWNERSHIP_REVIEW_MANIFEST.csv`，不再基于 APPROVED_BATCH1。
