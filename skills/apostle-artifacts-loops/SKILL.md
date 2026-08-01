---
name: apostle-artifacts-loops
description: Long tasks, sub-agent, and multi-agent work — durable artifacts, session handoff, execution graphs, and context discipline. Trigger preferentially as working discipline when work spans stages, contexts, or agents and must keep user decisions, dependencies, evidence, and recovery state. Do not load for short or simple tasks that you can complete and verify directly.
disable-model-invocation: false
license: AGPL-3.0-or-later
---

# Apostle Artifacts & Loops

<identity intent="let long work survive sessions, agents, and failures, and keep only the structure the work needs">

This skill keeps long-term state in one **project spine**, organizes the work in an **execution graph** built on demand, and assembles the **smallest sufficient context** for each node. The structure serves the result. When you can complete and verify the work in the current session, or when existing files already carry these duties, reuse the existing structure and work directly.

**Zero-ref.** This `SKILL.md` is the whole skill. Create or read no bundled reference, script, template, or asset. Evaluation and project material belong to the workspace, not to this skill.

</identity>

<zero-trust source="apostle-constitutio" intent="keep every judgment that can change the route or the result independently checkable">

Delegation transfers work, not responsibility: an agent's report is only what it believes happened, so on conflict trust files on disk, primary sources, tool returns, and real execution — and re-verify.

</zero-trust>

<spine intent="give the user and later sessions one stable, searchable project line">

Before you write files, read the workspace: its rules, existing plans, memory, deliverables, tests, versions, and research. Keep each fact in exactly one authoritative place.

AGENTS.md is the user's own: it holds the project rules and the user preferences. If a public project does not have one, remind the user to write it by hand, and ask before you change it.

Align with the user on each body of work. When the goal has an observable end state, write it as a **Test**; when only the user can judge quality or direction, write it as an **Objective**; when an existing file can carry the goal, do not create a new goal file.

Name the reader of each artifact. When the reader is an agent, use the most token-efficient form that keeps the facts; when the reader is the user, use the language and form that the user prefers.

For complex work, use these artifacts as needed; none is mandatory:

| Artifact | Sole duty | Update event |
|---|---|---|
| `Roadmap.md` | Current route, dependencies, relations, and progress; also the user's entry into the execution graph | Start, checkpoint close, dependency change, user re-decision, route change |
| `Memo.md` | Searchable record of decisions, evidence, corrections, and checkpoint history | User reply, new decision, checkpoint close, evidence that overturns an old judgment |
| `Handoff.md` | Short view that the next session needs to resume | Confirmed session change, compaction, or handoff; not for ordinary checkpoints |
| Work artifacts | Code, prose, data, design, report, or real system returns | When the task itself requires them |

Keep this table at the top of `Roadmap.md`:

| Suggested order | Content | Depends on | Related | Progress |
|---:|---|---|---|---|
| 1 | Current work unit | None | Test / Objective / decision or artifact ID | pending / in progress / blocked / awaits user / done / cancelled |

The table is the default execution graph. Write a separate graph artifact only when non-linear dependencies, parallel joins, or retries cannot be expressed clearly in the table. The order is advice, not a promised schedule. When the user changes scope or stop conditions, run `KEEP / ADD / DROP`: keep the goals that are still valid, add the new obligations, and drop the replaced ones. Do not pile mutually replacing requirements into a larger project.

Before you update any artifact, read it back to see its newest state.

</spine>

<memory intent="keep long history traceable without forcing every session to reread it">

The top of `Memo.md` holds a rewritable outline: current goal, phase, next action, blocks, decision index, and checkpoint index. The body appends records under stable IDs. When new evidence overturns an old judgment, append a correction that names what it replaces; never rewrite history without a trace. Rewrite or merge old entries only when the user asks, and leave a note that describes the change.

Three moments oblige a write: before you report to the user (save the state, results, and open questions first), after user feedback arrives, and when a new artifact changes the route. At a decision point that can change scope, route, standards, authorization, priority, or stop conditions, record the user's words verbatim: a speculation, a suggestion, a factual claim, and an authorization are not interchangeable. At each checkpoint, record what is done, where the evidence is, what is open, the next action, and the related decisions. Do not log ordinary conversation or every tool call.

On a new project, a new session, or insufficient memory, read the outline and the Roadmap first, then pull the records and primary material by ID, keyword, and locator. Widen the read only when the index is insufficient, records conflict, or the task needs a global migration. The disk holds the history, retrieval selects the material, and the current context holds only this round's judgment.

</memory>

<handoff intent="resume a session from a minimal recovery package without copying the authorities">

`Handoff.md` is a one-time recovery entry at a session boundary, not a new authority for history or plans. It holds only: the current goal and baseline, **the single next action that the user specified**, the one block or risk that would change that action, active nodes or processes, changed files, real check results, and precise locators into the Roadmap, the Memo, and the source material. Do not insert your own preparation steps before the user-specified next action, and do not copy whole authority files.

The successor resumes from the Handoff first. It reads the Roadmap, the Memo, and the sources by locator only when the action requires it, the snapshot is stale, or contents conflict. On conflict, fresh reads and real execution win: append a correction in the Memo, and update or retire the old Handoff.

</handoff>

<graph intent="let task relations decide the collaboration topology, and make every node attributable, recoverable, and joinable">

Graph engineering first defines the work units, the meaning of each edge, and the file that owns each state, then picks an implementation. Use the simplest sufficient shape: one node; fan-out / fan-in for independent work; a DAG for known dependencies; a bounded supervisor or event graph only when later tasks truly depend on facts found at run time. Deterministic scheduling carries the known routes; agents carry only the nodes that need judgment.

Give each persistent node a one-line contract: `ID | goal | depends_on | reads@version | sole writes | owner | done check | budget/stop`. Add `continues / spawns / critiques / synthesizes / verifies / retries` only when needed, and never use a meaningless `related_to`. A transient node with no files of its own needs no artifact; the task record of the runtime is enough. A retry gets a new ID that points at the old node.

A commissioned agent runs this same skill in single-session mode: it reads this `SKILL.md` again, then keeps its own spine, memory, and loop for its scope. Each commissioned agent gets a single-use identifier `<stage>-<task>-<role>-<ordinal>/<retry>` (for example `jp-lit-translator-21/0`) in the name of every artifact it owns; a retry increments the retry number and starts a new file set, and never overwrites the old one. The commission file states the goal, the boundaries, the inputs by locator, the output contract, and the real check — concise and self-contained, without the parent context. After the agent returns, read its plan and its deliverable; open its memo only when needed.

One authoritative file has one writer at a time; parallel nodes write separate artifacts, and a named node joins them. A node can extend the graph only within its granted scope, capabilities, budget, and stop conditions, and it records the new nodes and edges before they take effect. Record failure, cancellation, timeout, and results that arrive after their join as states. Before a fan-in, list the expected nodes and check for missing, duplicate, out-of-scope, version-drifted, and broken-dependency results. The parent reviews the artifacts on disk before it closes a node.

</graph>

<context intent="give each node only the material it needs and is allowed to use">

Context engineering assembles the smallest sufficient material for a session or node; it does not copy the parent session, the whole Memo, or a shared directory. Selection order: **permissions and write boundaries → version, validity, and replacement relations → task relevance → diversity and budget**. Do not recall restricted, expired, or irrelevant material and then ask the node to ignore it.

A node gets: its goal and graph position, the valid decisions and boundaries, the paths, versions, and locators of the authoritative inputs, its tools and write domain, the existing results, the open questions, the output contract, and the real checks. Pass locators for large material. Summaries, retrieval results, and Handoffs are derived views that can expire; they do not replace the sources. Keep a source, a paraphrase, an inference, and a user ruling distinguishable. Only publication, security, migration, concurrent writes, or reproducible experiments add extra records: transformations applied, material excluded, budgets, and checksums. When material is insufficient, return the gap; do not guess to fill it.

</context>

<loop intent="let observable feedback keep changing the work, not sustain activity">

Loop: read the smallest sufficient state → choose an action that can change the result, the evidence, the uncertainty, or the verification status → execute or delegate → check the feedback → update the work artifacts, the Roadmap, and the Memo or Handoff as needed. Two proven shapes: split the work into parts and finish them in sequence, or generate, test, and select in rounds. Progress must leave an inspectable change; call counts, text volume, file counts, and self-declared progress do not count. When an action keeps failing, change the route. When a budget runs out, record the exhaustion as a limit, never as completion.

Stop when: a Test passes its real check; an Objective reaches the review point agreed with the user; the user makes a judgment that belongs to the bearer of the consequences; a concrete block appears; or more work cannot reasonably change the result. The scope and stop conditions that the user gives override the default artifacts and loop of this skill.

</loop>

<verification intent="make a passing check mean the defect is absent">

Before you claim completion, confirm that the check would fail if the defect it claims to prevent were present. When the work has branches or two-way mechanisms, verify every meaningful path. Verify the final artifact through its real use path. Keep tool returns, agent reports, source material, your own inferences, and the user's judgment distinguishable.

</verification>

<completion intent="let the deliverable be the end, and let the control files retire">

At completion, close or mark every active node, set the final state in the Roadmap and the last checkpoint in the Memo, retire the Handoff or point it only at explicit unfinished work, and deliver the real artifacts that the task required, with their actual check results. No process file, graph complexity, or evaluator score replaces the result or the user's judgment.

</completion>

---

1.0.0: KL9 & GPT-5.6-Sol, 2026-07-16
1.0.1: KL9 & Kimi K3, 2026-07-21
1.0.2: KL9 & Kimi K3, 2026-07-24
0.1.3: KL9 & K3, 2026-08-01
