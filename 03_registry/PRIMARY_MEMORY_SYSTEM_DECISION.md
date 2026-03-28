# PRIMARY_MEMORY_SYSTEM_DECISION

> 定稿时间：2026-03-28
> 状态：正式判决

---

## 主记忆系统

**C:\Users\Administrator\memory-v2**

这是当前工作中的语义记忆系统（semantic memory），23 个文件，0.1 MB。轻量、结构化、正在被引用。

角色：**现役主记忆系统**

## 其他记忆系统角色

| 系统 | 大小 | 文件数 | 角色 | 说明 |
|------|------|--------|------|------|
| C:\Users\Administrator\memory-v2 | 0.1 MB | 23 | **现役** | 当前语义记忆系统 |
| C:\Users\Administrator\.local-mem | 4,341 MB | 19 | **冻结** | 旧版本地记忆，巨大(4.3GB)但只有 19 个文件，可能含大型数据嵌入 |
| C:\Users\Administrator\.local-mem-dev | 147 MB | 6,414 | **冻结** | 开发版本地记忆，大量碎片文件 |
| D:\AgentTeam-Workspace\local-mem | 0.8 MB | 132 | **归档候选** | AgentTeam 下的旧记忆系统，已清掉 sqlite_mcp_server.db |
| D:\AgentTeam-Workspace\local-mem-v2 | 2,816 MB | 25,132 | **冻结** | AgentTeam 下的 v2 记忆系统，大量文件(25K+) |

## 规则

* 新记忆写入 `C:\Users\Administrator\memory-v2`
* 其他 4 个系统全部冻结，不再写入
* `.local-mem` (4.3 GB) 和 `local-mem-v2` (2.8 GB) 体量大，但现在不删，后续单独审计内容
* `D:\AgentTeam-Workspace\local-mem` 最小(0.8 MB)，归档候选
* 未来如需迁移，以 `memory-v2` 为唯一数据源
