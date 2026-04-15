<!--
  GitHub profile README for https://github.com/Brentbin
  Publishing path: create a public repo named `Brentbin/Brentbin`, put this file as README.md.
  Audit-grade: every claim has a verifiable pointer (repo path, commit SHA, or measurable fact).
-->

### Lee Bin · 李斌 · [@Brentbin](https://github.com/Brentbin)

做零售业务的 AI 与数据分析。公开代码不多，写下来的比推上来的多。

---

#### 关于这个 Profile（范围声明）

这是一次诚实的审计，不是简历。

- 账号建于 **2015-08**，前 10 年几乎沉寂；唯一一次实质性原创发生在 2025-02。
- 30 个公开仓库：**29 个是 fork**（当书签收藏，零贡献）、**1 个原创**（`adaptive_network`）。
- 日常工作（零售数据分析、内部 AI 工具编排、方法论沉淀）发生在**私有仓库和公司内部系统**，不在这里。
- 换句话说：**只看 GitHub 评估我，读到的是一本研究日记，不是工程履历**。

#### [adaptive_network](https://github.com/Brentbin/adaptive_network) — 自适应"思考"网络的一次 14 天探索

| 项 | 值 |
|---|---|
| 活跃窗口 | 2025-02-05 → 2025-02-19（14 天，4 个 commit） |
| 状态 | **搁置至今**，未重启 |
| 语言 | Python (PyTorch) · 374 KB 源码 |
| 动机 | 试图让一个网络在固定权重外，按任务类型做"动态子图激活 + 多轮思考" |
| 结构 | Phase 1：baseline (MLP) vs 自适应子图网络；Phase 2：多层"思考控制"（设计稿）|

**读过的、写进 `references/` 的论文**

- **MoBA** (Mixture of Block Attention) — Moonshot 2025
- **Progressive Neural Networks** — DeepMind 2016

**实证结果（`phase1/experiments/exp2/`，我自己跑的）**

| 任务 | Adaptive test loss | MLP baseline | 结论 |
|---|---:|---:|---|
| 算术序列 | 0.00069 | **0.00040** | MLP 胜 |
| 几何序列 | **42.06** | 44.22 | Adaptive 略胜 |
| 乘法序列 | **91.52** | 98.71 | Adaptive 略胜，但绝对误差都极差 |

**没 work 的部分（诚实披露）**

- `specialization_scores` 全程停在 `0.3333...`（1/3 均匀分布）——**节点专门化机制没激活**，设计假设未被验证（见 `phase1/experiments/exp2/results/adaptive_results.json`）
- pretrain 阶段 addition 任务 eval loss 在第 4 epoch 飙到 39.6（前一轮是 4.3）——训练不稳定，未深究
- Phase 2 `docs/design.md` 留了 10+ 个 `TODO:`，多层思考控制的形式化从未完成
- 工程纪律曾经不合格：`.DS_Store` / `__pycache__` / ~149 MB 训练日志入库，目录名拼写错误 `adptive_network`。**2026-04-15 用 `git filter-repo` 清理了历史（`.git` 28 MB → 1.3 MB）+ 重命名目录**（commit `f0a3d4f`）。承认问题，修复问题，保留证据。

**值得记录的一件事**

`experiment_plan.md` 如实写下了"假设在 3 个任务中 2 个不成立"——而不是把负面结果删掉。这是我对自己实验报告的最低要求。

---

#### 其他公开痕迹

- 29 个 fork：Auto-GPT、tensorflow、julia、spark、mahout、DIG、cygen、DEFMap、faceswap 等——**只是书签**，不代表任何贡献。
- 我不维护公开库、不跑 OSS side project、不刷绿格子。

#### Inner Portfolio · 私有项目清单

除了公开的 [`adaptive_network`](https://github.com/Brentbin/adaptive_network)，我的日常代码集中在 org [`brentlee-personal-group`](https://github.com/brentlee-personal-group) 下。这些仓库**全部 private**（点进去会 404 或看到"Access required"），此处列出是为了让读者知道**存在什么、规模多大、大致在做什么**——不是展示、是审计可见性。

| Repo | 语言 | 最近活动 | 审计描述（按 README 事实陈述，非自卖自夸）|
|---|---|---|---|
| `Argus` | JavaScript | 2026-04 | Visual Feedback Oracle for AI Coding Agents——给 AI 补上"看见自己写的 UI"的能力。**Early design phase**（README 自述）|
| `Nomos` | Go | 2026-03 | Tick-based 游戏模拟引擎 + MCP 接入。600 ms/tick，12 阶段 pipeline，4 层交互模型（Command / Policy / Law / Prediction），有正式术语表和 30 分钟阅读路径。**51 MB Go 代码，持续活跃**——目前最有规模的项目 |
| `agent-hub` | Python | 2026-01 | 双 Agent 数据分析系统（AutoGen v0.4+ · Azure OpenAI gpt-5 · Databricks Genie）。Planner + Executor 两角色拆分，有 pre-commit、Dockerfile、CODE_REVIEW_CHECKLIST |
| `skills` | Python | 2026-01 | **Anthropic 官方 `anthropics/skills` 的 fork**，非原创。想看内容请直接去 https://github.com/anthropics/skills |
| `next` | JavaScript | 2026-01 | Next.js 脚手架项目，产出有限 |
| `workflow` | Python | 2025-10 | Workflow / orchestration 实验（api_servers + db + n8n_nodes + playground + tests） |
| `Ratropolis_First_Whiskers_setting` | Markdown | 2026-02 | 独立游戏 Ratropolis 的世界观/剧情设定文档库（实验室叙事框架、种族、角色）|
| `Ratropolis_First_Whiskers` | C# | 2024-11 | 同系列 C# 代码，活跃度低 |

#### 申请访问（Request Access）

如果你想看上表中某个 repo，请在 [`Brentbin/Brentbin`](https://github.com/Brentbin/Brentbin/issues/new) 开一个 issue，写清楚：

1. **你是谁**（来自哪家团队 / 做什么 / GitHub handle）
2. **你想看哪个 repo**（单个或多个）
3. **用途**（只读 / collab / 参考 / 评估合作 / 其他）
4. **身份证明**（可选：LinkedIn / 公司邮箱 / 介绍人）

**回复 SLA**：7 个工作日内一条回复——同意 / 拒绝+理由 / 约 15 分钟视频聊再定。

**默认允许的用途**：阅读、给我提 issue、讨论架构。
**默认需要额外谈的用途**：fork / 二次分发 / 用于商业产品 / 用于招聘评估（正式 offer 场景下优先）。
**直接拒绝的用途**：爬数据训练模型、未声明的评估、转卖。

#### Notes · Housekeeping

- [x] ~~修复 `adaptive_network` 的 git 卫生~~ 完成于 2026-04-15，commit `f0a3d4f`（清理 ~149 MB 训练日志 + `.DS_Store` / `__pycache__` / `.pyc` from history；修 `adptive_network` 目录拼写；强化 `.gitignore`）
- [~] 合并 `HexBerlin` 账号下的 commit 归属 — **不修，改为声明**（见下一节"透明声明")
- [ ] 若 Phase 2 重启，先把 `design.md` 的 TODO 转成可执行验收标准

#### 透明声明：关于 `HexBerlin` 账号

本人 2022-05 建过一个备用 GitHub 账号 [`HexBerlin`](https://github.com/HexBerlin)——0 repo、0 event、10 个技术 star，基本是僵尸号。当时把 `lib1292914@icloud.com` 绑在它上面；2025-02 用同一封邮箱 push [`adaptive_network`](https://github.com/Brentbin/adaptive_network) 时，GitHub 按 email 自动把 4 个 commit 的 attribution 挂到了 `HexBerlin` 的头像上，而不是仓库所有者 `Brentbin`。

**为什么不修**：
- GitHub 规则：每个账号至少一封 verified email。该邮箱是 `HexBerlin` 的唯一 email → 无法直接解绑。
- 选项 1：删 `HexBerlin` 账号 → 解绑 → 加到 `Brentbin` → 归属自动迁移。技术上可行，但账号删除不可逆。
- 选项 2：给 `adaptive_network` 做第二次历史重写，把 commit author email 改为 `users.noreply.github.com`。代价是又一次 force push、新 commit SHA 失效。
- **选择**：两条都不走。成本 > 收益。这份声明本身就是解。

**对读者的影响**：如果你在 `adaptive_network/commits` 页看到 "Lee Bin" 但头像链到 `HexBerlin`——那就是我。同一个人，两个 GitHub id，一个 email。透明度优先于表面整洁。

---

<sub>最后一句：这个 profile 的价值不在于它展示了什么，而在于它承认了什么没展示。</sub>
