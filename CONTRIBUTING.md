# Contributing to apostle-skills

Real failure reports beat everything else. If you ran a skill on an actual task and it broke, drifted into ceremony, or missed a case — that's what we want. Open an issue with what broke, or a PR if you already have the fix.

最有用的贡献是真实的失败报告。你把某本 skill 用在真任务上，它崩了、滑进了仪式、漏了某种情形——开个 issue 说清楚，有修法直接开 PR。

## Include these two things

Your model and harness (e.g. *Claude Opus 4.x via Claude Code*, *GPT-4 via Cursor*). A lot of "the skill is broken" turns out to be the model or harness, not the skill — naming your setup up front saves a diagnosis.

Before pasting logs or diffs, scrub anything local or private: absolute file paths, API keys and tokens (`sk-…`, `ghp_…`, session cookies — never paste these even expired), real names and internal hostnames, and any unpublished or copyrighted text you were translating or reading. Quote only what's needed to show the failure.

请附上两样：你的模型与 harness（例如 Claude Opus 4.x + Claude Code、GPT-4 + Cursor）。相当一部分「skill 坏了」最后是模型或 harness 的问题，先讲清配置能省下一轮排查。

粘贴日志或 diff 前，清掉本地或私密的东西：绝对文件路径、API key 和 token（`sk-…`、`ghp_…`、会话 cookie——哪怕已过期也别贴）、真名和内网主机名，以及你当时在翻译或阅读的、未发表或受版权保护的文本。只引用足以说明问题的最小片段。

## Proposing a change

Typos, broken links, unclear sentences: PR directly. A behavioral change to a skill — new step, changed rule, removed section: open an issue first, or explain the reasoning in the PR, including what real task exposed the need. A new `opusmethodology` skill from a book that changed how you think: open a Discussion — that's the collaboration we most want.

错字、坏链接、讲不清的句子：直接 PR。skill 的行为性改动——新步骤、改规则、删段落：先开 issue，或在 PR 里写清理由和暴露需求的那个真任务。一本从改变了你思考方式的书里做出的新 `opusmethodology`：开个 Discussion——这是我们最想要的合作。

If you touch a kernel in one of the `opusmethodology` skills, the verbatim quotation must still verify against its original-language source (line number + MD5).

如果你动了 `opusmethodology` 系里的内核，逐字引文必须仍能对着原文（行号 + MD5）核实。

Before publishing AI-assisted prose here, run it through [`apostle-antislop`](./skills/apostle-antislop/).

在这里发布 AI 参与写的文字前，先让 [`apostle-antislop`](./skills/apostle-antislop/) 扫一遍。

## Licensing and attribution

Contributions are licensed AGPL-3.0-or-later, same as the rest of the repo. Don't submit material you don't have the right to license this way. Contributors are credited; if an AI agent co-authored your change, record it as a commit trailer — `Co-authored-by: Claude <noreply@anthropic.com>` — the convention this repo already uses.

贡献按 AGPL-3.0-or-later 授权，与仓库其余部分一致；不要提交你无权如此授权的材料。贡献者会被署名；若改动由 AI 智能体共著，用 commit trailer 记录——`Co-authored-by: Claude <noreply@anthropic.com>`——本仓库已在用的惯例。
