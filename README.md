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

#### Notes · Housekeeping

- [x] ~~修复 `adaptive_network` 的 git 卫生~~ 完成于 2026-04-15，commit `f0a3d4f`（清理 ~149 MB 训练日志 + `.DS_Store` / `__pycache__` / `.pyc` from history；修 `adptive_network` 目录拼写；强化 `.gitignore`）
- [ ] 合并 `HexBerlin` 账号下的 commit 归属（email 配置错位导致的映射问题）
- [ ] 若 Phase 2 重启，先把 `design.md` 的 TODO 转成可执行验收标准

---

<sub>最后一句：这个 profile 的价值不在于它展示了什么，而在于它承认了什么没展示。</sub>
