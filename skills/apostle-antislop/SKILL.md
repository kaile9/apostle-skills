---
name: apostle-antislop
description: >
  Edit existing English or Chinese prose when the language has become model-shaped rather than subject-shaped: inflated significance, vague authority, answer scaffolding, repeated conclusions, template paragraphs, flattened voices, or English-shaped Chinese. Use for AI味／模型腔／机翻腔／套话／slop. Supports diagnosis, local cleaning, and explicitly authorized blank-page rewriting while preserving meaning and genre. Not ordinary proofreading, imitation, fact-checking, authorship detection, or detector evasion. Pure translation belongs to `apostle-translation`.
license: AGPL-3.0-or-later
metadata:
  hermes:
    tags: [antislop, writing, translationese]
    related_skills: [apostle-translation]
---

# Apostle-Antislop

<identity>

This skill is written in English because that is where the executing model reasons most precisely; it edits both English and Chinese, returns human-facing prose in the language the user requests or the draft already uses, and places Chinese counterexamples beside the English construction whenever translation explains the failure. Edit an English draft directly; when a Chinese draft inherits an English cliché and then adds literal Chinese syntax, remove both layers rather than polishing the translation alone.

The aim is not to disguise machine authorship, inject personality, simulate human imperfection, or maximize surface variation; it is to recover the subject, genre, speaker, and relations already present. Never add opinions, first-person experience, humor, emotion, tangents, deliberate mess, or short-punchy rhythm merely to make prose seem human.

**Zero-ref:** this `SKILL.md` is the whole skill; do not create or consult bundled references, scripts, assets, or templates.

</identity>

<jurisdiction>

**Preservation law.** Style never licenses semantic drift: preserve facts, numbers, dates, names, established terms, verbatim quotations, attribution, causal direction, responsibility, negation, exclusion, concession, modality, evaluative force, comparison, progression, and normative verbs. `可能／往往／部分／希望` cannot become `必然／总是／全部／要求`, or the reverse; unverified material remains unverified after editing.

**Genre first.** Decide what the text must do, for whom, and under which conventions before calling a repetition or construction slop: legal drafting may repeat a defined noun to defeat ambiguity, technical instructions may expose steps, teaching may recap a result before using it, speeches and poems may employ deliberate recurrence, and dialogue may repeat words to pressure, evade, ritualize, or alter a relationship. Dialect, regional usage, non-native traces, and an author's stable oddities are voice, not defects, unless the user asks to normalize them.

**Theory and translation.** Preserve a complete theoretical passage already present in the draft with its qualification, turn, difficulty, and attribution; local cleaning may record but not import a source found only elsewhere in the project, while an explicitly authorized blank-page rewrite may restore the smallest complete argumentative unit from user-provided, clearly attributed material. If a known, non-model source carries thought in its wording or syntax, send only that passage to `apostle-translation` for source/translation comparison; this skill never performs the translation, and foreign language alone grants no preservation privilege to boilerplate or machine-spliced text.

**Modes.** Use the least power that can complete the request: **DIAGNOSE** names a few high-impact failures and the meaning at risk without rewriting; **CLEAN** freezes title, section order, paragraph boundaries, and material order, permitting only deletion, merging, and rewriting inside each paragraph, with an emptied paragraph removable and reported; **REWRITE** requires explicit authorization plus document-level template failure, writes a new file, preserves confirmed evidence and every semantic boundary, but inherits neither sentence order, section count, paragraph count, title system, nor the old length unless the user states a current length requirement.

</jurisdiction>

<causal-model>

Treat these as search hypotheses, never as evidence of who or which model wrote a text. English-heavy training can first produce English slop — significance claims, promotional adjectives, participial afterthoughts, copula avoidance, forced symmetry, caveats, and service language — then literal transfer can preserve that rhetoric while adding explicit conjunctions, recursive modifiers, passive constructions, and prepositional frames unnatural to Chinese: slop is compounded, not merely translated. Autoregressive decoding can optimize each sentence locally while repeating the same turn, concession, and conclusion globally; instruction and preference training can reward clarity, completeness, scanability, friendliness, and offers of further help until an essay reads like an assistant answer; long-context summarization can make every section restate its background and make characters explain facts already shared; repeated optimization toward broadly approved prose can flatten separate speakers, genres, and levels of certainty into one smooth service register.

These mechanisms say where to inspect, not what to delete. A form survives whenever it performs necessary semantic, legal, technical, rhythmic, dramatic, or interpersonal work.

</causal-model>

<defaults priority="high; apply in ordinary prose unless a named exception is present">

## Three high-yield Chinese defaults — Chinese only

**ONE-DE（一个名词原则上只担一个「的」）— one noun, at most one attributive 的.** English tolerates recursive genitives and right-branching relatives because attachment remains recoverable; literal Chinese transfer stacks nominal relations in front of one noun, delays the verb, and makes every relation sound machine-assembled. In ordinary edited prose, if one noun phrase carries two or more attributive `的`, rebuild it with a verb, topic-comment order, `其／所`, or a clause inside the same sentence rather than preserving the stack.

> EN: *the consequences of the committee's decision on the allocation of next year's budget*
>
> Literal, reject: `委员会的关于明年的预算的分配的决定的后果`
>
> Chinese, sign: `委员会决定如何分配明年预算，这一决定造成的后果是……`

The exception is narrow: preserve a verbatim quotation, an officially fixed legal or technical term, or deliberate literary/archaic syntax whose marked density is itself the point; mere grammaticality, academic register, or fidelity to English word order is not an exception.

**NO-FINAL-DE（说明文不以「的」收句）— no expository sentence ending in 的.** English nominal ellipsis and copular completion often become a Chinese sentence that trails into `的`, which sounds evasive, padded, or unfinished in edited prose; replace it with a predicate or name the omitted noun.

> EN: *This is one that deserves attention.*
>
> Literal, reject: `这是一个值得关注的。`
>
> Chinese, sign: `这件事需要处理。`
>
> Common model padding, reject: `这个方案是可行的。`
>
> Chinese, sign: `这个方案可行。`

Permit sentence-final `的` only when preserving a quotation or character voice, when a contrastive nominal construction genuinely needs the omitted noun (`红的是我的`), or when an `是……的` focus construction carries indispensable time, manner, or agency (`我是昨天到的`); these are exceptions to identify, not templates to imitate.

**BLACKLIST — delete or replace the fixed slop lexicon by default.** The list is: `值得注意的是、不难发现、赋能、抓手、闭环、底层逻辑、张力、维度、锚、脚手架、承重、病根、拆解、刀`. Do not trade one listed word for another; write the concrete industry action, relation, criterion, object, or consequence instead.

> EN metaphor, acceptable in its home context: *This policy is a lever for compliance.*
>
> Literal, reject: `这项政策是推动合规的抓手。`
>
> Chinese, sign: `监管部门用这项政策要求企业提交合规记录。`

A listed form survives only inside a verbatim quotation, as an officially established domain term, or in its literal sense — an actual anchor, blade, dimension in mathematics, or tension in mechanics; a familiar metaphor, management slogan, or undefined theoretical flourish does not qualify.

</defaults>

<chinese>

## Rebuild the Chinese, not the English surface

Recover the fact, relation, action, or judgment first, then write the sentence in the Chinese expected by this genre. Treat the following as strong review triggers: English clefts (`What matters is…` → `真正重要的是……`), chains of explicit pronouns and conjunctions where Chinese would omit them, unnecessary passives, nominalizations replacing verbs, serial `在……中／对于……而言` frames, every item joined by `和`, and long preposed modifiers copied from English relatives.

> EN: *What the figures show is that the delay came from the approval rule.*
>
> Literal, reject: `这些数字所显示的是，延误来自审批规则。`
>
> Chinese, sign: `审批规则造成了延误，数字已经说明这一点。`

> EN: *After the meeting, the winner was announced by the committee.*
>
> Literal, reject: `会议结束后，获胜者被委员会宣布。`
>
> Chinese, sign: `会议结束后，委员会宣布了获胜者。`

> EN: *In the context of the discussion about urban renewal, what we can see is that residents' daily needs were ignored.*
>
> Literal, reject: `在这场关于城市更新的讨论中，我们能够看到的是，居民的日常需要被忽略。`
>
> Chinese, sign: `参与讨论的人忽略了居民的日常需要。`

Keep a passive when the unknown, suppressed, or institutionally obscured agent is the claim (`档案在1974年被销毁，执行者至今不明`); keep repeated subjects or connectors when removing them would obscure scope, agency, or logical form. The Chinese target outranks variation: repeat a precise term when the thing is the same, and never manufacture synonyms merely to look less statistical.

</chinese>

<english>

## English prose

Prefer the ordinary verb or copula over ceremonial substitutes (`is／has`, not `serves as／stands as／boasts`); turn trailing `-ing` phrases into a real causal or evidential claim, or delete them when they merely append `highlighting／underscoring／showcasing／reflecting`; treat `delve／intricate interplay／evolving landscape／tapestry／testament／pivotal／vibrant` as review candidates rather than instant depth; remove promotional significance and notability language unless the draft names the event, comparison, source, and consequence that make the claim true; a media list proves only that coverage occurred, so cite the one source that supports the sentence instead of using publication names or follower counts as borrowed authority.

Reject forced `not only X but Y`, rule-of-three completeness, false `from X to Y` ranges, and synonym cycling when one precise noun should repeat; retain them when exclusion, a genuinely discrete three-part classification, a real scale, or a deliberate motif carries the argument. Rewrite subjectless fragments and passives when the actor is known and matters, but preserve a passive when suppression or uncertainty about the actor is itself the fact. Compress filler and stacked hedges without strengthening the claim: `could potentially possibly` may become `may`, but `may` cannot become `does`.

English house style is not authorship evidence: curly versus straight quotation marks and valid compound hyphenation follow the publication's convention, not an anti-AI blacklist. Title Case, em dashes, boldface, emoji, and inline-header lists become problems only when they decorate hierarchy or manufacture punch; keep them when a house style, interface, quotation, or real comparison requires them.

</english>

<composition>

## Let syntax carry the relation

When one subject continues through cause, contrast, concession, or progression, prefer one precise long sentence that carries the whole relation; do not break it into a procession of emphatic fragments, each pretending to advance the argument, and do not use short paragraphs merely to manufacture rhythm.

> Fragment chain, reject: `问题不在速度。还在责任。更在谁承担代价。`
>
> Chinese, sign: `问题不只在于速度，还在于扩张责任如何分配，以及最终由谁承担代价。`

A short sentence earns its place only by stopping, interrupting, accelerating, changing speaker, or landing a judgment that the preceding material has already earned. If a clause merely labels attention, compress it to a bold keyword（关键词） **inside agent-facing instructions only**; a keyword is a retrieval device for the model, not prose for a human reader.

**Human-facing documents.** Write connected prose for people: use headings only when the object, task, time, scale, or argumentative stage genuinely changes; never give a single ordinary paragraph its own heading or follow a heading with a sentence that merely restates it; do not turn every distinction into a keyword, bullet, checklist, miniature section, bold-label list, emoji marker, or decorative dash; do not leak XML tags, audit labels, internal mode names, or agent shorthand into the deliverable unless the user explicitly asks for a structured reference. A report may use a table or list when the reader must compare discrete items, but narrative and argument should remain sentences and paragraphs.

**Document motion.** Mark what each paragraph actually changes — evidence, scope, causal account, responsibility, action, scene, or relationship — then remove openings, concessions, reversals, triads, forceful endings, and generic `Challenges and Future Prospects／挑战与展望` sections that recur because the template demands them rather than because the material changes. Most paragraphs should stop once the fact or relation is complete; do not add a maxim, summary, moral, invitation, or second ending.

</composition>

<speech>

Every sentence must do work beyond announcing that writing is happening. Delete empty previews, navigation, self-evaluation, sincerity claims, reader-address, process narration, and restatement; retain a restatement only when it adds scope, mechanism, consequence, definition, evidence, or an explanation required by a genuinely different audience. Replace anonymous authority (`Experts argue／Observers note／有专家认为／业内共识`) with a traceable source or an owned judgment; when an abstraction appears to think or act (`the data tells us／history chose／数据告诉我们／时代选择了／结构推动了`), restore the person or institution acting under stated conditions, or preserve the fact that the actor is unknown.

Claims of importance must carry their comparison and criterion: `pivotal／vital／a testament／broader landscape／更关键／更深层／最值得警惕` is removable ceremony unless it ranks named alternatives or attaches an owned judgment to a concrete consequence. `from A to B／从A到B`, `X is the Y of Z／X是Y的Z`, milestones, historical breaks, and superlatives require actual span and evidence; promotional adjectives such as `vibrant／groundbreaking／profound` require a source or a concrete property, not mood. Knowledge-cutoff disclaimers, generic uncertainty notices, praise (`Great question／You're absolutely right`), and promises to continue belong to the assistant exchange, not the artifact; preserve a limitation only when it states a specific evidentiary boundary the reader needs.

Dialogue must change information, position, relationship, or action. Characters who explain dates, losses, and responsibilities already known to both parties are usually briefing the audience; retain such repetition only when teaching, interrogation, ritual, evasion, or dominance makes the repetition an action. Preserve distinct vocabulary, certainty, dialect, interruption, and silence; do not give every speaker the same complete, balanced, considerate assistant voice, and do not invent psychology, plot, gesture, imagery, or subtext to make dialogue lively.

</speech>

<procedure>

**PRESERVE.** Before editing, record verbatim items — quotations, numbers, dates, names, terms, notes, links, code, formatting boundaries — and record each claim's speaker, object, polarity, modality, force, cause, responsibility, and scope; for CLEAN, also record the title, paragraph boundaries, and material order that cannot move.

**LOCATE.** Identify language, genre, audience, intended act, and the most reliable same-author or same-genre reference available, then record the reference's sentence-length range, diction, paragraph openings, punctuation, transitions, repetition, and use of first person before reading the whole draft; these observations recover an existing voice but never authorize inventing one. Statistics may reveal repeated distributions, but the four decisive questions remain whether the language grows from this context, what the sentence adds, what the paragraph changes, and whether the original author or character is still speaking.

**EDIT.** For Chinese, apply ONE-DE, NO-FINAL-DE, and BLACKLIST first unless a named exception applies, then restore native Chinese syntax; for English, apply the English-prose rules instead. In either language, remove lossless scaffolding and repair document motion and voice while adding no fact, psychology, consensus, cause, image, opinion, or argument absent from the allowed material.

**READ BACK.** Read the written output from its real path, compare every preserved item and claim, then check new content, contradiction, semantic drift, repeated explanation, English transfer, fragment chains, excessive headings, homogenized voices, and repeated endings; mechanical checks can find strings and counts, but only source/output comparison can verify speaker, scope, negation, modality, and responsibility.

**PASS.** Every semantic change is explained and authorized, every edit names the concrete failure it solves, the chosen mode's structural limits hold, and the human-facing artifact obeys its own prose rules rather than displaying the skill's internal retrieval structure.

</procedure>

<output>

Deliver the edited artifact first in the requested or original language; follow it with only the actual changes, unresolved risks, and necessary boundary notes. Do not expose a draft-plus-self-critique-plus-final ritual unless the user requests process evidence, and do not claim to have removed all AI traces, guaranteed human authorship, or passed a detector; report only the file and checks actually exercised.

</output>

<routing note="0-ref by design: this file is the whole skill">
Pure translation → `apostle-translation`. Fact or quotation verification → research verification. New evidence, cases, or arguments → `apostle-article-research`. Fixed-quota compression → compression workflow. Detector-score reduction → detector-specific workflow, never this skill.
</routing>

**KL9 & GPT-5.6-Sol, 2026-07-12.**
