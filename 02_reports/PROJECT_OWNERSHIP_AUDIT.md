# PROJECT_OWNERSHIP_AUDIT

> 审计时间：2026-03-28
> 原则：**先按项目归属判，再按文件类型判**
> 对象范围：LOW_RISK_MOVE_APPROVED_BATCH1.csv 中 55 项 + ISSUES 中 14 项 = 69 项

---

## A. 属于具体项目，应留在项目内（43 项）

### A1. 飞书项目文档（20 项）→ 属于飞书集成项目

| 文件 | 归属项目 | 判定依据 |
|------|----------|----------|
| FEISHU_CONFIGURATION_SUMMARY.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_FEATURES_RESEARCH.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_FILES_LIST.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_IMPLEMENTATION_PLAN.md | 飞书集成 | 文件名含 FEISHU，88KB 核心设计文档 |
| FEISHU_INTEGRATION_ROADMAP.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_P0_FIXES.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_P0_REVIEW_FINAL.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PHASE0_PRETASKS.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PHASE0_PRETASKS_STATUS.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PLAN_REVIEW_CC.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PLAN_REVIEW_CC_ROUND2.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PLAN_REVIEW_CODEX.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PLAN_REVIEW_CODEX_ROUND2.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_PLAN_REVIEW_FINAL.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_ROUND3_ANSWERS.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_ROUND3_QUESTIONS.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_ROUND4_ANSWERS.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_SIMPLE_REPORT.md | 飞书集成 | 文件名含 FEISHU |
| FEISHU_USER_REQUIREMENTS_ROUND2.md | 飞书集成 | 文件名含 FEISHU |
| 飞书配置完成报告.md | 飞书集成 | 中文文件名含飞书 |

**建议归位**：`D:\AgentTeam-Workspace\2026-03-09_openclaw-feishu-setup\docs\`（这是更完整的飞书项目目录）

**为什么不该去 Dev\notes\feishu-research**：这些不是"泛泛的飞书研究笔记"，它们是飞书集成项目的核心上下文文档（需求、设计、review、交接）。拆到中央 notes 会破坏项目的上下文完整性。

### A2. 飞书项目 HTML 抓取（9 项）→ 属于飞书集成项目

| 文件 | 归属项目 | 判定依据 |
|------|----------|----------|
| temp-feishu-app-permissions.html | 飞书集成 | 名含 feishu，是飞书权限页面截取 |
| temp-feishu-download.html | 飞书集成 | 名含 feishu |
| temp-feishu-page-1~4.html | 飞书集成 | 名含 feishu |
| temp-feishu-privacy.html | 飞书集成 | 名含 feishu |
| temp-feishu-search-jsapi.html | 飞书集成 | 名含 feishu |
| temp-lark-home.html | 飞书集成 | 名含 lark（飞书国际版） |

**建议归位**：`D:\AgentTeam-Workspace\2026-03-09_openclaw-feishu-setup\captures\`（项目目录已有 captures 子目录）

### A3. 视频自动化项目文档（14 项）→ 属于视频自动化研究

| 文件 | 归属项目 | 判定依据 |
|------|----------|----------|
| video-automation-10-questions.md | 视频自动化 | 名含 video-automation |
| video-automation-round2~4-questions(-v2).md (5个) | 视频自动化 | 名含 video-automation |
| video-tools-test-report.md | 视频自动化 | 名含 video-tools |
| viral-video-replication-research.md | 视频自动化 | 名含 viral-video |
| ai-video-editing-research.md | 视频自动化 | 名含 video-editing |
| ai-video-editing-final-summary.md | 视频自动化 | 名含 video-editing |
| ai-video-editing-solution.md | 视频自动化 | 名含 video-editing |
| ai-models-for-video.md | 视频自动化 | 名含 video |
| ai-vs-manual-editing-layman-guide.md | 视频自动化 | AI vs 手工剪辑对比，视频项目上下文 |

**建议归位**：`D:\AgentTeam-Workspace\bilibili-video-absorber\docs\research\`

**为什么不该去 Dev\notes\video-automation-research**：这些文档是视频自动化研究的核心上下文，与 `bilibili-video-absorber` 项目直接相关。分离出去会破坏研究链条。

---

## B. 属于项目，但项目归属还不明确（8 项）

| 文件 | 可能归属 | 不确定原因 |
|------|----------|-----------|
| adobe-bridge-tools-guide.md | 视频自动化? | 名含 adobe，可能是视频后期工具调研，但也可能是独立兴趣 |
| cc-codex-video-workflow.md | 视频自动化? / Codex? | 名含 cc-codex 和 video，交叉归属 |
| cc-codex-video-workflows.md | 视频自动化? / Codex? | 与上面疑似重复，交叉归属 |
| deep-automation-tech-routes.md | 视频自动化? | 名含 automation 但更泛 |
| douyin-effects-guide.md | 视频自动化? | 名含 douyin，可能属于视频项目 |
| jimeng-playwright-research.md | 视频自动化? | 名含 jimeng（即梦），可能属于视频项目 |
| local-tools-test-report.md | 视频自动化? | 本地工具测试，可能属于视频工具调研 |
| jimeng_video_common_config.json | 视频自动化? | 名含 jimeng_video，但也含 config |

**后续处理**：需人工确认。如果属于视频项目则归入 `bilibili-video-absorber\docs\`，否则归入中央 Archive。

---

## C. 不属于具体项目，是真正散落研究（7 项）

| 文件 | 判定依据 | 建议归位 |
|------|----------|----------|
| temp-bing-h5support.html | Bing 搜索抓取，与任何项目无关 | D:\Archive\web-captures\ |
| temp-bing.html | Bing 搜索抓取 | D:\Archive\web-captures\ |
| adobe-davinci-automation-capabilities.json | 工具能力扫描，泛研究 | D:\Archive\research-data-2026\ |
| ai-video-api-top30.json | API 排名扫描，泛研究 | D:\Archive\research-data-2026\ |
| video-editing-tools-scan.json | 工具扫描，泛研究 | D:\Archive\research-data-2026\ |
| video-editing-tools-scan.raw.json | 工具扫描原始数据 | D:\Archive\research-data-2026\ |
| video-plugins-scan.json | 插件扫描，泛研究 | D:\Archive\research-data-2026\ |

**为什么判为散落**：这些是泛研究型扫描结果，不是为了某个具体项目做的，更像是"先扫再看"的探索性数据。文件名不含特定项目关键词。

---

## D. 属于个人内容（1 项）

| 文件 | 判定依据 | 建议 |
|------|----------|------|
| ex-girlfriend-context.json | 个人情感内容 | 需人工指定具体目录，不按项目归位 |

---

## E. 属于临时输出 / 待删候选 / 杂项（10 项）

| 文件 | 分类 | 建议 |
|------|------|------|
| tmp-playwright-output.txt | 临时调试 | 待删候选 |
| _tmp_tool_names.txt | 临时调试 | 待删候选 |
| task-list.md | 旧会话残留 | 候审（可能属于某个会话上下文） |
| conversation-history.md | 旧会话记录 | 候审 |
| dashboard.md | 用途不明 | 候审 |
| cc-windows-snapshot-2026-03-06.md | 系统快照 | 候审 |
| AGENTS.backup.2026-02-16.md | 配置备份 | 留在 backups/ |
| 【ggs心委】_3月_信息反馈表.docx | 个人事务 | 人工处理 |
| 写代码必备.txt | 用途不明 | 候审 |
| 微信图片_20260323.jpg | 个人图片 | 人工处理 |
| ai-os-automation-flowchart.html | 用途不明 | 候审（可能属于某个项目？） |

---

## 审计总结

| 类别 | 数量 | 占比 | 之前处理方式 | 纠正后处理方式 |
|------|------|------|-------------|---------------|
| A 属于项目 | 43 | 62% | 全部送中央 notes/archive | **归入项目内 doc/** |
| B 项目不明确 | 8 | 12% | 全部送中央 notes | **候审，人工确认** |
| C 真正散落 | 7 | 10% | 送 Archive | **仍然送 Archive（正确）** |
| D 个人内容 | 1 | 1% | 送"体系" | **人工处理** |
| E 临时/杂项 | 10 | 14% | 部分送 Archive | **候审/待删/人工** |
| **合计** | **69** | 100% | — | — |

**结论**：之前 55 项"可自动执行"中，实际只有 7 项适合去中央 Archive。其余 43 项属于具体项目的上下文文档，不应拆出去。
