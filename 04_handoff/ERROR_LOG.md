# ERROR_LOG

> 规则：每一轮任务结束后追加写入
> 无错误也要写"本轮无新错误"
> 发现重复错误时同步更新 ERROR_PATTERNS.md

---

## 2026-03-28 Round 1 ~ Round 2

### 本轮任务

全盘扫描 + 决策文件创建

### 本轮无新错误

扫描和文件创建全部正常完成。

---

## 2026-03-28 Round 3 — 批次 1 清理

### 本轮任务

执行 SAFE_CLEANUP_PLAN 第一栏"可直接清理"

### 出错步骤

空目录清理（12 个目录中 10 个实际有内容）

### 错误现象

SAFE_CLEANUP_PLAN.md 中将 12 个 AgentTeam-Workspace 子目录标记为"空目录"，但实际执行时发现其中 10 个有文件（1~8 个文件不等）。

### 原始报错 / 表现

```
SKIPPED_NOT_EMPTY | 2 items | D:\AgentTeam-Workspace\project-scripts
SKIPPED_NOT_EMPTY | 1 items | D:\AgentTeam-Workspace\.claude-projects-old
SKIPPED_NOT_EMPTY | 4 items | D:\AgentTeam-Workspace\healthcheck-config
...（共 10 个）
```

### 影响范围

无损害。代码逻辑在删前检查了是否真空，非空的全部跳过。

### 临时处理

跳过所有非空目录，只删除了 2 个确认为空的目录。

### 最终状态

* 已解决 — 安全处理，无误删

### 是否疑似重复错误

* 是 — 属于"路径/目录判断错误"模式 (ERROR_PATTERNS #4)

### 关联错误模式

* #4 路径/目录判断错误，误以为空但实际有文件

---

## 2026-03-28 Round 4

### 本轮任务

归位分类方案

### 本轮无新错误

---

## 2026-03-28 Round 5

### 本轮任务

HTML 仪表盘 + 交接体系建立

### 出错步骤

浏览器预览 dashboard.html

### 错误现象

Antigravity 内置浏览器无法打开本地 file:/// 协议的 HTML 文件，返回 `net::ERR_ABORTED`。

### 原始报错 / 表现

```
navigate to URL: Frame.Goto file:///D:/AgentTeam-Workspace/local-memory-governance/dashboard.html: playwright: net::ERR_ABORTED
```

### 影响范围

无损害。仅影响预览，不影响文件生成。

### 临时处理

改用 `Start-Process` 在系统默认浏览器中打开。

### 最终状态

* 已解决 — 用户可在外部浏览器正常查看

### 是否疑似重复错误

* 否 — 这是 Antigravity 内置浏览器的已知限制

### 关联错误模式

* 无（属于环境限制，非流程错误）

---

## 2026-03-28 Round 6 — DROP_RULES 归位规则体系

### 本轮任务

创建 DROP_RULES.md 归位规则 + DROP_RULES_EXAMPLES.md 示例

### 本轮无新错误

规则文件创建和交接更新全部正常完成。未发现已有文件之间的冲突。

---

## 2026-03-28 Round 7 — 高风险运行资产纠偏

### 本轮任务

创建高风险纠偏规则 + 51 条高风险资产盘点 + 桌面高风险报告 + 依赖风险说明

### 本轮无新错误

扫描和文件创建全部正常完成。纠偏规则与已有判决无冲突。

---

## 2026-03-28 Round 8 — 批次 3A 低风险拟归位清单

### 本轮任务

扫描低风险文件并创建拟归位清单（只列候选，不执行移动）

### 本轮无新错误

扫描和文件创建全部正常完成。69 个候选对象全部为纯文档/HTML/JSON数据/图片，无高风险资产误入。

---

## 2026-03-28 Round 9 — 低风险拟归位执行前预检

### 本轮任务

对 69 项低风险候选做执行前预检（目标路径/同名冲突/敏感性/人工确认需求）

### 发现的问题（非系统错误）

1. **路径不具体**：`ex-girlfriend-context.json` 的目标写成"01-content 至 05-ideas 体系"，不是绝对路径
2. **部分对象不该归位而该删**：`tmp-playwright-output.txt` 和 `_tmp_tool_names.txt` 应改为待删候选
3. **部分对象超出项目范围**：`【ggs心委】_3月_信息反馈表.docx` 与本项目无关

### 本轮无系统错误

预检逻辑全部正常。上述 3 类问题属于上一轮清单编制时的判断精度不足，已在 ISSUES 文件中记录。

---

## 2026-03-28 Round 10 — 项目归属审计

### 本轮任务

项目归属审计：重新按"项目归属优先"审查 69 项候选

### 发现的系统性问题

**按文件类型整理破坏项目上下文**：之前按 .md / .html / .json 类型将文件送到中央 Dev\notes\，但这 43 项实际属于飞书集成和视频自动化两个具体项目。拆到中央 notes 会破坏项目的上下文完整性。

### 处理

已新增 ERROR_PATTERNS #8，创建 PROJECT_OWNERSHIP_RULES.md，暂停 APPROVED_BATCH1.csv。

---

## 2026-03-28 Round 11 — 批次 3B 执行归位

### 本轮任务

执行 49 项归位（20 飞书md + 9 飞书html + 13 视频md + 2 散落html + 5 散落json）

### 本轮无新错误

49 项全部成功移动，0 失败。目标目录文件计数验证通过。
