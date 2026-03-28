# DROP_RULES

> 这是"新文件 / 新脚本 / 新研究 / 新截图 / 新安装包 / 新项目 / 新一次性任务"产生后的默认落点规则。
> 以后任何 AI 或人工处理新内容时，优先按这个文件执行，不再临时凭感觉决定放哪。
>
> 定稿时间：2026-03-28
> 状态：正式写死

---

## 1. 总原则

* 新东西**不允许**继续散落在 HOME 根目录（`C:\Users\Administrator\`）
* 桌面**默认只允许快捷方式**，不允许长期堆安装包、zip、文档、截图、解压目录
* 新正式项目**只建在** `D:\AgentTeam-Workspace\Dev\` 下
* 新一次性任务**只建在** `D:\AgentTeam-Workspace\` 根下，用 `YYYY-MM-DD_task-name` 格式命名
* 主 Vault 相关内容遵循 `PRIMARY_VAULT_DECISION.md`（主 Vault = iCloud 同步版）
* 主记忆系统相关内容遵循 `PRIMARY_MEMORY_SYSTEM_DECISION.md`（主系统 = memory-v2）
* 任何不确定的内容**先进入"候审"**，不要乱删也不要乱归位

---

## 2. 新研究文档默认落点

| 类型 | 默认落点 |
|------|----------|
| 飞书相关研究文档 | `D:\AgentTeam-Workspace\Dev\notes\feishu-research\` |
| 视频自动化研究文档 | `D:\AgentTeam-Workspace\Dev\notes\video-automation-research\` |
| 通用方法论 / 调研总结 | `D:\AgentTeam-Workspace\Dev\notes\{对应主题}\` |
| 产品理解 / 项目分析文档 | 对应项目的 `doc\` 子目录 |
| 历史已冻结研究（查完不再更新） | `D:\Archive\{对应主题}\` |
| 个人内容 / 情感类文档 | `C:\Users\Administrator\01-content\` 到 `05-ideas\` 体系内 |

**规则**：研究文档产生时就归位，不要先扔 HOME 根再说。如果不确定主题归属，先放 `Dev\notes\misc\`。

---

## 3. 新脚本默认落点

| 类型 | 默认落点 | 说明 |
|------|----------|------|
| 正式长期工具脚本 | `D:\AgentTeam-Workspace\Dev\tools\` | 有明确用途、会反复使用的 |
| 与系统启动强耦合的脚本/配置 | 保留在 HOME | 必须注明原因（如被计划任务引用） |
| 一次性临时研究脚本 | 对应项目目录，或 `D:\Archive\scripts-loose-{年份}\` | 研究完毕后不应留在 HOME |
| 调试脚本 / 验证脚本 | 对应项目的 `sandbox\` 或 `temp\` 子目录 | 不允许长期散落在 HOME 根 |
| 项目内部脚本 | 对应项目目录 | 跟随项目走 |

**规则**：脚本写完第一时间放到正确位置。如果是在某个项目的上下文里写的脚本，放到那个项目目录里。

---

## 4. 新数据文件默认落点

| 类型 | 默认落点 |
|------|----------|
| JSON 扫描结果 / 原始研究数据 | `D:\Archive\research-data-{年份}\` |
| 临时 HTML 抓取 / JS 抓取 / 页面缓存 | `D:\Archive\web-captures\` |
| 临时 XML dump / PID / 输出文件 | 对应 `temp\` 目录，任务结束后进入待删候选 |
| 项目数据库（.db / .sqlite） | 对应项目 `data\` 子目录 |
| MCP 自动生成的空壳 sqlite_mcp_server.db | **不保留**，直接进入待删候选 |
| 上传/导入进度 JSON | 对应项目目录，任务完成后删除 |

**规则**：数据文件不允许散落在 D:\ 根目录或 HOME 根目录。

---

## 5. 新安装包 / zip / 解压目录默认落点

| 类型 | 默认落点 |
|------|----------|
| 新安装包 (.exe / .msi) | `D:\software\` |
| zip / rar 压缩包 | `D:\software\` 或 `D:\Downloads\`，解压后原包进入待删候选 |
| 解压后的长期使用工具 | 正式目录如 `D:\software\{工具名}\` |
| 解压后的临时使用工具 | 用完后进入待删候选 |

**规则**：
* 安装包用完即删（已安装的不需要保留安装包）
* zip 解压后，原 zip 默认进入待删候选
* 软件运行目录**不能长期放桌面**
* 不允许在桌面放解压后的目录

---

## 6. 新截图 / 图片 / 导出默认落点

| 类型 | 默认落点 |
|------|----------|
| 一般截图 | `C:\Users\Administrator\Pictures\` 或 `D:\Archive\captures\` |
| 项目过程截图 | 对应项目 `doc\` 或 `captures\` 子目录 |
| 临时验证截图 | 任务完成后进入待删候选 |
| 聊天/界面抓图 | 对应项目目录，不允许长期散落在 HOME 根 |
| 微信图片 | 确认后归入 `Pictures\` 或删除 |

**规则**：截图和图片不允许长期散落在 HOME 根目录或桌面。

---

## 7. 新项目 / 新任务目录默认落点

| 类型 | 默认落点 | 命名规则 |
|------|----------|----------|
| 新正式项目 | `D:\AgentTeam-Workspace\Dev\{项目名}\` | 英文短横线命名 |
| 一次性任务 | `D:\AgentTeam-Workspace\{YYYY-MM-DD}_{task-name}\` | 日期前缀 |
| 实验 / 沙盒 | `D:\AgentTeam-Workspace\Dev\sandbox\` | — |
| 不确定是否长期保留 | 先以一次性任务格式建在 AgentTeam 根 | 后续确认后再移入 Dev |

**规则**：
* 正式项目只进 Dev
* 不确定的先候审，不要直接塞进 Dev 正式层
* 想开新工作区？答案是"不要"（见 WORKSPACE_DECISION.md）

---

## 8. HOME 根目录允许长期存在的东西（白名单）

以下内容**允许**留在 `C:\Users\Administrator\` 根目录：

| 文件/目录 | 原因 |
|-----------|------|
| AGENTS.md | 主 Agent 配置，工具从 HOME 读取 |
| CLAUDE.md | Claude 配置，工具从 HOME 读取 |
| .mcp.json | MCP 配置 |
| .claude.json | Claude 配置 |
| .gitconfig | Git 全局配置 |
| .wezterm.lua | 终端配置 |
| .wslconfig | WSL 配置 |
| .zshrc / .bashrc / .bash_profile | Shell 配置 |
| 01-content ~ 05-ideas | 用户内容体系目录 |
| memory-v2 | 主记忆系统（PRIMARY_MEMORY_DECISION 判决） |
| iCloudDrive | iCloud 同步（含主 Vault） |
| AppData | 系统应用数据 |
| Desktop / Documents / Downloads / Pictures / Videos / Music | 系统默认目录 |
| .codex / .gemini / .antigravity* | 工具配置目录 |
| .ssh / .aws / .azure | 凭证目录 |
| diary | 日记目录 |
| backups | 备份目录 |

**除白名单之外的内容，都不应该长期留在 HOME 根目录。**

---

## 9. 桌面允许长期存在的东西（硬规则）

| 类型 | 允许？ |
|------|--------|
| 应用快捷方式 (.lnk / .url) | **允许** |
| 安装包 (.exe / .msi) | **不允许** — 移到 D:\software\ |
| zip / rar | **不允许** — 解压后原包删除 |
| 解压后的目录 | **不允许** — 移到正式目录 |
| 文档 (.docx / .md / .txt) | **不允许** — 归位到对应项目或 Documents |
| 截图 / 图片 | **不允许** — 归位到 Pictures 或项目目录 |
| 游戏修改器 / Trainer | **不允许** — 移到 D:\game\trainers\ |
| desktop.ini | 保留（系统文件） |

---

## 10. 候审机制

遇到以下情况时，**不要直接删或直接归位**，要先标成候审：

* 不确定是否仍被工具自动调用（如计划任务、启动脚本引用）
* 路径可能有外部依赖（如其他程序硬编码了这个路径）
* 不确定是否仍在活跃使用
* 含个人内容 / 敏感内容
* 大目录但内部结构不明（如 opencode 29.7 GB）
* 不知道这个文件是谁创建的、为什么存在

**候审的处理方式**：
1. 不删除、不移动
2. 在 `PATH_REGISTRY.csv` 或 `ACTIVE_ASSET_REGISTRY.csv` 中标记 status = 候审
3. 在下一轮任务中专门确认

---

## 11. 归位动作完成后的强制记录

每一轮实际执行归位、移动、删除、跳过之后，**必须同步更新**：

1. `04_handoff\HANDOFF_NEXT_AI.md` — 覆盖更新
2. `04_handoff\EXECUTION_LOG.md` — 追加写入
3. `04_handoff\ERROR_LOG.md` — 追加写入（无错误也写"本轮无新错误"）
4. `03_registry\ERROR_PATTERNS.md` — 如果出现重复错误

并且必须写清楚：**本轮影响了哪些路径**（移动了什么、从哪到哪、删了什么、跳过了什么）。

---

## 12. 已知例外

以下内容不能简单套规则，需要特殊对待：

| 内容 | 例外原因 |
|------|----------|
| AGENTS.md / CLAUDE.md / .mcp.json | 系统配置，必须在 HOME，不能移 |
| 主 Vault（iCloudDrive\iCloud~md~obsidian） | 已判决，路径固定 |
| 主记忆系统（memory-v2） | 已判决，路径固定 |
| Dev 核心项目区 | 已判决，禁止删除或迁移 |
| opencode (29.7 GB) | 未审计，不能套规则移动或删除 |
| my_projects (16.8 GB) | 未审计，不能套规则移动或删除 |
| new idea (13 GB) | 最近有活动，不能套规则归档 |
| local-mem-v2 (2.8 GB) | 已判决冻结，但体量大不能直接删 |
| .local-mem (4.3 GB) | 已判决冻结，可能含大型嵌入数据 |
| gmn-proxy.mjs / start-gmn-proxy.* | 可能被计划任务引用，需确认后再移 |
| codex-watchdog.sh / codex-cron-check.sh | 可能被系统服务引用 |
| cc-window-manager.ahk | 可能被 AHK 热键引用 |
| D:\Projects\ObsidianVault | 已判决冻结，不移不删 |
| .obsidian-backup-* 系列目录 | 备份，在确认主 Vault 安全前不动 |
