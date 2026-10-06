# Abstracts and conclusions

For abbreviation definitions across the abstract, introduction, and conclusion, follow [prose style](prose-style.md#connect-sentences-through-meaning).

Make the abstract's argument easy to follow at the requested level of intervention. Adapt its progression to the genre: a theoretical result may need assumptions and a theorem, while an empirical study needs its design, population, finding, and interpretation. Use problem → approach → evidence → implication as a diagnostic when helpful, without forcing a causal claim or a fixed sentence pattern.

Keep abstracts at or below **2,000 characters, including spaces**, as the user's established preference. Also satisfy any stricter current venue constraint; a later explicit user instruction can change this preference. A word count does not replace the character check.

Count the final reader-facing abstract mechanically, including punctuation and displayed mathematical text. Exclude the heading, LaTeX command syntax, and environment delimiters, but include text displayed through command arguments. For plain text, normalise source line wraps and repeated whitespace to single spaces, then use `len(" ".join(abstract.split()))`. Count the intended accepted reading when markup is present and recount after further edits. Use the venue's counting convention too when it differs. Preserve claims, conditions, and definitions when shortening.

When both are in scope, compare the abstract's conclusion with the concluding section. Their principal claim, certainty, and scope should agree, including material assumptions and limitations. Repeat phrasing exactly only when the user requests it; otherwise let each section serve its own purpose. End with the strongest supported implication or boundary; a negative or unresolved finding can be consequential. Remove generic praise and empty future-work endings, while retaining a specific open question when it follows from the evidence and fits the requested structure.
