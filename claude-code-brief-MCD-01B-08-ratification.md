Update MCD-01B-08.md on branch claude/mcd-01b-08-family-architecture
(base this off the current tip of that branch, commit bfc0927 — do
NOT branch from main).

Do not modify MCD-01A or MCD-01B-01 through MCD-01B-07.

---

## 1. Ratify the three Decision Register entries

Locate each entry below and update its status language from "pending
ratification by Nazmil Ghany" to "confirmed by Nazmil Ghany, 19 Jul
2026." Preserve the existing reasoning in each entry — this is a
ratification-status update, not a rewrite.

**Entry 1 — Construction Groups (§2).** Ratified as concluded: Full-
Frame Bead-Mounted System and Side-Guide Window-Mounted System are two
genuinely distinct Construction Groups. The distinction is structural
and mechanical, not merely configurational — one uses a joined
perimeter frame that contains the blind; the other uses separate
profiles and side guides with the blind tensioned between them.

**Entry 2 — Supplier Capability Engine (§6).** Ratified as concluded:
Configured. The richer role model adds provenance and organisational
granularity, but does not introduce a new kind of runtime capability
decision beyond what the existing engine already resolves. Append the
following as a distinct, clearly-labelled future-watch note within
this same entry (not a new entry — a recorded condition for revisiting
this specific conclusion, not a new open question):

"Future-watch condition: reassess this Configured conclusion only if
a later implementation requires role-dependent fallback or resolution
logic — for example, choosing pricing, technical authority, or
manufacturing responsibility based on missing or alternative
organisational roles. That would be a new engine behaviour. The
present model, as designed in this document, does not require it."

**Entry 3 — Shared Service Profile (§11/§12).** Ratified as concluded:
the full twelve-service profile stands exactly as independently
reasoned in the document, including the Measurement Engine conclusion
that glass-size measurement is a Configured measurement basis rather
than an Extension. No service should be changed merely for
consistency with earlier products — the reasoning in this document
stands on its own merits.

## 2. Final verification sweep — required before any promotion

This step is mandatory and must be completed and pass before Part 3
(promotion) proceeds. Do not promote merely because the three
ratifications above are now recorded.

* Re-run a full, fresh supplier-neutrality sweep across the entire
  document (Decision Register, Open Evidence Items, Version History
  included) — do not rely on the sweep already recorded from the
  prior task; confirm it still holds after these edits.
* Confirm the document contains no Blind-Technology-specific rules and
  no populated supplier capability records, per its own stated scope
  (§ "Scope of This Document").
* Confirm internal consistency: the ratified Construction Group names,
  the Blind Technology axis treatment, and the Shared Service Profile
  conclusions are used consistently throughout the document — no
  section contradicts what the Decision Register now states as
  confirmed.
* Confirm the "Perfect Fit" controlled-reference rule (already
  ratified in the prior task) is still correctly applied throughout —
  this edit pass should not have reintroduced or loosened it.
* Review the full Decision Register end to end. Confirm every entry
  is now either resolved (including the three ratified above) or is a
  genuine open item appropriate for a family architecture document at
  this stage (e.g. the standing MCD-00A missing-dependency note) — not
  an unresolved architectural or business decision. If anything reads
  as an open architectural or business question rather than an
  appropriate open item, flag it clearly and do not promote — report
  exactly what's blocking promotion instead.
* Confirm MCD-01A and MCD-01B-01 through MCD-01B-07 remain unmodified.

## 3. Promotion — only if Part 2's verification passes

If the Part 2 sweep finds no blocking issue: update Status from
"Working Draft — Unverified" to "Approved Draft Baseline – Product
Specification" (noting this document's type is Family Architecture
Document, not a full Product Specification — retain that distinction
in the Status/Document Type lines as already established), set
Version to 1.0, and add a version-history entry naming the remaining
open items by content (the MCD-00A dependency note, and the deferred-
by-design absence of Blind-Technology-specific rules and populated
supplier records, which are not gaps in this document but its
intended scope).

If Part 2's verification finds a blocking issue: do not change the
Status line. Report exactly what's blocking promotion instead.

## Verification

* Confirm all three ratified entries read "confirmed by Nazmil Ghany,
  19 Jul 2026" and no longer say "pending ratification."
* Confirm the Supplier Capability Engine entry's future-watch condition
  is present, clearly labelled as a reassessment trigger (not a new
  open question), and worded as given above.
* Confirm the promotion decision (or lack thereof) matches what Part 2's
  sweep actually found.
* Confirm no supplier names, trademarks, product names, or part
  numbers were introduced anywhere in the document during this task.
* Confirm MCD-01A and MCD-01B-01 through MCD-01B-07 remain unmodified.
* Commit and push to the existing branch. Do not open a pull request
  or merge — that remains a manual step.
