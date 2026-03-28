# ERROR_PATTERNS

> 规则：发现某种错误重复出现或属于同一类问题时更新此文件
> 这是沉淀下来的"错误模式库"，新 AI 接手时必读

---

## 1. 工作区反复切换导致旧残骸堆积

### 典型表现

* 同一功能出现在多个路径（D:\Projects、D:\Workspace、D:\Workspace-ing、~\Projects 等）
* 每次迁移留下一批旧目录，没人回收
* 新 AI 或新工具默认在不同位置创建项目，加剧分裂

### 常见触发条件

* 用户或 AI 对"项目该建在哪"没有固定规则
* 每次新会话使用不同 AI 工具，各自有默认路径偏好
* 迁移做到一半中断，旧的没删新的已建

### 已出现位置

* D:\Projects（旧主工作区）
* D:\Workspace（迁移中断，有 MIGRATION-INVENTORY.md）
* D:\Workspace-ing（另一次迁移中断）
* C:\Users\Administrator\Projects
* C:\Users\Administrator\codex-work
* C:\Users\Administrator\global-project-hub

### 已知解决方式

* WORKSPACE_DECISION.md 已正式写死唯一主工作区
* 其他工作区标记为冻结/归档候选

### 规避规则

* 新项目只建在 D:\AgentTeam-Workspace\Dev 下
* 一次性任务建在 D:\AgentTeam-Workspace 根下（日期命名）
* 禁止在其他位置新开主工作区

### 当前状态

* 已解决 — 通过 WORKSPACE_DECISION.md 正式判决

---

## 2. 只收不判，文件落地后不归位

### 典型表现

* HOME 根目录散落 160+ 个文件（.md / .py / .json / .html / .apk 等）
* 桌面堆积 142 个文件（安装包、修改器、文档、截图混杂）
* 下载文件夹 3.4 GB 安装包从不清理，重复下载
* AgentTeam-Workspace 64 个子目录平铺在一级

### 常见触发条件

* AI 生成文件直接丢在当前工作目录（通常是 HOME）
* 下载完安装包后不清理
* 研究完一个话题后相关文件留在原地
* 没有"文件收下后归位到哪"的固定流程

### 已出现位置

* C:\Users\Administrator\（47 个 .md + 26 个脚本 + 大量临时件）
* C:\Users\Administrator\Desktop\（安装包 + 修改器直接放桌面）
* C:\Users\Administrator\Downloads\（多个重复下载）
* D:\ 根目录（6 个临时脚本）

### 已知解决方式

* HOME_ROOT_CLASSIFICATION.md 已分 9 类
* DESKTOP_CLASSIFICATION.md 已分 6 类
* 待执行实际归位

### 规避规则

* AI 生成研究文件应存入 D:\AgentTeam-Workspace\Dev\notes\ 对应子目录
* 安装包用完即删
* 临时脚本完成后归入 Archive 或 Dev\tools

### 当前状态

* 部分解决 — 已分类但未实际归位

---

## 3. AI 做完任务但没有固定交接文件

### 典型表现

* 上一次 AI 做了磁盘整理（disk-governance-2026-03-04），但没有留下接手说明
* 多轮对话之间信息断裂，新 AI 不知道前一轮做了什么
* 整理结果本身变成混乱的一部分（中文命名的元标注目录散落在 HOME）

### 常见触发条件

* 会话结束时没有固定的交接流程
* 没有约定"任务结束必须更新哪些文件"
* 不同 AI 工具的记忆系统互不相通

### 已出现位置

* D:\AgentTeam-Workspace\disk-governance-2026-03-04（上次整理残骸，无接手文件）
* C:\Users\Administrator 根下三个中文命名的元标注目录（上次 AI 整理留下的）
* 多个 .claude-projects-old / .vscode-projects-old 目录

### 已知解决方式

* 本轮建立了 4 文件交接体系（HANDOFF_NEXT_AI / EXECUTION_LOG / ERROR_LOG / ERROR_PATTERNS）
* 永久规则：每轮结束必须更新这 4 个文件

### 规避规则

* 任务结束前检查：这 4 个文件都更新了吗？
* 没更新 = 任务没完成

### 当前状态

* 已解决 — 交接体系已建立

---

## 4. 路径/目录判断错误，误以为空但实际有文件

### 典型表现

* 扫描阶段标记某些目录为"空目录，可删"
* 实际执行清理时发现目录内有 1~8 个文件
* 如果没有删前检查，会导致误删

### 常见触发条件

* 扫描时使用 `Measure-Object` 的 size=0 判断，但 size=0 可能是因为文件太小或扫描时跳过了某些文件
* 上一轮扫描时目录确实是空的，但后续操作产生了新文件
* Git 操作产生 .git 相关文件

### 已出现位置

* 批次 1 清理中的 10 个"空目录"（project-scripts / .claude-projects-old / healthcheck-config / learn-coding 等）

### 已知解决方式

* 代码在删除前硬检查 `Get-ChildItem` 是否返回空
* 非空目录一律跳过
* 跳过项记录到 CLEANUP_EXECUTION_BATCH1.md

### 规避规则

* 任何清理操作必须在删前用 `Get-ChildItem -Force` 验证目录为空
* 扫描阶段的"空目录"判断仅作为候选，不作为执行依据
* 永远不要基于 size=0 判断就直接删除

### 当前状态

* 已解决 — 防护逻辑已生效，无误删

---

## 5. 多个记忆系统并存，主系统未正式写死

### 典型表现

* 5 个不同的"记忆系统"目录散落在 HOME 和 AgentTeam-Workspace
* 不清楚哪个是当前在用的
* 新 AI 可能向错误的记忆系统写入数据

### 常见触发条件

* 记忆系统迭代（v1 → v2 → dev），但旧版没有下线
* 不同 AI 工具使用不同的记忆路径
* 没有唯一性判决

### 已出现位置

* C:\Users\Administrator\memory-v2（0.1 MB，23 文件 — 当前主力）
* C:\Users\Administrator\.local-mem（4.3 GB，19 文件 — 旧版巨大）
* C:\Users\Administrator\.local-mem-dev（147 MB，6414 文件 — 开发版）
* D:\AgentTeam-Workspace\local-mem（0.8 MB — 旧版）
* D:\AgentTeam-Workspace\local-mem-v2（2.8 GB，25132 文件 — 旧 v2）

### 已知解决方式

* PRIMARY_MEMORY_SYSTEM_DECISION.md 已正式判决 memory-v2 为唯一主系统
* 其他 4 个标记为冻结/归档候选

### 规避规则

* 新记忆只写入 C:\Users\Administrator\memory-v2
* 其他记忆目录不再写入
* 迁移时以 memory-v2 为唯一数据源

### 当前状态

* 已解决 — 通过 PRIMARY_MEMORY_SYSTEM_DECISION.md 正式判决

---

## 6. Obsidian Vault 多副本并存，主 Vault 不明确

### 典型表现

* 1 个正式 Vault + 1 个 iCloud 同步 Vault + 4 个备份散落
* 不清楚应该在哪个 Vault 里写笔记

### 常见触发条件

* Vault 备份/迁移操作留下多个副本
* iCloud 同步创建了额外路径

### 已出现位置

* C:\Users\Administrator\iCloudDrive\iCloud~md~obsidian（iCloud 同步主力）
* D:\Projects\ObsidianVault（旧正式 Vault）
* C:\Users\Administrator\backups\obsidian-vault-old
* C:\Users\Administrator\.obsidian-backup-20260226
* C:\Users\Administrator\.obsidian-indexeddb-backup-20260226
* C:\Users\Administrator\.obsidian-large-files-backup

### 已知解决方式

* PRIMARY_VAULT_DECISION.md 已正式判决 iCloud 同步版为主 Vault

### 规避规则

* 日常笔记写入 iCloud 同步 Vault
* D:\Projects\ObsidianVault 冻结
* 备份目录保留不动
* 如需迁移，以 iCloud 版为准

### 当前状态

* 已解决 — 通过 PRIMARY_VAULT_DECISION.md 正式判决

---

## 7. 高风险运行资产被当普通文件归位

### 典型表现

* 把 exe / 解压目录 / 便携软件 / 配置文件按 DROP_RULES 归位到 D:\software 或 Archive
* 移动后快捷方式失效、代理断裂、脚本找不到文件
* 风灵月影修改器移走后游戏启动后报错
* gmn-proxy.mjs 移走后代理不工作

### 常见触发条件

* AI 把 exe 等同于普通文件，套用 DROP_RULES 的归位逻辑
* 没有检查是否有快捷方式指向该路径
* 没有检查是否有脚本硬编码该路径
* 没有检查旁边是否有 dll / config / data 等伴随文件

### 已出现位置

* 在 SAFE_CLEANUP_PLAN.md 和 DESKTOP_CLASSIFICATION.md 中，曾将桌面 exe / 解压目录列入"应移出桌面"
* DROP_RULES.md 中曾写"安装包默认落到 D:\software\"
* 用户在 Round 7 纠偏，指出这些是高风险运行资产

### 已知解决方式

* 创建 HIGH_RISK_NO_MOVE_RULES.md，优先级高于 DROP_RULES
* 高风险资产在未审计前一律：不移动、不删除、不归档、不改名
* 创建 HIGH_RISK_ASSET_REGISTRY.csv 盘点全部高风险对象

### 规避规则

* 遇到 exe / 解压目录 / 配置 / 脚本 / dll，先查 HIGH_RISK_NO_MOVE_RULES.md
* 移动前必须回答 5 个问题：安装器还是运行体？单文件还是目录依赖？旁边有伴随文件吗？有快捷方式指向吗？像便携软件/修改器/启动器吗？
* 回答不了就标候审，不要动

### 当前状态

* 已解决 — 通过 HIGH_RISK_NO_MOVE_RULES.md 正式纠偏

---

## 8. 按文件类型整理破坏项目上下文

### 典型表现

* 项目自己的研究文档（需求分析、设计 review、数据采集 HTML）被按 .md / .html / .json 类型归入中央 `Dev\notes\` 或 `Archive\`
* 文件从项目语境中脱离，变成"孤立的文档"
* 未来想回溯某个项目的研究过程时，找不到配套文档

### 常见触发条件

* 以"文件类型"为第一分类维度（.md → notes / .html → web-captures / .json → research-data）
* 没有先判断"这个文件属于哪个项目"
* 误以为"统一收纳 = 整洁"，忽略了项目上下文的价值
* `Dev\notes\` 被设计成"万能收纳箱"但实际吞并了项目文档

### 已出现位置

* Round 8-9 中 55 项"可自动执行"中，43 项实际属于飞书集成和视频自动化两个项目
* 20 个飞书文档差点被送到 Dev\notes\feishu-research（应去项目 docs\）
* 14 个视频文档差点被送到 Dev\notes\video-automation-research（应去 bilibili-video-absorber\docs\）
* 9 个飞书 HTML 差点被送到 Archive\web-captures（应去项目 captures\）

### 已知解决方式

* 创建 PROJECT_OWNERSHIP_RULES.md：先按项目归属判，再按文件类型判
* 暂停 APPROVED_BATCH1.csv，改用 OWNERSHIP_REVIEW_MANIFEST.csv
* 项目文档默认跟项目走，不进中央目录

### 规避规则

* 遇到文件先问："这个文件属于哪个项目？"
* 文件名含项目关键词（feishu / video / botdrop）→ 属于该项目
* 只有确认"不属于任何项目"的文件才进中央 Archive / notes
* `Dev\notes\` 只用于"真正不属于任何项目的散落研究"
* 项目文档去项目自己的 doc/ / docs/ / research/ / captures/

### 当前状态

* 已解决 — 通过 PROJECT_OWNERSHIP_RULES.md 正式纠偏
