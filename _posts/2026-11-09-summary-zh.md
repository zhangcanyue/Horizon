---
layout: default
title: "Horizon Summary: 2026-11-09 (ZH)"
date: 2026-11-09
lang: zh
---

> 从 55 条内容中筛选出 5 条重要资讯。

---

**科技新闻**
1. [KetchUp：用 Rust 与 WebGPU 打造的开源浏览器版 SketchUp 替代品](#item-tech-news-1) ⭐️ 7.0/10
2. [高盛据报收回银行家和交易员的 Claude Code 权限](#item-tech-news-2) ⭐️ 7.0/10
3. [Outlook.com 被指拒收未配置 DMARC 域名的邮件](#item-tech-news-3) ⭐️ 7.0/10
4. [SQLite parse\_number\(\) 扩展：C 与 Rust 实现对比](#item-tech-news-4) ⭐️ 7.0/10
5. [Nvidia 董事会启动独立调查，审查黄仁勋与涉华情报人员关系](#item-tech-news-5) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [KetchUp：用 Rust 与 WebGPU 打造的开源浏览器版 SketchUp 替代品](https://ketchup3d.github.io/app/) ⭐️ 7.0/10

KetchUp 是一个用 Rust 和 WebGPU 实现、可在浏览器中运行的开源 SketchUp 替代品，项目已发布并在 Hacker News 上引发讨论。它面向 3D 建模用户；有评论称赞其浏览器端界面和文本渲染效果，但整体反馈显示项目仍处于早期阶段。现有信息没有给出具体版本号或许可协议，也没有独立测试证明其建模能力与 SketchUp 对等。

hackernews · dcoulmbe · 11月8日 22:35 · [社区讨论](https://news.ycombinator.com/item?id=50418176)

**「背景」** WebGPU 是浏览器中用于调用 GPU 进行图形渲染与计算的新接口，WebAssembly 则让 Rust 等编译型语言的代码能在网页里运行；两者结合，是在不安装插件的情况下于浏览器中运行 3D 建模器的重要前提。KetchUp 用 Rust 和 WebAssembly 构建、以 WebGPU 渲染，并提供浏览器和桌面两种使用方式。

**「影响」** 对触控板用户来说，有反馈称当前操作“似乎只支持鼠标”，这会直接影响笔记本上的平移、缩放和旋转操作；在项目补齐触控板手势前，这类用户需要外接鼠标或改用其他工具。

**「社区讨论」** 多位评论者对浏览器中的 Rust UI 和文本渲染表示肯定，一名用户称其为 SketchUp 的“精神续作”，另有 3D 打印爱好者表示 SketchUp 8 最容易上手。最具体的可用性反馈是触控板支持缺失，同时有评论建议在落地页补充功能展示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Ketchup3D/app">GitHub - Ketchup3D/app: Free, open-source 3D modeling ...</a></li>
<li><a href="https://ketchup3d.github.io/app/">KetchUp — Free 3D Woodworking &amp; Furniture Design App</a></li>

</ul>
</details>

**标签**: `#open-source`, `#rust`, `#webgpu`, `#3d-modeling`, `#sketchup-alternative`

---

<a id="item-tech-news-2"></a>
### [高盛据报收回银行家和交易员的 Claude Code 权限](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 7.0/10

据报道，高盛正从投行人员和交易员手中收回 Claude Code 的使用权限。目前可核对的信息仅限于标题和社区讨论，具体范围、生效时间与撤回原因均未确认。现有材料没有给出技术细节，因此无法判断这是全面禁用，还是只针对部分岗位或工作站。

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**「背景」** 相关报道称，Goldman Sachs 此前数月允许银行家和交易员将 Anthropic 的 Claude Code 与 Microsoft 的 GitHub 一起用于跟踪客户资金流和搭建市场模型。同一报道还提到，该行此前已对香港员工的 Claude 使用做过地区性限制，而最新报道所述的限制则覆盖交易和投行岗位。

**「影响」** 若撤回属实，受影响的银行家和交易员将失去在这些工作机上使用 Claude Code 的选项，只能改用其他工具或转入审批后的受控环境。对计划在同类岗位部署编码代理的机构，讨论中最具体的操作警示是把代理与客户/交易数据、邮件和公网访问隔离，并保留可审计的权限链，否则现有权限边界很难约束代理行为。

**「社区讨论」** 讨论中最集中的技术担忧是“致命三要素”：编码代理与客户/交易数据、邮件和互联网同机运行，风险过高。另有评论者报告所在机构因消费计费长期超支而回收 Claude 权限，并称 Gemini 的固定计费更有吸引力；也有人把宣布时机与高盛据称牵头 Anthropic IPO 联系起来，质疑其动机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers">Goldman Sachs Is Pulling Claude Code From Its Bankers and ...</a></li>
<li><a href="https://www.fa-mag.com/news/goldman-restricts-traders-and-bankers-from-using-some-ai-tools-89026.html">Goldman Restricts Traders And Bankers From Using Some AI Tools</a></li>

</ul>
</details>

**标签**: `#enterprise AI adoption`, `#AI coding agents`, `#security and compliance`, `#financial services`, `#Anthropic Claude Code`

---

<a id="item-tech-news-3"></a>
### [Outlook.com 被指拒收未配置 DMARC 域名的邮件](https://mailroute.net/blog/outlook-rejecting-email-without-dmarc) ⭐️ 7.0/10

Mailroute 博客及 Hacker News 讨论称，Outlook.com 正在拒收来自未配置 DMARC 的域名所发邮件；目前没有微软官方说明，具体生效范围、起始时间和判定规则仍不明确。受影响的主要是向 Outlook.com 用户发信、但域名缺少 DMARC 记录的发送方，自建邮件服务器和小型服务商尤其需要检查 DNS 配置。按 DMARC 的基本要求，发送方需发布相应策略记录，并保证 SPF 或 DKIM 与发信域名对齐，否则送达率可能下降。

hackernews · xmddmx · 11月8日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50416158)

**「背景：DMARC 与邮箱服务商的认证要求」** DMARC 是建立在 SPF 和 DKIM 之上的邮件认证策略，域名发布 DMARC 记录后，接收方服务器才能据此判断一封邮件是否获得该域名的授权，而不仅是拦截伪造发件人。大型邮箱服务商收紧这类要求已有先例：2024 年 2 月起，Gmail 开始要求发件方配置邮件认证，对每天向 Gmail 发送超过 5000 封邮件的批量发件人提出更严格的 SPF、DKIM 与 DMARC 要求，Yahoo 也同期跟进。此次 Outlook.com 对无 DMARC 域名的拒收，属于同一认证要求扩展至另一家主要消费级邮箱服务商的情况。

**「对发信方的影响」** 对向 Outlook.com 发信的域名运营者来说，未发布 DMARC 可能导致邮件被拒收；若收到 5xx 退信，应把它当作永久性投递失败处理，而不是继续重试。应先核对并配置 SPF、DKIM 与 DMARC 的对齐，再根据退信码排查，因为仅凭 SMTP 接收成功并不能保证邮件进入收件箱。

**「社区讨论」** 讨论中，Neikius 认为要求 DMARC 本身可以接受，但批评 Outlook 还会依据不公开、难以申诉的封禁名单拦截其 VPS；codethief 则称即使 SPF/DKIM/DMARC 齐全，邮件也会在日志显示已接收后未投递。dwm 反驳“悄悄拒收”的说法，称发件方收到的是 5xx 永久退信；这些均为参与者经验，未获微软确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://resend.com/blog/gmail-and-yahoo-bulk-sending-requirements-for-2024">Gmail and Yahoo’s bulk sending requirements for 2024 · Resend</a></li>
<li><a href="https://www.proofpoint.com/us/blog/email-and-cloud-threats/google-and-yahoo-set-new-email-authentication-requirements">DMARC Policy &amp; Setup Requirements for Google &amp; Yahoo Email</a></li>
<li><a href="https://learn.microsoft.com/en-us/answers/questions/5790042/outlook-com-rejecting-email-messages-for-security">outlook . com rejecting email messages for security... - Microsoft Q&amp;A</a></li>

</ul>
</details>

**标签**: `#DMARC`, `#email authentication`, `#Microsoft Outlook`, `#email deliverability`, `#self-hosted email`

---

<a id="item-tech-news-4"></a>
### [SQLite parse\_number\(\) 扩展：C 与 Rust 实现对比](https://simonwillison.net/2026/Nov/8/sqlite-parse-number-c-vs-rust/) ⭐️ 7.0/10

Simon Willison 发布了一项研究：他让 Claude Opus 5.5 分别用 C 和 Rust 实现 SQLite 的 parse\_number\(\) 扩展。该函数会把“-$1,234.56”“12.5%”这类字符串清理为可求和、可排序的数值，无法解析时返回 NULL。初版 Rust 扩展的 .so 文件为 321 KB（使用 Rusqlite）和 298 KB（使用 sqlite-loadable-rs），C 版仅 14 KB；但 Rust 版最初更快，作者认为原因是 Rust 中与 C 的 strtod 等价的实现速度约为 C 的两倍。随后他让模型手写自定义 C 解析函数，在 200 万行数据上把混合数据的每行净开销从 67 ns 降到 19 ns，而 Rusqlite 和 sqlite-loadable-rs 分别为 46 ns 和 41 ns；纯整数场景为 16 ns 对 36/32 ns，纯小数场景为 18 ns 对 55/47 ns。上述数字来自作者的实验性研究，尚未经过独立验证。

rss · Simon Willison · 11月8日 22:26

**「背景」** SQLite 允许通过可加载扩展（loadable extension）动态注册自定义 SQL 函数：扩展被编译成共享库（.so/.dylib/.dll），再由连接 API 或 load\_extension\(\) 载入。C 是 SQLite 的原生扩展接口，Rust 则要经由 Rusqlite、sqlite-loadable-rs 这类绑定层来封装。C 标准库的 strtod 是常用的字符串转数值函数，而本次实验中最初的性能差距，正源于 Rust 侧等价实现与 strtod 的解析速度不同。

**「影响」** 对需要分发 SQLite 可加载扩展的开发者来说，这项对比说明仅凭编程语言不足以判断性能：初版 C 版产物只有 14 KB，却慢于约 300 KB 的 Rust 版；改写后的 C 解析器则在测试负载上反超。实际选型应针对目标数据和平台复测，不能只凭“Rust 更快”或“C 更小”的预设决定。

**标签**: `#SQLite`, `#Rust`, `#C`, `#extensions`, `#performance`

---

<a id="item-tech-news-5"></a>
### [Nvidia 董事会启动独立调查，审查黄仁勋与涉华情报人员关系](https://www.theverge.com/ai-artificial-intelligence/1029562/nvidia-investigating-jensen-huang-relationship-chinese-spy) ⭐️ 7.0/10

Nvidia 董事会宣布启动一项独立调查，起因是有报道称公司创始人兼 CEO 黄仁勋成为外国情报活动的目标；报道涉及他与 Megaspeed 高管 Alice Huang 的关系，后者据称被中国国家安全部招募来针对 Nvidia 进行情报活动。根据董事会发布的声明，调查将由一个独立董事委员会负责监督，并聘请外部独立律师协助。需要说明的是，有关间谍活动的指控目前来自媒体报道，在所提供的文本中未获独立证实，且董事会声明引文在原文中被截断，仅到“董事会将美国国家和经济安全置于首位”为止。

rss · The Verge · 11月8日 20:22

**「背景」** 此次调查的直接背景是美方此前对 Megaspeed 的审查：据《纽约时报》报道，美国政府曾调查这家公司是否可能将英伟达的先进 AI 芯片转运至中国，并对 Alice Huang 进行了超过一年的监控。相关报道公开后，国会议员也表示希望就黄仁勋与 Alice Huang 的关系质询他。

**「影响」** 调查由独立董事委员会而非管理层内部处理，并配有外部律师，意味着结论将直接提交董事会；在调查结果公布前，与 Nvidia 及 Megaspeed 有业务往来的合作方所面临的合规不确定性难以消除，而董事会声明把美国国家和经济安全列为优先事项，也暗示审查可能触及公司对华业务往来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/08/jensen-huang-nvidia-china-spy-congress.html">Nvidia CEO faces Congress scrutiny over Chinese spy reports</a></li>
<li><a href="https://www.nytimes.com/2026/11/08/technology/nvidia-investigation-jensen-huang-china.html">Nvidia Opens Investigation Into Jensen Huang’s Relationship ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#China espionage`, `#AI hardware`, `#corporate governance`

---