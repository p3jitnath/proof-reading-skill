# Reference integrity audit

Use the full workflow for an explicit reference or bibliography audit, or a comprehensive manuscript or submission review whose requested scope includes reference integrity. Once a full audit is in scope, check every citation and bibliography entry relevant to that manuscript rather than sampling suspicious references. Citations or associated bibliography files alone do not trigger a full audit during a small language edit.

For requested citation checks, affected bibliography entries, or a concrete suspected error, use only the relevant inventory, authoritative verification, correction, and validation steps. Preserve unchanged references and keys; report the checked scope and unresolved findings concisely. A focused check does not require a manuscript-wide inventory, `reference_audit.md`, or `references_corrected.bib`. Expand coverage only when the request or evidence of a wider integrity problem warrants it. Findings-only and protected-file instructions take precedence.

The workflow is **read-only audit → report → supported corrections → overwrite active bibliography → second validation against authoritative sources**. Do not modify manuscript or bibliography sources during the initial audit. Writing the requested report and correction artefacts follows that initial inspection; it does not authorise unrelated manuscript edits or publication actions.

## 1. Establish the manuscript and citation inventory

- Identify the active manuscript, supplements, bibliography files, build route, current revision, and existing local changes. Discover all relevant `.tex`, `.bib`, `.md`, and supplementary source files, including other formats used by this manuscript. Follow includes, bibliography declarations, Markdown bibliography metadata, and separately built supplements. Distinguish active inputs from unrelated papers, backups, old exports, and generated files. Record the files and revision actually audited.
- Extract every citation key actually used, with source locations. Cover `\cite`, `\citep`, `\citet`, `\autocite`, `\parencite`, `\textcite`, and similar commands, including starred forms, optional arguments, multiple keys, multiline commands, multicite commands, and locally defined citation wrappers. Inspect wrapper definitions rather than treating a single regular expression as exhaustive. For Markdown, include the project's citation syntax such as `[@key]` and `@key` in prose, excluding code and examples that are not manuscript citations.
- Exclude commented-out and inactive sources from the active count, while recording materially different review and accepted states. Reconcile with a fresh `.aux` or `.bcf` when available; stale generated files are not proof of coverage. Report `\nocite{key}` separately as bibliography inclusion; expand `\nocite{*}` to the selected database without calling every included work an in-text citation. Verify these deliberately included works too.
- Parse every relevant `.bib` file with a suitable BibTeX/BibLaTeX parser and inspect its warnings. Preserve name particles, suffixes, group authors, braces, Unicode/LaTeX accents, string macros, `crossref`, and `xdata` inheritance. Expand dependencies for verification without mistaking structural records for cited papers. For a handwritten reference list, enumerate entries and citation mappings directly rather than inventing BibTeX keys.
- Cross-check used keys and database entries for missing keys, uncited entries, repeated keys, duplicate records, the same paper under different keys, malformed BibTeX, and inconsistent key spelling/case. Check duplicate works through identifiers and title/author identity, not title similarity alone. Distinguish a preprint from a materially different published version. Do not remove uncited records or merge duplicates automatically.

The main audit covers every distinct actively cited key, including unresolved keys. Audit the other entries in the relevant bibliography as well, with their results separate from cited-reference totals. For a supplied excerpt without repository access, audit each identifiable reference using available evidence and state exactly which files, entries, or mappings could not be checked. Missing source material is an incomplete audit, not a reason to mark an unknown reference PASS.

## 2. Verify each work independently online

For **every cited work**, and every other publication entry in the relevant bibliography, consult external sources. Treat the existing `.bib` as a claim to check, never as ground truth. Prefer sources in this order, adapting to the type and publication version of the work:

1. DOI registration records/Crossref and the DOI's resolved record.
2. The official publisher or proceedings page; inspect the paper's title page when metadata is abbreviated or inconsistent.
3. The official arXiv abstract/version record and manuscript when applicable.
4. DBLP for computer science papers as a corroborating bibliographic record.
5. Semantic Scholar or OpenAlex only as secondary checks, not the sole basis for a PASS or a correction where primary evidence is missing.

For books, datasets, software, and other non-paper references, use the corresponding authoritative publisher, repository, release, or institutional record. A DOI is not mandatory for a work that has none. Search snippets and automatically formatted citations are discovery aids only; open the underlying record. A resolving DOI can still belong to the wrong paper. Check its identity, and distinguish publisher access denial from an invalid DOI.

Use the version actually being cited. Do not combine a preprint's date and author list with a journal version's venue, pages, or DOI unless the relationship is explicitly verified and represented correctly. When authoritative sources disagree, inspect the primary document and version history, record the disagreement, and leave uncertain fields unresolved. Do not guess a merged record. In particular, absence from search results alone does not establish that a paper is nonexistent.

### Field-by-field comparison

Compare and record the current value, verified value, evidence URL, and any uncertainty for each applicable field:

- Title, including meaningful punctuation, acronyms, mathematical symbols, and subtitles.
- **Complete author list**, exact ordering, every author's first and last names, initials, spelling, diacritics, particles, and suffixes. Preserve a verified group author as such.
- Publication year and the version to which it belongs.
- Full journal, conference, workshop, proceedings, or book title.
- Volume, issue/number, pages or article number, and publisher where applicable.
- DOI, arXiv identifier and relevant version, and any URL used to identify the work.

Distinguish verified absent/not applicable from not yet verified. Never fill a missing field with a plausible value. An arXiv identifier is not applicable to every paper; neither are page ranges or issue numbers. Representation differences such as a correct LaTeX accent versus its Unicode equivalent are not name errors. Venue abbreviation or permitted capitalisation may be a minor style matter; a different venue or title identity is substantive.

Be particularly strict about missing, extra, misspelled, reordered, or hallucinated authors and incorrect initials. Retrieve the full authoritative list; `et al.` or a truncated search result cannot establish completeness. Do not expand an initial from memory or from a different person's profile. If the available authoritative evidence cannot verify the needed spelling, mark that field unverified. Compare title, authors, venue, and identifiers **together** to catch records assembled from two different papers. Do not repair such a hybrid by keeping whichever fields look plausible.

## 3. Classify and report before corrections

Assign one status to every distinct cited key in the original source:

| Status | Meaning |
| --- | --- |
| PASS | Work identity and all important applicable metadata, including the complete author list and order, are verified. |
| MINOR ISSUE | Only non-substantive formatting, capitalisation, or equivalent representation discrepancies remain; important metadata is verified. |
| MAJOR ISSUE | Wrong, missing, or extra author; wrong spelling, initials, or author order; wrong title or venue; wrong DOI; evidence of a nonexistent work; hybrid metadata; or a structural defect that prevents an unambiguous valid citation, such as a missing BibTeX key. |
| UNVERIFIED | Authoritative evidence is insufficient to verify important metadata or identify the work, without a confirmed major error. |

A confirmed major error takes precedence over incomplete verification; record the unverified fields as well. Otherwise incomplete important metadata prevents PASS or MINOR ISSUE. Missing keys are MAJOR ISSUE, with identity unresolved unless authoritative evidence identifies the intended work. Duplicate keys that make lookup ambiguous are major; an uncited duplicate with a different key is recorded separately. Do not turn a failed search into a confirmed nonexistent-paper claim.

Create **`reference_audit.md`** in the manuscript project. Begin with:

- Total distinct cited references and the counting convention; count keys, not repeated citation occurrences, and separately report duplicate works.
- PASS, MINOR ISSUE, MAJOR ISSUE, and UNVERIFIED counts; these must sum to the cited-key total, including missing keys.
- Missing BibTeX keys and their source locations.
- Uncited BibTeX entries; distinguish deliberately included `\nocite` entries and structural dependencies.
- Audit scope, source files/revision, verification date, and any unavailable material or coverage limitation.

Include one row per cited key using this exact table structure. Include full author details here or in a clearly linked per-key field comparison; do not conceal omissions behind `et al.`.

| Key | Status | Title | Authors | Venue/Year | DOI/arXiv | Problems found | Authoritative source |
| --- | --- | --- | --- | --- | --- | --- | --- |

Then add a section ranked by severity, with **all MAJOR issues first**, followed by UNVERIFIED cases and minor issues. For every problematic entry, explicitly show **Current BibTeX value** and **Verified value** field by field, plus the direct authoritative source supporting each proposed change. If no value can be verified, write “Unverified; no correction proposed.” State confirmed absences or inapplicable fields explicitly. Include exact full original and verified author lists for any author-list problem. For unresolved missing keys, show the citation location and missing-entry state rather than inventing a record.

List uncited-entry findings, duplicates, malformed records, key inconsistencies, and dependency problems separately so none disappears from the report. Keep original audit counts and findings after repairs; add final validation results separately rather than replacing the original failures with PASS. A completed structural scan or successful parser run does not establish bibliographic integrity.

## 4. Produce corrected entries and update the bibliography

Once the audit and report are complete, apply only corrections supported by authoritative external evidence. An authorised full audit includes supported corrections unless the request limits the work to findings or protects the bibliography; do not ask again merely because the audit found errors. If the current request explicitly forbids file changes, protects the bibliography, or asks for findings only, deliver the report/proposed values and omit overwriting. Preserve all unrelated edits and keep the original bibliography recoverable through an existing exact version or a separate backup, including any uncommitted changes.

Write **`references_corrected.bib`** containing corrected entries and unchanged unresolved records. Preserve existing citation keys wherever possible, record order, comments, case-protecting braces, strings, and cross-reference dependencies. Do not impose a new key scheme during this audit. A duplicate-key repair must identify the intended work at each citation location before changing keys; record any unavoidable mapping and update only verified dependent citations. Do not delete unused entries or merge distinct versions to tidy the database. Add a missing record only when the intended work and metadata are externally established.

Check that the corrected file parses and that no entries or fields disappeared unintentionally. Then overwrite the **actual active bibliography file(s)** with the supported corrections; a sidecar alone does not complete the normal workflow. Preserve the manuscript's existing bibliography filename and linkage. If the active file already has the name `references_corrected.bib`, stage its replacement separately. For multiple active databases, retain file boundaries, produce a clearly mapped corrected copy of each (for example `<stem>_corrected.bib`), and update the corresponding originals without merging databases or duplicating keys. State every source-to-output mapping in the report.

Leave unresolved values unchanged and clearly labelled in the report rather than inventing a repair. Report whether each entry was corrected, left unchanged pending evidence, or withheld because the intended work could not be identified. Metadata validation does not establish that a paper supports a manuscript's scientific claim; do not rewrite claim attribution solely from this audit.

## 5. Run the second validation against the sources

After correction and overwrite, independently compare **every entry in `references_corrected.bib` and any mapped corrected files** against the authoritative records again. Check actual saved values, not only the proposed patch or prior summary. Revisit the source evidence for work identity, complete author lists and order, spelling, and every applicable field. Use an additional primary record to resolve discrepancies when available. A second parser pass or comparison of two local files is not this source-based validation.

- Verify that each active bibliography matches its validated corrected counterpart, with all original keys and entries accounted for and only documented changes.
- Re-extract active citations and check missing keys, duplicate keys/works, malformed records, and inconsistent names/identifiers. Reconcile counts and any key mapping with the original inventory.
- Build with the actual bibliography workflow when available. Inspect generated reference text and embedded link destinations, including author truncation caused by style settings, wrong-work links, duplicated DOI prefixes, or rendering macros that override correct metadata. Distinguish correct source metadata from permitted venue abbreviation/truncation; do not change a required bibliography style without authorisation.
- If validation finds a supported correction, apply it consistently to the corrected and active files, document it, and repeat the affected checks. If sources remain unavailable or contradictory, stop guessing and report the remaining uncertainties. Do not claim a complete PASS while important fields or entries remain unchecked.

Append second-pass results, remaining uncertainties, build/visual-check status, and the exact files overwritten to `reference_audit.md`. The delivery should link the report and corrected bibliography, distinguish initial findings from final verified status, and name every unresolved major issue or unverified reference. No actual metadata correction is justified merely because this skill contains a verification instruction.
