---
layout: default
title: "Horizon Summary: 2026-11-08 (EN)"
date: 2026-11-08
lang: en
---

> From 51 items, 5 important content pieces were selected

---

**Technology News**
1. [GitHub’s Rubicon Git storage targets AI-agent concurrency](#item-tech-news-1) ⭐️ 8.0/10
2. [MaxxBench tests whether a strong DeepSWE score generalizes](#item-tech-news-2) ⭐️ 7.0/10
3. [Microsoft Research&\#x27;s AI Frontiers group reported to be ending](#item-tech-news-3) ⭐️ 7.0/10
4. [METR Report Finds Anthropic AI R&amp;D Accelerating Model Improvement](#item-tech-news-4) ⭐️ 7.0/10
5. [Apple researchers report HALO humanoid control system using two Qwen models](#item-tech-news-5) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [GitHub’s Rubicon Git storage targets AI-agent concurrency](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 8.0/10

GitHub introduced Rubicon, a new Git storage architecture for high-concurrency AI-agent workloads on a single repository; it stores Git objects in Azure Blob Storage and manages reference state through Ref-CAS, with virtual replicas handling reads and writes and background nodes compacting packfiles. In internal tests, GitHub reported 5,000 agents collaborating, 7,200 pushes per second, and low read latency, though these are vendor-reported test results rather than independently measured production figures. The architecture is currently in limited private preview, and GitHub says it will expand availability gradually.

telegram · zaihuapd · Nov 7, 14:12

**「Background」** Git separates immutable content—commits, trees, and blobs—from mutable references such as branches and tags. A push must write new objects and advance the relevant ref, so high concurrency stresses both object storage throughput and coordination of competing reference updates.

**「Limited preview」** For teams running many AI agents against a single repository, the 7,200-pushes-per-second figure is not yet an available service level: Rubicon is in a limited private preview, so most existing repositories cannot use it yet. The throughput result comes from GitHub&\#x27;s internal test, not an independent benchmark.

<details><summary>References</summary>
<ul>
<li><a href="https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/">Inside GitHub &#x27;s new Git storage architecture - The GitHub Blog</a></li>
<li><a href="https://trashexpert.ru/news/software-news/github-rubicon-git-storage-stress-test">GitHub : до 7200 пушей в секунду в тесте архитектуры Rubicon</a></li>

</ul>
</details>

**Tags**: `#GitHub`, `#Git 存储架构`, `#Azure Blob Storage`, `#AI 智能体`, `#基础设施`

---

<a id="item-tech-news-2"></a>
### [MaxxBench tests whether a strong DeepSWE score generalizes](https://maxxbench.unlap.ai/research/why-maxxbench/) ⭐️ 7.0/10

MaxxBench published an analysis testing whether a strong DeepSWE score holds up when the benchmark&\#x27;s task specification is varied, rather than treating the single result as a stable measure of model capability. It is a critique of LLM benchmark validity for people who use DeepSWE scores to compare models, not a new model release or a corrected leaderboard. The supplied summary reports no numeric before-and-after scores, so the size of any shift is not established here.

hackernews · antiuniverse · Nov 7, 17:19 · [Discussion](https://news.ycombinator.com/item?id=50406222)

**「Background」** DeepSWE is a widely used benchmark that scores AI coding agents by their pass rate on a fixed set of repository tasks graded by hidden tests. Like most leaderboards, it reduces performance to a single number, which is meaningful only if a model&\#x27;s score would survive small changes to how the same tasks are worded or constrained. MaxxBench tests that assumption by taking 89 DeepSWE tasks and altering each specification — for example, requiring lowercase filenames — then re-scoring the same models.

**「Impact」** For teams using DeepSWE results in model selection, the analysis makes a single score conditional on how the task is specified: they should check whether the ranking survives changes to that specification before treating it as decisive.

**「Community discussion」** Commenters largely welcomed the critique, with one describing parameter variation as a simple first-order test of whether a benchmark score generalizes and another saying reported DeepSWE bugs deepened their skepticism. A separate exchange argued that smaller models collapse most on the varied test and debated whether the cause is overfitting or labs building RL environments that poorly reflect benchmark tasks; those are commenter interpretations, not findings established by the source.

<details><summary>References</summary>
<ul>
<li><a href="https://www.systemdesign.academy/explained/maxxbench-deepswe">MaxxBench vs DeepSWE: what the coding benchmark found</a></li>

</ul>
</details>

**Tags**: `#LLM benchmarks`, `#evaluation methodology`, `#benchmark validity`, `#DeepSWE`, `#model robustness`

---

<a id="item-tech-news-3"></a>
### [Microsoft Research&\#x27;s AI Frontiers group reported to be ending](https://hunch.net/?p=13764006) ⭐️ 7.0/10

The item reports that Microsoft Research&\#x27;s AI Frontiers group, an MSR unit focused on fundamental advances in AI, is ending. The report and discussion frame the closure as part of a shift by large labs toward transformer scaling and incremental model development rather than exploratory research. The supplied excerpt is incomplete, so Microsoft&\#x27;s official rationale, staffing changes, and timing are not established.

hackernews · srean · Nov 7, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50406563)

**「Background」** AI Frontiers was a Microsoft Research group focused on fundamental advances in AI. John Langford, a partner researcher manager at Microsoft Research New York, announced that the group was over as he left Microsoft; the group had also built a monorepo shared by default across Microsoft Research to support coherent, shared research efforts.

**「Impact」** For researchers in the group, the reported closure removes an institutional home for fundamental AI work; the supplied material does not say whether staff will be reassigned or whether individual projects will continue elsewhere.

**「Community Discussion」** Commenters disagree about what the closure signals: some describe a broader industry retreat from exploratory AI research in favor of transformer scaling, while another argues the post points more specifically to management and technology-transfer problems at MSR. One commenter says the implicit MSR bargain of doing good work and being rewarded has been broken under current leadership, calling it culture-destroying.

<details><summary>References</summary>
<ul>
<li><a href="https://businessexaminer.ca/victoria-articles/item/microsoft-researcher-john-langford-exits-as-ai-frontiers-group-is-declared/">Microsoft Researcher John Langford Exits as AI Frontiers Group Is...</a></li>
<li><a href="https://hunch.net/?p=13764006">The End of AI Frontiers – Machine Learning (Theory)</a></li>

</ul>
</details>

**Tags**: `#AI research`, `#Microsoft Research`, `#organizational change`, `#transformer models`, `#research funding`

---

<a id="item-tech-news-4"></a>
### [METR Report Finds Anthropic AI R&amp;D Accelerating Model Improvement](https://www.theverge.com/ai-artificial-intelligence/1029126/anthropic-metr-report-accelerating-ai-development) ⭐️ 7.0/10

A METR report based on an 11-week investigation inside Anthropic finds that the company&\#x27;s AI-assisted research and development is improving its models roughly twice as fast as a year ago, with little indication of slowing. The Verge reports that the findings are alarming researchers and offer some of the clearest evidence yet of AI being used to automate AI development. METR&\#x27;s assessment is separate from a program giving safety researchers employee-like access to Anthropic systems after high-profile hacking incidents over the summer; the available excerpt does not include the report&\#x27;s methodology, numerical estimates, or caveats.

rss · The Verge · Nov 7, 12:30

**「Background」** AI R&amp;D acceleration refers to AI systems speeding up the research and engineering work used to build more capable models, creating a feedback loop in which better models can further accelerate their own development. METR notes that Anthropic&\#x27;s Responsible Scaling Policy lists AI R&amp;D acceleration as a key risk indicator.

**「What It Means for Auditors」** For outside safety researchers and auditors, the practical consequence is that Anthropic&\#x27;s internal AI use is now on the record as a measured development input rather than an informal productivity claim, giving evaluators a baseline to track in future assessments. The roughly twofold acceleration, however, comes from an 11-week internal assessment of Anthropic&\#x27;s own R&amp;D rather than an independently replicated measurement, so treating it as a sustained trend depends on repeat measurement. The METR probe is also separate from the program granting safety researchers &quot;employee-like&quot; access to Anthropic systems, so the report&\#x27;s figures do not by themselves give external reviewers ongoing visibility into the company&\#x27;s development pipeline.

<details><summary>References</summary>
<ul>
<li><a href="https://metr.org/blog/2026-11-05-anthropic-ai-rd-acceleration-assessment/">Independent Assessment of AI R &amp; D Acceleration at... - METR</a></li>
<li><a href="https://www.remio.ai/post/anthropic-ai-development-metrics-expose-the-race-between-automation-and-oversigh">Anthropic AI Development Metrics Expose the Race Between...</a></li>
<li><a href="https://coderfacts.com/advanced-topics/when-ai-builds-itself-inside-anthropic-s-evidence-on-recursive-self-improvement/">When AI Builds Itself: Inside Anthropic ’s Evidence on Recursive ...</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#AI R&amp;D automation`, `#Anthropic`, `#METR`, `#recursive self-improvement`

---

<a id="item-tech-news-5"></a>
### [Apple researchers report HALO humanoid control system using two Qwen models](https://weibo.com/1642634100/RqjjGllvw) ⭐️ 7.0/10

Apple researchers reportedly described HALO, a three-layer humanoid control system, in a Nov. 4 arXiv preprint and validated it on a Unitree G1 by transferring learned motions from simulation to an unfamiliar real room. The top layer uses Qwen3.6-35B-A3B to orchestrate tasks, the middle layer uses Qwen3.5-2B to generate actions, and the bottom layer is an RL-trained action tracker. The team reportedly released data-generation, model-training, and deployment code; the supplied item is a brief secondary report without a paper link, so the claims have not been independently verified.

telegram · zaihuapd · Nov 7, 13:35

**「Background」** An earlier model in the same Qwen line, Qwen3.5-35B-A3B, was released on Feb. 24, 2026 as a mixture-of-experts system with 35B total parameters but only about 3B active per pass \[tool-1-3\]; the Qwen3.6-35B-A3B name in HALO uses the same A3B naming convention. HALO&\#x27;s sim-to-real test refers to taking a control policy learned in simulation and running it on a physical Unitree G1 in an unfamiliar real room, where sensing and dynamics differ from the simulated environment.

**「Impact」** The released code gives other robotics researchers a concrete way to reproduce the data-generation, training, and deployment pipeline and test the Qwen-based control stack on their own robots; the report only establishes validation on the Unitree G1, so performance and compatibility on other hardware remain unverified.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ai-stat.ru/news/2026-03-12-qwen35-35b-uncensored">Qwen 3 . 5 - 35 B - A 3 B без ограничений: 675 апвоутов... | AI-Stat</a></li>

</ul>
</details>

**Tags**: `#humanoid robotics`, `#robot learning`, `#sim-to-real transfer`, `#Qwen models`, `#open-source code`

---