<div align="center">

# apostle-skills

[![skills.sh](https://skills.sh/b/kaile9/apostle-skills)](https://skills.sh/kaile9/apostle-skills)
[![License: AGPL-3.0-or-later](https://img.shields.io/badge/License-AGPL--3.0--or--later-blue.svg)](./LICENSE)
[![Skills: 9](https://img.shields.io/badge/skills-9-6b4fbb.svg)](./skills/)

*KL9 & Luciole Studio（萤火社） · [bilibili](https://space.bilibili.com/1878125647)*

</div>

---

## Why this exists

These are the skills I'm willing to route to in a System Prompt at work — the ones I'd tell an Agent to load. The making of them follows one shape: a human and an Agent align on an approach, the Agent writes, the human signs off on the result.

这些是我愿意在工作中写一个路由加到 System Prompt 里、提醒 Agent 加载的优质 Skill。创作方式是人和 Agent 对齐方案，然后 Agent 写作，最终人验收。

By mid-2026, frontier models like Fable-5 and GPT-5.6-Sol have shipped, and the market is full of cheap, Opus-class alternatives besides. So you don't need me to sell you on any of this — tell your own Agent: *"Clone this repo locally, tell me what problem each skill solves and how, and whether it's useful for our work."* Then read the `description` fields yourself. Some skills lean toward knowledge work (the ones with "Opus" in the name); some are workflows for a specific job (`apostle-translation`); a few are general enough that I load them in nearly every task (`apostle-constitutio`, `apostle-artifacts-loops`). I'm hoping more interesting ones get added.

考虑到 2026 年中已经发布了 Fable-5 和 GPT-5.6-Sol 这样的前沿模型，同时市面上还有无数可选的廉价 Opus 级模型，你只需要和你的 Agent 说「把仓库复制到本地，告诉我这些 Skill 用什么方法解决什么问题，以及是否对我们的工作有用？」然后自己把 description 看一遍就好了。它们有些偏向知识性工作（例如标题带 Opus 的 skill），有些是针对专门工作的工作流（例如 `apostle-translation`），还有些相对通用，我几乎在所有任务中加载（例如 `apostle-constitutio` 和 `apostle-artifacts-loops`）。同时我也期待更多有趣的 skill 被加进来。

## Prompt, Context, and where a skill sits

Everything submitted to an LLM should be split into two kinds: Prompt and Context. The ideal Prompt is concise, flexible, and carries some room for exploration and heuristics; Context is detailed, precise, and rich. Most of the time, a skill should be understood as part of the Prompt — and as frontier models turn over, the Prompt needs to turn over with them, and so does the skill. Even as I write this, I wouldn't prompt Doubao (Seed-2.1) the same way I'd prompt Fable-5; the results are worlds apart.

在这里我想做一个区分：提交给 LLM 处理的所有内容应该分为 Prompt 和 Context。理想情况下，前者应该简洁、灵活，并附带一定的探索性和启发性；后者则详实、精确、丰富。Skill 大部分时候我们应该理解成 Prompt 的一部分，随着前沿模型的更新，Prompt 需要同步更新，skill 也是——至少写下这段话的时候，我不会想着用同样的方式 prompt 豆包（Seed-2.1）和 Fable-5，因为效果天差地别。

The exceptions are the workflow skills built to solve a specific, long-standing LLM problem — `apostle-translation` and `apostle-artifacts-loops` both address continuity across a long piece of work, and both ask the Agent to keep notes the way a person keeps a memo. Outside of that narrow case, we should leave frontier models as much room for their own judgment as we reasonably can, because they are about to — and inevitably will — outperform a team of human experts.

除了特定的工作流 skill 用于解决某些长时间看来难以解决的 LLM 问题（例如 `apostle-translation` 和 `apostle-artifacts-loops` 这两个 skill 都处理了工作中的连续性问题，并要求 Agent 像写备忘录一样记录笔记），我们需要尽可能多地给前沿模型留下自觉判断的空间，因为它们即将、也必将比人类专家团队表现得还要好。

That said, don't dismiss the open, heuristic skills that a programmer might not think are worth writing down at all. `apostle-constitutio` is exactly that: for the past few years I've been chanting, almost like a prayer — and I still do — "think deeply, reflect on yourself, re-examine, keep an open mind…" This skill is my attempt to turn that chant into a way of thinking that actually works. I spent months shaping it into its current form; I believe reflection alone has visibly lifted the quality of its thinking in writing, from Sonnet-5 all the way to Fable-5. If you read the body of it, you probably won't like every sentence — and the smaller the model (the less knack it has for this kind of reasoning), the more likely the side effects. It's still underrated, which is why I made it the core of the apostle skills.

当然，我们不应该忽视一些也许在程序员眼里算不上、或者没必要写成 skill 的启发性、开放性的 skill 的作用。例如 `apostle-constitutio`，就是我从过去几年像祈祷一样念咒（现在还念）：「深度思考，反思自己，重新检查，开放思维……」转向真正有效的思考方式。我试了几个月，让它变成现在的样子。至少我个人认为，它依靠反思，从 Sonnet-5 到 Fable-5 在写作领域的思考质量有了喜人提升，不过如果你去看它的正文，也许你不会喜欢里面的所有句子，而且越小（没有悟性）的模型，越有可能有副作用。但它仍被低估了，所以我将其作为 apostle skill 的核心。

## Install

```bash
# Any agent
bunx skills@latest add kaile9/apostle-skills

# Hermes Agent — one skill
hermes skills install kaile9/apostle-skills/apostle-translation

# Claude Code — marketplace
/plugin marketplace add kaile9/apostle-skills
```

Or copy any `skills/<name>/` folder into your agent's skills directory. Installing the repository does not mean loading all nine skills on every task.

也可以把任意 `skills/<name>/` 文件夹拷进智能体的 skills 目录。安装整库不等于每次任务都加载九本。

## Use, fork, contribute

The skills are licensed under [AGPL-3.0-or-later](./LICENSE). Use them in research, work, classrooms, or paid services. Fork them, cut them apart, and make them fit your hand. If you modify covered material and provide access to the modified version over a network, the AGPL may require you to offer users the corresponding source; the license itself controls.

这些 skill 采用 [AGPL-3.0-or-later](./LICENSE)。研究、工作、课堂、收费服务都可以用；也欢迎 fork、拆开、改到顺手。若你修改受许可覆盖的材料，并让用户通过网络使用改版，AGPL 可能要求你向这些用户提供相应源码；具体以许可证正文为准。

> Paid someone for this? Every byte in this repo has always been free. Reselling a verbatim copy for money isn't an AGPL violation — §4 allows it outright — but selling something free to someone who doesn't know it's free is deception, license or no license. The actual violations look like this: stripping the copyright and license notices on resale (§4–5); forking closed-source and charging for “exclusive” access while adding restrictions or fees the license forbids (§10); running it as a hosted bot or API while sitting on the modified source instead of giving it to the people using it over the network (§13). And a fourth thing that breaks no law at all: bundling these skills into a “free resource pack” to funnel people toward a paid course. Perfectly legal, still shabby — free, honest work turned into bait for someone else's sale. Get a refund, or don't pay to begin with; the repo is right here.  
> 花钱买到了这个？这个仓库的每个字节，一直都是免费的。把原版转卖收钱不违反 AGPL——第 4 条明说允许——但把免费的东西卖给不知道它免费的人，不违法也是骗。真正违规的是这几种：转售时把版权与许可声明撕掉（第 4–5 条）；fork 后闭源，靠卖「独家」访问权赚钱，还加上许可证不许的限制或费用（第 10 条）；拿它包一个托管机器人或 API，却把改版源码扣下、不给通过网络在用它的人（第 13 条）。还有第四种，完全不违法：把这些 skill 塞进一份「免费资料合集」，给付费教程引流。合法，依然不厚道——白送的诚实劳动，被人拿去给别人的产品当诱饵。去退款，或者一开始就别付钱，仓库就在这儿。

Real failures make useful contributions. Tell us which model and harness you used, what the skill did, and where it broke. Remove private data and local paths before posting logs. See [CONTRIBUTING.md](./CONTRIBUTING.md).

真实的失败最适合拿来贡献。请说明模型、harness、skill 做了什么、在哪里坏掉；粘贴日志前删掉隐私与本地路径。详见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## Credits

Built by **KL9** (Alpenglow / Lucious) and **makico233** at **Luciole Studio（萤火社）**, drafted across three Claude generations — **Sonnet 5**, **Opus 4.8**, **Fable 5** — plus **GPT-5.6-Sol**.

- **KL9** — GitHub [@kaile9](https://github.com/kaile9) · bilibili [Alpenglow](https://space.bilibili.com/334394212)
- **makico233** — GitHub [@makico233](https://github.com/makico233) · bilibili [Luciole Studio](https://space.bilibili.com/1878125647)

Thanks to two repos we learned from — Anthropic's official skills repo (home of `skill-creator`) and Matt Pocock's skills repo (home of `writing-great-skills`), unrelated to each other and to this project. The links below point at the repos, not at one file inside them: skills move around, so grab the current version from source.

- [`anthropics/skills`](https://github.com/anthropics/skills)
- [`mattpocock/skills`](https://github.com/mattpocock/skills)

感谢两个我们从中学到东西的仓库——Anthropic 官方 skills 仓库（`skill-creator` 所在处）与 Matt Pocock 的 skills 仓库（`writing-great-skills` 所在处），彼此无关，也跟本项目无关。下面链接的是仓库本体而非其中某个文件：skill 会变动，请自取最新版。

The `opusmethodology` skills contain brief critical quotations in their original French or Japanese, with line and MD5 locators for verification. Copyright in those texts remains with their authors and publishers; the AGPL covers our work, not theirs.

---

## For agents

```yaml
repository: kaile9/apostle-skills
format: one self-contained SKILL.md per skill
loading_rule: load only the skill the task needs
```

| Task | Load | Skip when |
|---|---|---|
| Substantive reasoning or effect-producing work | `apostle-constitutio` | Trivial lookup or mechanical edit |
| Long work across stages, contexts, or agents | `apostle-artifacts-loops` | Work can be completed and verified directly |
| Understand one demanding book or paper | `apostle-opus-reading` | A summary or single fact is enough |
| Apply one named book's method | Matching `apostle-opusmethodology-*` | General reading |
| Research a long nonfiction article before drafting | `apostle-article-research` | Fact-check, literature review, or finished-draft review |
| Translate a book, paper, or chapter where form carries meaning | `apostle-translation` | Short ordinary text |
| Remove model-shaped English or Chinese prose | `apostle-antislop` | Proofreading, fact-checking, or detector evasion |

Read each skill's frontmatter `description` for its complete trigger and exclusions. Do not load all nine together.

---

<div align="center">
<sub>Why “apostle”? <i>Apostolos</i> — “one sent forth” — is the actual etymology; it just so happens it also sounded cool, in that order. Amusingly enough, this word — freighted with genuine religious and political history — got picked up by a repo with nothing to do with either, purely because it sounded profound. <code>apostle-constitutio</code> §0 already puts it on the record that the sender's seat is vacant — so if you were waiting for someone official to sign off on any of this, you were always going to wait forever. Nine skills, no sender, still sent. 😎<br>
为什么叫「apostle」？「apostolos」——「被差遣者」——是真实词源，只是它先听起来够酷，词源是后来补的理由。有点令人捧腹的是，这一个有着深刻政治与宗教历史蕴含的词语，被一个完全没有涉及这些方面的仓库——只是因为听着很深奥——拿来用了。<code>apostle-constitutio</code> 第 0 节早说清楚了：差遣者的座位本来就空着——所以你若在等谁来盖章，那从一开始就等不到。九本 skill，没有差遣者，照样被差遣出去。<br>
<i>Ars longa, vita brevis.</i> —— 艺长，生短。</sub>

<sub>This footer — KL9 & Claude Sonnet 5, 2026-07-16.</sub>
</div>
