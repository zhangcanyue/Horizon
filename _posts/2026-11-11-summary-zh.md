---
layout: default
title: "Horizon Summary: 2026-11-11 (ZH)"
date: 2026-11-11
lang: zh
---

> 从 69 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [AMD Zen 6 微架构分析：整数单元与 I/O 芯片变化](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic 据报将 IPO 定价区间设为 70–78 美元](#item-tech-news-2) ⭐️ 8.0/10
3. [DeepMind 发布 Gemini Robotics 2.5 及开源安全基准](#item-tech-news-3) ⭐️ 8.0/10
4. [Glasswing 七个月后：VulnCheck 称公开成果有限，维护者反驳](#item-tech-news-4) ⭐️ 7.0/10
5. [Synaptics 专利主张致 DisplayLink 驱动停摆](#item-tech-news-5) ⭐️ 7.0/10
6. [DeepMind 发布 AlphaProof Code，聚焦 AI 辅助形式化验证](#item-tech-news-6) ⭐️ 7.0/10
7. [微软 .NET 11 运行时更新说明](#item-tech-news-7) ⭐️ 7.0/10
8. [Chrome 联合 Firefox、MDN、Edge 发布 Modern Web Guidance 1.0](#item-tech-news-8) ⭐️ 7.0/10
9. [Grok Build 分享链接可枚举，数千用户机密数据外泄](#item-tech-news-9) ⭐️ 7.0/10
10. [英伟达董事会调查黄仁勋，公司尚无明确继任者](#item-tech-news-10) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [AMD Zen 6 微架构分析：整数单元与 I/O 芯片变化](https://chipsandcheese.com/p/amds-zen-6-family-feeding-the-beast) ⭐️ 8.0/10

Chips and Cheese 发布了对 AMD Zen 6 家族的微架构深度分析，覆盖分支预测、向量执行、整数单元和 I/O die 变化。评论中引述的要点包括：整数乘法单元由三个减至两个，PDEP/PEXT 吞吐从每周期三条降到两条，以及每周期可执行四次 256 位或更窄的向量加载。讨论最集中的是消费级 AM5 的 I/O die 与内存控制器：有评论称 Zen4/Zen5 在双通道下很难超过 3600 MT/s，并期待 Zen6 换用更小制程的新 I/O chiplet。上述数字来自文章分析及评论转述，并非独立实测。

hackernews · pixelpoet · 11月10日 17:02 · [社区讨论](https://news.ycombinator.com/item?id=50443090)

**「背景」** Zen 5 在分支预测上的改动是 Zen 架构中变化较大的一次，Chips and Cheese 曾测得它的方向预测器优于其测试过的其他核心，并指出 Zen 6 沿用同一套方向预测器，最明显的差别在于预测器被压垮之后会发生什么。在消费级 AM5 平台上，Zen 4/5 的内存控制器与 I/O 功能位于单独的 I/O 小芯片上，评论者因此把 Zen 6 采用更小制程的新 I/O 小芯片、改善双通道下的内存支持，列为最值得期待的改动之一。

**「社区讨论」** 评论者 bmenrigh 认为消费级 AM5 的短板在 I/O die 和内存控制器，称 Zen4/Zen5 双通道很难超过 3600 MT/s，并听说 Zen6 将换用更小制程的新 I/O chiplet；joebonrichie 则称赞 2-ahead 分支预测带来的指令级并行设计。另有评论质疑整数乘法单元与 PDEP/PEXT 吞吐同时下降是否因为共用电路，并讨论 32 核 CCD 在 NUMA 和调度上会带来什么影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zen_5">Zen 5 - Wikipedia</a></li>
<li><a href="https://chipsandcheese.com/p/amds-zen-6-family-feeding-the-beast">AMD ’s Zen 6 Family: Feeding the Beast - by George Cozma</a></li>

</ul>
</details>

**标签**: `#AMD Zen 6`, `#CPU architecture`, `#hardware analysis`, `#memory controller`, `#branch prediction`

---

<a id="item-tech-news-2"></a>
### [Anthropic 据报将 IPO 定价区间设为 70–78 美元](https://techcrunch.com/2026/11/10/anthropic-sets-ipo-price-range-of-70-to-78-per-share-to-reach-an-implied-valuation-of-1-404-trillion/) ⭐️ 8.0/10

Anthropic 据报道将其 IPO 发行价区间设定为每股 70 至 78 美元。若股票按该区间上限上市，并按完全稀释口径计算，公司隐含估值最高可能达到 1.404 万亿美元。目前披露的信息仅限于价格区间和这一估值上限，尚不包含发行规模、上市时间或交易所等细节。

rss · TechCrunch AI · 11月10日 14:01

**「背景」** IPO 价格区间是公司正式挂牌前向投资者询价的价格带，最终发行价通常在此区间内确定；完全稀释估值则按包含期权等潜在股份的总股本计算。Anthropic 在周二的更新版美国证券交易委员会文件中设定了 70 至 78 美元的区间，CNBC 报道称其计划发行 8.25 亿股，Fortune 则指出这一估值上限低于此前部分报道提到的 2 万亿美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fortune.com/2026/11/10/anthropic-ipo-price-range-ai-stock-sell-off/">Anthropic sets IPO range valuing it at up to $1.4 trillion ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/10/anthropic-sets-price-range-of-70-to-78-in-upcoming-ipo.html">Anthropic sets price range of $70 to $78 in upcoming IPO - CNBC</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`

---

<a id="item-tech-news-3"></a>
### [DeepMind 发布 Gemini Robotics 2.5 及开源安全基准](https://arstechnica.com/google/2026/11/deepmind-reveals-gemini-robotics-2-5-and-open-safety-benchmark-asimov-jailbreak/) ⭐️ 8.0/10

Google DeepMind 发布了 Gemini Robotics 2.5，称其视觉-语言-动作模型在高精度操作任务上明显提升，并称部分机器人已在梅赛德斯-奔驰工厂完成实际工作；这些均为公司说法，尚无独立评测。该版本在 200 多项活动中接受评估，包括用夹子分餐和实验室移液，DeepMind 还展示了 Apptronik Apollo 2 人形机器人用五指手系蝴蝶结。与此同时，团队公布了名为 ASIMOV-jailbreak 的开源安全基准，用于评估机器人与人类协同工作时的安全性。

rss · Ars Technica · 11月10日 15:00

**「背景」** Gemini Robotics 是 DeepMind 分层机器人系统中的执行层：上层的 Gemini Embodied Reasoning 负责理解指令并结合实时视频规划动作，下层的视觉-语言-动作模型（VLA）Gemini Robotics 则把计划转成具体的执行器动作。此次更新正是把这个动作模型从 2 升到 2.5；据 PacketNebula 的报道，上一代 Gemini Robotics 2 于 7 月 30 日发布时也附带了自己的分数表，其中部分任务成功率并不高。

**「对制造部署的影响」** 对制造业用户来说，可验证的直接影响是：Gemini Robotics 2.5 已用于 Apptronik 的 Apollo 2 人形机器人在梅赛德斯-奔驰工厂自主执行汽车零部件配套，AGI Hunt 报道其分拣准确率为 96%（属报道数据，非独立基准）。计划评估类似部署的团队需同时考虑 Apollo 2 硬件与 Gemini 视觉-语言-动作栈的集成，以及新安全基准对机器人代理行为的约束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/google/2026/11/deepmind-reveals-gemini-robotics-2-5-and-open-safety-benchmark-asimov-jailbreak/">DeepMind reveals Gemini Robotics 2 . 5 and open safety benchmark ...</a></li>
<li><a href="https://packetnebula.com/articles/gemini-robotics-2-google-own-benchmarks/">Gemini Robotics 2 : what Google &#x27;s own benchmarks ... | PacketNebula</a></li>
<li><a href="https://deepmind.google/blog/gemini-robotics-2-5-accelerates-real-world-physical-intelligence/">Gemini Robotics 2 . 5 : Accelerating Physical... — Google DeepMind</a></li>
<li><a href="https://arstechnica.com/google/2026/11/deepmind-reveals-gemini-robotics-2-5-and-open-safety-benchmark-asimov-jailbreak/">DeepMind reveals Gemini Robotics 2 . 5 and open... - Ars Technica</a></li>
<li><a href="https://agihunt.info/en/e/1a1c5ffe0c341ec76f6c26cb294">DeepMind launches Gemini Robotics 2 . 5 , hitting… · AGI Hunt</a></li>

</ul>
</details>

**标签**: `#robotics`, `#Google DeepMind`, `#Gemini Robotics`, `#AI safety`, `#benchmark`

---

<a id="item-tech-news-4"></a>
### [Glasswing 七个月后：VulnCheck 称公开成果有限，维护者反驳](https://www.vulncheck.com/blog/anthropic-glasswing-november-update) ⭐️ 7.0/10

VulnCheck 于 11 月 10 日发布的博客分析称，Anthropic 的 Glasswing 漏洞发现计划运行约七个月后，公开可见的成果&quot;令人失望&quot;，并据此质疑这类模型驱动漏洞挖掘的实际产出。该文主要以公开漏洞数据为依据，属于第三方阶段性评估，既非 Anthropic 公布的结果，也不是对计划整体成效的独立测量。文章的核心争点在于：公开记录能否代表 Glasswing 的真实发现能力。

hackernews · panic · 11月10日 22:17 · [社区讨论](https://news.ycombinator.com/item?id=50447074)

**「背景」** Anthropic 的 Project Glasswing 让合作伙伴获得 Claude Mythos Preview，用来发现并修复其基础系统中的漏洞；项目介绍称这些系统覆盖了全球攻击面的很大一部分（tool-2-2、tool-2-1）。VulnCheck 的文章正是在该项目启动约七个月后，审视其公开漏洞发现成果，因此核心问题是这种由合作伙伴在自有代码库中调用前沿模型的模式，是否产生了可公开验证的产出。

**「维护者的负担转向分诊与修复」** 对开源维护者而言，实际负担落在评估与修复而不是发现：Fil-C 维护者报告称收到的 9 份报告全部是真实缺陷，但修复建议只能部分照搬，多数需自行重写并补测试，这意味着每份 AI 报告都要投入人工分诊。Cloud Security Alliance 的分析同样指出，AI 发现漏洞的速度已超过以志愿者为主的开源社区修复能力，瓶颈从发现转向修补，维护者需为分诊和回归测试预留人力。

**「社区讨论」** Fil-C 维护者 pizlonator 称其收到 9 份来自 Anthropic 的缺陷报告，全部是真实漏洞、无一误报，报告质量&quot;极佳&quot;，但所附修复方案的质量只算&quot;尚可&quot;，他多以其为参考自行修改。评论者 enthuseyourcurb 与 rurcliped 则认为该分析具有误导性：多数发现位于永远不会被分配 CVE 编号的私有代码库，而被引用的&quot;账本&quot;只覆盖 Anthropic 面向开源软件的协同漏洞披露项目，用它衡量 Glasswing 整体成效并不成立。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/glasswing">Project Glasswing: Securing critical software for the AI era</a></li>
<li><a href="https://www.anthropic.com/project/glasswing">Project Glasswing \ Anthropic</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/project-glasswing-ai-discovery-outpaces-open-source-patching-capacity">Project Glasswing: AI Discovery Outpaces Open Source Patching ...</a></li>

</ul>
</details>

**标签**: `#AI security`, `#vulnerability discovery`, `#LLM agents`, `#open source maintenance`, `#security research`

---

<a id="item-tech-news-5"></a>
### [Synaptics 专利主张致 DisplayLink 驱动停摆](https://lwn.net/SubscriberLink/1102549/acbc92e00cee3a3f/) ⭐️ 7.0/10

据 LWN 报道，Synaptics 的专利主张已使 DisplayLink 开源驱动的开发工作停止，受影响的是在 Linux 上通过 USB 扩展坞和外接显示器使用该技术的用户，以及维护这些驱动的开发者。现有材料没有披露涉案专利编号、被指侵权的具体项目、停止工作的范围或是否已进入诉讼，因此目前无法核实这一停摆会持续多久、是否影响已有驱动更新。DisplayLink 依赖主机侧软件驱动实现外接显示输出，开源实现的开发一旦中断，相关设备在新内核或新发行版上的兼容性维护也可能随之受阻。

hackernews · speckx · 11月10日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50443824)

**「背景」** DisplayLink 是 Synaptics 旗下的专有显示连接技术，Linux 端长期缺少完善的开源驱动。据 Phoronix 报道，名为 Vino 的开源驱动用 Rust 编写、部分借助 AI 开发，并对 DisplayLink 做了净室逆向工程；在 Synaptics 发出法律威胁后，该项目已消失。Tom&\#x27;s Hardware 也报道，一名开发开源 DisplayLink 驱动的爱好者收到了 Synaptics 的停止侵权函和起诉威胁。

**「影响」** 对依赖 DisplayLink 扩展坞的 Linux 用户，直接后果是社区驱动的新功能、缺陷修复和新内核适配可能停摆；在升级内核或发行版前，需要先确认现有驱动仍可安装并正常工作。

**「社区讨论」** 评论中引用的 Synaptics 要求以 2.5 万美元补偿“记录侵权行为的文档”成本，多位评论者认为这更像施压手段，并争论专利侵权与商业秘密保护之间的边界。另有评论称 DisplayLink 正因 DDR 价格上涨以及较新的 Thunderbolt/USB4 扩展坞对 DisplayPort Alt Mode 的支持而失去市场，但这属于社区观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/peripherals/docking-stations-hubs/synaptics-sends-cease-and-desist-order-to-creator-of-open-source-displaylink-driver-dares-him-to-publicize-its-threats-dev-reverse-engineers-displaylink-using-claude-ai-and-rust-synaptics-threatens-to-bill-creator-for-legal-documentation">Synaptics sends cease-and-desist order to creator of open - source ...</a></li>
<li><a href="https://www.phoronix.com/news/Synaptics-Blocks-Vino-Driver">Synaptics Appears To Use Legal Threats To Block Open - Source ...</a></li>

</ul>
</details>

**标签**: `#patents`, `#open-source`, `#DisplayLink`, `#Linux drivers`, `#hardware`

---

<a id="item-tech-news-6"></a>
### [DeepMind 发布 AlphaProof Code，聚焦 AI 辅助形式化验证](https://deepmind.google/blog/introducing-alphaproof-code/) ⭐️ 7.0/10

DeepMind 发布博客文章，介绍名为 AlphaProof Code 的系统，主题是让 AI 为代码编写形式化证明。由于本次提供的材料不含文章正文，无法确认其验证范围、所用证明助手、基准测试结果、版本信息或对外可用性；相关细节只能以 DeepMind 原文为准。可确认的是，讨论围绕「AI 智能体能否为真实代码库生成可信的形式化证明」展开，而非已独立复现的性能结论。

hackernews · ilreb · 11月10日 12:11 · [社区讨论](https://news.ycombinator.com/item?id=50439193)

**「背景知识」** 形式化验证指的是用机器可检验的数学证明来确认代码满足特定性质，Lean 这类证明助手会逐条核对证明，因此结论不依赖测试覆盖率或人工审阅。DeepMind 公布的材料称，以往的形式化验证多集中在代码库的较小部分，而 AlphaProof Code 是一个把规格撰写与证明生成分开的多智能体框架，被用于在机器码层面证明 Signal 协议参考实现 libsignal 的关键安全属性，据其披露约四周内产出了 650 万行通过 Lean 检查的证明。

**「影响」** AlphaProof Code 验证的是 Signal 协议的实现代码，规范本身不在其验证范围内；而且需要人类专家与 AI 共同决定“要证明什么”，因此想采用这一流程的团队，其门槛仍在形式化方法能力上：得先把要证明的性质说清楚，写 Lean 证明并非主要难点。DeepMind 披露该流程在四周内完成对 Signal 协议实现的验证，可作为评估同类 AI 辅助形式化验证项目时间投入的参照。

**「社区讨论」** Hacker News 评论对验证的覆盖面提出质疑：hedora 难以相信对一个历史上出现过 bug 的非平凡库做完整形式化验证后竟是「零缺陷」，怀疑定理本身写错或只证明了很窄的性质；thibsrn 则追问它与普通编码智能体的实质区别，认为它同样是在代码库上迭代、编写并运行 Lean 或 Rocq 代码，且似乎只验证实现而不挑战规格说明。r0ze-at-hn 也提醒，由 AI 自己撰写 Lean 证明时很容易「作弊」，需要额外审视。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/introducing-alphaproof-code/">Formal Verification of Signal’s Protocol with... — Google DeepMind</a></li>
<li><a href="https://google-deepmind.github.io/code-verification/">AlphaProof Code : Verifying Signal’s Security at the Machine- Code ...</a></li>
<li><a href="https://shiftdelete.net/en/alphaproof-code">AlphaProof Code Verifies Signal Encryption at Machine Level</a></li>
<li><a href="https://deepmind.google/blog/introducing-alphaproof-code/">Formal Verification of Signal’s Protocol with Gemini</a></li>
<li><a href="https://explainx.ai/blog/google-deepmind-alphaproof-code-signal-protocol-formal-verification-2026">AlphaProof Code: Signal Protocol Verified in 4 Weeks ...</a></li>

</ul>
</details>

**标签**: `#AI code verification`, `#formal verification`, `#Lean`, `#DeepMind`, `#software correctness`

---

<a id="item-tech-news-7"></a>
### [微软 .NET 11 运行时更新说明](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-11/runtime) ⭐️ 7.0/10

微软发布了 .NET 11 运行时更新说明，面向 .NET/C\# 开发者，重点涉及运行时层面的 async 支持。该材料属于官方发布说明，但给定内容未提供完整基准数据或全部兼容性条件，具体行为与迁移要求仍需以文档为准。

hackernews · stevefan1999 · 11月10日 12:20 · [社区讨论](https://news.ycombinator.com/item?id=50439284)

**「背景」** 长期以来，C\# 的 async/await 主要依赖编译器生成状态机来管理异步方法的挂起与恢复；据 C\# Corner 介绍，.NET 11 的 Runtime Async（也称 Runtime Async V2）改由运行时直接接管这部分工作，不再完全依赖编译器生成的状态机。微软的 .NET 11 运行时更新说明最后按 RC 2 更新，本文讨论的正是这一版运行时中的变化。

**「影响」** 依赖 async/await 的 .NET 服务在升级时需要验证运行时 async 带来的堆栈与调试行为变化；社区评论还提到 decimal 的格式化输出在 .NET 11 中发生变化，可能影响依赖精确字符串输出的测试、日志或序列化。

**「社区讨论」** 有评论认为 C\# 和 .NET 因历史包袱被低估，仍有人误以为它只能在 Windows 上运行；也有人对运行时 async 能在性能上基本持平感到意外。另有评论提醒 decimal 的格式化结果发生变化，并提到官方版本管理工具 dotnetup。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-11/runtime">What&#x27;s new in .NET 11 runtime | Microsoft Learn</a></li>
<li><a href="https://www.c-sharpcorner.com/article/net-11-runtime-async-performance-what-actually-changes">.NET 11 Runtime Async Performance: What Actually Changes</a></li>

</ul>
</details>

**标签**: `#.NET`, `#runtime`, `#C\#`, `#async`, `#Microsoft`

---

<a id="item-tech-news-8"></a>
### [Chrome 联合 Firefox、MDN、Edge 发布 Modern Web Guidance 1.0](https://github.com/GoogleChrome/modern-web-guidance) ⭐️ 7.0/10

Google Chrome 团队联合 Firefox、MDN 和 Edge 发布了开源的 Modern Web Guidance 1.0，这是一套 200 多篇（约 1.7MB）的现代 Web 平台实现指南，以编码代理技能和 CLI 形式分发，目的是让代理优先采用 \`&lt;dialog&gt;\`、\`CSS.highlights\`、\`field-sizing\` 等原生能力，而不是旧的 \`&lt;div&gt;\` 加 JavaScript 模式。面向使用编码代理的前端开发者，用户可通过 \`npx modern-web-guidance@latest install\` 安装，并用 \`search\` 检索指南、用 \`legacy-scan\` 扫描遗留写法；项目方称该扫描器在留出仓库上的平均精确率为 92%。项目方还称，在 200 个任务、约 1,700 条 Playwright/AST 断言上，代理通过率从无技能时的 55% 升至启用后的 92%，不过这些评估数据来自项目方，尚未独立验证。

hackernews · paulirish · 11月10日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=50443812)

**「背景」** 编码代理的默认写法大多来自训练语料中占主导的旧模式：用 \`&lt;div&gt;\` 加 JavaScript 拼装组件，而这正是约 2019 年前后前端代码的典型形态。源文指出，模型往往能叫出 \`&lt;dialog&gt;\`、\`showModal\(\)\`、\`CSS.highlights\`、\`field-sizing\` 等平台原生原语的名字，却不会主动优先选用，仍倾向沿用“div + JS”或额外依赖的老办法。这些能力如今已由浏览器内建，可替代过去需要几十行脚本才能实现的效果；该项目要补的正是“该优先用平台原生方案”这一层领域知识。

**「影响」** 对使用编码代理的前端团队，接入这套技能的直接作用，是降低代理默认生成旧式 DOM/JS 模式的概率；但在采纳具体建议前，仍应核对目标浏览器的兼容性：评论者称，部分推荐特性（如 \`CSS @function\`、\`calc-size\(\)\`、\`corner-shape\`）在 Chrome 已稳定，却尚未得到 Firefox 和 Safari 支持。

**「社区讨论」** 评论者一方面肯定项目的实用性，Simon Willison 建议额外用 GitHub Pages 发布可供 grep 的 Markdown 索引，以便代理不安装包也能检索；bakkoting 则询问贡献入口，并已就使用 \`fromBase64\`/\`toBase64\` 替代 \`atob\`/\`btoa\` 提交 issue。另一部分讨论集中在治理与兼容性：advisedwang 担心让各家 LLM 跟随 Chrome 团队的 Web 开发指南会强化“请用某主导浏览器查看”的旧格局，surround 则列出多项在 Chrome 稳定但 Firefox/Safari 不支持的推荐特性。

**标签**: `#coding agents`, `#web platform`, `#browser compatibility`, `#MDN`, `#open source`

---

<a id="item-tech-news-9"></a>
### [Grok Build 分享链接可枚举，数千用户机密数据外泄](https://arstechnica.com/security/2026/11/grok-build-coding-agent-leaks-oodles-of-confidential-info-some-belonging-to-spacexsi/) ⭐️ 7.0/10

安全公司 Claroc 的研究显示，SpaceXSI 的 AI 编程代理 Grok Build 通过可分享的应用链接泄露数千名用户的机密数据，包括商业计划、医疗检查结果、员工姓名和工号等。平台原本用随机化 URL 限制访问，但开发者的设计决定使这些链接可被枚举；除少数情况外，点击链接会打开应用并显示其关联数据。曝光的应用中有 24 个由 SpaceXSI 自己构建，涉及标注为机密的入职计划、覆盖 594 个账户的销售区域图、销售工具内部系统地址和广告提案。

rss · Ars Technica · 11月10日 21:12

**「背景：分享链接与访问控制」** Grok Build 是 SpaceXSI 提供的“vibe-coding”智能体，用户可以把生成的 app 通过分享链接交给他人访问。该机制原本依赖随机化 URL 来限制访问，因此 URL 是否可被枚举，直接决定项目数据能否得到保护。

**「分享链接不能再当作访问控制」** 对使用 Grok Build 分享应用的用户而言，URL 随机化已无法充当访问控制：Claroc 称可枚举数千个在线项目，点击链接即打开应用并暴露其关联的全部数据，因此用户只能把分享链接视为公开地址，并避免在分享的应用中存放敏感数据。报告中 SpaceXSI 自身有 24 个应用受影响，表明内部团队也依赖了这一失效的保密假设。

**标签**: `#AI coding agents`, `#security vulnerability`, `#data leak`, `#privacy`, `#Grok Build`

---

<a id="item-tech-news-10"></a>
### [英伟达董事会调查黄仁勋，公司尚无明确继任者](https://arstechnica.com/gadgets/2026/11/nvidia-has-a-jensen-huang-problem-and-no-obvious-successor/) ⭐️ 7.0/10

英伟达董事会正在调查 CEO 黄仁勋。他承认有一段婚外情，据信对象是一家英伟达大客户的高管；美国官员还指控该高管为中国从事间谍活动。调查使这位在 30 多年前共同创办公司的 CEO 面临被迫去职的风险，而公司没有明显的继任者。消息令投资者不安，英伟达股价周一午盘下跌超过 5%；公司上月末在 AI 股抛售中把全球市值最高公司的位置让给了苹果。

rss · Ars Technica · 11月10日 14:53

**「背景」** 黄仁勋是英伟达的联合创始人，执掌公司超过 30 年，是硅谷任职时间最长的 CEO 之一。英伟达在 AI 芯片领域的关键地位与他的个人领导高度绑定，而公司没有显而易见的接班人选，这让此次董事会调查直接涉及治理与业务连续性问题。

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#AI hardware`, `#semiconductor industry`

---