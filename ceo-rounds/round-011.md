# CEO Round 011 - 发布版内容评估 + Website 升级 + 公开发布

## 触发

用户指令(2026-04-29):
1. 针对发布版本进行内容评估
2. 更新 website 页面
3. 使用 gei-imagine 生成更多插图,尤其是针对人物设定中的内容给出全面的人物角色图片
4. 将 GEI 创作过程放在最上方,原文阅读放在最后
5. Website 加入作者信息: https://x.com/LukeLiu95 刘仙升
6. 把项目提交到 GitHub (https://github.com/lukeliu95) 并通过 Vercel 部署 website

## 本轮目标

1. 对 `release/第二次署名-发布版.md`(2371 行 / 24 章)做新一轮独立内容评估,落到 `release/release-evaluation.md`。
2. 用 gei-imagine 双路径(Gemini 直连为主)为人物设定中的 8 + 1 位主要角色生成肖像插图,落到 `website/assets/characters/`。
3. 重构 `website/index.html`:
   - 顶部:Hero → GEI 创作过程时间线(11 轮)
   - 中部:作品亮点 + 全人物画廊(每人物配图 + 设定卡)
   - 底部:24 章原文阅读
   - 页脚:作者信息(刘仙升 / @LukeLiu95)
4. 项目静态页发布:
   - 在 `https://github.com/lukeliu95` 建仓 → push project
   - Vercel 链接 GitHub repo → 部署 `website/` 子目录为静态站点

## 基线说明(legacy 项目)

本项目 `ceo-rounds/.skip-verify` 标记 — 9 轮 round 已在 v6.1 baseline-snapshot 防线落地之前完成,无 `round-000-baseline.md`。Round 011 沿用 round-010 评分基线(95/100)作为隐式 baseline,不重新构造历史快照。

## Phase D 进入参数

- output_dir: output/jimei-rebirth-revenge-novel
- 起始评分: 95 / 100 (Round 010 维持)
- 现有发布物: release/第二次署名-发布版.md (24 章 · 2371 行) · website/index.html (R010)
- 现有插图: hero-cover.png · process-studio.png · reading-atmosphere.png

## 子任务路径

- T1 内容评估 → `release/release-evaluation.md`
- T2 人物插图(Gemini 直连) → `website/assets/characters/{role}.png` × 9
- T3 Website 重构 → `website/index.html` (整体重写) + 保留 `website/data/novel.md`
- T4 GitHub repo → `lukeliu95/jimei-second-signature`(待用户/工具确认仓库名)
- T5 Vercel 部署 → 链接 GitHub + root directory = `website/`

## 后续

执行完毕后写 round-011 retrospective + 更新 `local/gei-memory/projects-registry.md` + `local/gei-memory/customers/me.md` + `local/gei-memory/learnings.md`。

## 评分目标

Round 011 不改正文质量,主要提升:发布完整度 + 视觉呈现 + 公开可访问性。GEI 综合评分预计 95 → 96(+1pp · 来源:发布完整度提升 + 全人物插图 + 公开 URL)。
