# CEO Round 010 - Website 介绍页与多模态配图

## 触发

用户指令：进入 `output/jimei-rebirth-revenge-novel` 项目《第二次署名》，生成 Website 介绍页面。

用户补充确认：`release/第二次署名-发布版.md` 是正式发布版本。

## 本轮目标

1. 生成作品 Website 介绍页。
2. 页面必须包含小说原文阅读。
3. 页面必须包含这部小说如何生成的整体过程介绍。
4. 为小说生成配图，并使用 GEI 多模态能力绘制插图。

## 内容来源

- 正文唯一来源：`release/第二次署名-发布版.md`
- 页面数据副本：`website/data/novel.md`
- 生成过程来源：`ceo-rounds/round-001.md` 到 `round-009.md`、`release/delivery-report.md`、`quality-assessment.md`
- 作品设定来源：`story-outline.md`、`characters.md`、`beat-map.md`

## Worker 派遣

已派只读 explorer worker 查看发布版正文、交付报告、大纲、人物、节奏表和 CEO round 记录。

worker 输出结论：

- Website 应定位为“作品阅读页 + 创作过程展示页”，不是单纯宣传落地页。
- 核心模块应包含 Hero、小说原文阅读、生成过程介绍、作品亮点、人物关系、爽点节奏和交付状态。
- 配图建议包含 hero/封面图、阅读区氛围图、过程/创作图三类。

## 多模态配图

使用 GEI 多模态能力生成 3 张项目插图，并复制到：

- `website/assets/hero-cover.png`
- `website/assets/reading-atmosphere.png`
- `website/assets/process-studio.png`

插图用途：

1. Hero / 封面：女博士、证据、校园湖景、署名权主题。
2. 阅读区：录音笔、项目书、证据索引和安静阅读氛围。
3. 生成过程：章节卡片、迭代时间线、AI 辅助创作工作台。

## Website 产物

新增：

- `website/index.html`
- `website/data/novel.md`
- `website/assets/hero-cover.png`
- `website/assets/reading-atmosphere.png`
- `website/assets/process-studio.png`

页面能力：

- 首屏作品介绍与立即阅读入口。
- 作品亮点和人物关系展示。
- 从正式发布版 Markdown 加载 24 章全文。
- 自动生成章节目录。
- 阅读进度条、夜间模式、字号调整、行距切换、返回顶部。
- 9 轮 Phase D 生成过程时间线，加 Round 010 Website 本轮说明。

## 质量变化

GEI 综合评分维持：95 / 100

本轮不是正文质量改写，而是发布展示能力增强：

- 正式发布版正文可通过网页直接试读。
- 生成过程从内部记录转为客户可理解的展示页面。
- 多模态插图补齐作品视觉呈现。

## 剩余建议

1. 如需公开发布，可把 `website/` 单独部署为静态站点。
2. 正式出版前仍建议法律专业读者复核法律措辞。
3. 如需最终交付包，下一步可执行“生成交付报告”标准打包流程。
