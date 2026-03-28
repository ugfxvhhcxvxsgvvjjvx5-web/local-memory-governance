# AGENTTEAM_ROOT_CLASSIFICATION

> 分类时间：2026-03-28
> 范围：D:\AgentTeam-Workspace 一级目录（64 个子目录，现已清理空目录后约 62 个）
> 原则：只分类，不移动。与 WORKSPACE_DECISION.md 保持一致

---

## 层级 1：正式项目区

**所在位置：D:\AgentTeam-Workspace\Dev**

这是 WORKSPACE_DECISION.md 写死的唯一核心项目区。

| 目录 | 大小 | 说明 |
|------|------|------|
| Dev\personnal research | ~变动 | 当前资格系统 V1 主仓库 |
| Dev\Personnal session | ~变动 | 当前工作会话 |
| Dev\Learning | ~变动 | 学习项目 |
| Dev\ob life os | ~变动 | Obsidian 生活系统 |
| Dev\sandbox | ~变动 | 沙盒实验 |
| Dev\notes | ~变动 | 笔记 |
| Dev\Projects | ~变动 | 子项目集合 |
| Dev\tools | ~变动 | 工具 |
| Dev\work | ~变动 | 工作相关 |

* 分类原因：结构清晰，命名有意义，当前活跃使用
* 后续建议：**不动**。新正式项目继续在 Dev/ 下面建

还有一个在根下但属于正式项目：

| 目录 | 大小 | 说明 |
|------|------|------|
| local-memory-governance | 微小 | 本项目（磁盘治理） |

---

## 层级 2：一次性任务区

以日期命名的任务目录（2026-03-xx_xxx 格式），做完后就不再活跃。

| 目录 | 大小 | 最后修改 | 当前状态 |
|------|------|----------|----------|
| 2026-03-10_botdrop-part2 | 5,607 MB | 2026-03-28 | **候审**（最近还有活动） |
| 2026-03-09_openclaw-feishu-setup | 854 MB | 2026-03-09 | 冻结 |
| 2026-03-04_file-clean-up | 639 MB | 2026-03-04 | 冻结（旧清理残骸） |
| 2026-03-08_multi-project-manager | 266 MB | 2026-03-08 | 冻结 |
| 2026-03-06_inspiration-pool-system | 180 MB | 2026-03-07 | 冻结 |
| 2026-03-09_clash-update | 84 MB | 2026-03-09 | 冻结 |
| 2026-03-09_feishu-bot-permissions | 60 MB | 2026-03-09 | 冻结 |
| 2026-03-08_vault-indexing-speedup | 14 MB | 2026-03-10 | 冻结 |
| 2026-03-09_phone-pc-sync | 15 MB | 2026-03-09 | 冻结 |
| 2026-03-05_elden-ring-mod | 17 MB | 2026-03-05 | 冻结 |
| 2026-03-04_sort-txt-mess | 8 MB | 2026-03-05 | 冻结 |
| disk-governance-2026-03-04 | 8 MB | 2026-03-04 | 冻结（上次磁盘整理残骸） |
| 2026-03-08_vault-indexing-optimization | 2 MB | 2026-03-08 | 冻结 |
| 2026-03-04_batch-ingest-fix | 0.3 MB | 2026-03-05 | 冻结 |
| 2026-03-06_methodology-extraction | 0.1 MB | 2026-03-06 | 冻结 |
| 2026-03-04_baidu-netdisk-organizer | 0 MB | 2026-03-05 | 冻结 |
| 2026-03-04_project-init-system | 微小 | 2026-03-04 | 冻结 |
| 2026-03-08_openclaw-android-setup+ | 微小 | 2026-03-08 | 冻结 |
| 2026-03-10_botdrop-part2+ | 微小 | 2026-03-10 | 冻结 |
| 2026-03-11_codex-cpu-remediation | 0 | 2026-03-19 | 冻结 |
| 2026-03-08_openclaw-android-setup | 384 MB | 2026-03-19 | 冻结 |
| 2026-03-09_obsidian-investigation | 49 MB | 2026-03-19 | 冻结 |

* 数量：**~22 个目录**
* 分类原因：日期前缀 + 任务描述命名，典型的一次性任务模式
* 后续建议：未来考虑建 `D:\AgentTeam-Workspace\_archive\` 把冻结的任务目录集中收纳。不急，先不动

---

## 层级 3：独立工具 / 项目区

非 Dev 子目录，也不是日期命名任务，是独立存在的工具或项目。

| 目录 | 大小 | 状态 | 说明 |
|------|------|------|------|
| new idea | 13,030 MB | 候审 | 项目孵化集合，最近有活动 |
| bilibili-video-absorber | 267 MB | 冻结 | B站视频采集工具 |
| bilibili-batch-processor | 0.3 MB | 冻结 | B站批处理 |
| zhihu-scraper | 165 MB | 冻结 | 知乎采集器 |
| wechat-article-absorber | 0.2 MB | 冻结 | 微信文章采集器 |
| chat-screenshot-extractor | 0.3 MB | 冻结 | 聊天截图提取 |
| bookmark-is-learned | 42 MB | 冻结 | 书签学习工具 |
| batch-ingest-v2 | 1.4 MB | 冻结 | 批量摄入 v2 |
| antigravity-auto-accept-independent | 65 MB | 冻结 | Antigravity 自动接受插件 |
| auto-accept-clean | 128 MB | 冻结 | 自动接受插件清理版 |
| trans-recovery-project | 19 MB | 冻结 | 翻译恢复项目 |

* 数量：**~11 个目录**
* 分类原因：独立工具性质，有 .git 仓库，但不在 Dev 的正式项目体系里
* 后续建议：确认不再活跃后可移到 `Dev\tools\` 或 `_archive\`

---

## 层级 4：冻结 / 归档候选区

大型目录，不确定内部结构，需先审计再决定。

| 目录 | 大小 | 状态 | 说明 |
|------|------|------|------|
| opencode | 29,756 MB | **冻结** | OpenCode 安装/数据，可能含重要配置。需单独审计 |
| my_projects | 16,768 MB | **冻结** | 含 whisper_auto_transcribe 等。需确认哪些还有价值 |
| local-mem-v2 | 2,816 MB | **冻结** | 旧记忆系统 v2，PRIMARY_MEMORY_DECISION 已判决冻结 |
| happy-ddz | 3,716 MB | **冻结** | 斗地主 AI |
| doudizhu-ai | 1,242 MB | **冻结** | 斗地主 AI（可能与 happy-ddz 重叠） |
| acceptance-test | 748 MB | 冻结 | 验收测试 |
| agnet_consult | 625 MB | 冻结 | Agent 咨询部署 |
| local-mem | 0.8 MB | **归档候选** | PRIMARY_MEMORY_DECISION 已判决归档候选 |

* 数量：**8 个目录**
* 分类原因：体量大、内容不明确、已被各决策文件判决为冻结或归档候选
* 后续建议：不急着动。后续逐个审计 opencode 和 my_projects 的内容

---

## 层级 5：基础设施 / 杂项

| 目录 | 说明 | 建议 |
|------|------|------|
| docs | 文档 | 保留 |
| logs | 日志 | 定期清理 |
| playground | 实验场 | 保留 |
| _tmp_vsix_diff | VSIX 对比 (258 MB) | 归档候选 |
| vsix_extract_1 / vsix_extract_2 | VSIX 解压 (36 MB) | 归档候选 |
| _scan_summary.json | 扫描结果 (29 KB) | 保留 |
| DASHBOARD.md / WORKSPACE-STATUS.md | 元数据文件 | 保留 |
| new | 新建目录 (15 MB) | 候审——命名太模糊 |
| After | 归档后续 (0.1 MB) | 候审 |
| dev-workspace / release-workspace | AgentTeam 内部旧布局 (214 MB) | 归档候选 |
| obsidian-sync-stabilization-20260304 | Obsidian 同步稳定化 | 冻结 |
| learn-coding / healthcheck-config / project-scripts / my-product-txt | 小目录 | 候审 |

---

## 汇总

| 层级 | 数量 | 后续方向 |
|------|------|----------|
| 正式项目区 (Dev) | 9 + 1 | 不动 |
| 一次性任务区 | ~22 | 冻结，未来收纳到 _archive |
| 独立工具区 | ~11 | 冻结，确认后移到 Dev/tools 或 _archive |
| 冻结/归档候选 | 8 | 不急，逐个审计 |
| 基础设施/杂项 | ~15 | 混合处理 |
| **合计** | **~66** | — |
