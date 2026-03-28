# DROP_RULES_EXAMPLES

> 不讲抽象规则，只讲"遇到这个情况该放哪"
> 对照 03_registry\DROP_RULES.md 使用

---

## 1. 新写了一份飞书接口研究文档

**放到**：`D:\AgentTeam-Workspace\Dev\notes\feishu-research\`
如果目录不存在，先建再放。不要丢在 HOME 根。

## 2. 新生成了一份视频自动化 JSON 扫描结果

**放到**：`D:\Archive\research-data-2026\`
原始数据不应散落在 HOME 或 D:\ 根。

## 3. 新下载了一个安装包（比如 Antigravity.exe）

**放到**：`D:\software\`
安装完成后，安装包进入待删候选。不要留在 Downloads 或桌面。

## 4. 新写了一个临时调试脚本（比如 check_something.py）

**放到**：对应项目目录的 `sandbox\` 或 `temp\`
如果不属于某个项目，放到 `D:\Archive\scripts-loose-2026\`
**绝对不要**丢在 HOME 根。

## 5. 新开了一个正式项目（比如 my-awesome-app）

**放到**：`D:\AgentTeam-Workspace\Dev\my-awesome-app\`
这是唯一正确的正式项目入口。不要在 D:\Projects 或 D:\Workspace 里开新坑。

## 6. 新建了一次性任务目录（比如修复某个 bug）

**放到**：`D:\AgentTeam-Workspace\2026-03-28_fix-some-bug\`
用日期前缀命名。做完后冻结，未来可收纳到 `_archive\`。

## 7. 新生成了一张验证截图

**放到**：对应项目的 `doc\` 或 `captures\` 子目录
如果是临时验证，任务完成后进入待删候选。
**不要**留在桌面或 HOME 根。

## 8. 新导出了一份数据库快照（比如 backup.db）

**放到**：对应项目的 `data\` 子目录
比如当前资格系统的库放在 `personnal v1\data\`
**不要**放在 D:\ 根或 HOME 根。

## 9. 新生成了一份 html 页面抓取

**放到**：`D:\Archive\web-captures\`
临时 HTML 之前大量散落在 HOME（jimeng_*.html / temp-feishu-*.html），以后统一归这里。

## 10. 新写了一个长期工具脚本（比如批量处理工具）

**放到**：`D:\AgentTeam-Workspace\Dev\tools\`
确认会反复使用的脚本才放这里。一次性的不要放。

## 11. 新写了一个个人内容 json（比如情感相关数据）

**放到**：用户内容体系 `C:\Users\Administrator\01-content\` 到 `05-ideas\` 中对应的目录
个人内容不要散落在 HOME 根。

## 12. 新的 Obsidian 相关文件

**规则**：遵循 `PRIMARY_VAULT_DECISION.md`
日常笔记写入 iCloud 同步 Vault（`iCloudDrive\iCloud~md~obsidian`）
不要往 `D:\Projects\ObsidianVault` 写新东西（已冻结）
不要在其他地方新建 Vault

## 13. 新的记忆系统文件

**规则**：遵循 `PRIMARY_MEMORY_SYSTEM_DECISION.md`
新记忆只写入 `C:\Users\Administrator\memory-v2`
不要往 `.local-mem` / `local-mem-v2` 等旧系统写入
不要新建第六个记忆系统

## 14. 新出现了一个 sqlite_mcp_server.db

**处理**：直接进入待删候选
这是 MCP 工具自动生成的空壳文件，无保留价值。
之前已清理过 11 个这样的文件，全部 0 bytes。

## 15. 不确定用途的新目录

**先进入候审状态**：
1. 不删除、不移动
2. 在 `PATH_REGISTRY.csv` 中登记，status 填候审
3. 在下一轮任务中找人确认

**绝对不要**：
* 直接塞进 Dev 正式层
* 直接删掉
* 放在 HOME 根就不管了

## 16. 新下载了一个 zip 并解压了

**处理**：
1. 解压后的目录移到正式位置（如 `D:\software\{工具名}\`）
2. 原 zip 进入待删候选
3. **不要**把解压目录留在桌面（v2rayN 的教训）

## 17. AI 帮你做了一轮研究，产生了 10 个 .md 文件

**放到**：`D:\AgentTeam-Workspace\Dev\notes\{研究主题}\`
或者放在对应项目的 `doc\` 目录
**绝对不要**直接散落在 HOME 根（飞书 20 个 + 视频自动化 19 个的教训）

## 18. 新生成了一个 APK / 移动端构建产物

**放到**：对应项目目录
比如 botdrop.apk 应该在 botdrop 项目目录内
**不要**丢在 HOME 根（108 MB APK 散落在 HOME 的教训）
