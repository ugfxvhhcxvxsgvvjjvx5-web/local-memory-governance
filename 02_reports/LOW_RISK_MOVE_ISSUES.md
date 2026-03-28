# LOW_RISK_MOVE_ISSUES

> 预检时间：2026-03-28 20:52
> 这是预检发现的问题清单，不包含 A 组（已通过预检的 55 项）

---

## 1. 目标路径不够具体

| 文件 | 原目标 | 问题 | 修正建议 |
|------|--------|------|----------|
| ex-girlfriend-context.json | "01-content 至 05-ideas 体系" | 不是绝对路径，无法执行 | 需人工指定具体目录 |

---

## 2. 必须人工确认的对象（10 项）

| 文件 | 原因 | 具体化目标 |
|------|------|-----------|
| cc-codex-video-workflows.md | 与 cc-codex-video-workflow.md 疑似重复 | `Dev\notes\video-automation-research\` |
| jimeng_video_common_config.json | 名含 config 可能是工具配置 | `D:\Archive\research-data-2026\` |
| ex-girlfriend-context.json | 个人敏感内容 + 目标不具体 | 需人工指定 |
| task-list.md | 旧会话残留，保留价值不明 | `D:\Archive\misc-docs-2026\` |
| conversation-history.md | 80KB 旧对话，保留价值不明 | `D:\Archive\misc-docs-2026\` |
| dashboard.md | 用途不确定 | `D:\Archive\misc-docs-2026\` |
| cc-windows-snapshot-2026-03-06.md | 用途不确定 | `D:\Archive\misc-docs-2026\` |
| AGENTS.backup.2026-02-16.md | 旧配置备份 | `C:\Users\Administrator\backups\` |
| 写代码必备.txt | 内容未读 | `Dev\notes\misc\` |
| 微信图片_20260323.jpg | 个人图片 | `C:\Users\Administrator\Pictures\` |

---

## 3. 不该进入归位批次的对象（3 项）

| 文件 | 原因 | 建议处理 |
|------|------|----------|
| tmp-playwright-output.txt | 应待删而非归位（0.4KB 临时调试输出） | 改为待删候选 |
| _tmp_tool_names.txt | 应待删而非归位（1.8KB 临时工具列表） | 改为待删候选 |
| 【ggs心委】_3月_信息反馈表.docx | 与本项目无关的个人文档 | 移出归位范围，人工单独处理 |

---

## 4. 同名冲突检查

**无冲突**。全部 9 个目标目录中均未发现与候选对象同名的文件。

---

## 5. 需要创建的目录（执行时先建）

| 目录 | 说明 |
|------|------|
| `D:\AgentTeam-Workspace\Dev\notes\feishu-research\` | 飞书研究文档归位目标 |
| `D:\AgentTeam-Workspace\Dev\notes\video-automation-research\` | 视频自动化研究归位目标 |
| `D:\AgentTeam-Workspace\Dev\notes\misc\` | 杂项笔记（C 组对象确认后使用） |
| `D:\Archive\` | Archive 根目录 |
| `D:\Archive\web-captures\` | HTML 抓取归位目标 |
| `D:\Archive\research-data-2026\` | 研究数据归位目标 |
| `D:\Archive\misc-docs-2026\` | 杂项文档归位目标（C 组对象确认后使用） |

---

## 6. 建议改为"待删候选"

| 文件 | 原因 |
|------|------|
| tmp-playwright-output.txt | 0.4 KB 临时调试输出，无保留价值 |
| _tmp_tool_names.txt | 1.8 KB 临时工具列表，无保留价值 |
