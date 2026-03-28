# LOW_RISK_MOVE_PRECHECK

> 预检时间：2026-03-28 20:52
> 原则：**只预检，不执行任何移动**
> 检查项：目标路径/目录存在性/同名冲突/人工确认需求/敏感性

---

## 目标目录状态

| 目标目录 | 是否存在 | 需创建 | 同名冲突 |
|----------|:--------:|:------:|:--------:|
| `D:\AgentTeam-Workspace\Dev\notes\feishu-research\` | 否 | 是（安全） | 无 |
| `D:\AgentTeam-Workspace\Dev\notes\video-automation-research\` | 否 | 是（安全） | 无 |
| `D:\AgentTeam-Workspace\Dev\notes\misc\` | 否 | 是（安全） | 无 |
| `D:\Archive\web-captures\` | 否 | 是（安全） | 无 |
| `D:\Archive\research-data-2026\` | 否 | 是（安全） | 无 |
| `D:\Archive\misc-docs-2026\` | 否 | 是（安全） | 无 |
| `C:\Users\Administrator\backups\` | 是（32 项） | 否 | 无（无同名） |
| `C:\Users\Administrator\Documents\` | 是（261 项） | 否 | 无（无同名） |
| `C:\Users\Administrator\Pictures\` | 是（25 项） | 否 | 无（有微信图片但不同名） |

**结论**：6 个目录需要新建（`Dev\notes` 已存在但子目录不存在，D:\Archive 也需创建）。所有目标目录无同名冲突。

---

## A. 可直接进入自动执行批次（55 项）

条件全部满足：目标路径明确绝对路径、无重名冲突、不需人工确认、不涉及删除、不涉及敏感内容。

### 飞书研究 .md → `D:\AgentTeam-Workspace\Dev\notes\feishu-research\`（20 项）

全部通过预检。文件名唯一，目标目录待创建无冲突。

| # | 文件名 | 大小 | 预检 |
|---|--------|------|:----:|
| 1 | FEISHU_CONFIGURATION_SUMMARY.md | 8 KB | PASS |
| 2 | FEISHU_FEATURES_RESEARCH.md | 23.4 KB | PASS |
| 3 | FEISHU_FILES_LIST.md | 3.7 KB | PASS |
| 4 | FEISHU_IMPLEMENTATION_PLAN.md | 88 KB | PASS |
| 5 | FEISHU_INTEGRATION_ROADMAP.md | 6.8 KB | PASS |
| 6 | FEISHU_P0_FIXES.md | 3.6 KB | PASS |
| 7 | FEISHU_P0_REVIEW_FINAL.md | 3.3 KB | PASS |
| 8 | FEISHU_PHASE0_PRETASKS.md | 8.5 KB | PASS |
| 9 | FEISHU_PHASE0_PRETASKS_STATUS.md | 4.6 KB | PASS |
| 10 | FEISHU_PLAN_REVIEW_CC.md | 18.3 KB | PASS |
| 11 | FEISHU_PLAN_REVIEW_CC_ROUND2.md | 13.3 KB | PASS |
| 12 | FEISHU_PLAN_REVIEW_CODEX.md | 16.9 KB | PASS |
| 13 | FEISHU_PLAN_REVIEW_CODEX_ROUND2.md | 5.3 KB | PASS |
| 14 | FEISHU_PLAN_REVIEW_FINAL.md | 10.4 KB | PASS |
| 15 | FEISHU_ROUND3_ANSWERS.md | 4.6 KB | PASS |
| 16 | FEISHU_ROUND3_QUESTIONS.md | 4.2 KB | PASS |
| 17 | FEISHU_ROUND4_ANSWERS.md | 3.3 KB | PASS |
| 18 | FEISHU_SIMPLE_REPORT.md | 16 KB | PASS |
| 19 | FEISHU_USER_REQUIREMENTS_ROUND2.md | 6.3 KB | PASS |
| 20 | 飞书配置完成报告.md | 8 KB | PASS |

### 视频自动化 .md → `D:\AgentTeam-Workspace\Dev\notes\video-automation-research\`（19 项）

包含原 11 个视频自动化 + 8 个其他研究（排除需人工确认的 cc-codex-video-workflows.md）。

| # | 文件名 | 大小 | 预检 |
|---|--------|------|:----:|
| 21 | video-automation-10-questions.md | 9.3 KB | PASS |
| 22 | video-automation-round2-questions.md | 8.2 KB | PASS |
| 23 | video-automation-round2-questions-v2.md | 5.3 KB | PASS |
| 24 | video-automation-round3-questions.md | 6.7 KB | PASS |
| 25 | video-automation-round4-questions.md | 5.9 KB | PASS |
| 26 | video-automation-round4-questions-v2.md | 5.7 KB | PASS |
| 27 | video-tools-test-report.md | 2.9 KB | PASS |
| 28 | viral-video-replication-research.md | 39.2 KB | PASS |
| 29 | ai-video-editing-research.md | 15 KB | PASS |
| 30 | ai-video-editing-final-summary.md | 10.8 KB | PASS |
| 31 | ai-video-editing-solution.md | 7.6 KB | PASS |
| 32 | ai-models-for-video.md | 21.9 KB | PASS |
| 33 | ai-vs-manual-editing-layman-guide.md | 9.1 KB | PASS |
| 34 | adobe-bridge-tools-guide.md | 14.9 KB | PASS |
| 35 | cc-codex-video-workflow.md | 16.9 KB | PASS |
| 36 | deep-automation-tech-routes.md | 33.2 KB | PASS |
| 37 | douyin-effects-guide.md | 33.1 KB | PASS |
| 38 | jimeng-playwright-research.md | 20.8 KB | PASS |
| 39 | local-tools-test-report.md | 29.1 KB | PASS |

### 临时 HTML 抓取 → `D:\Archive\web-captures\`（11 项）

| # | 文件名 | 大小 | 预检 |
|---|--------|------|:----:|
| 40 | temp-feishu-app-permissions.html | 1223 KB | PASS |
| 41 | temp-feishu-download.html | 171 KB | PASS |
| 42 | temp-feishu-page-1.html | 373 KB | PASS |
| 43 | temp-feishu-page-2.html | 6 KB | PASS |
| 44 | temp-feishu-page-3.html | 373 KB | PASS |
| 45 | temp-feishu-page-4.html | 171 KB | PASS |
| 46 | temp-feishu-privacy.html | 338 KB | PASS |
| 47 | temp-feishu-search-jsapi.html | 6 KB | PASS |
| 48 | temp-lark-home.html | 482 KB | PASS |
| 49 | temp-bing-h5support.html | 95 KB | PASS |
| 50 | temp-bing.html | 95 KB | PASS |

### 研究数据 JSON → `D:\Archive\research-data-2026\`（5 项）

排除需人工确认的 jimeng_video_common_config.json。

| # | 文件名 | 大小 | 预检 |
|---|--------|------|:----:|
| 51 | adobe-davinci-automation-capabilities.json | 92 KB | PASS |
| 52 | ai-video-api-top30.json | 21 KB | PASS |
| 53 | video-editing-tools-scan.json | 45 KB | PASS |
| 54 | video-editing-tools-scan.raw.json | 6491 KB | PASS |
| 55 | video-plugins-scan.json | 24 KB | PASS |

---

## B. 需要先修正目标路径（1 项）

| 文件名 | 原目标 | 问题 | 修正后目标 |
|--------|--------|------|-----------|
| ex-girlfriend-context.json | "01-content 至 05-ideas 体系" | 不是绝对路径，无法执行 | `C:\Users\Administrator\01-content\` 或由人工指定具体子目录 |

---

## C. 需要人工确认（10 项）

| # | 文件名 | 原因 | 建议目标 |
|---|--------|------|----------|
| 1 | cc-codex-video-workflows.md | 与 cc-codex-video-workflow.md 疑似重复 | Dev\notes\video-automation-research\ |
| 2 | jimeng_video_common_config.json | 名含 config 可能是工具配置 | D:\Archive\research-data-2026\ |
| 3 | ex-girlfriend-context.json | 个人敏感内容 + 目标路径不具体 | 需人工指定 |
| 4 | task-list.md | 用途不确定，可能是旧会话残留 | D:\Archive\misc-docs-2026\ |
| 5 | conversation-history.md | 80KB 对话记录，保留价值不明 | D:\Archive\misc-docs-2026\ |
| 6 | dashboard.md | 用途不确定 | D:\Archive\misc-docs-2026\ |
| 7 | cc-windows-snapshot-2026-03-06.md | 用途不确定 | D:\Archive\misc-docs-2026\ |
| 8 | AGENTS.backup.2026-02-16.md | 旧版配置备份，需确认参考价值 | C:\Users\Administrator\backups\ |
| 9 | 写代码必备.txt | 内容不确定 | D:\AgentTeam-Workspace\Dev\notes\misc\ |
| 10 | 微信图片_20260323201557.jpg | 个人图片，需确认保留价值 | C:\Users\Administrator\Pictures\ |

---

## D. 暂不处理（3 项）

| # | 文件名 | 原因 | 处理建议 |
|---|--------|------|----------|
| 1 | tmp-playwright-output.txt | 应该待删而不是归位（0.4 KB 临时调试输出） | 移入待删候选，不进归位批次 |
| 2 | _tmp_tool_names.txt | 应该待删而不是归位（1.8 KB 临时工具列表） | 移入待删候选，不进归位批次 |
| 3 | 【ggs心委】_3月_信息反馈表.docx | 与电脑文件整理无关的个人文档，不属于研究/代码归位范围 | 需人工决定：Documents 或直接保留桌面 |

---

## 特别检查 10 项结论

### 1. ex-girlfriend-context.json (48.5 KB)
* **结论**：不进入自动批次。目标路径必须人工指定。
* **建议**：用户决定放到 `01-content\` 还是 `03-relationships\` 还是其他。

### 2. tmp-playwright-output.txt (0.4 KB)
* **结论**：从归位清单移出，改为待删候选。
* **原因**：临时调试输出，无保留价值。

### 3. _tmp_tool_names.txt (1.8 KB)
* **结论**：从归位清单移出，改为待删候选。
* **原因**：临时工具名列表，无保留价值。

### 4. task-list.md (18.5 KB)
* **结论**：留在清单，但需人工确认。
* **具体化目标**：`D:\Archive\misc-docs-2026\task-list.md`

### 5. conversation-history.md (80.5 KB)
* **结论**：留在清单，但需人工确认。
* **具体化目标**：`D:\Archive\misc-docs-2026\conversation-history.md`

### 6. dashboard.md (10.3 KB)
* **结论**：留在清单，但需人工确认。
* **具体化目标**：`D:\Archive\misc-docs-2026\dashboard.md`

### 7. AGENTS.backup.2026-02-16.md (14.5 KB)
* **结论**：留在清单，但需人工确认。
* **具体化目标**：`C:\Users\Administrator\backups\AGENTS.backup.2026-02-16.md`
* **无同名冲突**：backups 目录下无此文件。

### 8. 【ggs心委】_3月_信息反馈表.docx (13.2 KB)
* **结论**：从归位清单移出。
* **原因**：与本项目（代码/研究归位）无关的个人文档，需人工单独处理。

### 9. 写代码必备.txt (13.4 KB)
* **结论**：留在清单，但需人工确认。
* **具体化目标**：`D:\AgentTeam-Workspace\Dev\notes\misc\写代码必备.txt`
* **原因**：内容未读，不确定是笔记还是教程。

### 10. 微信图片_20260323201557.jpg (1032 KB)
* **结论**：留在清单，但需人工确认。
* **具体化目标**：`C:\Users\Administrator\Pictures\微信图片_20260323201557_167_2554.jpg`
* **无同名冲突**：Pictures 下有其他微信图片但无此文件。

---

## 预检总结

| 组别 | 数量 | 说明 |
|------|------|------|
| A 可自动执行 | 55 | 全部通过预检 |
| B 需修正路径 | 1 | ex-girlfriend-context.json |
| C 需人工确认 | 10 | 含敏感/不确定/疑似重复 |
| D 暂不处理 | 3 | 2 个改待删 + 1 个移出归位范围 |
| **合计** | **69** | — |
