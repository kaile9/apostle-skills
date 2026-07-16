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

> Paid someone for this? You got hosed — every byte here has always been free, and AGPL-3.0-or-later exists to make sure it stays that way. Charging money isn't the violation — §4 explicitly lets anyone resell verbatim copies for any price. What is a violation: reselling while stripping the copyright and license notices instead of keeping them intact (§4–5), forking it closed and charging for “exclusive” access while tacking on extra restrictions or a licensing fee nobody's allowed to demand for exercising these rights in the first place (§10), or wrapping it in a hosted bot/API and quietly sitting on the modified source instead of handing it to the people using it over the network (§13). None of that is a business model — it's a tollbooth on a road somebody else paved for free. Go get your money back, then come grab the real thing right here.  
> 花钱买到了这个？你被坑了——这里的每个字节一直都是免费的，AGPL-3.0-or-later 存在就是为了保住这一点。收钱本身不是违规——第 4 条明说任何人都能按任意价格转售原版拷贝。真正违规的是：转售时把版权与许可声明撕掉、不保持完整（第 4–5 条）；fork 后闭源、靠卖「独家」访问权赚钱，还给这份行使权利本就不许收费的许可外加限制或授权费（第 10 条）；或是拿它包一个托管机器人或 API，悄悄把改版源码扣下、不给通过网络在使用它的人（第 13 条）。这些都不是生意，是在别人免费铺好的路上私设收费站——先去退款，再回这儿拿真货。

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
