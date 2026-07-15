Update MCD-01B-03.md only, on branch claude/mcd-01b-03-final-review.
Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, or MCD-04.

This document has three stale cross-references: "Open Evidence Items,
§26" appears in three places, but Open Evidence Items is actually §25
— §26 is Version History. This is the same category of defect as the
§19/§23 cross-reference issue found and fixed in MCD-01B-02 earlier in
this project: a reference that was correct when written became stale
after later sections were renumbered, and survived because a
narrowly-scoped review (this document's own §9/§25 reconciliation)
only touched the sections in its own scope, not a full-document sweep.

Fix these three exact locations — change "§26" to "§25" in each,
changing nothing else on the line:


Near §7 (Survey Requirements) / §8, the sentence beginning "Not
yet specified: whether Breakaway Control is offered on No-Drill —
needs Supplier Capability confirmation (see Open Evidence Items,
§26)."
Within §13 (Motor Implementation), the sentence "Defaults to
Manual per §4.2. No dedicated motor family is assigned unless a
future Supplier Capability record confirms motorised No-Drill
eligibility (not assumed either way — see Open Evidence Items,
§26)."
Within §17 (Child Safety), the sentence "The exact chain formula
and safety device mapping come from Supplier Capability and the
Child Safety Engine (Open Evidence Items, §26)."


After making these three corrections, run a full-text search for
"§26" across the whole document and confirm the only remaining
occurrences correctly refer to Version History (the "## 26. Version
History" heading itself, and any reference that is actually about
version history, not Open Evidence Items). Report what you find.

Also run a full-text search for "§25" and confirm every occurrence
now correctly refers to Open Evidence Items.

Add a version-history entry (still v1.1 — this is a correction, not a
new promotion) noting: "Corrected three stale §26 cross-references to
§25 (Open Evidence Items) — found during independent review after the
final-review reconciliation pass, which only touched §9/§25 directly
and did not sweep the rest of the document for the same defect."

Commit and push to the existing branch. Do not open a pull request or
merge.
