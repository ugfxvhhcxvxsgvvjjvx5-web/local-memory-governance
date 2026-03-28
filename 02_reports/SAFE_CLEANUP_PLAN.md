# SAFE_CLEANUP_PLAN

> 制定时间：2026-03-28
> 原则：超保守，只清确定无用的东西

---

## 一、可直接清理

以下内容**确定无用**，清理不需要任何决策：

### Downloads 重复安装包

| 文件 | 大小 | 原因 |
|------|------|------|
| C:\Users\Administrator\Downloads\BaiduNetdisk_8.2.7.101 (1).exe | 471 MB | 重复副本（保留无括号的那个也没意义，已安装） |
| C:\Users\Administrator\Downloads\GoogleDriveSetup (1).exe | 331 MB | 重复副本 |
| C:\Users\Administrator\Downloads\Antigravity (1).exe | 160 MB | 重复副本 |

### 旧日志

| 文件 | 大小 | 原因 |
|------|------|------|
| C:\Users\Administrator\gmn-proxy-debug.log | 8.9 MB | 调试日志，无保留价值 |
| C:\Users\Administrator\codex-watchdog.log | 578 KB | 看门狗日志，无保留价值 |
| C:\Users\Administrator\claude-debug.log | 34 KB | 调试日志 |
| C:\Users\Administrator\resolve_diag.stderr.txt | 1 KB | 诊断输出残留 |
| C:\Users\Administrator\resolve_diag.stdout.txt | 0 KB | 诊断输出残留 |
| C:\Users\Administrator\out.txt | 0 KB | 临时输出 |
| C:\Users\Administrator\err.txt | 0 KB | 临时输出 |

### 散落的 sqlite_mcp_server.db（保留 0 个即可，它们都是 MCP 工具自动生成的空壳）

| 文件 | 原因 |
|------|------|
| C:\Users\Administrator\sqlite_mcp_server.db | 自动生成 |
| C:\Users\Administrator\Documents\sqlite_mcp_server.db | 自动生成 |
| C:\Users\Administrator\Downloads\sqlite_mcp_server.db | 自动生成 |
| C:\Users\Administrator\baidu-netdisk-organizer\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\2026-03-04_file-clean-up\backups\projects-loose\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\Dev\Learning\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\Dev\sandbox\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\Dev\Learning\2026-03-15_case-prep-detective-lab\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\acceptance-test\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\doudizhu-ai\sqlite_mcp_server.db | 自动生成 |
| D:\AgentTeam-Workspace\local-mem\sqlite_mcp_server.db | 自动生成 |

### 空目录（AgentTeam-Workspace 下 size=0 的空壳）

| 目录 | 原因 |
|------|------|
| D:\AgentTeam-Workspace\project-scripts | 空目录 |
| D:\AgentTeam-Workspace\work-trans-center | 空目录 |
| D:\AgentTeam-Workspace\.claude-projects-old | 空目录 |
| D:\AgentTeam-Workspace\work-trans | 空目录 |
| D:\AgentTeam-Workspace\.vscode-projects-old | 空目录 |
| D:\AgentTeam-Workspace\healthcheck-config | 空目录 |
| D:\AgentTeam-Workspace\learn-coding | 空目录 |
| D:\AgentTeam-Workspace\2026-03-08_openclaw-android-setup+ | 空目录 |
| D:\AgentTeam-Workspace\2026-03-10_botdrop-part2+ | 空目录 |
| D:\AgentTeam-Workspace\obsidian-sync-stabilization-20260304 | 空目录 |
| D:\AgentTeam-Workspace\2026-03-04_project-init-system | 空目录 |
| D:\AgentTeam-Workspace\my-product-txt | 空目录 |

**预估释放空间：~972 MB（重复安装包） + ~10 MB（日志） + ~0（DB 和空目录）**

---

## 二、清理前确认一次

以下内容**大概率无用**，但清理前看一眼确认：

### Downloads 已安装的安装包

| 文件 | 大小 | 确认点 |
|------|------|--------|
| BaiduNetdisk_8.2.7.101.exe | 471 MB | 确认百度网盘已装好 |
| GoogleDriveSetup.exe | 331 MB | 确认 Google Drive 已装好 |
| Antigravity.exe | 173 MB | 确认当前 Antigravity 版本更新 |
| Trae-Setup-x64.exe | 231 MB | 确认是否还需要 Trae |
| ocs-2.9.24-setup-win-x64.exe | 273 MB | 确认 OCS 已装好 |
| DWRG_setup.exe | 191 MB | 确认已装好 |
| Vortex-1-1-16-6-1772448630.exe | 326 MB | 确认 Vortex 已装好 |
| TimeScribe-1.11.0-setup.exe | 150 MB | 确认 TimeScribe 已装好 |
| Linear Setup 1.28.13 - x64.exe | 100 MB | 确认 Linear 已装好 |
| sysdiag-all-x64-6.0.9.1-2026.02.28.1.exe | 68 MB | 系统诊断工具，用完即删 |
| activitywatch-v0.13.2-windows-x86_64.zip | 115 MB | 确认已解压使用 |
| Resident.Evil.Requiem.v1.0.Plus.4.Trainer.rar | 45 MB | 游戏修改器，确认是否还玩 |

### 桌面安装包和解压残留

| 文件 | 大小 | 确认点 |
|------|------|--------|
| 桌面\Maestro-Setup-0.14.5.exe | 143 MB | 安装包不该在桌面 |
| 桌面\v2rayN-windows-64.zip | 143 MB | 已解压，zip 可删 |
| 桌面\先开插件再开第五务必这样操作.exe | 128 MB | 游戏辅助，确认是否还需要 |
| 桌面\Resident Evil 2 Trainer.exe | 1.3 MB | 游戏修改器 |
| 桌面\Crimson Desert Trainer.exe | 1.6 MB | 游戏修改器 |

### HOME 临时目录

| 目录 | 确认点 |
|------|--------|
| C:\Users\Administrator\_temp | 看里面有没有重要文件 |
| C:\Users\Administrator\_tmp_adobe_premiere_mcp_20260310 | 临时 Adobe 研究，确认不需要 |
| C:\Users\Administrator\_tmp_pymiere_20260310 | 临时 Pymiere 研究，确认不需要 |
| C:\Users\Administrator\_tmp_research | 临时研究，确认不需要 |
| C:\Users\Administrator\tmp-shen-rerun | 临时目录 |
| C:\Users\Administrator\tmp-shen-rerun2 | 临时目录 |
| C:\Users\Administrator\tmp | 临时目录 |

### D 盘根目录临时脚本

| 文件 | 确认点 |
|------|--------|
| D:\batch_upload.py | NLM 上传脚本，确认是否还在用 |
| D:\check_cdp.py / debug_cookies.py / extract_cookies.py | 调试脚本，确认不再用 |
| D:\merge_vault.py / upload_text.py | Obsidian/NLM 工具脚本，确认不再用 |
| D:\upload_progress.json / nlm_text_upload_progress.json | 上传进度记录，确认已完成 |

**预估可释放空间：~2.5 GB（安装包） + ~270 MB（桌面残留） + 待确认（临时目录）**

---

## 三、现在绝对不要动

| 内容 | 原因 |
|------|------|
| D:\AgentTeam-Workspace\Dev | 唯一核心项目区 |
| D:\AgentTeam-Workspace\opencode (29.7 GB) | 可能含重要配置，需先了解内容 |
| D:\AgentTeam-Workspace\my_projects (16.8 GB) | 含 whisper 转写项目 |
| D:\AgentTeam-Workspace\new idea (13 GB) | 最近有活动 |
| D:\AgentTeam-Workspace\local-mem-v2 (2.8 GB) | 记忆系统，需先确认 |
| D:\Projects\ObsidianVault | 唯一有 .obsidian 的正式 Vault |
| C:\Users\Administrator\iCloudDrive | iCloud 同步内容 |
| C:\Users\Administrator\AGENTS.md / CLAUDE.md | 系统配置 |
| C:\Users\Administrator\memory-v2 | 语义记忆系统 |
| C:\Users\Administrator\01-content ~ 05-ideas | 用户内容体系目录 |
| C:\Users\Administrator\backups | 备份目录 |
| C:\Users\Administrator\diary | 日记目录 |
| C:\Users\Administrator\.codex | Codex 配置 |
| C:\Users\Administrator\codex-work | 候审，未确认 Codex 是否仍用此目录 |
| 所有 .obsidian-backup-* 目录 | 在确认主 Vault 安全前不动 |
| D:\AgentTeam-Workspace\2026-03-10_botdrop-part2 (5.6 GB) | 飞书 bot 项目，最近还在活动 |
| HOME 根目录 47 个 .md 文件 | 需要分类归位，不是删除 |
| HOME 根目录 26 个脚本 | 需要分类归位，不是删除 |
