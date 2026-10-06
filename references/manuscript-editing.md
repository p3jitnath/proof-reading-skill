# Manuscript editing and consistency

Use for manuscript-scale proofreading or a requested source, structural, or layout edit. Apply only the checks needed for the supplied scope and its dependencies.

## Identify the source and permitted changes

For files, establish the active root document, included sources, bibliography, relevant assets, output, and build route. Inspect existing changes when version control is present. Similar filenames, old exports, and earlier completion notes do not establish the current revision. A pasted passage needs only its supplied context.

Distinguish findings-only review, proofreading, polishing, rewriting, layout work, and accepting tracked edits. Preserve protected sections and the delivery format. When wording is protected, improve only permitted presentation or return suggestions. Separate alternatives do not replace the accepted document automatically.

Use the current request and document for English variety, notation, review colours, caption spacing, source formatting, page limits, and venue rules. A small consistency list helps a long document, but a local repair does not need a new project record.

## Read the intended revision state

When reviewing tracked changes, inspect the intended accepted reading after insertions are retained and deletions removed. Check that a deletion has not removed a subject, conjunction, antecedent, definition, or qualification. Apply acceptance only to the requested revision layer, preserving scientific colours, mathematics, and ordinary emphasis.

In LaTeX, unwrap designated review-colour commands or groups, such as `\textcolor{review}{...}` or `{\color{review} ...}`, while retaining their accepted contents and nested equation or emphasis commands. Preserve connective words, punctuation, and spacing at wrapper boundaries. Inspect the rendered accepted reading rather than deleting colour commands indiscriminately; inspect embedded figure assets too when they are in scope.

A row marked for deletion still belongs to the displayed table until it is excluded. Match bolding, ranking claims, and comparison language to the applicable displayed or accepted state. Keep marking and deletion distinct.

## Reference checking

Match reference work to the requested scope. Preserve citations during a language edit; check affected works when citation or bibliography changes are requested or a concrete error needs verification. Run the full [reference integrity audit](reference-integrity.md) only for an explicit audit or a comprehensive manuscript or submission review that includes reference integrity. In that full workflow, finish the initial read-only audit before edits, then complete the report, supported corrections, and second source-based validation. Respect findings-only and protected-file instructions. A citation-key or syntax scan does not establish bibliographic identity or metadata correctness.

## Check prose and dependent objects

- Define abbreviations where needed in the abstract, main text, and self-contained captions; keep one stable term per scientific object.
- Preserve the source-to-claim relationship of citations. Group citations only when authorised and attribution remains unambiguous; verify the rendered placement when it matters.
- Keep numerical values, units, uncertainty, comparison populations, and direction of improvement consistent across the edited text and dependent captions or tables.
- Review headings, captions, table labels, and cross-references as prose. When a figure becomes a table, update the object name and language about points, bars, or shading.
- Distinguish absolute scores, percentage changes, and score points. Preserve actual meanings of missing values rather than guessing data for a visual gap.
- Keep headings useful and sections proportionate to their job. Do not pad paragraphs or impose a universal number of subsections.
- Connect result claims to recoverable evidence and introduce relevant figures, tables, and appendices. A number need not be repeated in a table solely because it appears in prose.
- Check rendered cross-references for duplicated names such as “Figure Figure” when macros already supply the prefix.

For an authorised method rename, update reader-facing names consistently and preserve a mapping to historical code or result identifiers. Do not rewrite immutable experimental records to match a new publication name.

## LaTeX and page fitting

Use the project's specified engine, bibliography workflow, and source-format conventions. Preserve supplied class, style, and template files unless changing them is explicitly in scope. Make a necessary package or definition addition narrowly and explain it. Avoid unrelated preamble cleanup.

Determine which pages the constraint covers, such as body, references, or supplement. Inspect rendered output to locate excess space: source figure canvas, inclusion scale, float allocation, table geometry, or surrounding document spacing. These need different repairs. Preserve explicit caption gaps, typography, protected wording, and figure aspect ratios.

Use only authorised changes. Citation-placement-only work does not permit prose rewriting, figure resizing, or spacing changes. Layout-only work does not permit shortening paragraphs. If prose compression is authorised, remove repetition while retaining definitions and qualifications; do not automatically trim particular sections by fixed percentages. Resolve remaining incompatible constraints through a concrete scope decision after completing independent permitted work.

After layout or reference changes, compile and inspect the affected pages and neighbouring float movement for overflow, legibility, reading order, and caption association. After whitespace-only reflow, confirm that rendered text and layout remain unchanged. Count the appropriate rendered pages rather than trusting a source comment or previous build.

## Complete the requested review

Finish with a continuous read of the changed passage and its neighbours. For result-changing work, identify the canonical evidence and update dependent in-scope text and assets together. Separate scientific verification from grammar and visual inspection in the report.

Use an available `paper-writing` skill for substantial changes to the scientific argument or evidence interpretation, and `graph-plotting` for figure data, design, or typography. Neither is a prerequisite for ordinary proofreading. If a needed source or renderer is unavailable, report the specific unverified part and finish independent edits.

Once applicable checks pass, repeat them only after another edit, a failure, or a concrete concern. Describe actual source checks, compilation, and visual review accurately; do not describe a source-only edit as PDF verification.
