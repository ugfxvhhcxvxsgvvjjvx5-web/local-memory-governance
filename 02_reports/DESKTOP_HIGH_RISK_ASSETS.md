# DESKTOP_HIGH_RISK_ASSETS

> 盘点时间：2026-03-28
> 范围：C:\Users\Administrator\Desktop
> 原则：只读不动。不移动、不删除、不归档

---

## 1. 安装器

### Maestro-Setup-0.14.5.exe
* **路径**：`C:\Users\Administrator\Desktop\Maestro-Setup-0.14.5.exe`
* **类型**：exe 安装器（单文件，137 MB）
* **为什么高风险**：虽然是安装器，但需先确认 Maestro 是否已成功安装。如果安装不完整，删除安装器就没法重装了。
* **当前建议**：**候审** — 先确认 Maestro 安装状态

---

## 2. 解压后运行目录

### v2rayN-windows-64/
* **路径**：`C:\Users\Administrator\Desktop\v2rayN-windows-64\`
* **类型**：便携软件完整运行目录（354 MB，内含嵌套子目录）
* **为什么高风险**：
  * 这是 v2rayN 的实际运行目录，不是普通文件夹
  * 内含 exe + dll + config + 订阅数据
  * 移动后所有配置路径可能失效
  * 可能有桌面快捷方式指向此目录内的 exe
  * 可能被系统代理设置引用
* **当前建议**：**不动** — 在确认代理切换方案前绝不能移

### v2rayN-windows-64.zip
* **路径**：`C:\Users\Administrator\Desktop\v2rayN-windows-64.zip`
* **类型**：已解压的原始压缩包（136 MB）
* **为什么高风险**：
  * 虽然已解压，但如果解压目录被损坏需要重新解压
  * 需先确认解压目录完整性
* **当前建议**：**候审** — 确认运行目录完整后再决定

### 注册机/
* **路径**：`C:\Users\Administrator\Desktop\注册机\`
* **类型**：工具目录（0.7 MB，4 个文件）
* **为什么高风险**：
  * 可能含有破解工具，直接动可能有法律和安全风险
  * 内容未知，需先查看
* **当前建议**：**先审计** — 看清楚内容再决定

---

## 3. 游戏修改器 / Trainer

### 先开插件再开第五务必这样操作.exe
* **路径**：`C:\Users\Administrator\Desktop\先开插件再开第五务必这样操作.exe`
* **类型**：游戏辅助工具（单文件，122 MB）
* **为什么高风险**：
  * 体积 122 MB 却是单文件，内部可能自解压并释放到特定目录
  * 来源不明，文件名是中文操作指示
  * 可能与第五人格游戏路径绑定
  * 移动后可能无法正常使用
* **当前建议**：**先审计** — 确认是否还在玩第五人格

### Resident Evil 2 v1.0-v20220613 Plus 20 Trainer.exe
* **路径**：`C:\Users\Administrator\Desktop\Resident Evil 2 v1.0-v20220613 Plus 20 Trainer.exe`
* **类型**：风灵月影游戏修改器（单文件，1.3 MB）
* **为什么高风险**：
  * 游戏修改器通常需要在游戏进程活跃时注入
  * 可能对运行路径有要求
  * Downloads 里也有一份重复的
* **当前建议**：**候审** — 确认是否还玩生化危机 2

### 桌面快捷方式指向的远程 Trainer
以下快捷方式指向 `E:\download\FLiNGTrainer\` 目录：
* `Crimson Desert v1.0 Plus 10 Trainer Updated 2026.03.23.exe - 快捷方式.lnk`
* `风灵月影修改器.lnk`

* **为什么高风险**：快捷方式指向 E 盘的修改器目录。如果移动或删除 E 盘那个目录，桌面快捷方式全部失效。
* **当前建议**：**不动** — 快捷方式和目标都不动

---

## 4. 系统文件

### desktop.ini
* **路径**：`C:\Users\Administrator\Desktop\desktop.ini`
* **类型**：系统配置文件
* **当前建议**：**不动** — 系统文件

---

## 汇总

| 对象 | 类型 | 大小 | 风险等级 | 建议 |
|------|------|------|----------|------|
| v2rayN-windows-64/ | 便携软件目录 | 354 MB | **极高** | 不动 |
| 先开插件再开第五.exe | 游戏辅助 | 122 MB | **极高** | 先审计 |
| Maestro-Setup.exe | 安装器 | 137 MB | 高 | 候审 |
| v2rayN-windows-64.zip | 已解压原包 | 136 MB | 高 | 候审 |
| 注册机/ | 工具目录 | 0.7 MB | 高 | 先审计 |
| RE2 Trainer.exe | 修改器 | 1.3 MB | 高 | 候审 |
| E:\FLiNGTrainer (快捷方式指向) | 修改器目录 | ? | **极高** | 不动 |
