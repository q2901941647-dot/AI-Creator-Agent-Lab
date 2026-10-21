# AI Creator Agent Lab

**AI 创作智能体策略与评测作品集 · 32 页
🔗 **在线预览**：`https://q2901941647-dot.github.io/AI-Creator-Agent-Lab/`
<!-- 上传后把上面这行替换成真实链接，并删掉这条注释 -->

---

## 这是什么

不是视频作品合集，而是一份**产品判断的可追溯记录**：把一个「创作者用 AI 做视频」的流程，
拆成 Agent 能执行的任务图，再用 24 条任务、6 维 Rubric、72 次执行去验证它到底行不行。

三个贯穿全篇的主张：

1. **Agent 的护城河不在生成，在「改」的成本。**
2. 可控性（计划可见 / 作用域明确 / 可回滚）是可以被设计出来的，不靠模型变聪明。
3. 评测的终点不是一份报告，是一个被改过的版本。

## 目录结构

| 文件 | 说明 |
|---|---|
| `index.html` | 作品集正文，32 页 A4 横向。滚动浏览，顶部有页码与进度条 |
| `prototype.html` | CreatorPilot 可交互原型：约束解析 → 计划 → 执行 → 交付，可注入失败、走确认卡、单节点重跑 |
| `portfolio.pdf` | 同一份作品的 PDF（32 页，A4 横向），适合直接作为附件发送 |
| `benchmark-tasks.csv` | 24 条标准化评测任务（4 类 × 3 难度） |
| `benchmark-runs.csv` | 72 条执行记录：6 维得分、加权分、判定、失败归因 |
| `feedback-50.csv` | 50 条**自建模拟**用户反馈及归因、需求映射 |

## 内容结构

| 页码 | 章节 |
|---|---|
| P.01–03 | 封面 · 个人定位 · 目录 |
| P.04–16 | **主项目 CreatorPilot**：场景 → 画像 → 痛点优先级 → 定位 → 架构 → 工作流 → 任务图 → 工具契约 → 确认分级 → 原型 → PRD → 路线图 |
| P.17–22 | **Agent Benchmark**：方法论 → 24 条任务 → Rubric → 结果 → 失败复盘 → 优化优先级 |
| P.23–26 | **竞品研究**：剪映 AI 成片 / Pippit / 即梦，同一组任务实测 → 能力矩阵 → 旅程断点 → 机会点 |
| P.27–29 | **反馈驱动迭代**：50 条数据集 → 5 Whys 归因 → 需求池 → 2 个实验方案 |
| P.30–31 | **机制专题**：Skill 定义（YAML）· Memory 分层策略 |
| P.32 | 五条产品判断 · 关于我 |

## 数据口径

作品集里每处数据都标了来源，请按标签理解：

- **实测** — 我在真实产品上完成的体验记录，正文标注了时间与版本
- **桌面推演** — 按固定规则模拟 Agent 决策，用于验证流程设计是否跑得通
- **模拟** — 自建合成数据，用于演示分析方法，**不代表真实用户调研结果**

评测分数是**原型态基线**（被测对象为自建原型，工具调用为演示实现），
用于验证评测流程本身可用，**不作为任何真实模型的能力结论**。

## 部署到 GitHub Pages

### 方式 A：网页拖拽（不需要命令行）

1. 新建仓库：`New repository` → 名称建议 `creator-agent-lab` → 选 **Public** → Create
2. 进入仓库 → `Add file` → `Upload files`
3. 把本文件夹里的**所有文件**（含 `.nojekyll`）一起拖进去 → `Commit changes`
4. `Settings` → 左侧 `Pages` → Source 选 `Deploy from a branch`
   → Branch 选 `main`、目录选 `/ (root)` → `Save`
5. 等 1–2 分钟，访问 `https://<你的用户名>.github.io/creator-agent-lab/`

> 右上角的「下载 PDF」会自动指向 `portfolio.pdf`，不需要改任何链接。

### 方式 B：命令行

```bash
git init
git add .
git commit -m "portfolio: AI Creator Agent Lab"
git branch -M main
git remote add origin https://github.com/<你的用户名>/creator-agent-lab.git
git push -u origin main
```

推送后同样在 `Settings → Pages` 里开启即可。

### 常见问题

- **页面 404**：Pages 首次构建需要 1–2 分钟；确认分支是 `main`、目录是 `/ (root)`。
- **样式正常但图片/附件打不开**：检查文件名大小写是否与 HTML 中的引用完全一致。
- **想换仓库名**：改名不影响页面，但预览地址会跟着变。

## 联系

唐睿 · 2027 届 · 网络与新媒体
📱 13410164607　✉️ 2901941647@qq.com

---

<sub>本作品集为个人原创的概念设计与分析，其中 CreatorPilot 为独立概念方案，与任何公司现有产品或路线图无对应关系。CSV 中的用户反馈为模拟数据，已在文件内标注。</sub>
