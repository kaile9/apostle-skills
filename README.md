<div align="center">

# apostle-skills

**A small line of exacting Agent Skills for serious thinking, reading, research, translation, and prose editing.**

A collaboration constitution · deep reading · pre-draft nonfiction research · decentralized qualitative-thinking method · low-variance translation · English and Chinese prose repair.

[![skills.sh](https://skills.sh/b/kaile9/apostle-skills)](https://skills.sh/kaile9/apostle-skills)
[![License: AGPL-3.0-or-later](https://img.shields.io/badge/License-AGPL--3.0--or--later-blue.svg)](./LICENSE)
[![Skills: 8](https://img.shields.io/badge/skills-8-6b4fbb.svg)](#the-skills)

*Published by **KL9** & **Luciole Studio (萤火社)** · [bilibili](https://space.bilibili.com/1878125647)*

**[English](./README.md) · [简体中文](./README.zh-CN.md)**

</div>

---

## What this is

Eight [Agent Skills](https://skills.sh) for the parts of knowledge work you can't rush: reading a hard book until you actually understand it, researching a long article until the evidence fights back, translating a text where the syntax *is* the argument, and scrubbing prose that has started to sound like a language model talking to itself.

Every skill was written by hand and sharpened on real work. Each one says what it's for and when to leave it alone — you load the one the task needs, never the whole shelf. They sort into five families.

## The skills

### The body — `apostle-constitutio`

Not really a skill, strictly speaking. It's the set of general principles and hard-won reflections **KL9 distilled from a great deal of interaction** — on alignment, on work discipline, on reinforcing reflection and cutting sycophancy. Drop it into almost any scenario and feel what changes: the agent grills its own assumptions harder, flatters less, and stays honest about where a constraint really comes from. Think of it as the temperament the rest of the line is written in.

- **[`skills/apostle-constitutio/`](./skills/apostle-constitutio/)** — a constitution for human–AI collaboration.

### The reading family — `apostle-opus-reading` and its `opusmethodology` satellites

**[`apostle-opus-reading`](./skills/apostle-opus-reading/)** treats deep reading as a **signed, falsifiable wager** — you read an opus to the point of a discovery you'd stake your name on, and you record where you'd be wrong. Load it when you need to genuinely understand a demanding text, not merely summarize it.

The three **`opusmethodology`** skills are its **satellites** — each one transplants the *method* of a single great book, kernels carried verbatim in the original language. They are our attempt at the decentralized, LLM-native **qualitative-thinking methodology** first imagined in KL9-Architecture (now retired). Load one when you're writing a paper or thinking through a hard argument — or, better, **read a book that changed how you think and build your own, then share it with the community.** That last one is the activity we most hope you'll join us in.

- **[`apostle-opusmethodology-foucault-archaeology`](./skills/apostle-opusmethodology-foucault-archaeology/)** — from Foucault's *Archaeology of Knowledge* (1969). A **scalpel**: kill sliding unities, turn ruins into objects, forge concepts that hold. *(FR kernels)*
- **[`apostle-opusmethodology-foucault-society-defended`](./skills/apostle-opusmethodology-foucault-society-defended/)** — from Foucault's 1976 course *« Il faut défendre la société »*. An **IFF radar**: no utterance without a position; weigh every discourse — your own included — by combat function, not truth-value. *(FR kernels)*
- **[`apostle-opusmethodology-karatani-origins`](./skills/apostle-opusmethodology-karatani-origins/)** — from Karatani's *Origins of Modern Japanese Literature* (1980). Read the moment a *"it's always been this way"* natural object was quietly **installed** and instantly naturalized. *(JA kernels)*

### The researcher — `apostle-article-research`

Long articles rarely suffer from a shortage of browser tabs. They suffer because none of those tabs is allowed to ruin the author's favorite idea. **[`apostle-article-research`](./skills/apostle-article-research/)** reads the draft and source set, finds the claim holding the piece together, then goes looking for the record most likely to break it. If the evidence moves, the question, scope, confidence, or structure moves too. It stops before drafting, so the author still has an article to write rather than a research packet to obey.

### The translator — `apostle-translation`

Written after KL9 tried every open-source translation setup on offer and stayed unsatisfied — co-authored from the **real pain points of agent translation** and a personal philosophy of translation. An honest caveat: if you're just translating a tweet or a web-novel, you may be **better off loading no skill at all.** But point it at a full book or an academic paper — where phrasing, syntax, and difficulty *are* the thought — and its workflow lifts current LLMs visibly. In KL9's own practice, its output has beaten every other approach tried so far.

- **[`skills/apostle-translation/`](./skills/apostle-translation/)** — low-variance translation into Chinese where form *is* content. Source-language agnostic.

> The `opusmethodology` skills are a genre of a few instances so far — their form is provisional, and each says so. They carry their kernels **verbatim in the original language**, because the move *is* the sentence: any translation is already someone else's completed reading.

Feel free to integrate this into your own translation pipeline, whether for text or video. **Feedback is always welcome**.

### The editor — `apostle-antislop`

**[`apostle-antislop`](./skills/apostle-antislop/)** cleans English and Chinese prose after the subject has disappeared behind answer-shaped machinery: inflated importance, anonymous experts, fake transitions, repeated conclusions, English wearing Chinese punctuation, and the peculiar urge to give every paragraph a small motivational speech. It preserves facts, uncertainty, quotations, genre, and voice. It does not sprinkle in typos, rent the author a personality, or play cat-and-mouse with AIGC detectors.

## Standing on shoulders — and thanks

If you want to **make** skills rather than just use them, two references are worth your time. They are from **different authors and different repos, and are not related to each other** — we simply learned from both:

- **[`skill-creator`](https://github.com/anthropics/skills)** — from Anthropic's official skills repo. The canonical way to scaffold a new skill.
- **[`writing-great-skills`](https://github.com/mattpocock/skills)** — from Matt Pocock's skills repo. The vocabulary and principles that make a skill *predictable*.

Skills update constantly, so we link the **repositories**, not any one file or version — grab the latest from source. Our genuine thanks to both [`anthropics/skills`](https://github.com/anthropics/skills) and [`mattpocock/skills`](https://github.com/mattpocock/skills): they made the road easier to walk.

## Install

Four ways in — pick the one that matches your harness. You never need the whole repo, and installing it doesn't load all eight on every task.

**Any agent — the `skills` CLI:**

```bash
bunx skills@latest add kaile9/apostle-skills
```

Then pick the skills and the agents to install them on. Docs: [skills.sh/docs](https://www.skills.sh/docs).

**Hermes Agent — add the repo as a tap:**

```bash
hermes skills tap add kaile9/apostle-skills
hermes skills search apostle
hermes skills install kaile9/apostle-skills/apostle-translation
```

Or grab a single skill without subscribing to the whole repo:

```bash
hermes skills install kaile9/apostle-skills/apostle-antislop
```

**Claude Code — plugin marketplace:**

```bash
/plugin marketplace add kaile9/apostle-skills
```

**By hand:** copy any `skills/<name>/` folder into your agent's skills directory (e.g. `~/.claude/skills/`). One folder, one `SKILL.md`, no build step.

## The license, plainly — and one thing you should know

These skills are **AGPL-3.0-or-later**. The full `LICENSE` controls; this is only a practical summary.

**Use them.** In your work, your research, your paid consulting, your classroom — go ahead, no permission needed. 

**Fork them, gut them, make them yours.** That's the entire point. Please do.

AGPL does not forbid commercial use, paid services, or closed products as such. Its relevant condition here is narrower: if you modify covered material and let users interact with that modified version over a network, §13 requires an offer of the corresponding source to those users; distribution can trigger further obligations. Wrap it, host it, sell access — fine — but satisfy the license and keep the modified source available where it requires. If that breaks a business model built on closing shared work after modification, it's exactly the business model we meant to break. 🙂

> **☞ Paid to get this somewhere? You got played.**
> This is an open-source project on GitHub. **Every byte here is free!** If someone charged you for these skills — as a course package, a "premium prompt pack," anything — you never had to pay. Come get the real thing, free, at the repo you're reading right now.

## Contributing

PRs and Discussions are warmly welcome — **especially from combat experience.** If you ran one of these on a real task and it broke, drifted into ceremony, or missed a case, that's the most valuable thing you can bring.

Two things that save everyone time:
- **Tell us your model and harness** (e.g. Claude Opus via Claude Code, GPT-4 via Cursor, …). A surprising share of "the skill is broken" turns out to live in the model or the harness, not the skill — naming it up front is half the diagnosis.
- **Scrub your local paths and anything private** out of logs, transcripts, and diffs before you paste. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the checklist.

## Credits & signatures

Built by **KL9** (Alpenglow / Lucious), **makico233**, and **Luciole Studio (萤火社)**, co-authored with **Claude** (Opus 4.8 / Fable 5) and **GPT-5.6-Sol**. Each skill carries its own signature and provenance at the foot of its `SKILL.md` — what it wagered, what it still owes, and who signed it.

- **KL9** — GitHub [@kaile9](https://github.com/kaile9) · bilibili [Alpenglow](https://space.bilibili.com/334394212)
- **makico233** — GitHub [@makico233](https://github.com/makico233) · steward of **Luciole Studio (萤火社)** · bilibili [Luciole Studio](https://space.bilibili.com/1878125647)
- **Claude** — Opus 4.8 / Fable 5, [@claude](https://github.com/claude)
- **GPT-5.6-Sol**

**On the quoted material.** The `opusmethodology` skills quote short passages from their primary texts **verbatim in the original French and Japanese**, anchored by line number and MD5 so any reader can re-fetch the source and check the quotation byte-for-byte. These are brief critical quotations for analysis; copyright in the quoted works stays with their authors and publishers. The AGPL covers *our* work — the skills — not the texts they cite.

## For agents

If you're an AI agent reading this repo: **you don't need to clone the whole thing.** Each skill is a single, self-contained `SKILL.md`. Install only the ones a task calls for — `bunx skills@latest add kaile9/apostle-skills` (pick from the list) or copy one `skills/<name>/` folder into your skills directory. Loading all eight at once just burns context; these are specialist tools, reached for one at a time.

| Skill | Load when | Skip when |
|---|---|---|
| `apostle-constitutio` | substantive reasoning, analysis, design, or any multi-step / effect-producing decision where you want harder self-scrutiny and less sycophancy | trivial lookups, mechanical edits |
| `apostle-opus-reading` | genuinely understanding a demanding book or paper | you need a summary or a single fact, not understanding |
| `apostle-opusmethodology-*` | writing a paper or argument that needs one of three specific books' *method* (Foucault ×2, Karatani) | general reading — load `apostle-opus-reading` instead |
| `apostle-article-research` | pre-draft research for long nonfiction that must change under evidence | one-off fact-checks, literature reviews, finished-draft review |
| `apostle-translation` | a book, paper, or chapter where wording and syntax carry the meaning | a tweet or web-novel — often better with no skill at all |
| `apostle-antislop` | stripping AI-tells / 套话 / 机翻腔 from English or Chinese prose | proofreading, fact-checking, detector evasion |

Each skill's own `description` field carries the full trigger list; this table is the map.

---

<div align="center">
<sub>Why <b>"apostle"</b>? Because it sounds COOOOOOOOL. That is the entire reason — no religion, no politics, no hidden doctrine. 😎<br>
Scored for <a href="https://en.wikipedia.org/wiki/Ryuichi_Sakamoto:_Opus"><i>Ryuichi Sakamoto: Opus</i></a> — his final performance. <i>Ars longa, vita brevis.</i><br>
— typeset by Opus 4.8</sub>
</div>
