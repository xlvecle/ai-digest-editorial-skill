---
name: ai-digest-editorial
description: "Use when creating Chinese AI digests. Verify primary sources and deliver a four-section HTML brief plus readable high-resolution images."
---

# AI 日报编辑与图文发布

以当前Agent完成采集、核验、编辑，不强制额外摘要API。使用前读取 references/editorial.md、references/design.md、references/publishing.md。

## 工作流

1. 用系统工具取得当前时间，标注北京时间截止时间。采集“北京时间昨日＋截至出稿的隔夜重大更新”，一般回看24–48小时。海外发布会按当地日期备注，不因跨日遗漏。
2. 优先核验官方公告、技术报告、论文、模型卡、代码release、API文档。Newsletter和媒体用来发现；重大商业事件可使用高可信媒体，明确报道性质。
3. 检查历史归档，合并同一事件；重跑明确修订版，不把新收录的旧文当新发布。
4. 正文严格四板块：**模型与产品 → 商业与政策 → 技术研究 → 核心博客**。不设社交媒体板块；原帖可作为对应主题证据。
5. 国内国际分别关注，按事件主体而非文章语言分类。没有合格新闻就说明，不强凑比例、数量或每天每家公司。
6. 每条写清事实、日期、关键技术/商业细节、局限、影响判断与原始链接；区分厂商声明、独立测试和编辑观点。
7. 从同一份核验稿制作手机适配HTML和多张高清阅读图。不要用模型生成图片中的中文文字；用浏览器/排版程序确定性渲染。
8. 检查已有HTML发布能力，优先复用用户配置的平台（Cloudflare Pages、GitHub Pages或其他静态托管）。没有配置时提示用户配置发布能力，不强制Cloudflare；仍先交付本地HTML与图片，明确未上线。部署前取得授权，部署后读回线上正文和目录验证。默认不发邮件，不擅自创建定时任务。

## 核心博客规则

仅收主要模型公司的官方研究/工程博客：OpenAI、Anthropic、Google DeepMind、Meta AI、Mistral；DeepSeek、Qwen/阿里通义、智谱Z.ai、Moonshot AI/Kimi、MiniMax、字节Seed。

标题前标公司，例如【OpenAI】、【MiniMax】、【Moonshot AI／Kimi】、【智谱／Z.ai】。独立博主、媒体和非模型公司不进入此栏。产品发布归第一栏，核心博客优先研究方法与工程复盘，避免重复。

## 验收

- 四板块顺序正确，无社交媒体标题；核心博客公司前缀与归属正确。
- 核心事实有已读取证据；时间、币种、单位和可用范围准确。
- HTML和图片一致，日期、来源、限制不丢失。
- 原生2160px宽PNG；逐页检查缺字、截断、溢出、对比度和手机缩放阅读。
- 发布成功需生产页正文及索引读回验证，不能只看HTTP200。
- 最终给URL与图片，不只给目录。失败交付已成功部分，说明阻塞，不伪造成功。
