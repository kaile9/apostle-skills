# Contributing to apostle-skills

*[English](#english) · [简体中文](#简体中文)*

---

## English

Thank you for considering a contribution. This repo has a particular temperament, and a few things up front will save us both time.

### What we most want

**Combat reports.** The single most valuable contribution is: *"I ran skill X on a real task, and here is exactly where it failed."* Drift into ceremony, a missed edge case, a kernel that no longer `grep`s, a section that has hardened into fill-in-the-blank — these are gold. Open an issue describing what you were doing and where it broke. If you already have the fix, open a PR.

### Two things to include in every report

1. **Your model and harness.** e.g. *Claude Opus 4.x via Claude Code*, *GPT-4 via Cursor*, *Llama via a custom loop*. A surprising share of "the skill is broken" turns out to live in the model or the harness — a weaker model ignores a step, a harness truncates the file, a different tool-loop never loads the reference. Naming your setup up front is half the diagnosis, and it stops us chasing a bug that was never in the skill.
2. **A clean paste.** Before you drop in logs, transcripts, or diffs, **scrub anything local or private** (see the checklist below). We don't want your machine paths, and you don't want them public.

### Privacy scrub checklist (do this before pasting)

- **Local paths** — remove machine-specific absolute paths and replace them with `<path>` or a generic stand-in.
- **API keys, tokens, cookies** — anything matching `sk-…`, `ghp_…`, `Bearer …`, session cookies. Never paste these, even "expired" ones.
- **Personal identifiers** — real names, emails, internal hostnames, private repo names, client names.
- **Private file contents** — the text you were translating/reading may itself be unpublished or under copyright. Quote only the minimum needed to show the failure.
- **Absolute research-tree references** — this repo deliberately does not ship its authors' local research tree; don't reintroduce paths to one.

A secret scanner plus a search for absolute filesystem paths catches most of it.

### The bar these skills hold themselves to

Before proposing a change, it helps to know what these skills value — because your change will be judged the same way:

- **Small interface over real depth.** A skill earns thickness only where every line changes behavior. If a paragraph could be deleted without changing what the agent does, it should be.
- **Inline the kernel; ration the refs.** We keep reference files to a minimum on purpose. The load-bearing core belongs in `SKILL.md` itself, where the agent actually reads it — not deferred to a `references/` file it may never open. A separate file has to earn its existence: a genuinely optional deep-dive, a large table, or an archived predecessor. If a ref only exists to hold a paragraph the skill needs every run, that paragraph should be inlined and the ref deleted. Falsification anchors (the CONFESS notes, validation runs, MD5-pinned sources) live in the authors' local research tree, not in the shipped skill — the body points at them, it does not carry them.
- **Structure with XML, deliver as Markdown.** When a passage needs explicit hierarchy — phases, roles, gates, decision branches — wrap it in lightweight XML tags (`<criterion>`, `<pitfall>`, `<mechanism>`, `<step>`) so the structure is machine-legible and the agent can find the part it needs. The prose inside stays clean, human Markdown. Scaffolding aids execution and later editing; it is not decoration, so don't tag what a plain list already makes clear.
- **Kernels that grep.** The `opusmethodology` skills carry verbatim original-language quotations anchored by line number and MD5. If you touch a kernel, the quotation must still verify against the source.
- **A stated wager.** Each skill names what it bets and how it can be proven wrong. Keep that honesty; don't launder a claim into confident vagueness.
- **No ceremony.** No announcing what you're about to do, no restating what you just did, no borrowed solemnity. Say the thing.

### How to propose a change

1. **Small fixes** (typos, a broken link, a clarified sentence): PR directly.
2. **Behavioral changes** to a skill (new step, changed rule, removed section): open an issue first, or write the reasoning into the PR description. Tell us what real task exposed the need — and on what model/harness.
3. **A new skill**: open a Discussion first. Not every good skill belongs in *this* line — the apostle skills share a specific stance, and a well-made skill with a different temperament may be better off in its own repo. **Building your own `opusmethodology` from a book that changed how you think, and sharing it, is exactly the activity we most hope you'll join us in.** We'll talk it through.

### Licensing of contributions

By contributing, you agree your contribution is licensed under **AGPL-3.0-or-later**, the same as the rest of the repository. Don't submit material you don't have the right to license this way. If your change adds a quotation from a copyrighted source, keep it short, critical, and anchored (line number / hash), consistent with how the existing skills cite.

### Attribution

Contributors are credited. If an AI agent co-authored your change, the idiomatic way to record it is a commit trailer — e.g. `Co-authored-by: Claude <noreply@anthropic.com>` — the same convention this repo itself uses.

---

## 简体中文

感谢你考虑参与。这个仓库有它自己的脾性，先讲清几件事，能替你我都省下时间。

### 我们最想要的

**实战报告。** 最有价值的一种贡献是：*「我把 skill X 用在一个真任务上，它恰好在这里失手了。」* 滑进仪式、漏掉的边缘情形、不再能 `grep` 的内核、硬化成填空的某一节——都是金子。开一个 issue，说清你在做什么、它在哪崩了；若你已有修法，直接开 PR。

### 每份报告都请带上两样

1. **你的模型与 harness。** 例如 *Claude Opus 4.x + Claude Code*、*GPT-4 + Cursor*、*Llama + 自研循环*。相当一部分「skill 坏了」，最后发现问题出在模型或 harness——弱一点的模型跳过了某步，某个 harness 把文件截断了，另一套工具循环压根没加载参考文件。先讲清你的配置，诊断就完成了一半，也免得我们去追一个根本不在 skill 里的 bug。
2. **一份干净的粘贴。** 在贴日志、转录、diff 之前，**清掉任何本地或私密的东西**（见下面的清单）。我们不想要你的机器路径，你也不会想让它们公开。

### 隐私清理清单（粘贴前做一遍）

- **本地路径** —— 删除机器专属的绝对路径，替换成 `<path>` 或通用占位。
- **API key、token、cookie** —— 任何形如 `sk-…`、`ghp_…`、`Bearer …`、会话 cookie 的东西。绝不粘贴，哪怕是「已过期」的。
- **个人标识** —— 真名、邮箱、内网主机名、私有仓库名、客户名。
- **私密文件内容** —— 你当时在翻/在读的文本本身可能未发表或受版权保护。只引足以说明问题的最小片段。
- **指向研究树的绝对路径** —— 本仓库刻意不同梱作者的本地研究树；别把指向它的路径再引进来。

用凭据扫描器再搜索一遍绝对文件系统路径，能抓出大半。

### 这些 skill 给自己立的标尺

提改动之前，最好先知道这些 skill 在意什么——因为你的改动会被同一把尺量：

- **小接口盖住真深度。** 只有当每一行都改变行为时，一本 skill 才配加厚。若一段话删掉也不改变 agent 的行为，它就该被删。
- **内核内联，ref 从俭。** 我们刻意把参考文件压到最少。承重的内核属于 `SKILL.md` 正文本身——agent 真正会读的地方，而不是甩进一个它可能永远不打开的 `references/` 文件。一个独立文件必须挣得它的存在：真正可选的深挖、一张大表、或一份归档前身。若某个 ref 的唯一作用是装一段 skill 每次都要用的话，那段就该内联进正文、把 ref 删掉。验伪锚点（CONFESS 笔记、验证运行、MD5 锁定的一手源）存于作者本地研究树，不随 skill 同梱——正文指向它们，而非携带它们。
- **用 XML 搭骨架，以 Markdown 交付。** 当一段内容需要显式的层级——阶段、角色、闸门、决策分叉——用轻量 XML 标签（`<criterion>`、`<pitfall>`、`<mechanism>`、`<step>`）包起来，让结构对机器可读、agent 能精准找到它要的那一块。标签内的散文保持干净的人类 Markdown。骨架是为执行与日后编辑服务的，不是装饰——一个普通列表已经讲清的东西，别去套标签。
- **内核能 grep。** `opusmethodology` 系携带原文逐字引用，以行号与 MD5 锚定。你若动了内核，引文必须仍能对着原文核实。
- **押注摆上台面。** 每本 skill 都说明自己押了什么、如何被证伪。守住这份诚实，别把一个论断洗成自信的含糊。
- **不要仪式。** 不预告将做什么，不复述刚做完什么，不借来庄严。把事说出来就好。

### 怎么提改动

1. **小修**（错字、坏链、把一句话讲清）：直接 PR。
2. **行为性改动**（新增步骤、改规则、删段落）：先开 issue，或把理由写进 PR 描述。告诉我们是哪个真任务暴露了这个需求——以及在什么模型／harness 上。
3. **一本新 skill**：先开 Discussion。不是每一本好 skill 都属于**这一**脉——apostle 系共享一个特定的姿态，一本脾性不同的好 skill，也许在它自己的仓库里更自在。**读一本改变了你思考方式的书，做一本自己的 `opusmethodology` 分享出来——这正是我们最希望大家一起参与的事。** 我们聊聊看。

### 贡献的授权

一旦贡献，即视为你同意你的贡献以 **AGPL-3.0-or-later** 授权，与仓库其余部分一致。不要提交你无权如此授权的材料。若你的改动引入了受版权保护来源的引文，请保持简短、批评性、有锚点（行号／哈希），与现有 skill 的引用方式一致。

### 署名

贡献者会被署名。若你的改动由 AI 智能体共著，惯例是用 commit trailer 记录——如 `Co-authored-by: Claude <noreply@anthropic.com>`——正是本仓库自己采用的约定。
