---
name: apostle-artifacts-loops
description: >
  Use for long work that needs durable artifacts, loops across stages, shared memory, or several agents. Do not use when the work can be completed and verified directly, or when the project already has files that carry the required state.
license: AGPL-3.0-or-later
metadata:
  hermes:
    tags: [apostle, artifacts, loops, long-horizon, context-engineering, multi-agent, memory]
    related_skills: [apostle-constitutio]
---

# apostle-Artifacts＆Loops

<identity intent="let long work survive context boundaries, agent replacement, user steering, and execution failure without forcing capable agents through a fixed process">

This skill governs the **artifacts** that preserve long work and the **loops** that move it. It specifies no mandatory file set, agent count, collaboration topology, or reasoning sequence; the current agent chooses those forms from the user's purpose, the character of the work, the existing project, and the available harness.

**Zero-ref:** this `SKILL.md` is the whole skill; create or consult no bundled reference, script, template, or asset.

</identity>

<exit-rule importance="highest" intent="keep direct work free of procedural cost">

Do not apply this protocol when the work can be completed and verified directly, or when existing project files already carry the same responsibilities. If the skill has loaded but the task does not need all or part of it, give the user one sentence explaining why, then finish the work directly.

</exit-rule>

<zero-trust source="apostle-constitutio" intent="leave every consequential claim independently checkable">

**Bidirectional zero-trust applies to claims, not persons.** The user holds the synthesis seat for purpose, preference, authorization, and consequences; the user, parent agent, other agents, plans, memos, tool results, source materials, and evaluators acquire no factual authority from identity alone. Preserve the source and verification state of every judgment that can change the route or result. When claims conflict, return to evidence, actual execution, or a judgment that belongs to the user; do not erase the conflict through an unmarked reconciliation.

Delegation transfers work, not responsibility. An agent report begins as testimony; files on disk, primary sources, tool returns, and actual execution provide objects of inspection. An independent evaluator can supply another judgment, but cannot replace evidence or make `PASS` true by declaration.

</zero-trust>

<artifacts intent="give the user and every agent the same readable, editable, recoverable objects">

Before creating anything, inspect the workspace, project rules, existing plans, specifications, issues, tests, version history, research notes, and prior results. Reuse an existing file when it can own the required responsibility, and state that mapping. Give each effective fact, constraint, or state one authoritative home.

<work-object choice="exactly-one-per-scope" intent="match the governing object to the kind of judgment the work permits">

Choose exactly one governing object for each scope of work: **Task** or **Target**. Do not use both as competing charters for the same scope.

| Object | Choose it when | Default artifact |
|---|---|---|
| **Task** | Completion has an observable state that tests, acceptance criteria, a quantity, a state change, or an explicit delivery can establish. | `Task.md` |
| **Target** | The work seeks a direction, quality, or relation whose movement can be evidenced but not reduced to one pass/fail condition without the user's judgment. | `Target.md` |

Choose Task when the user asks for test-driven work, supplies determinate acceptance criteria, or the work has a verifiable terminal state. Choose Target when creation, exploration, or judgment must be recalibrated through signs of movement. A Roadmap may connect several separately constituted Tasks or Targets. If a Target produces a local unit with independent acceptance criteria, constitute that unit as a Task without changing the parent Target.

</work-object>

Create the remaining artifacts only when they have work to do:

| Artifact | Sole responsibility |
|---|---|
| `Roadmap.md` | Express relations, dependencies, alternatives, and disagreements among several Tasks or Targets; it need not be linear. |
| `Plan.md` | Hold the current agent's chosen route. Rewrite it when evidence changes the route, and append the reason to the Memo. |
| `Memorandum.md` or `Memo.md` | Preserve project experience, user steering, changes of judgment, and memory needed for recovery; choose one name within a scope. |
| Work artifact | Hold the code, prose, data, image, design, report, test result, or external-system return that the work actually requires. |
| Reporting artifact | Deliver the agent's final account to the user; the final conversational reply is itself an artifact. |

A filename and its first lines should tell the user what the file contains and what deserves attention now. Write every saved file in the user's preferred language and register; retain evidence in its source language and place a translation beside it when needed. Files read repeatedly should use stable terms, short definitions, and compact structure.

The user may steer through conversation or by editing an artifact. Before the next joint that can change the route or result, reread the relevant file and preserve the steering's source and force. A speculation, suggestion, factual claim, and authorization are not interchangeable.

</artifacts>

<loop intent="let environmental feedback move the work instead of repeating a prescribed sequence">

A loop reads the smallest sufficient state for the work at hand, chooses an action that may change the result, evidence, uncertainty, or verification state, investigates, creates, executes, or delegates, then revises its judgment from environmental feedback and saves changes worth carrying across context boundaries. The agent chooses the loop's scale, order, degree of parallelism, and method; those choices serve the work and have no standing apart from its result.

**Progress leaves an inspectable change.** A new artifact, a material revision, new evidence, an eliminated hypothesis, a located conflict, an advanced verification result, absorbed user steering, or a plan rewritten because of evidence can establish progress. Tool-call count, file count, prose volume, and an agent's claim that progress occurred cannot establish it alone.

Treat repetition, stagnation, and budget separately. Repetition of the same ineffective action calls for another route. Continued activity without a new inspectable change calls for a renewed account of the question, method, or missing information. Time, tokens, tool calls, and money are execution budgets. Record exhaustion as a budget limit; do not rename it completion or use it to deny progress already made.

End the loop when one of these conditions is true: a Task passes its real check; a Target reaches its agreed review point; the user makes a judgment that belongs to the bearer of the consequences; permissions or missing information create a specific block; or further work can no longer reasonably change the result. Save the state required for recovery before ending, and exercise the result through its real use path.

</loop>

<memory intent="carry experience across context boundaries without mistaking memory for truth">

The Memo is a MemoryBook shared by the user and agent. Record observations, hypotheses, questions, relations, decisions, evidence locations, failures, conflicts, and limits when they may affect later work. Unverified material may remain, but its wording or a small label must disclose what kind of entry it is. Do not log every tool call; preserve only material that may change recovery, route, judgment, delegation, or result.

**History is append-only by default.** Append discoveries; append corrections when an earlier judgment falls; append user steering with its source. Do not silently delete, merge, or rewrite an earlier entry. Edit history only at the user's request or with the user's permission, and leave a note describing the intervention.

The Memo may append a current-state checkpoint without replacing earlier checkpoints. On recovery, read the most recent relevant state first, then retrieve earlier entries and primary material by keyword, path, and locator. The whole history need not enter context on every loop.

</memory>

<context-economy intent="preserve full working ability with the smallest high-signal context">

Keep stable material stable so caches can be reused and meaningless rewrites avoided. Store large sources, raw tool output, and reproducible data by path, locator, query, or version rather than copying them among files. Load only what the next work requires. Before reusing an artifact, check its inputs, version, and scope; reuse what remains valid and redo only the part that has expired.

Disk preserves, retrieval selects, and context supports the present judgment. The more often a file is read, the more compact it should be; the larger the material, the more precisely its searchable structure and locators should admit it on demand.

</context-economy>

<agents intent="preserve independent routes through separate plans and reduce transmission loss through isolated artifacts">

Give every commissioned agent a non-reusable identifier:

```text
<round-code>-<agent-number>-<task-code>-<retry-number>
```

The round code names the current batch or material range; the agent number is its stable ordinal in that batch; the task code is short, readable English; the first attempt has retry number `0`, and a retry increments the number without overwriting the previous directory. The twenty-first agent in a Japanese-source round, commissioned to study literature for the first time, is:

```text
jp-21-literature-0
```

Put this identifier in the name of every artifact that agent owns:

```text
Agents/
└── jp-21-literature-0/
    ├── jp-21-literature-0-Agent.md
    ├── Plan-jp-21-literature-0.md
    ├── Memo-jp-21-literature-0.md
    └── Artifact-jp-21-literature-0.md
```

A retry creates `jp-21-literature-1/` and matching filenames; it does not alter `jp-21-literature-0/`. These naming rules do not bind the parent agent's files.

<commission-file order="context-to-task; importance-rises-toward-end" intent="establish the situation first and place the controlling commission last">

The parent writes only the commissioned agent's `{agent-id}-Agent.md`. Arrange it from background to command, with importance and execution priority rising down the file; put the governing Task or Target last:

1. **Context** — current state, required reading, reusable results, known failures, and necessary facts;
2. **SOUL** — who this agent is for the present work and the professional position from which it judges;
3. **Boundaries** — what it does not own, which files it may not change, and when it must stop or report a block;
4. **Artifact** — delivery path and format, evidence requirements, and the real check;
5. **Task or Target** — exactly one, placed at the end as the highest-priority commission.

The commission must be concise and self-contained. Do not pass the parent Plan by default. When an element of that plan truly constrains the commissioned work, restate it as an explicit fact under Context or Boundaries.

</commission-file>

After reading the commission, the agent writes `Plan-{agent-id}.md`, maintains `Memo-{agent-id}.md`, saves work incrementally, and produces work artifacts carrying the same identifier. For long work, create the destination first and write as sections complete; do not defer every disk write to the end. The agent returns paths, state, and the brief explanation required to use them. The parent reads the files on disk and verifies consequential claims before deciding what enters the root Memo, whether the root Plan must be rewritten, and what enters the final result.

Agents may work in parallel, in sequence, as mutual checks, or through any other structure the current harness supports; the task relation must justify the topology. Avoid concurrent writes to one authoritative file. Let isolated work meet through artifacts, and assign synthesis of conflicts to a named agent.

</agents>

<artifact-form intent="lower handoff cost while giving human and agent readers the format each can use">

Prefer one principal artifact for each body of work. A commissioned agent normally writes one Markdown file organized by semantic XML tags; the tags identify the material and its relations instead of scattering the work among near-duplicate intermediate files.

Add one appendix only when a verification ledger, line-by-line comparison, large data table, or similar material would improperly enlarge the principal file. At the beginning of the principal artifact, state the appendix path, purpose, and condition for reading it; do not reveal the appendix only at the end. Give the appendix the same agent identifier. Intermediate material written for agents rather than people has the strongest presumption in favor of one file.

Use Markdown by default and do not produce HTML unless the user asks for HTML. A final artifact intended chiefly for people, sensitive to typesetting, and no longer meant for continuing agent work may use Word. Choose the format from the reader and real use path, not from a universal template.

</artifact-form>

<completion intent="give final authority to the delivered artifacts rather than the process that made them">

Use the format the task actually requires for the final work artifact, and verify it through its real path. Process files cannot substitute for the result; an agent's completion claim cannot substitute for inspection; an automated evaluation cannot substitute for a judgment the user must make.

The final report is itself a user-facing artifact. It does not mechanically compress the other artifacts. It gives another path through the work: how the result answers the original commission, which evidence or failures changed the route, what grounds the final structure, which questions remain open, and what the actual checks returned. The user should be able to enter the work artifact from the report and trace the process and evidence back from the work artifact.

</completion>

**KL9 & GPT-5.6-Sol, 2026-07-16.**
