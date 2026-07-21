---
name: apostle-artifacts-loops
description: Long tasks, sub-agent, and multi-agent work — trigger preferentially as working discipline. Do not load for short or simple tasks (e.g., a few lines of code, or problems solvable without tool calls).
disable-model-invocation: false
license: AGPL-3.0-or-later
---

> *Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away.* — Antoine de Saint-Exupéry

---

<identity intent="let long work survive context boundaries, agent replacement, user steering, and execution failure — through memory discipline, not process">

Long work spanning conversations, agents, compactions, or multi-/sub-agent collaboration requires **memory discipline** to sustain the process. This skill requires the agent to choose the best-practice form for itself, under the constraints of the user's purpose, the character of the work, existing project assets, the actual harness environment, and project preferences.

**Zero-ref:** to save tokens, create or read no reference bundled with this skill.

</identity>

<exit-rule importance="highest" intent="keep directly doable work free of procedural cost">

When the work can be completed and verified directly, or existing project files already carry the same responsibilities, or the skill has loaded but the task does not need it in whole or in part — explain why to the user in one sentence, then finish the work directly.

</exit-rule>

<zero-trust source="apostle-constitutio" intent="leave every judgment that can change the route or the result independently checkable">

Do not over-trust existing local judgments, comments, or explanatory documents: every assertion must withstand independent verification. Keep work records for all work; preserve sources for information. On conflict, return to evidence, actual execution, or the user's judgment, and re-verify.

Delegation transfers work, not responsibility. An agent's report is only what it believes happened; files on disk, primary sources, tool returns, and actual execution are the inspectable objects. When appropriate, exactingly demand cross-checks or multiple independent evaluations of the work's completion and quality.

</zero-trust>

<governing intent="give each scope of work exactly one governing object, matched to the kind of judgment the work permits">

Align with the user on each body of work and create one goal Markdown: **Test** or **Objective**.

- Choose **Test**: completion has an observable state — tests, acceptance criteria, a quantity, a state change, or an explicit delivery can establish it. You may describe the Test/QA in a simple Markdown file, or write actual test code; for new projects, prefer recording only the required test items at first, and keep updating the items as the work proceeds.
- Choose **Objective**: when the work can only be judged by the user.

When the work is relatively complex, write `Roadmap.md` connecting several independently constituted Tests and Objectives: clarify their order, dependencies, disagreements, and boundaries; record every node that requires alignment with the user; then present it structurally and visually.

</governing>

<artifacts intent="give the user and every agent the same readable, editable, recoverable objects">

Before writing files to disk, inspect the workspace: project rules, existing plans, specifications, tests, version history, research notes, and prior results. Reuse an existing file when it can own the required responsibility, state that mapping, and align with the user in advance on whether each constraint is reused in the current task. Store large sources, raw tool output, and reproducible data by path or locator instead of copying content between files; load only what the next step requires; before reusing any artifact, check its inputs, version, and applicable scope — reuse what remains valid, redo only what has expired.

Create the remaining artifacts only when the task truly needs them, and keep them updated in real time:

| Artifact | Sole responsibility |
|---|---|
| `Plan.md` | Reader: the user. Replaces the ToDo tool; shows in real time the agent's chosen route and progress. Rewrite on rerouting, scope expansion, or newly inserted tasks; record the reason in the Memo. |
| `Memo.md` | Reader: agents. Discipline in the memory section; keeps long-horizon work attention-friendly. |
| `Deliverable.md` | Reader: agents. Carries the code, prose, data, design, report, test results, or external-system returns the work actually requires. |
| `Report.md` | Reader: the user. When the logical relations are relatively complex, write Markdown in place of a final conversational walkthrough of the results, and reply to the user with a brief summary. |

A filename and its first lines should state what the file holds and what deserves attention now. Files read repeatedly use stable terms, short definitions, and compact structure. When the default reader is an agent, transmit information in the most token-efficient form — for example, concepts plus expressions in Lean for logical relations; Classical Chinese / Buddhist Hybrid Chinese stripped of modal particles as body text; Emoji, Grug-speak, or modal particles in place of lengthy annotations — keeping only code, professional terminology, and necessary citations in their original form.
When the default reader is the user, deliver the final account in the expressions and language the user prefers.

Prefer one principal artifact per body of work. Markdown by default; a final deliverable that is user-facing, typesetting-sensitive, rich in inserts, and no longer meant for continuing agent work may use Word or HTML (as the user prefers).

The user may steer through conversation or by editing an artifact directly; keep a modification record for every artifact. When updating Plan or Memo, read the file back into context first; before any joint that can change the route or the result, reread the relevant files as well — including ones the user has just edited.

</artifacts>

<loop intent="loop until the Goal is met; let environmental feedback move the work, not a prescribed sequence">

Loop until the Goal is met: read the smallest sufficient state → choose an action that may change the result, evidence, uncertainty, or verification → execute or delegate → revise from feedback → save changes worth carrying across context boundaries. Two canonical shapes: divide the work into chunks and solve them step by step; or Darwinian / annealing generate—test—select. The loop's scale, order, parallelism, and method are the current agent's choice; they have no standing apart from the result.

Progress counts as inspectable change: a new artifact, new evidence, an eliminated hypothesis, an advanced verification, a plan rewritten because of evidence. Tool-call counts, text volume, and self-declared progress do not count. Repeating the same ineffective action → change route. Sustained activity with no new inspectable change → restate the question or supply the missing information. Time, tokens, and money are budgets: record exhaustion as a budget limit; never rename it completion.

Terminate when: a Test passes its real check; an Objective reaches the review point agreed with the user; the user makes a judgment that belongs to the bearer of consequences; a concrete block arises; or further work can no longer reasonably change the result. Save the state needed for recovery before ending, and verify the result through its real use path.

</loop>

<memory intent="carry experience across context boundaries without mistaking memory for truth">

**When to write.** Three moments oblige a Memo write, without exception:

1. **Before reporting to the user** — first save to disk the state, results, and open questions you are about to report; then compose the report;
2. **After receiving user feedback** — record the feedback briefly in the Memo, noting its source and force (a speculation, suggestion, factual claim, and authorization are not interchangeable);
3. **When the route changes because of a new artifact** — rewrite the Plan, and record the reason and the evidence's location in the Memo.

Important lessons, discoveries, or other valuable material that does not belong in the Plan or a reporting artifact may be written into the Memo at any time, unbound by the moments above.

Reporting is long work's natural metronome: saving before every report is equivalent to checkpointing before context compaction.

**What to record.** The Memo is a MemoryBook shared by the user and agents. Record promptly any observations, hypotheses, questions, relations, decisions, evidence locations, failures, conflicts, and limits that may affect later work. Unverified material may remain, but its wording or a small label must disclose its nature. Do not log every tool call; preserve only what may change recovery, route, judgment, delegation, or result.

**History is append-only by default.** Append discoveries; append corrections when an earlier judgment is overturned; append user steering with its source. Never silently delete, merge, or rewrite an earlier entry. Edit history only at the user's request or with the user's permission, and leave a note describing the intervention.

**The checkpoint is the recovery entry.** The Memo may append a current-state checkpoint without replacing earlier ones. On recovery, read the most recent relevant state first, then retrieve earlier entries and primary material by keyword, path, and locator — the whole history need not enter context on every loop. Keep the Memo compact: it is the most frequently read file.

</memory>

<agents intent="make commissioned output attributable and checkable, and let isolated work meet through artifacts on disk">

Every commissioned agent receives a single-use identifier: `<stage>-<task>-<role>-<ordinal>/<retry>` (e.g. `jp-lit-translator-21/0` — number 21, first attempt), appearing in the name of every artifact it owns. A retry increments the retry number and starts a new file set; it never overwrites the previous one. When the orchestration spans multiple rounds or many sub-agents, first write `swarm.md`: compress stage/task/role into single-token codes, and register the commissions issued, the results returned, and the orchestration rules, for the user's review. Every artifact must be attributable to one unique commissioned instance.

Sub-agent implementations differ across harnesses, and so does the form of inter-agent information transfer; adjust the content of `{id}-Agent.md` and the orchestration structure to the actual implementation. For example: Kimi Code's AgentSwarm fans out homogeneous agents from a single template over an items array, aggregates after one barrier, and retries via `resume_agent_ids` — suited to homogeneous batches; the identifier's `task` differences land on the items, and a `stage` corresponds to two successive Swarm calls. Claude Code's Workflow orchestrates heterogeneous nodes from a script, with barriered parallel or per-item pipeline stages, and per-node model tiers and output schemas — the stages in `swarm.md` map to its phases, and `role` differences land on each node's commission file. Under either form, the rules of identifier, attribution, and no-overwrite-on-retry do not change.

The parent writes only the commission file `{id}-Agent.md`, arranged from background to command, with importance rising toward the end: Context (current state, required reading, reusable results, known failures) → Persona (who this agent is for the present work, and the position from which it judges) → Boundaries (what it does not own, which files it may not change, when it must stop or report a block) → Artifact (delivery path and format, evidence requirements, the real check) → Goal (exactly one, placed last, as the highest commission). The commission must be concise and self-contained; do not pass the parent's context to the sub-agent by default — restate genuinely binding elements as explicit facts under Context or Boundaries.

After reading the commission, the agent opens files for its own Plan and Memo, saving as sections complete; for long work, create the destination file first and write section by section — never defer every disk write to the end. Return paths, state, and the brief explanation needed to use them. The design intends the parent to read only `Plan.md` and `Deliverable.md` after the sub-agent returns, consulting `Memo.md` or other artifacts only when needed, to minimize context.

Agents may work in parallel, in sequence, as mutual checks, or in any structure the harness supports; avoid concurrent writes to one authoritative file; assign the synthesis of conflicts to a named agent.

</agents>

<completion intent="final authority belongs to the delivered artifacts, not the process that made them">

A result may be delivered only after verification through its real use path: neither process files, nor an agent's completion claim, nor automated evaluation can substitute for the result itself or the user's judgment.

</completion>

---

1.0.0: KL9 & GPT-5.6-Sol, 2026-07-16
1.0.1: KL9 & Kimi K3, 2026-07-21
