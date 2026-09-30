# AI Digest Editorial Skill

中文AI日报的可移植Agent技能包：一手来源优先，国内外兼顾，四板块正文，HTML静态发布＋高清多图交付。

## 正文结构
1. 模型与产品
2. 商业与政策
3. 技术研究
4. 核心博客（仅主要模型公司官方博客，标题带公司标签）

重点覆盖OpenAI、Anthropic、DeepMind、Meta、Mistral、DeepSeek、Qwen、MiniMax、Moonshot/Kimi、智谱及字节Seed。整合TLDR AI、The Rundown AI、Import AI、InfoQ AI快讯作为信息参考与发现入口。

## 安装
下载Release中的ZIP，解压后将包含SKILL.md的目录放到你的Agent技能目录。

Hermes默认profile示例（若目标目录已存在，先备份/比较，不直接覆盖）：

```bash
git clone https://github.com/xlvecle/ai-digest-editorial-skill.git
mkdir -p ~/.hermes/skills
cp -R ai-digest-editorial-skill ~/.hermes/skills/ai-digest-editorial
```

然后新建会话或重新加载技能，提出：

> 使用ai-digest-editorial生成今天AI日报，按四板块制作HTML和2160px宽阅读图，发布到我的Cloudflare Pages并发送图片。

首次检查已有HTML发布能力；没有则提示配置GitHub Pages、Cloudflare Pages或Netlify等静态托管。未配置时可先交付本地HTML与图片，不阻塞制作。本包不自动创建cron，不附带任何个人账号、网站、凭据或历史日报。非默认Hermes profile请放入对应profile的skills目录。

## 能力与边界
这是**编辑与交付工作流skill**，不是无人值守的RSS抓取软件。它依赖宿主Agent具备网页读取、文件操作、HTML渲染、截图及部署能力。来源可能限流或拦截，必须核验并披露缺口；模型会犯错，不能省略事实校对。Cloudflare发布可配合独立的cloudflare-pages-slides技能或官方部署工具。

- 默认昨日＋隔夜重大更新，不因时区漏发布会。
- 不强制Gemini或其他单独摘要API。
- 图片原生2160px宽，克制杂志式排版，不生成中文文字图像。
- 不默认发邮件。

## 文件
- SKILL.md：执行入口与验收
- references/editorial.md：来源、归类与核验
- references/design.md：高清图片设计规范
- references/publishing.md：安全发布与附件交付
- NOTICE.md：来源和再分发边界

## License
本仓库新编写的技能说明采用MIT。仅涵盖本仓库文件，不涵盖引用网站、新闻内容或任何外部项目。
