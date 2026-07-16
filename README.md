<div align="center">

# apostle-skills

[![skills.sh](https://skills.sh/b/kaile9/apostle-skills)](https://skills.sh/kaile9/apostle-skills)
[![License: AGPL-3.0-or-later](https://img.shields.io/badge/License-AGPL--3.0--or--later-blue.svg)](./LICENSE)
[![Skills: 9](https://img.shields.io/badge/skills-9-6b4fbb.svg)](./skills/)

*KL9 & Luciole Studio（萤火社） · [bilibili](https://space.bilibili.com/1878125647)*

</div>

---

<!-- TODO(kl9): write the human-facing intro + skills table by hand. Everything from ## Install down is kept. -->

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

Built by **KL9** (Alpenglow / Lucious), **makico233**, and **Luciole Studio（萤火社）**, with **Claude** (Opus 4.8 / Fable 5) and **GPT-5.6-Sol**.

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
<sub>Why “apostle”? It sounded cool. No religion, politics, or hidden doctrine. 😎<br>
为什么叫「apostle」？因为听起来酷。无关宗教政治，也没有暗藏教义。<br>
<i>Ars longa, vita brevis.</i></sub>
</div>
