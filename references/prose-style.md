# Technical prose style

Use the sections relevant to the passage. A spelling repair does not require a new argument or a full scientific review.

## Punctuation

Apply the [prose punctuation rule](../SKILL.md#prose-punctuation) to edited prose and author queries. Recast semicolons and colons rather than deleting them mechanically. Allow punctuation in titles and preserve required literal syntax and protected text, then read the revised sentences together for grammatical and scientific fidelity.

## Academic narrative

Use polished and fluid publication-quality academic English for research manuscripts. When writing for the Journal of Advances in Modeling Earth Systems (JAMES), carry the requested academic convention through the manuscript and captions. Preserve the selected English variety, the author's effective voice and any explicitly requested teaching audience. Current submission rules require separate verification when submission work is in scope.

Develop observation → problem → response → result → consequence continuously across the edited argument. Make the relationships explicit so each idea motivates the next. Every sentence must advance the scientific argument through necessary context, a definition, reasoning, evidence, interpretation or consequence. Connect a disconnected fact to its role, or remove it when redundant and within scope. Preserve the first two introduction paragraphs for context and motivation when substantially revising a complete introduction. A local language repair does not authorise inventing missing evidence or restructuring unrelated sections.

Where the evidence supports the connection, prefer a coherent sentence combining the result, its interpretation and the underlying tension or trade-off. Keep it readable rather than forcing multiple unrelated claims together. Use bridges such as “To address this trade-off…” or “This distinction motivates…” when one finding actually motivates the next step. A transition must express the scientific relationship rather than conceal a missing premise.

## Connect sentences through meaning

Read the preceding sentence, the revision, and the following sentence together. Identify what is already known, what the revision adds, and what the next sentence needs. Name the relationship before choosing a connector: definition, elaboration, evidence, consequence, contrast, qualification, or a new topic. A transition word cannot supply a missing premise. Repeating a precise noun often provides a clearer bridge than adding “moreover”. Name a changed comparator, population, or condition explicitly. Flag topic jumps, implicit links, and paragraphs that read as disconnected facts; make each idea's relevance, connection to the next, and consequence explicit.

Give each sentence a principal job, keep its subject near the main verb, and introduce familiar context before new information when that helps. Short definitions and longer connected arguments can both work. Split overloaded qualification chains and repair disconnected fragments according to meaning, without a word-count target or a ban on particular sentence openings. Preserve logical premises while shortening.

Each sentence must be understandable from prior context. Define every acronym, specialised term, metric and architectural component at first use. Explain a component's function and relationship to the architecture. For a metric, state what it measures and, where relevant, its units, reference and direction of improvement. Introduce symbols before relying on them and explain unfamiliar ideas in the sentence where they first appear. Ordinary nontechnical words do not need glosses. Redefine every abbreviation used in the abstract at its first use in both the introduction and conclusion, even if it was defined earlier. For a symbol or concept last explained several sections or subsections earlier, add a brief reminder and a verified section cross-reference when helpful. Use one term for each defined object and retain necessary specialist terminology when it provides precision. Explain it rather than replacing it with a vague synonym. A model, estimator, distribution, sample, and prediction need not be interchangeable. Replace “this”, “it”, “they”, or “the same” when multiple antecedents are plausible, and reintroduce a term when a section break makes its referent remote.

## Give paragraphs distinct jobs

For sustained polishing or structural work, summarise each paragraph's role briefly: question, definition, construction, evidence, interpretation, or limitation. Use this to find duplication and missing links, not to enforce a fixed paragraph template. Preserve useful reminders in self-contained captions and summaries. Compress repeated wording or duplicated facts while retaining the premises, inferential steps, qualifications, and sentence links that make the reasoning recoverable. Similar wording can serve distinct logical roles; do not delete a needed definition or justification merely to reduce repetition.

Order information so the argument advances through observation → problem → response → result → consequence across the passage and sections. Object → operation → consequence can explain a method and question → evidence → interpretation can explain a result within that wider progression. Adapt the form to the genre without requiring all five moves in every paragraph. A physical application may need its setting and governing process first. A theoretical passage may need definitions and assumptions.

A closing sentence should add an implication or finish the explanation. Remove one that only repeats that the result matters. Keep qualifications where they change interpretation, consolidating repeated caveats only when the local claim remains accurate. Do not replace an empty conclusion with a stock disclaimer or force every paragraph to end positively.

## Integrate equations and technical operations

Introduce the object's purpose, present the expression, define new notation, and explain the consequence needed by the argument. Read punctuation across displayed mathematics as part of the sentence. A useful explanation may identify a sign, limit, invariant, scaling, or operational role; translating every symbol into words usually adds little.

Preserve equation environments, labels, assumptions, index sets, normalisation, units, and boundary cases during language edits. A proposed algebraic simplification also has to transform stabilisers and other additive terms consistently. If mathematical equivalence is uncertain, flag it separately rather than treating a changed expression as a wording repair.

Explain what a numerical constant controls or prevents when needed for interpretation. Distinguish a documented tuning result from an engineering choice or numerical safeguard; do not invent a rationale. For physical balances, identify source, sink, storage, transport, and sign conventions where relevant.

Use verbs that name the documented operation, such as projects, averages, estimates, constrains, or compares. A metaphor can motivate an idea but cannot replace a technical definition. Replace an abstract phrase only when its concrete meaning is recoverable; otherwise ask an author query.

## Preserve evidence and voice

State supported results positively, precisely and confidently, preserving all numerical values and scientific distinctions. Remove unnecessary hedges and repeated caveats while retaining calibrated uncertainty and every qualification that determines scientific meaning. Keep the essential comparator, conditions and numerical uncertainty beside the affected result. Concentrate broader limitations, scope exclusions and unresolved issues neutrally in the appropriate Discussion or Scope section. Each local statement must remain accurate on its own. Never invent superiority, causality or statistical significance for a more fluent narrative.

Keep effect, comparator, population, conditions, and uncertainty aligned. “Positive point estimates” does not mean “significant improvements”. An interval for a difference that includes zero leaves its direction unresolved under that analysis; it does not establish equivalence or no effect. Do not change a mean to a median or a group summary to a pooled result for fluency.

Lead with the strongest supported finding and retain a material adverse result or trade-off. Distinguish theoretical guarantees from empirical outcomes and association from causation. These are scientific choices; verify them against supplied evidence or flag the ambiguity while finishing routine language repairs.

Use concrete subjects and precise verbs. First-person plural can make author choices clear when it fits the established voice. Passive voice can keep the scientific object in focus. Retain the author's effective voice while applying the requested argument progression. Bridge phrases should name a real link rather than become mandatory sentence openings.

Review promotional language and generic endings for their function. “Shows great promise” can become a specific supported consequence or be removed if redundant. A request to remove “AI slop” calls for clearer reasoning, referents, and language, not authorship detection. Honour an explicit user or project list of words to avoid while preserving protected text and technical meaning. Such a preference is separate from a general test of readability; legitimate technical terms are not inherently evidence of poor prose.

## Mechanical and contextual reading

Check ordinary grammar as well as specialist terminology: duplicated words, possessives, agreement, misplaced commas, spelling, and awkward constructions. Protect symbols, citation keys, official names, code, and quoted text from automatic replacements. Follow the established English variety and legitimate variants within it; consistency does not make every alternative spelling incorrect.

After mechanical checks, read the revised passage naturally with its neighbours, including prose around equations and figures. Verify premise, explanation, evidence, and interpretation. For larger work, also read section openings and closings. A successful build, regex scan, or numerical check does not establish coherent prose.

## Constructed editing examples

These examples illustrate decisions, not findings about a real method. Use a proposed wording only when the supplied evidence supports its operation and claim.

**A missing relationship.** “Boundary conditions are specified. The solver is iterative. Constraints remain satisfied.” If each update excludes fixed boundary coordinates, a connected explanation is: “The solver updates only unconstrained coordinates. Coordinates fixed by the boundary conditions are excluded from every update and therefore retain their prescribed values.” This establishes the stated boundary property, not every possible constraint.

**An ambiguous referent.** “The encoder feeds a classifier. It is trained with a margin loss.” If only the classifier receives the objective, write “The encoder feeds a classifier, which is trained with a margin loss.” If training is joint, name both objects. Grammar alone cannot choose between these meanings.

**A local repair.** “The final optimisation objective finally combines both terms” can become “The optimisation objective combines both terms.” The edit removes repetition without adding a mechanism, changing the equation, or rewriting the paragraph.

**Interpreting an equation.** For `L(theta) = mean_i r_i(theta)^2 + lambda * ||theta||^2`, explain that the objective combines mean squared residual error with a parameter-magnitude penalty and that `lambda` controls its relative contribution. Do not infer generalisation or an optimal coefficient from the expression alone.

**Retaining uncertainty.** If all point estimates favour a method but one difference interval contains zero, replace “All settings show significant improvement” with “Point estimates favour the method at every setting, while the difference at the smallest setting remains unresolved.” Retain the interval convention and comparator in nearby context.

## Conditional Earth-science terminology

For weather and climate prose, check spatial and temporal scales, sign conventions, flux directions, and distinctions among forcing, feedback, adjustment, response, and sensitivity. Separate observational, dynamical, thermodynamic, and radiative arguments. Define averages, anomalies, reference periods, and boundary conditions.

When several clocks appear, distinguish issue time, target interval, nominal forecast lead, observation age, and model forecast age. Keep the terminology consistent in Methods, captions, and the abstract. At first use of a skill score or decision-value curve, name its reference, zero level, and direction of improvement. These domain checks are unnecessary in an unrelated passage.
