# CLEANUP_EXECUTION_BATCH1

> 执行时间：2026-03-28 19:15
> 依据：02_reports\SAFE_CLEANUP_PLAN.md 第一栏"可直接清理"
> 原则：超保守，只删确定无用的东西

---

## 实际删除清单

### 重复安装包（3 项，释放 938.6 MB）

| 状态 | 大小 | 路径 |
|------|------|------|
| OK | 470.8 MB | C:\Users\Administrator\Downloads\BaiduNetdisk_8.2.7.101 (1).exe |
| OK | 315.4 MB | C:\Users\Administrator\Downloads\GoogleDriveSetup (1).exe |
| OK | 152.4 MB | C:\Users\Administrator\Downloads\Antigravity (1).exe |

### 旧日志（7 项，释放 9.7 MB）

| 状态 | 大小 | 路径 |
|------|------|------|
| OK | 8.9 MB | C:\Users\Administrator\gmn-proxy-debug.log |
| OK | 565 KB | C:\Users\Administrator\codex-watchdog.log |
| OK | 34 KB | C:\Users\Administrator\claude-debug.log |
| OK | 1 KB | C:\Users\Administrator\resolve_diag.stderr.txt |
| OK | 0 KB | C:\Users\Administrator\resolve_diag.stdout.txt |
| OK | 0.1 KB | C:\Users\Administrator\out.txt |
| OK | 0 KB | C:\Users\Administrator\err.txt |

### sqlite_mcp_server.db（11 项，全部 0 bytes 空壳）

| 状态 | 路径 |
|------|------|
| OK | C:\Users\Administrator\sqlite_mcp_server.db |
| OK | C:\Users\Administrator\Documents\sqlite_mcp_server.db |
| OK | C:\Users\Administrator\Downloads\sqlite_mcp_server.db |
| OK | C:\Users\Administrator\baidu-netdisk-organizer\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\2026-03-04_file-clean-up\backups\projects-loose\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\Dev\Learning\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\Dev\sandbox\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\Dev\Learning\2026-03-15_case-prep-detective-lab\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\acceptance-test\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\doudizhu-ai\sqlite_mcp_server.db |
| OK | D:\AgentTeam-Workspace\local-mem\sqlite_mcp_server.db |

验证方式：删除前逐个核查，全部为 0 bytes 空文件。

### 空目录（2 项删除成功，10 项跳过）

| 状态 | 路径 | 原因 |
|------|------|------|
| OK | D:\AgentTeam-Workspace\work-trans-center | 真空目录 |
| OK | D:\AgentTeam-Workspace\work-trans | 真空目录 |
| SKIPPED | D:\AgentTeam-Workspace\project-scripts | 实际有 2 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\.claude-projects-old | 实际有 1 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\.vscode-projects-old | 实际有 2 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\healthcheck-config | 实际有 4 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\learn-coding | 实际有 1 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\2026-03-08_openclaw-android-setup+ | 实际有 2 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\2026-03-10_botdrop-part2+ | 实际有 3 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\obsidian-sync-stabilization-20260304 | 实际有 6 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\2026-03-04_project-init-system | 实际有 8 个文件 |
| SKIPPED | D:\AgentTeam-Workspace\my-product-txt | 实际有 1 个文件 |

---

## 汇总

| 类别 | 删除数 | 释放空间 |
|------|--------|----------|
| 重复安装包 | 3 | 938.6 MB |
| 旧日志 | 7 | 9.7 MB |
| sqlite_mcp_server.db | 11 | 0 MB (全是空壳) |
| 空目录 | 2 | 0 MB |
| **合计** | **23 项** | **~948 MB** |

## 删除失败

无。全部 23 项操作成功。

## 需人工确认

以下 10 个目录原计划作为"空目录"清理，但实际检查发现内含文件，已跳过。如需清理需人工确认：

* D:\AgentTeam-Workspace\project-scripts (2 项)
* D:\AgentTeam-Workspace\.claude-projects-old (1 项)
* D:\AgentTeam-Workspace\.vscode-projects-old (2 项)
* D:\AgentTeam-Workspace\healthcheck-config (4 项)
* D:\AgentTeam-Workspace\learn-coding (1 项)
* D:\AgentTeam-Workspace\2026-03-08_openclaw-android-setup+ (2 项)
* D:\AgentTeam-Workspace\2026-03-10_botdrop-part2+ (3 项)
* D:\AgentTeam-Workspace\obsidian-sync-stabilization-20260304 (6 项)
* D:\AgentTeam-Workspace\2026-03-04_project-init-system (8 项)
* D:\AgentTeam-Workspace\my-product-txt (1 项)
