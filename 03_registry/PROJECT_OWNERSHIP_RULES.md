# PROJECT_OWNERSHIP_RULES

> 定稿时间：2026-03-28
> 状态：正式写死
> 优先级：高于 LOW_RISK_MOVE_APPROVED_BATCH1.csv

---

## 核心原则

**先按项目归属判，再按文件类型判。**

之前按"文件类型（.md / .html / .json）"直接归入中央 notes / archive 的思路已暂停。改为先判断"这个文件属于哪个项目"，再决定它应该去项目内还是中央归位目录。

---

## 规则 1：项目自己的文档跟项目走

项目自己的文档，默认跟项目走，不进入中央归位目录。

**项目文档包括但不限于**：
- README / QUICKSTART / ARCHITECTURE / SUMMARY
- 研究文档（为了做这个项目而产生的研究）
- 设计说明 / 需求分析 / 计划文档
- 调试记录 / 测试报告
- 交接文件 / 操作手册
- html 页面抓取（为了这个项目做的数据采集）
- json 扫描结果（为了这个项目做的数据采集）

## 规则 2：项目文档的默认归位

项目自己的文档应优先进入该项目自己的 `doc/` / `docs/` / `research/` / `reports/` 体系。

如果项目目录里没有这些子目录，应在项目内新建，而不是往中央目录塞。

## 规则 3：只有"真正散落"的才进中央目录

只有明确"不属于任何项目"的材料，才进入中央 Archive 或 Dev\notes。

判断标准：
- 文件名不含任何项目关键词
- 文件内容不是为了某个项目而产生的
- 创建时间和已知项目活跃期无关

## 规则 4：local-memory-governance 的边界

`local-memory-governance` 负责：规则、索引、判决、审计、指针。

`local-memory-governance` **不负责**吞并所有项目文档。它是"治理中枢"不是"文档仓库"。

## 规则 5：归位暂停条件

在项目归属未判清前，暂停执行 `LOW_RISK_MOVE_APPROVED_BATCH1.csv`。

只有当一个对象的项目归属已经明确判定为"不属于任何项目"时，才允许进入中央归位批次。

---

## 项目归属判定流程

```
1. 文件名含项目关键词？
   → 是 → 属于该项目 → 归入项目内
   → 否 → 继续

2. 文件内容是为了某个已知项目而产生的？
   → 是 → 属于该项目 → 归入项目内
   → 否 → 继续

3. 文件创建时间与某个项目活跃期重叠？
   → 是 → 候审（可能属于该项目）
   → 否 → 继续

4. 上面全不是？
   → 真正散落 → 可进中央 Archive / notes
```

---

## 已知项目关键词映射

| 项目 | 关键词 | 路径 |
|------|--------|------|
| 飞书集成 | feishu / lark / 飞书 / openclaw | `2026-03-09_feishu-bot-permissions`, `2026-03-09_openclaw-feishu-setup` |
| 视频自动化 | video / whisper / transcri / automation / bilibili / 剪辑 / 即梦 / jimeng / douyin | `bilibili-video-absorber` |
| Botdrop | botdrop / bot-drop | `2026-03-10_botdrop-part2` |
| Codex 修复 | codex / codex-cpu | `2026-03-11_codex-cpu-remediation` |
| 本地治理 | governance / cleanup / scan | `local-memory-governance` |
