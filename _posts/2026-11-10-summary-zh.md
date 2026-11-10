---
layout: default
title: "Horizon Summary: 2026-11-10 (ZH)"
date: 2026-11-10
lang: zh
---

> 从 108 条内容中筛选出 12 条重要资讯。

---

**科技新闻**
1. [HN 讨论称消费级 Gemini 可能将邮件与 Drive 内容交人工审阅](#item-tech-news-1) ⭐️ 8.0/10
2. [Show HN：查询任意地点过去一周的卫星过境与实拍影像](#item-tech-news-2) ⭐️ 8.0/10
3. [E-means 声称以十分之一 epoch 超越 k-means](#item-tech-news-3) ⭐️ 8.0/10
4. [OpenSSH 与 musl 交互漏洞遭在野利用，可无密码登录高权限账户](#item-tech-news-4) ⭐️ 8.0/10
5. [Claude Code 设置文件在 GitHub 上泄露数千条密钥](#item-tech-news-5) ⭐️ 8.0/10
6. [谷歌发布 TPU 8tx 与 8i Max 两款专用芯片](#item-tech-news-6) ⭐️ 8.0/10
7. [Anthropic 发布 Mythos 与 Fable 模型，称编码推理视觉有改进](#item-tech-news-7) ⭐️ 7.0/10
8. [英伟达董事会据报调查黄仁勋，CEO 留任概率被估五五开](#item-tech-news-8) ⭐️ 7.0/10
9. [MIT 报道单一 AI 模型跨域模拟沙粒流动与蛋白质折叠](#item-tech-news-9) ⭐️ 7.0/10
10. [LingBot-Touch：潜空间预测优于重建的触觉预训练](#item-tech-news-10) ⭐️ 7.0/10
11. [XGBoost 提前 2 小时预测县级新增停电，PR-AUC 约为基线 2.4 倍](#item-tech-news-11) ⭐️ 7.0/10
12. [欧盟草案拟限制成瘾性设计并标注虚拟币真实币值](#item-tech-news-12) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [HN 讨论称消费级 Gemini 可能将邮件与 Drive 内容交人工审阅](https://github.com/thisisme6598/gemini_files/) ⭐️ 8.0/10

2026 年 11 月 9 日 Hacker News 上的一则讨论称，消费级 Google Gemini 在用户启用 Connected Apps 后，可能把来自 Gmail 和 Drive 的个人邮件与文件交给人工标注者审阅；这是讨论中的指控，帖子没有提供 Google 的确认或可复核的完整证据。评论者指出范围应限定为消费级 Gemini：他们引用的 Workspace 管理文档仍称 Workspace Gemini 不受人工审阅，并称消费级 Gemini 的数据处理路径与 Workspace 不同。讨论没有说明人工审阅的触发频率、数据保留期限或适用地区，因此无法判断哪些具体内容会进入审阅。

hackernews · gf74918 · 11月9日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=50429426)

**「消费级与 Workspace 的差异」** 消费级 Gemini 的 Connected Apps 需要用户逐项授权 Gmail、Drive 等应用，授权后 Gemini 才能调用这些应用中的个人数据来完成检索或操作，这正是本次争议涉及的功能边界。作为对照，讨论中援引的 Google Workspace 帮助页称 Workspace 版 Gemini 不受人工审核约束，因此相关担忧主要集中在消费级账户，而非企业 Workspace 账户。

**「影响」** 对已授权 Connected Apps 的消费级 Gemini 用户，直接影响是 Gmail 邮件和 Drive 文件可能进入与 Workspace 不同的数据处理路径，而评论者引用的 Workspace 文档称后者不受人工审阅。重视隐私的用户可检查并撤销不必要的 Connected Apps 授权，或考虑改用 Workspace 账户；但现有讨论没有说明审阅触发条件，无法据此判断哪些文件会被选中。

**「社区讨论」** 评论者主要争论适用范围：bri3d 强调涉事的是消费级 Gemini 的 Connected Apps，Workspace Gemini 仍声称不受人工审阅；rustyhancock 则报告 Gemini 的回答似乎异常贴合其收到的邮件，但未给出可验证证据。EMM\_386 等人把担忧扩大到 Google Photos 的数据推断和行业数据实践，这些属于观点与个人体验，不能视为已确认事实。

**标签**: `#Google Gemini`, `#privacy`, `#AI data governance`, `#human annotation`, `#connected apps`

---

<a id="item-tech-news-2"></a>
### [Show HN：查询任意地点过去一周的卫星过境与实拍影像](https://www.watched.earth/) ⭐️ 8.0/10

开发者 a585gupt 发布 Show HN 项目 watched.earth：在浏览器中输入任意地点，即可列出过去 7 天经过该地上空的卫星，并调取相应过境的 Sentinel-2、Landsat 和 NASA 实际影像。过境搜索基于 CelesTrak 目录运行 SGP4，作者称在浏览器内约半秒完成，并用极点、反子午线和小幅宽场景与暴力算法对比，得出 0 漏检。页面把约 1.7 万个在轨目标交给 GPU 渲染、逐帧求解开普勒方程；作者还指出 Sentinel-2 时间戳与卫星实际过境常相差 5–10 分钟。工具只在确有真实影像时显示“watched”，不存储用户位置，代码已在 GitHub 开源发布。

hackernews · a585gupt · 11月9日 17:51 · [社区讨论](https://news.ycombinator.com/item?id=50428907)

**「背景」** SGP4/SDP4 是根据公开轨道根数推算卫星位置的传播模型；一些现有三维卫星追踪器就用 CelesTrak 的根数和这套模型来显示轨道并预测过境。CelesTrak 还提供 Pass Scheduler，可按观测点和 NORAD 两行轨道根数批量生成卫星过境时间表。

**「影响」** 对需要确认某地近期由哪颗卫星拍摄、并直接查看影像的规划者和地理空间用户，这把过境计算、轨道可视化和多源影像检索放在同一个浏览器界面中，无需另行搭建后端；开源代码也允许用户自行部署或扩展数据源。

**「社区讨论」** 评论者普遍称赞执行与视觉呈现，有人说这是自己见过的风格与实质最佳结合之一；一位地理空间从业者特别肯定能直接看到卫星拍下的具体影像，而不只是轨道总览。还有用户表示自己原本用 Copernicus 规划背包行程，认为该项目数据更多、访问更方便。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://celestrak.org/software/tskelso-sw.php">CelesTrak : Satellite Tracking Software by T.S. Kelso</a></li>
<li><a href="https://trackthesky.com/">Track The Sky — Real-Time 3D Satellite Tracker</a></li>

</ul>
</details>

**标签**: `#satellite-tracking`, `#geospatial`, `#SGP4`, `#open-source`, `#browser-visualization`

---

<a id="item-tech-news-3"></a>
### [E-means 声称以十分之一 epoch 超越 k-means](https://e-means.github.io/) ⭐️ 8.0/10

E-means 项目页面提出一种 k-means 替代算法，声称仅用 k-means 约十分之一的 epoch 就能取得更好的聚类结果，面向大规模聚类和索引工作负载；这一核心性能主张尚未得到独立验证。评论者报告的适配结果不一：有人称在 GPU 上改造 IVF 索引后获得 146 倍加速，也有人称全量重建索引快 2.5 倍，但整体插入时间变化不大。还有评论者用其替换 Lloyd 算法来做球面网格松弛，结果并不更好。

hackernews · porridgeraisin · 11月9日 18:45 · [社区讨论](https://news.ycombinator.com/item?id=50429734)

**「背景」** k-means 的常用实现是 Lloyd 算法：交替执行“把每个样本分配给最近质心”和“把质心更新为簇内均值”两步，直到收敛；在大规模数据上，反复扫描全量样本是主要开销来源。e-means 针对的正是这一迭代过程，项目标题宣称只用约十分之一轮次便能取得优于 k-means 的效果，但这属于项目自述的对比结果，尚未独立验证。评论者 shiandow 把此类更新规则类比为带摩擦项的期望最大化，并注意到该规则能让质心保持在凸包内。

**「影响」** 对准备替换 k-means 的团队，应先按自身负载验证端到端收益：现有报告显示 IVF 索引和全量重建可能明显加速，但增量插入改善有限，且并非所有几何优化任务都适用。

**「社区讨论」** 除上述实测外，shiandow 猜测该算法可理解为带摩擦项的期望最大化，并指出其更新规则使质心保持在凸包内；wood\_spirit 则希望它能进入 SciPy，以便在更多环境中使用。

**标签**: `#k-means`, `#clustering algorithms`, `#GPU acceleration`, `#performance optimization`, `#machine learning`

---

<a id="item-tech-news-4"></a>
### [OpenSSH 与 musl 交互漏洞遭在野利用，可无密码登录高权限账户](https://arstechnica.com/security/2026/11/vulnerability-that-lets-hackers-ssh-into-linux-devices-is-under-active-exploitation/) ⭐️ 8.0/10

多家研究机构报告，一个被命名为 \*sshole 的严重漏洞正被活跃利用：它源于 OpenSSH 与 musl 代码库的交互，同时使用这两个组件并满足其他条件的 Linux 系统，可在数秒内被未认证地获取高权限账户访问权。该漏洞于上周四公开，四天后的 11 月 9 日（周一），安全公司 Greynoise 称其位于东南亚的蜜罐遭到其追踪为 GT10 的组织攻击，并称对方实施了“成熟的入侵”；Greynoise 随后访问了 GT10 的一台服务器，从中发现其他潜在受害者和部分攻击工具。Greynoise 表示，该组织使用的后门带有中文注释，且似乎由 AI 生成。上述利用与归因均来自研究人员的说法，现有报道内容不完整，未提供受影响版本范围或修复方案等细节。

rss · Ars Technica · 11月9日 19:41

**「背景」** 该漏洞源于 OpenSSH 与 musl 这一 C 代码库的交互：只有在同时使用两者并满足其他条件的 Linux 系统上，未认证攻击者才能获得高权限账户访问。Ars 报道称，该问题上周四才公开，四天后 Greynoise 已报告其蜜罐遭遇实际入侵。

**「影响与处置」** 受影响范围集中在使用 musl 且未启用 PAM 的 Linux 系统，包括 Alpine 的默认安装：在 OpenSSH 与 musl 交互出错时，未设置密码的账户可被无密码登录。据 The Hacker News 报道，攻击者已在一台 Alpine 蜜罐上取得 root 权限；OpenSSH 10.6p2 修复了该缺陷，受影响用户应升级到该版本或发行版提供的修补包，并重启 sshd 使修复生效。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://radar.cloudflare.com/security/zero-wire/sshole">sshole : OpenSSH password bypass on musl Linux | Cloudflare Radar</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploited-openssh-sshole-flaw.html">Hackers Target OpenSSH SSHole Flaw Within Hours of Disclosure...</a></li>

</ul>
</details>

**标签**: `#Linux security`, `#OpenSSH`, `#musl`, `#vulnerability exploitation`, `#cybersecurity`

---

<a id="item-tech-news-5"></a>
### [Claude Code 设置文件在 GitHub 上泄露数千条密钥](https://arstechnica.com/ai/2026/11/claude-code-settings-files-expose-thousands-of-secrets-on-github/) ⭐️ 8.0/10

AI 安全研究机构 Apiiro 发现，数千条敏感信息——包括数据库密码、API 令牌和 root 登录凭据——出现在 GitHub 公开仓库的 Claude Code 设置文件中。问题出在 Claude Code 对自动化 shell 命令的授权方式：用户选择“是，且不再询问”后，这一批准会以规则形式写入本地的 \`.claude/settings.local.json\`，而命令本身常被原样保存，内嵌的密钥也随之写入该文件。Anthropic 在文档中称该文件会被加入开发者的全局 .gitignore，通常能避免被公开，但 Apiiro 的发现表明这层默认保护并非总能生效。上述数量与机制来自 Apiiro 的研究，Ars Technica 未做独立测量。

rss · Ars Technica · 11月9日 17:24

**「审批持久化机制」** Claude Code 默认在执行大多数 shell 命令前询问用户；当用户选择“是，且不再询问”时，这一许可会作为允许规则写入项目本地的 \`.claude/settings.local.json\` 文件。Anthropic 文档称，该文件会被加入开发者的全局 \`.gitignore\`，通常可防止它被公开提交；但一旦该文件被提交到公开仓库，写入其中的命令及内嵌凭据也会随之暴露。

**「影响」** 使用 Claude Code 的开发者应把 \`.claude/settings.local.json\` 视为可能含有机密的文件：检查个人仓库及其 git 历史中是否已提交该文件，若发现凭据外泄应直接轮换，而不是只删除文件，因为密钥已留在版本历史中。团队还应在 pre-commit 钩子或 CI 中显式检查该路径，而不是仅依赖全局 .gitignore 这一本地默认设置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/claude-codes-dont-ask-again-file.html">Claude Code &#x27;s “Don&#x27;t Ask Again” File Exposes Passwords and Keys...</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#security`, `#secrets management`, `#GitHub`, `#Claude Code`

---

<a id="item-tech-news-6"></a>
### [谷歌发布 TPU 8tx 与 8i Max 两款专用芯片](https://www.bloomberg.com/news/articles/2026-11-09/google-escalates-nvidia-rivalry-with-new-versions-of-its-tpu-systems) ⭐️ 8.0/10

谷歌宣布推出两款新的张量处理单元：面向政府机构及受严格监管行业、用于处理安全机密数据的 TPU 8tx，以及面向超长上下文 AI 应用、将两颗 TPU 集成在同一封装内以提升算力和内存容量的 TPU 8i Max。报道称，TPU 8tx 将与 AMD 芯片协同工作；谷歌正打破过去每两年推出一款新处理器的节奏，转为针对不同场景扩充专用芯片。苹果、Meta、甲骨文和 Anthropic 已被列为客户，但现有报道未提供两款芯片的上市时间、价格、功耗或独立性能数据，因此其相对英伟达 GPU 的实际竞争力仍无法从现有信息判断。

telegram · zaihuapd · 11月9日 13:36

**「背景」** 在 AI 加速器市场，英伟达 GPU 是主要选择，TPU（张量处理单元）则是谷歌自研的替代方案；此前谷歌大致每两年推出一款新处理器。此次谷歌在一年内连续扩充 TPU 产品线，显示其正按安全、超长上下文等不同场景拆分专用型号。

**「影响」** 对受监管行业用户而言，TPU 8tx 提供了一个按报道可与 AMD 芯片协同的谷歌自研加速器选项；对需要超长上下文的开发者，8i Max 以双芯片封装指向更强算力和更大内存容量。但由于上市时间、兼容性细节和性能/价格数据未披露，相关组织的采用决策仍缺少可比较的依据。

**「社区讨论」** Hacker News 讨论集中在缺少能效与成本数据：有评论者追问每 token 的功耗和美元成本，以及与英伟达同级产品的对比；另一人则提到 Colab 目前能用的最强 TPU 仍是 v6e-1，认为规模太小，不足以做严肃工作。还有评论者问谷歌为何不直接出售这些芯片。

**标签**: `#Google TPU`, `#AI chips`, `#Nvidia competition`, `#semiconductor hardware`, `#long-context AI`

---

<a id="item-tech-news-7"></a>
### [Anthropic 发布 Mythos 与 Fable 模型，称编码推理视觉有改进](https://techcrunch.com/2026/11/09/anthropic-releases-new-mythos-and-fable-models-amid-rsi-concerns/) ⭐️ 7.0/10

Anthropic 发布了名为 Mythos 和 Fable 的新模型。公司称这些模型在编码、推理和视觉等方面有所改进，并且能更清晰地与用户沟通。TechCrunch 的简短报道没有提供基准测试、技术细节、可用性或定价信息，也没有解释标题中提到的 RSI 担忧，因此这些改进的幅度尚无法独立判断。

rss · TechCrunch AI · 11月9日 19:24

**「背景」** Anthropic 此前最广为人知的是 Claude 系列专有大型语言模型，该系列长期被视为其旗舰产品。此次发布的新模型改用 Mythos 和 Fable 两个名称，但现有报道尚未说明它们与 Claude 系列的具体关系。

**「访问路径分化」** 对开发者而言，最直接的后果是两款模型的获取方式并不相同：据 Anthropic 的模型页面，Claude Mythos 5.2 只通过可信访问计划向经过审核的网络安全防御人员和生命科学研究者开放，起价为每百万输入 token 8 美元、每百万输出 token 40 美元；OpenRouter 则把 Claude Fable 5.2 列为面向高难度技术工作的通用模型，并称其在编码、推理和视觉上优于 Fable 5.1。因此，需要 Mythos 级能力的团队必须先申请该计划，否则只能改用 Fable 系列，并按其定价与配额做预算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/claude/mythos">Claude Mythos \ Anthropic</a></li>
<li><a href="https://openrouter.ai/anthropic/claude-fable-5.2">Claude Fable 5.2 - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI model release`, `#LLMs`, `#coding and reasoning`, `#vision`

---

<a id="item-tech-news-8"></a>
### [英伟达董事会据报调查黄仁勋，CEO 留任概率被估五五开](https://techcrunch.com/2026/11/08/is-jensen-huangs-job-on-the-line-yales-jeffrey-sonnenfeld-estimates-its-about-a-50-50/) ⭐️ 7.0/10

据 TechCrunch 报道，英伟达董事会正在调查 CEO 黄仁勋与一名疑似中国间谍的关系，此事直接涉及这家 AI 芯片公司最高管理层的去留。耶鲁大学的杰弗里·索南菲尔德（Jeffrey Sonnenfeld）估计，黄仁勋留任 CEO 的可能性约为“五五开”。该报道没有提供调查的具体依据、时间线或董事会结论；索南菲尔德的数字也只是分析人士的个人估计，并非已经确认的结果。

rss · TechCrunch AI · 11月9日 05:26

**「背景」** 黄仁勋是英伟达的创始人兼首席执行官。据 TechPowerUp 援引的董事会声明，在近期有报道指黄仁勋成为外国情报行动的目标后，英伟达董事会启动了独立调查；TechCrunch 的报道则把焦点放在他与一名疑似中国间谍的关系上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/08/is-jensen-huangs-job-on-the-line-yales-jeffrey-sonnenfeld-estimates-its-about-a-50-50/">Is Jensen Huang ’s job on the line? Yale’s Jeffrey Sonnenfeld ...</a></li>
<li><a href="https://www.techpowerup.com/354594/nvidia-launches-investigation-into-jensen-huangs-relationship-with-suspected-chinese-spy?cp=6">NVIDIA Launches Investigation Into Jensen Huang &#x27;s Relationship...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#AI hardware`, `#semiconductor industry`

---

<a id="item-tech-news-9"></a>
### [MIT 报道单一 AI 模型跨域模拟沙粒流动与蛋白质折叠](https://news.google.com/rss/articles/CBMiiAFBVV95cUxNcmx2REFMbEkxUzJ5MDhRQUNLckhuNjdDaUhZdkExQVpIRWNocXQyWWtMTFVnWHRadzc5T3BfTF8zZHVabEN0ZWFfRm5PSGdkUlktUXZjUFA4eWtXdUxPdmp1eFR5VU1kMGtPcE1qWE1pWFd6bkxCTUNsczNwZlEtZ3RDX2dUQlVR?oc=5) ⭐️ 7.0/10

MIT News 报道了一种单一 AI 模型，声称可以模拟从沙粒滑动到蛋白质折叠等多种物质的行为，目标是用同一套模型跨领域处理颗粒材料与生物分子模拟。该报道未给出模型名称、架构、训练数据规模、精度指标，也未说明代码或权重是否公开，同时未提及同行评审或独立复现结果。因此目前只能确认这项研究已被报道；其跨领域模拟能力，以及相对专用模型的准确性和成本优势，都仍未经外部验证。

rss · Google News - AI · 11月9日 05:00

**「背景：为何统一的多物质模拟模型受关注」** 传统上，模拟沙粒流动、流体变形或蛋白质折叠各自依赖不同领域的数值方法：颗粒材料常用离散元方法，分子体系常用分子动力学，不同物质类型和时空尺度往往需要分别建模、分别调参。因此，“能否用同一个模型跨物质类型完成模拟”一直是计算科学与机器学习交叉领域受关注的问题。MIT News 的这篇报道标题提出的正是这样一个统一模型，但现有摘要未给出模型架构、训练数据或验证结果等细节。

**标签**: `#AI for science`, `#materials simulation`, `#protein folding`, `#machine learning`, `#physics simulation`

---

<a id="item-tech-news-10"></a>
### [LingBot-Touch：潜空间预测优于重建的触觉预训练](https://www.reddit.com/r/MachineLearning/comments/1xs05uo/latent_prediction_beats_reconstruction_for/) ⭐️ 7.0/10

Robbyant 在 Reddit 发布研究帖，介绍自监督触觉编码器 LingBot-Touch：它采用 JEPA 式做法，预测被遮蔽接触的潜表示，而不是重建原始传感器信号。在与同尺寸 MAE、VAE 重建基线使用相同数据的对比中，触觉到视频检索的 top-5 召回率在 1K 小时数据上分别为 32.1%、5.6%、4.4%；到 4K 小时时 JEPA 升至 49.3%，MAE 仍低于 9%，VAE 反而降至 3.1%。作者解释，触觉片段大部分是接近零的背景，重建损失可以在不学到真实接触的情况下下降，因此重建目标不适合这类稀疏信号。两项设计细节为：掩码比例在 300 步内从 40% 热身升至 80%，因为一开始就用高掩码会遮住稀疏信号中所有接触点并引发梯度爆炸；磁、压阻、视触觉三类传感器通过规范化的指尖坐标和 5D RoPE（时间、手指、三维位置）接入同一个 Transformer。在 26 个真实机器人任务和 4 种策略组成的 104 个组合中，冻结编码器特征在其中 89 个组合得分最高；在一个预训练中未见过的磁性手上，LingBot-VLA 从 57.21 提升到 75.04。作者已公开推理代码与检查点，但上述数字均为作者自述，尚未见独立复现或同行评审。

reddit · r/MachineLearning · /u/Zealousideal-War7154 · 11月9日 18:52

**「背景」** JEPA（联合嵌入预测架构）不在像素或原始传感器信号上重建被遮挡部分，而是在潜空间中预测这些部分的表示；这与 MAE、VAE 等重建式掩码自监督方法不同。触觉信号往往稀疏，且大部分时段接近零背景，重建损失可能在尚未学到接触特征时就已下降，因此需要比较潜空间预测是否更适合触觉预训练。

**「对触觉预训练实践者的直接影响」** 对做触觉预训练和灵巧操作策略的团队而言，可直接检验的部分是：作者已公开推理代码与检查点，因此可以把冻结的编码器特征接入现有策略，不必重跑预训练。在其 26 个真机任务与 4 种策略组成的 104 个组合中，冻结特征在 89 个组合里得分最高；在预训练中未见过的磁传感器手上，LingBot-VLA 从 57.21 提升到 75.04。不过发布物是推理代码与检查点，不包含训练代码，若要复现 40%→80% 的掩码预热等预训练细节仍需自行实现；且上述数字均为作者自报，尚无独立复现。

**标签**: `#self-supervised learning`, `#tactile sensing`, `#dexterous manipulation`, `#JEPA`, `#representation learning`

---

<a id="item-tech-news-11"></a>
### [XGBoost 提前 2 小时预测县级新增停电，PR-AUC 约为基线 2.4 倍](https://www.reddit.com/r/MachineLearning/comments/1xs4hq8/forecasting_new_power_outages_per_county_hourly_2/) ⭐️ 7.0/10

一位 Reddit 用户发布了覆盖密苏里州和伊利诺伊州 216 个县的逐小时停电风险预报：用 XGBoost 估计“从当前起 2 小时后开始的 6 小时内，某县新增停电客户达到 5% 及以上”的概率，目标是只预测新增停电，不对已在进行的停电计分。模型使用 HRRR 风暴相关预报特征、县级属性、当前停电和邻县信息，2020–2024 年训练、2024 年验证，并在留出的 2025 年测试；测试输入是当时发布的 HRRR 预报（最近 5 次运行的均值），不是观测天气。作者报告 2025 年 PR-AUC 为 0.094，对比 NWS 预警加 SPC 第 1 天展望的费率表基线 0.039，约为 2.4 倍（95% 区间 2.0–3.3 倍）；在相同告警量下，新增停电捕获率 30% 对 17%，精确率 15% 对 11%。这些是作者自报、未经同行评审的结果，且地理范围限于上述两州；系统自 11 月 1 日起在线运行并保存每次预报，供后续盲测，早期迁移测试在艾奥瓦、印第安纳和密歇根合计取得 31% 对 19% 的捕获率。

reddit · r/MachineLearning · /u/CarRepresentative843 · 11月9日 21:34

**「背景：PR-AUC、HRRR 与“新增停电”口径」** 这项任务要预测的是县级范围内未来 6 小时（从 2 小时后开始）新出现的停电，即某县新增至少 5% 用户断电的概率；作者刻意排除已在进行的停电，因此比“预报当前停电”更难。评估采用 PR-AUC（精确率-召回率曲线下面积），它适合正例极稀少的情形——这里县级-小时的正例基准率仅约 0.5%，所以即便精确率不高，PR-AUC 与等报警量下的召回率对比仍能反映模型相对基线的增益。模型输入中的 HRRR 是 NOAA 的高分辨率快速更新数值天气预报，按小时滚动更新并给出阵风、切变、CAPE、结冰等要素；对照基线则是把 NWS 预警与 SPC 第一天展望拟合成一张比率表，在同一批样本上拟合。

**「影响」** 在相同告警量下，它能覆盖更多新增停电，但 15% 的精确率意味着大量误报；若用于县级应急或电力运营，应把它当作风险排序和补充信号，而不是单独触发动作。

**标签**: `#machine learning`, `#XGBoost`, `#power outages`, `#weather forecasting`, `#applied ML`

---

<a id="item-tech-news-12"></a>
### [欧盟草案拟限制成瘾性设计并标注虚拟币真实币值](https://www.mlex.com/mlex/articles/2546584/digital-businesses-face-addictive-design-controls-under-draft-eu-consumer-law) ⭐️ 7.0/10

一份泄露的草案显示，欧盟委员会计划通过《数字公平法案》限制数字服务的成瘾性设计和订阅陷阱，并要求游戏虚拟货币标明真实币值。草案要求企业允许用户关闭自动播放、连续使用奖励等诱导过度使用的功能；在线订阅须提供取消按钮、续费提醒和人工客服，免费试用转为付费订阅前须取得用户明确同意。面向未成年人的游戏付费抽奖、“付费获胜”和画像广告将被禁止，违规企业最高可被罚全球营业额的 6%。欧盟委员会定于 11 月 11 日提交该法案并同步改革消费者保护合作框架，但两项提案仍需欧洲议会和欧盟各国政府同意才能生效。

telegram · zaihuapd · 11月9日 16:42

**「背景」** 这份草案目前仍处于泄露阶段，欧盟委员会计划于 11 月 11 日正式提交，届时文本内容仍可能调整；它还与消费者保护合作框架的改革提案同步推进。两项提案都需经欧洲议会与欧盟各国政府同意才能生效，因此现阶段约束的是立法方向而非企业的即时义务。

**「影响」** 若草案按现文通过，游戏和订阅类数字企业需要调整虚拟货币的真实币值展示、未成年人付费抽奖限制、订阅取消与续费提醒流程；最高达全球营业额 6%的罚款会提高不合规成本。由于目前只是泄露草案，这些要求尚未生效。

**标签**: `#EU tech regulation`, `#consumer protection`, `#addictive design`, `#subscription traps`, `#virtual currencies`

---