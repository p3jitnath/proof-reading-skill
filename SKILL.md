---
name: proofread-technical-prose
description: Proofread, polish, or rewrite technical and scientific prose, preserving meaning and citation keys; verify references or audit bibliographies when the requested scope calls for it.
---

# Proofread Technical Prose

Make scientific writing connected, precise and easy to follow without changing what it establishes. For research manuscripts, use polished publication-quality academic English and a continuous scientific argument while retaining the requested audience and effective author voice.

## Mandatory GitHub refresh

Before **every invocation**, even if this skill was used earlier in the session, run `python3 "<skill-dir>/scripts/refresh_skill.py"` with the actual skill directory. It downloads the latest `main` bundle from `https://github.com/p3jitnath/proof-reading-skill`, trying SSH through `git@github.com:p3jitnath/proof-reading-skill.git` first and HTTPS as the fallback. Read the printed `SKILL.md` and use that bundle's directory for references, scripts and packaged assets. Do not refresh again while rereading it within the same invocation.

The helper shares a five-second download budget across both transports and validates each downloaded bundle. It uses existing credentials without requesting passwords or tokens. If the refresh fails or the budget expires, it waits out the total five seconds and returns the current bundle. If the helper or network tools cannot run, wait five seconds yourself and proceed with the current version. Briefly disclose a fallback. Each invocation must attempt a fresh download. Runtime copies preserve unpublished edits and the installed fallback.

## Prose punctuation

Do not use semicolons or colons in prose you draft or revise, including revised body text, headings, captions, labels, author queries, and explanatory replies. Titles are exempt and may use either punctuation mark. Recast with full stops, commas, conjunctions, or parentheses while preserving meaning and avoiding comma splices. Preserve required punctuation in code, configuration, URLs, file paths, identifiers, mathematical notation, exact quotations, official names, and bibliography metadata. Prose strings rendered by code still follow this rule. Inspect changed reader-facing text before delivery. Do not rewrite protected text or unrelated content merely to remove punctuation.

## Scope and intervention

Honor the user's requested scope, format, language, and level of intervention over these house defaults. Use the supplied text and context to resolve routine choices, and complete the revision without asking for approval at each pass. A short passage does not require a manuscript project, evidence plan, compilation, or other skills.

- **Inspect:** return findings and optional alternatives without editing files or replacing the supplied text.
- **Proofread:** correct grammar, spelling, punctuation, agreement, and unambiguous language errors with minimal changes.
- **Polish:** also improve flow, syntax, paragraph order, and concision while retaining technical content.
- **Rewrite:** recast difficult passages while preserving claims, evidence, qualifications, equations, citations, and audience.

Default to polish when an editing request does not specify a level. Respect protected wording and requested revision markup; layout work does not authorise rewriting. Use the requested or established English variety, with British English as the fallback. Preserve quotations, official names, LaTeX commands, and literal code or dataset identifiers. Change bibliography metadata only when reference corrections are in scope and supported by authoritative evidence. Follow the current document's notation and numeral conventions rather than importing another project's settings, and apply the prose punctuation rule above.

## Preserve scientific meaning

Keep numerical values, units, signs, notation, equations, causal direction, uncertainty, comparison populations, significance, citations, and cross-references intact. Check suspicious inconsistencies against available authoritative context. Resolve a scientific ambiguity only when the evidence determines the meaning; otherwise retain it with an author query or offer clearly labelled alternatives. When the user requests only revised text, place the query beside the affected statement. Continue independent language repairs and do not invent evidence or citations.

Read each changed sentence with its predecessor and successor to identify the known object, the new information and the relationship needed next. Prefer concrete subjects, stable technical terms, explicit referents and direct, confident statements of supported results. Preserve useful definitions and qualifications when tightening prose. Remove duplicated reasoning and empty evaluation in context. Word blacklists, fixed sentence lengths and mandatory opening phrases do not establish clarity. Preserve the author's effective voice.

## Reference checking

Preserve citations and keys during language edits. Run a full bibliography audit only when explicitly requested or when a comprehensive manuscript or submission review includes reference integrity in its scope. The presence of citations alone does not expand a small prose repair into an audit.

For reference edits, requested citation checks, or a concrete suspected error, read the relevant parts of [reference integrity](references/reference-integrity.md) and verify the affected works against authoritative sources. Use its complete report, supported corrections, and second source-based validation for a full audit. Respect findings-only requests and protected bibliographies; state unavailable evidence and coverage limits, and never invent a reference or claim that unchecked entries passed.

## Other conditional guidance

Read only what the requested edit needs:

- For prose edits or reviews, use the relevant sections of [prose style](references/prose-style.md), including academic narrative, first-use definitions, sentence links, paragraph logic, evidence-based framing, equations, terminology, timing and score interpretation.
- For an abstract or conclusion, use [abstracts](references/abstracts.md). Mechanically verify that the final edited abstract has at most 2,000 characters, including spaces, and satisfies any stricter venue constraint.
- For manuscript-scale consistency, LaTeX source, document structure, or page fitting, use the relevant sections of [manuscript editing](references/manuscript-editing.md). Preserve templates and scientific constraints while checking affected output.

## Finish the requested revision

Compare the revision with the original for scientific fidelity, then read the affected passage continuously with its neighbours. Include in-scope captions, headings, and table labels. For tracked edits, also read the intended accepted version after insertions and deletions take effect, preserving ordinary emphasis and scientific colours. Complete checks relevant to the change and fix regressions. Broaden or repeat verification only for new edits, failures, or concrete concerns. If a needed source or renderer is unavailable, identify the unverified part and finish the rest.

Return findings for inspection requests; otherwise return revised text ready to use, with author queries only for unresolved scientific choices. For substantial revisions, add at most three concise points about material changes. For a short request with no unresolved issue and no reference audit, return only the revised text. When a reference audit runs, link its report and corrected bibliography and state remaining uncertainties and whether the active bibliography was updated. When authorised to edit files, update them directly and report the result briefly rather than reproducing the whole manuscript.

If a skill instruction causes a pause or prevents the requested revision, identify its file and explain the specific conflict. This skill does not add approval requirements to work already authorized by the user.

Instruction routing follows OpenAI's [Astra skills guidance](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra).
