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

---

## 执行结果

### T1 · 内容评估 ✅

`release/release-evaluation.md` 已写入。综合评分 **95.5/100**(Round 010 95.0 → +0.5)。7 维度评分:

| 维度 | 分数 |
|---|---:|
| 类型契合度 | 94 |
| 女权视角 | 93 |
| 人物张力 | 92 |
| 情节推进 | 94 |
| 文学表达 | 92 |
| 原创性 | 90 |
| 发布完整度 | 95 |

结论:**发布版可对外发布**。

### T2 · 全人物插图 ✅

`website/assets/characters/` 新增 9 张肖像(中国当代文学水彩水墨混合风格,3:4 portrait,1K):

1. `01-lin-shuning.jpg` — 林书宁(主角 26 岁,书桌前 + 项目书 + 录音笔)
2. `02-shen-yan.jpg` — 沈砚(男一 28 岁,法学院走廊 + 法律材料夹)
3. `03-lu-zhibai.jpg` — 陆知白(男二 27 岁,工作墙 + 笔记本电脑)
4. `04-zhou-yuheng.jpg` — 周予衡(反派 27 岁,夜晚校园湖边 + 深灰大衣)
5. `05-song-qinian.jpg` — 宋绮年(反派 28 岁,雨中长廊 + 黑伞 + 珍珠耳环)
6. `06-he-man.jpg` — 何蔓(证人 25 岁,合租屋 + 手机)
7. `07-jiang-manqing.jpg` — 蒋曼青(合作导师 34 岁,办公室 + 论文堆)
8. `08-liu-guifen.jpg` — 刘桂芬(关键证人 54 岁,教学楼走廊 + 暗酒红外套)
9. `09-lin-parents.jpg` — 林家父母(书房双人场景)

调用方式:`bash skills/gei-imagine/scripts/gemini-image.sh` 9 个并行 background bash,~30s 总耗时。Gemini API 实际返回 JPEG bytes,脚本自动从 `.png` 改名为 `.jpg`。

### T3 · Website 重构 ✅

`website/index.html` 重写。新结构:

| 区块 | 位置 | 用途 |
|---|---|---|
| Hero | 顶部 | 书名 + Round 011 kicker + 阅读/过程 CTA + 三项 stat(24 章 / 11 轮 / 95.5 分) |
| § GEI 11 轮创作过程 | **置顶**(用户指定)| 12 个时间线节点(Phase A-C 基底 + Round 001-011),含 phase-tag + 评分变化 |
| § 作品亮点 | 中部 | 8 张特性卡(署名权 / 录音键 / 女性话术反杀 / 男一男二 / 证词协作员 / 湖边反杀 / 制度性打脸 / 脑内豆包) |
| § 全人物画廊 | 中部 | **9 张大图卡片**(image + name + role tag + meta + bio + 招牌台词引言) |
| § 关于作者 | 中部 | 刘仙升 author card + 𝕏 / GitHub 链接 |
| § 原文阅读 | **底部**(用户指定)| 24 章 markdown reader + TOC + 字号/行距/夜间模式控制 |
| Footer | 末尾 | 版权 + 𝕏 + GitHub |

`website/data/novel.md` 与 `release/第二次署名-发布版.md` 保持同步(diff 0)。

### T4 · GitHub 公开仓库 ✅

`https://github.com/lukeliu95/the-second-signature`(public)

- `git init -b main`
- 42 文件首次 commit(`c274d8f` · 含 release/website/ceo-rounds/全部产物)
- `gh repo create --public --source=. --push` 一步推送
- 首次推送完成后追加一次 commit `1bf05fe` 把 vercel link 产生的 `website/.gitignore` 收进 repo

### T5 · Vercel 部署 ✅

`https://the-second-signature.vercel.app`(production aliased)

- `vercel project add the-second-signature`(创建项目)
- `cd website && vercel link --yes --project=the-second-signature`(链接 .vercel/)
- `vercel deploy --prod --yes`(14MB 上传 / 28s 部署)
- `vercel git connect https://github.com/lukeliu95/the-second-signature.git`(连接 GitHub)

线上验证(curl):
- `/` → 200
- `/data/novel.md` → 200
- `/assets/characters/01-lin-shuning.jpg` → 200
- `/assets/hero-cover.png` → 200

### T6 · 留痕 ✅

- `local/gei-memory/projects-registry.md` 追加 Round 011 行
- `local/gei-memory/customers/集美文学复仇小说.md` 加 GitHub/Vercel/作者元数据 + Round 011 retro 段
- `local/gei-memory/learnings.md` 追加 Round 011 retro(3 个 pattern 候选 / 3 个 pitfall 候选)

## 已知 follow-up

1. ~~**Vercel rootDirectory**: 当前默认 `.`。git-triggered auto-deploy 要 dashboard 改成 `website`~~ — **已解决**。把 `vercel.json` 从 `website/` 提升到 repo 根并加 `outputDirectory: "website"`,git push 自动重部署可正常工作。验证:`git push` 后 17s 内新 production deployment ready,所有路由 200。
2. **gemini-image.sh set -e bug**: 脚本末行 `[[ -f X.txt ]] && echo` 在文件不存在时触发 `set -e` 让脚本 exit 1,但图片实际已写入。9 张图全部正常,但 background task notification 显示 "failed"。已写入 learnings.md follow-up,等 GEI 工具维护轮修。
3. **法律措辞专业校验**: 仍按 release-evaluation 第 4 条建议保留(正式出版前)。

## 评分变化

GEI 综合评分:**95.0 → 95.5**(+0.5pp,来源:发布完整度从 90 → 95 + 全人物视觉呈现完整度 + 公开可访问性)。

---

## Round 011 addendum · 首页 10s 介绍视频(2026-04-29 同日完成)

用户追加要求:首页 10 秒 16:9 视频,介绍小说,多镜头切换 + 文字动态。

**用户选择(AskUserQuestion 确认)**: A 文学意象蒙太奇 · 一次出片不重做(省钱)。

**生成参数**:
- 模型: `doubao-seedance-2.0`(APImart 异步任务模式)
- 分辨率: 720p · 16:9 · 10s
- `generate_audio=true`(钢琴 + 大提琴温暖叙事)
- 8 镜头蒙太奇 prompt:湖面涟漪 → 项目书署名页(钢笔写"林书宁")→ 录音笔指示灯 → "證詞協作員"胸牌 → 法院红章盖判决书 → 发布会发言 → 书页飘起 → 黑底白金"第二次署名"。

**实测**:
- 提交 → 50% 卡帧合成 → 99% → completed,end-to-end ~6 分钟(比文档示例 1-3 分钟略慢,可能因 10s 比 5s 默认翻倍 + 配音合成)。
- 产物 2.96 MB · H.264 1280×720 · 10.04s · AAC 44.1kHz。
- 24h URL 已立即下载到 `website/assets/intro-video.mp4`。

**网站集成**:
- `index.html` topbar 下、hero 上新增 `.intro-video` section,16:9 frame 自动播放静音循环 inline。
- poster 用现有 `assets/hero-cover.png` 作为加载前占位。
- `aria-label` 描述 8 镜头内容,SR 友好。
- 不引入新 JS(纯 HTML5 video 标签 + autoplay/muted/loop/playsinline)。

**评分**:维持 95.5(视频是发布完整度的进一步增强,但本轮已计入发布完整度满分 · 视为 0 分增量但显著提升首屏冲击力)。

**费用**:单次出片 ~¥4-8(估算,实际取 APImart 账单)。

## 留痕(addendum)

- `local/gei-memory/customers/集美文学复仇小说.md` 加 video 段落
- `local/gei-memory/learnings.md` 加 doubao 50% 卡帧观察 + intro-video hero 集成 pattern
