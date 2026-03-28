# WORKSPACE_MAP

## 当前最像主工作区

* 路径：D:\AgentTeam-Workspace
* 原因：64 个子目录，最近修改日期集中在 2026-03，包含当前所有活跃项目（personnal research / Personnal session / Dev / new idea 等），所有新项目都在这里创建

## 互相重叠的工作区

1. **D:\AgentTeam-Workspace** — 当前主力，64 个子目录，~87 GB
2. **D:\Projects** — 旧工作区，14 个子目录，含音乐解密工具、ObsidianVault、0-inbox 等零散项目
3. **D:\Workspace** — 迁移中间产物，有 MIGRATION-INVENTORY.md 但 active/ 目录几乎空
4. **D:\Workspace-ing** — 另一次迁移尝试，只有 2 个项目（codexx、inspiration-pool-system）
5. **C:\Users\Administrator\Projects** — HOME 下的 Projects，只有 local-mem-v2 和 win11-system-perfecting
6. **C:\Users\Administrator\codex-work** — Codex 专用工作区
7. **C:\Users\Administrator\global-project-hub** — 又一个项目管理尝试

## 每个工作区的判断

### D:\AgentTeam-Workspace

* 路径：D:\AgentTeam-Workspace
* 像什么：当前真正的主工作区
* 状态建议：**现役**
* 备注：但内部极度膨胀（64 个子目录），大量是日期命名的一次性任务目录（如 2026-03-04_file-clean-up），需要内部分类。Dev/ 子目录是最核心的，里面有 personnal research、Personnal session 等

### D:\AgentTeam-Workspace\Dev

* 路径：D:\AgentTeam-Workspace\Dev
* 像什么：AgentTeam 内部的"正式项目区"
* 状态建议：**现役核心**
* 备注：9 个子目录（Learning / Personnal session / Projects / notes / ob life os / personnal research / sandbox / tools / work），结构最清晰

### D:\Projects

* 路径：D:\Projects
* 像什么：更早期的项目收集区
* 状态建议：**冻结**
* 备注：含 ObsidianVault（唯一有 .obsidian 目录的 Vault）、音乐解密工具（AudioDecrypt / KgmFilesTransfer / qmc-decode 等）、trans-organize。多数项目已不活跃

### D:\Workspace

* 路径：D:\Workspace
* 像什么：一次没完成的迁移
* 状态建议：**归档候选**
* 备注：有 MIGRATION-INVENTORY.md（7KB）和 MIGRATION-BATCH-01.md 记录迁移计划，但 active/ 目录只有一个 README.md。这次迁移显然中断了

### D:\Workspace-ing

* 路径：D:\Workspace-ing
* 像什么：另一次没完成的迁移
* 状态建议：**归档候选**
* 备注：只有 codexx/ 和 inspiration-pool-system/，可以合并回 AgentTeam-Workspace

### C:\Users\Administrator\Projects

* 路径：C:\Users\Administrator\Projects
* 像什么：HOME 下开的项目坑
* 状态建议：**归档候选**
* 备注：只有 local-mem-v2 和 win11-system-perfecting，可以合并回 D 盘

### C:\Users\Administrator\codex-work

* 路径：C:\Users\Administrator\codex-work
* 像什么：Codex 的工作目录
* 状态建议：**候审**
* 备注：需要确认是否还在被 Codex 使用

### C:\Users\Administrator\global-project-hub

* 路径：C:\Users\Administrator\global-project-hub
* 像什么：又一个项目管理尝试
* 状态建议：**归档候选**
* 备注：看名字像是和 D:\AgentTeam-Workspace\2026-03-08_unified-project-hub 重叠的概念

## AgentTeam-Workspace 内部分层

AgentTeam-Workspace 内部实际上有三类东西混在一起：

### 正式项目 (在 Dev/ 下, ~10 GB)

* Dev\personnal research — 主项目（当前资格系统）
* Dev\Personnal session — 当前工作会话
* Dev\Learning — 学习项目
* Dev\ob life os — Obsidian 生活系统
* Dev\sandbox — 沙盒实验

### 日期命名的一次性任务 (20+ 个)

* 2026-03-04_file-clean-up (639 MB)
* 2026-03-04_batch-ingest-fix
* 2026-03-04_sort-txt-mess
* 2026-03-05_elden-ring-mod
* 2026-03-06_inspiration-pool-system (180 MB)
* 2026-03-06_methodology-extraction
* 2026-03-08_multi-project-manager (266 MB)
* 2026-03-08_vault-indexing-optimization
* 2026-03-08_unified-project-hub
* 2026-03-09_clash-update (84 MB)
* 2026-03-09_feishu-bot-permissions (60 MB)
* 2026-03-09_openclaw-feishu-setup (854 MB)
* 2026-03-09_phone-pc-sync
* 2026-03-10_botdrop-part2 (5.6 GB)
* 2026-03-11_codex-cpu-remediation
* ... 等共 20+ 个

### 独立工具/项目 (散落在根目录)

* bilibili-video-absorber (267 MB)
* bilibili-batch-processor
* bookmark-is-learned
* chat-screenshot-extractor
* doudizhu-ai (1.2 GB)
* happy-ddz (3.7 GB)
* opencode (29.7 GB — 最大！)
* zhihu-scraper (165 MB)
* wechat-article-absorber
* local-mem / local-mem-v2 (2.8 GB)
* my_projects (16.8 GB)
* new idea (13 GB)

## 最大混乱来源

1. **HOME 根目录散落**：47 个 .md + 26 个脚本 + 大量 JSON/HTML/APK 直接丢在 C:\Users\Administrator 下面，从未归类
2. **AgentTeam-Workspace 膨胀**：64 个子目录平铺在一级，正式项目和一次性任务混在一起，没有分层
3. **重复工作区**：D:\Projects、D:\Workspace、D:\Workspace-ing、C:\Users\Administrator\Projects 互相重叠，每次迁移都留下残骸
4. **sqlite_mcp_server.db 病毒式扩散**：至少 11 个副本散落在各处
5. **下载文件夹从不清理**：3.4 GB 安装包堆积，多个重复下载

## 当前不要做什么

* 不要删 D:\Projects\ObsidianVault（可能是唯一正式 Vault）
* 不要删 iCloudDrive 下的 Obsidian 同步目录
* 不要动 D:\AgentTeam-Workspace\Dev（核心项目区）
* 不要删 HOME 下的 AGENTS.md / CLAUDE.md（系统配置）
* 不要把 opencode (29.7 GB) 直接删了（可能有重要数据/配置）
