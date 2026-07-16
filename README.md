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

> If someone sold you this repo as a “premium prompt pack,” ask for a refund. Every byte is free here.  
> 若有人把这个仓库包装成「高级提示词礼包」卖给你，请去退款。这里的每个字节都免费。

Real failures make useful contributions. Tell us which model and harness you used, what the skill did, and where it broke. Remove private data and local paths before posting logs. See [CONTRIBUTING.md](./CONTRIBUTING.md).

真实的失败最适合拿来贡献。请说明模型、harness、skill 做了什么、在哪里坏掉；粘贴日志前删掉隐私与本地路径。详见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## Credits

Built by **KL9** (Alpenglow / Lucious), **makico233**, and **Luciole Studio（萤火社）**, with **Claude** (Opus 4.8 / Fable 5) and **GPT-5.6-Sol**.

- **KL9** — GitHub [@kaile9](https://github.com/kaile9) · bilibili [Alpenglow](https://space.bilibili.com/334394212)
- **makico233** — GitHub [@makico233](https://github.com/makico233) · bilibili [Luciole Studio](https://space.bilibili.com/1878125647)

Thanks to Anthropic's [`skill-creator`](https://github.com/anthropics/skills) and Matt Pocock's [`writing-great-skills`](https://github.com/mattpocock/skills), two unrelated projects from which we learned.

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
