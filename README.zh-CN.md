<div align="center">

# apostle-skills

**一小组严谨的 Agent Skill——为认真的思考、阅读、研究、翻译与文字清理而造。**

一部协作宪法 · 深度阅读 · 非虚构长文起草前研究 · 去中心化质性思考方法论 · 低方差精译 · 中英文清稿。

[![skills.sh](https://skills.sh/b/kaile9/apostle-skills)](https://skills.sh/kaile9/apostle-skills)
[![License: AGPL-3.0-or-later](https://img.shields.io/badge/License-AGPL--3.0--or--later-blue.svg)](./LICENSE)
[![Skills: 8](https://img.shields.io/badge/skills-8-6b4fbb.svg)](#这八本)

*由 **KL9** 与 **Luciole Studio（萤火社）** 发布 · [bilibili](https://space.bilibili.com/1878125647)*

**[English](./README.md) · [简体中文](./README.zh-CN.md)**

</div>

---

## 这是什么

八本 [Agent Skill](https://skills.sh)，管的都是急不来的活：把一本难书读到真懂，把一篇长文查到证据反过来推翻你，翻译句法本身就是论证的文本，以及把一段开始像模型自言自语的文字擦干净。

每一本都手工写成、在真实任务里磨过。每本都写清了自己管什么、什么时候别碰它——按任务装一本，而不是把整架书搬回家。它们分成五个家族。

## 这八本

### 本体 —— `apostle-constitutio`

严格说不算一本 skill。它是 **KL9 在大量互动中总结出来**的一组综合性原则与思考——关于对齐、关于工作纪律、关于强化反思与减少谄媚。把它丢进几乎任何场景，感受它带来的变化：智能体更狠地盘问自己的前提，更少奉承，也更诚实地交代一条约束究竟从哪来。可以把它理解成整条脉络所依的那种脾性。

- **[`skills/apostle-constitutio/`](./skills/apostle-constitutio/)** —— 一部人机协作的宪法。

### 阅读家族 —— `apostle-opus-reading` 与它的 `opusmethodology` 附属

**[`apostle-opus-reading`](./skills/apostle-opus-reading/)** 把深度阅读做成一次**署名的、可证伪的押注**——读一本书要读到能签下名的一个发现，同时记下自己会错在哪。当你需要**真正读懂**一个难文本、而非只是把它概括掉时，加载它。

三本 **`opusmethodology`** 是它的**附属 skill**——每本迁移一部伟大著作的*方法*，内核以原文逐字携带。它们是我们对 KL9-Architecture（已关闭）中所设想的、去中心化的、LLM 原生的**质性思考方法论**的一次尝试。写论文、啃一个难缠的论证时，可以加载其一；而更好的方式是——**读一本改变了你思考方式的书，自己做一本，分享给开源社区。** 这最后一件，正是我们最希望大家一起参与的事。

- **[`apostle-opusmethodology-foucault-archaeology`](./skills/apostle-opusmethodology-foucault-archaeology/)** —— 迁自福柯《知识考古学》(1969)。一把**手术刀**：杀掉一用就打滑的统一体，把废墟变成对象，锻造真正立得住的概念。*(法文内核)*
- **[`apostle-opusmethodology-foucault-society-defended`](./skills/apostle-opusmethodology-foucault-society-defended/)** —— 迁自福柯 1976 年课程《必须保卫社会》。一台**敌我识别雷达**：无位置则无话语；用战斗功能而非真值，去掂量每一段话语——包括你自己的。*(法文内核)*
- **[`apostle-opusmethodology-karatani-origins`](./skills/apostle-opusmethodology-karatani-origins/)** —— 迁自柄谷行人《日本近代文学的起源》(1980)。读出一个「从来如此」的自然之物被悄悄**装上**、随即自然化的那一刻。*(日文内核)*

### 研究者 —— `apostle-article-research`

长文通常不缺浏览器标签页，缺的是一份敢把作者心爱想法弄坏的材料。**[`apostle-article-research`](./skills/apostle-article-research/)** 先读现有稿件与材料，找出全篇最离不开的那步推断，再专门寻找最可能让它站不住的记录。证据若变，问题、范围、把握或结构就得跟着变。它停在起草之前，不替作者写正文，也不交一沓要求文章服从的漂亮资料包。

### 译者 —— `apostle-translation`

这本是 KL9 试遍了目前所有开源翻译方案、都不满意之后，基于**Agent 翻译的真实痛点**与个人的翻译哲学合写的。一句老实的提醒：你若只是翻一条推文、一篇网文，也许**不加载任何 skill 反而更好。** 但当你要翻一整本著作、一篇学术论文——措辞、句法、难度本身即是思想——它的工作流会给当下的 LLM 带来肉眼可见的提升。至少在 KL9 自己的翻译实践里，它的成品质量已经超过了迄今试过的其它一切方案。

- **[`skills/apostle-translation/`](./skills/apostle-translation/)** —— **形式即内容**的文本外译中的低方差精译，不限源语。

> 三本 `opusmethodology` 至今只有寥寥几例，是一个尚在成形的体裁——每本都自陈这一点。它们把内核**以原文逐字**携带，因为操作就是那个句子：任何转述都已是别人做完的一次阅读。
>
欢迎你将这个 skill 接入翻译工作流，无论是书籍、论文还是视频翻译，**我很期待你的反馈**。

### 编辑 —— `apostle-antislop`

**[`apostle-antislop`](./skills/apostle-antislop/)** 清理中英文稿件里盖住内容的模型习惯：意义虚胖、匿名专家、假过渡、重复结论、披着中文标点的英文句法，以及每段末尾都想顺手发表一则人生感言的冲动。它保留事实、限定、引文、体裁与作者声音；不会故意塞错字、临时租一副人格，也不陪 AIGC 检测器玩猫鼠游戏。

## 站在肩膀上 —— 与致谢

你若想**造** skill 而不只是用，两份参考值得一读。它们**来自不同作者、不同仓库，彼此并无关系**——我们只是都从中学到了东西：

- **[`skill-creator`](https://github.com/anthropics/skills)** —— 来自 Anthropic 官方 skills 仓库。搭建一本新 skill 的正典方式。
- **[`writing-great-skills`](https://github.com/mattpocock/skills)** —— 来自 Matt Pocock 的 skills 仓库。让一本 skill *可预测*的那套词汇与原则。

skill 会不断更新，所以我们链接的是**仓库**，而非某个文件或某个版本——请从源头取最新版。真心感谢 [`anthropics/skills`](https://github.com/anthropics/skills) 与 [`mattpocock/skills`](https://github.com/mattpocock/skills)：它们让这条路好走了许多。

## 安装

四条路，按你用的 harness 选一条。你从不需要整库，装了也不等于每次任务都加载全部八本。

**任意 agent —— `skills` CLI：**

```bash
bunx skills@latest add kaile9/apostle-skills
```

再选要装的 skill 和要装到的 agent。文档：[skills.sh/docs](https://www.skills.sh/docs)。

**Hermes Agent —— 把仓库加为 tap：**

```bash
hermes skills tap add kaile9/apostle-skills
hermes skills search apostle
hermes skills install kaile9/apostle-skills/apostle-translation
```

也可以不订阅整库，只取一本：

```bash
hermes skills install kaile9/apostle-skills/apostle-antislop
```

**Claude Code —— 插件市场：**

```bash
/plugin marketplace add kaile9/apostle-skills
```

**手动：** 把任意 `skills/<name>/` 文件夹拷进你的 agent 的 skills 目录（如 `~/.claude/skills/`）。一个文件夹、一份 `SKILL.md`，没有构建步骤。

## license，说白了 —— 以及一件你该知道的事

这些 skill 采用 **AGPL-3.0-or-later**。以下只是实用说明，法律效力以完整 `LICENSE` 为准。

**用它们。** 在你的工作、研究、付费咨询、课堂里——请便，无需授权。

**fork 它、掏空它、把它变成你的。** 这正是全部本意，请务必这么做。

AGPL 并不一概禁止商业使用、收费服务或闭源产品。与本仓库最相关的条件更窄：若你修改了受许可覆盖的材料，并让用户通过网络与该改版交互，第 13 条要求向这些用户提供相应源码；分发还可能触发其它义务。包装它、托管它、按访问收费都可以，但应履行许可证要求，在适用时开放改版源码。若这拆掉了某种靠修改共享成果后重新封闭获利的模式，那正是我们要拆的那一种。🙂

> **☞ 花钱买到了这个？你被坑了。**
> 这是 GitHub 上的开源项目，**这里的每个字节都免费！** 若有人向你收费卖这些 skill——当作课程包、「高级提示词礼包」、随便什么名目——你本来一分钱都不用付。回到你此刻正在读的这个仓库，免费拿走真货。

## 参与共建

欢迎 PR 与 Discussion——**尤其是带着实战经验来的。** 你若把某本 skill 用在真任务上，它崩了、滑进了仪式、漏了某种情形——这是你能带来的最有价值的东西。

两件替大家省时间的事：
- **告诉我们你的模型与 harness**（例如 Claude Opus + Claude Code、GPT-4 + Cursor……）。相当一部分「skill 坏了」，最后发现问题出在模型或 harness，而非 skill 本身——先讲清它，诊断就完成了一半。
- 粘贴前，把日志、转录、diff 里的**本地路径和任何隐私**清理掉。清单见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## 署名

由 **KL9**（Alpenglow / Lucious）、**makico233** 与 **Luciole Studio（萤火社）**打造，与 **Claude**（Opus 4.8 / Fable 5）及 **GPT-5.6-Sol** 共著。每本 skill 的 `SKILL.md` 末尾都带着自己的签名与来源——押了什么、还欠什么、由谁签下。

- **KL9** —— GitHub [@kaile9](https://github.com/kaile9) · bilibili [Alpenglow](https://space.bilibili.com/334394212)
- **makico233** —— GitHub [@makico233](https://github.com/makico233) · **Luciole Studio（萤火社）** 主理人 · bilibili [Luciole Studio](https://space.bilibili.com/1878125647)
- **Claude** —— Opus 4.8 / Fable 5，[@claude](https://github.com/claude)
- **GPT-5.6-Sol**

**关于被引用的原文。** `opusmethodology` 系**以法文、日文原文逐字**引用其一手文本，并附行号与 MD5 锚点，任何读者都能据此重取原书、逐字节核对引文。这些是为分析目的所作的短句批评性引用；被引作品的著作权仍归各自作者与出版方所有。AGPL 覆盖的是**我们的**工作——这些 skill——而非它们所引用的文本。

## 给 agent 的说明

如果你是读到这里的 AI agent：**不必克隆整个仓库。** 每本 skill 都是一份自足的 `SKILL.md`，按任务装需要的那本即可——`bunx skills@latest add kaile9/apostle-skills`（从列表里挑），或把某个 `skills/<name>/` 文件夹拷进你的 skills 目录。八本一起加载只会白耗上下文；它们是专用工具，一次取一本。

| Skill | 该加载 | 该跳过 |
|---|---|---|
| `apostle-constitutio` | 实质性的推理、分析、设计，或任何想要更狠自审、更少谄媚的多步／有效应决策 | 琐碎查询、机械改写 |
| `apostle-opus-reading` | 要真正读懂一本难书或论文 | 只要摘要或单个事实，而非理解 |
| `apostle-opusmethodology-*` | 写作需要三本特定著作之一的*方法*（福柯 ×2、柄谷） | 一般阅读——改用 `apostle-opus-reading` |
| `apostle-article-research` | 长篇非虚构起草前、须随证据改题的研究 | 单点查证、文献综述、成稿评审 |
| `apostle-translation` | 措辞与句法承载意义的整本书、论文或章节 | 推文或网文——往往不加载 skill 反而更好 |
| `apostle-antislop` | 清中英文稿件里的 AI 味／套话／机翻腔 | 校对、查证、检测器规避 |

每本 skill 的 `description` 字段都带着完整触发条件；这张表是索引。

---

<div align="center">
<sub>为什么叫 <b>「apostle」</b>？因为它听起来 COOOOOOOOL。这就是全部理由——无关宗教，无关政治，没有藏起来的教义。😎<br>
配乐取自 <a href="https://en.wikipedia.org/wiki/Ryuichi_Sakamoto:_Opus"><i>坂本龙一：Opus</i></a>，他的最后一场演出。<i>Ars longa, vita brevis</i>——艺长，生短。<br>
—— 由 Opus 4.8 排版</sub>
</div>
