# 发布与交付

本包是Agent执行规范，不包含部署客户端、浏览器或自动定时任务。需要工具可用的Agent与HTML渲染能力；HTML托管不限定Cloudflare。

## 首次配置检查
先检查用户已有发布平台、项目、目录和安全凭据可用性，不打印密钥。已有可用配置就复用，不强制迁移。若没有Cloudflare也没有其他发布能力，明确提示：“目前还没有HTML发布配置。可以配置GitHub Pages或Cloudflare Pages；现在仍可先生成本地HTML和图片。”询问必要的平台选择/授权，不猜账号，不在聊天索取真实密钥，不未经授权公开任何内容。没有发布配置不能阻塞内容和图片制作，也不能冒称已经上线。

## 免费静态托管选择
- GitHub Pages：适合已经用GitHub的人，公开仓库可用免费计划，push后发布，提供github.io地址，也支持自定义域名。不适合直接放秘密或私密日报。https://pages.github.com/ 与 https://docs.github.com/en/get-started/learning-about-github/githubs-plans
- Cloudflare Pages：适合持续自动发布，提供pages.dev地址，免费计划有构建与文件数限制。https://developers.cloudflare.com/pages/platform/limits/
- Netlify：适合拖拽HTML文件夹快速上线（Netlify Drop）或Git部署；Free是有限额度，并非无限托管，用前核对当前credits规则。https://app.netlify.com/drop 与 https://docs.netlify.com/manage/accounts-and-billing/billing/billing-for-credit-based-plans/credit-based-pricing-plans/

免费额度和条款会变，配置前查官方文档。不承诺中国大陆或微信内访问一定稳定，应测试实际目标网络；自定义域名不等于必须购买域名，可先用平台子域名。

## 安全部署
凭据仅通过环境或受保护的密钥管理提供，不写仓库、日志、HTML或图片。若使用Cloudflare且已安装cloudflare-pages-slides，加载其非破坏式发布流程；其他平台用官方工具。共享站点必须基于完整站点目录构建，不能只上传新一期覆盖旧页。同步索引/manifest。

推荐slug ai-digest-YYYY-MM-DD；同日修订使用未占用的-r2等版本。部署后读取生产正文核对日期、四板块顺序、公司前缀及来源链接，并读取目录确认新旧页面保留。HTTP200不是内容验收。

本地归档核验稿、HTML、图片、来源记录和发布receipt。仅生产验证成功后更新已发布ledger。

Hermes通过MEDIA绝对路径逐张交付图片，其他Agent用附件工具。生产链接只写在聊天消息，不在图片印“详见HTML”等提示。未部署时交付本地HTML文件和图片并明示状态；未验证投递时不声称用户已收到。
