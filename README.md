# 第二次署名

> 一部经过 11 轮 GEI Agent 协作迭代的中文女性向重生复仇小说。
> 24 章 · 约 8 万字 · 发布版 GEI 综合评分 95.5 / 100。

[![Author](https://img.shields.io/badge/author-%E5%88%98%E4%BB%99%E5%8D%87-9d3326)](https://x.com/LukeLiu95)
[![X](https://img.shields.io/badge/%F0%9D%95%8F-@LukeLiu95-1f6b5f)](https://x.com/LukeLiu95)
[![GitHub](https://img.shields.io/badge/GitHub-lukeliu95-171512)](https://github.com/lukeliu95)

---

## 内容简介

林书宁，社会学女博士。前世死在湖边，前男友周予衡和"年度女性榜样"宋绮年联手把她从项目书署名页删除，把她的田野材料改成别人的青年项目，把她推下湖，让她"自己走进了情绪不稳定"。

第二世，她回到博士开题前。她不再是那个"轻一点，再轻一点"的女孩。她把每一次羞辱转化成录音、备份、证据链、项目策略和组织方案。脑内豆包像一个过分严谨又偶尔吐槽的 AI 助手，把情绪事件翻译成行动建议:

> "检测到煤气灯话术：他正在把署名要求改写成你太功利。"
> "符合组织要求[强]：保留原话、备份录音、延迟回应。"
> "警告：你现在想解释，是因为前世习惯性自证。建议改为提问。"

她要夺回的不是爱情。她要夺回的是知识劳动、女性证词和被轻视的人名进入档案的权利 — 也就是**第二次署名**。

## 主要看点

- **署名权 + 智性取证**: 录音键、网页存证、时间戳校验、匿名墙取证、判决书署名页
- **女权视角双重反讽**: 宋绮年"让女性成为彼此的光"被林书宁问回"互助的前提是普通女孩献祭吗"
- **男一男二双线**: 沈砚（法学博士后）负责程序，陆知白（计算社科博士+陆氏寰球家族公子）负责技术。他们可以争风吃醋,但权限只有"仅可评论"
- **女性证词链**: 同门何蔓 + 合作导师蒋曼青 + 保洁员刘桂芬，从"沉默"到"证词协作员"
- **现实主义后段**: 第 19-21 章用七个月调查、学术审查、刑民分轨、判决书三章承担反爽文的真实重量

## 怎么读

- **网站阅读**: 部署后的 Vercel 链接（创作过程置顶 / 全 9 张人物插图 / 24 章正文置底）
- **本地阅读**: 直接打开 [`release/第二次署名-发布版.md`](release/第二次署名-发布版.md)
- **本地预览**: `python3 -m http.server 8000` 后访问 `http://localhost:8000/website/`

## 仓库结构

```
.
├── release/                       # 发布版
│   ├── 第二次署名-发布版.md         # 24 章正式正文
│   ├── delivery-report.md
│   ├── release-evaluation.md      # Round 011 独立评估
│   └── README.md
├── website/                       # 静态站点 (Vercel root directory)
│   ├── index.html
│   ├── data/novel.md              # 渲染源 (与 release 同步)
│   └── assets/
│       ├── hero-cover.png         # 封面
│       ├── process-studio.png     # 创作过程氛围图
│       ├── reading-atmosphere.png # 阅读区氛围图
│       └── characters/            # 9 张人物肖像 (gei-imagine 生成)
│           ├── 01-lin-shuning.jpg
│           ├── 02-shen-yan.jpg
│           ├── ... 等
│           └── 09-lin-parents.jpg
├── novel.md                       # 工作稿 (含 Round 001-011 历史轨迹)
├── story-outline.md               # 24 章大纲
├── characters.md                  # 人物设定
├── worldbuilding.md               # 世界观
├── beat-map.md                    # 爽点/痛点/泪点节奏表
├── content-review.md              # 文学大师 agent 评审
├── quality-assessment.md          # GEI 质量评估
├── publication-checklist.md       # 出版前清单
└── ceo-rounds/                    # Phase D 11 轮迭代记录
    ├── round-001.md ~ round-011.md
    └── ...
```

## GEI 创作过程

| 阶段 | 描述 | 评分 |
|---|---|---:|
| Phase A-C | 需求识别 / 世界观 / 人物 / 大纲 / 开篇 / 质量评估 | → 88.5 |
| Round 001 | 节奏设计与新增元素整合 | 88.5 → 91.2 |
| Round 002 | 女博士与世界五百强项目升级 | 91.2 → 92.4 |
| Round 003 | 全章草稿与文学大师评审 | → 84 |
| Round 004 | 文学性与现实阻力增强 | 84 → 88 |
| Round 005 | 法律程序与时间跨度精修 | 88 → 90 |
| Round 006 | 可读性与沉浸感提升 | 90 → 92 |
| Round 007 | 语言润色与读者钩子 | 92 → 93 |
| Round 008 | 出版前清稿与一致性检查 | 93 → 94 |
| Round 009 | 发布版排版与交付报告 | 94 → 95 |
| Round 010 | Website 介绍页与多模态配图 | 维持 95 |
| **Round 011** | **发布版评估 + 全人物画廊 + 公开发布** | **95 → 95.5** |

## 关于 GEI Agent

GEI 是一个面向任意用户、任意项目的自主交付 Claude Code agent。一个 orchestrator + 7 个 worker + 3 个横切 + 1 个 meta，按 Phase A→B→C→D 四阶段编排,在阶段边界跑反思检查点(Reflection Checkpoint),并在 Phase D 用 CEO 循环做产品进化。

本作品由 GEI 完成 Phase A-C 的需求识别、世界观/人物/大纲设计、24 章正文撰写、文学评审，再走 11 轮 Phase D CEO 循环精修出来；作者负责整体方向、阶段决策和公开发布。

GEI Agent 仓库未公开。

## 作者

**刘仙升** · 独立创作者
- 𝕏: [@LukeLiu95](https://x.com/LukeLiu95)
- GitHub: [@lukeliu95](https://github.com/lukeliu95)

## 版权与免责

- 文本与角色版权 © 2026 刘仙升,保留所有权利。
- 本作为 AI 协作创作。所有人物、机构、事件均为虚构;南江大学、陆氏寰球、宋氏基金会等设定均不指代任何现实组织。
- 法律程序与刑民分轨为戏剧化处理;正式出版前建议法律专业读者复核措辞。
- 插图由 gei-imagine(Gemini 3.1 Flash Image)生成,均为虚构人物,不指代任何真实个人。
