# Claude Code Brief — MCD-01B-08A: Ratify DR-01 and Promote

Work on the existing branch `claude/mcd-01b-08a-ratification-review`
(base off its current tip, commit `9935838`). Do not branch from main.

Modify **MCD-01B-08A.md only**. Do not modify MCD-01A, MCD-01B-01
through MCD-01B-08, MCD-01B-08B, or MCD-04.

---

## Context

You correctly identified that DR-01 was never addressed by the
ratification-review report or the prior apply-and-promote pass, and
correctly withheld promotion rather than self-ratify it or promote
past it. DR-01 is now ratified in full by Nazmil Ghany (29 Jul 2026).
Apply it, then re-run the promotion gate.

---

## 1. Ratify DR-01(a) — Document classification: Product Specification

Update DR-01's status language to "confirmed by Nazmil Ghany, 29 Jul
2026." Preserve the existing reasoning; append this ratified
confirmation:

MCD-01B-08A defines a complete, orderable product variant that
inherits its base blind technology from MCD-01B-07, uses the
Side-Guide Window-Mounted Construction Group defined in MCD-01B-08,
and adds the product-specific configuration, capability, survey, and
validation rules required for ordering. It is therefore not merely a
generic Construction Group document or a supplier capability record.
This is consistent with the established relationship used by the
existing product specifications.

## 2. Ratify DR-01(b) — Application-context classification: Configuration/Survey-Validation field

Append this ratified confirmation to the same entry:

Application contexts (standard window; bi-fold door; patio door;
tilt-and-turn window) must not be treated as Product Families or
Construction Groups. Changing the opening type does not change the
blind's core manufacturing or assembly route — the same product and
Side-Guide construction remain in use. The application context is
necessary for obstruction checks, opening/closing clearances, handle
compatibility, movement validation, suitability warnings, and
installation-route checks, and therefore belongs in the Survey and
Validation layer. This aligns MCD-01B-08A with the already-ratified
treatment in MCD-01B-08B (its own DR-03, ratified 26 Jul 2026).

Check §2/§3 and any classification content in the document for
consistency with this ratified distinction, matching the pattern
already applied to MCD-01B-08B in its own DR-03 correction pass.

## 3. Ratify DR-01(c) — UI sequencing: Ordering Supplier after Blind Technology

Append this ratified confirmation to the same entry:

Ordering Supplier appears after Blind Technology and before
supplier-dependent selections, following the existing MCD-01A
hierarchy (Product Family → Construction/System → Supplier System →
Collection → Material/Fabric → Colourway → Configuration →
Accessories). For this product, the advisor-facing sequence is:
Blind Technology → Ordering Supplier → Collection/Fabric → Colourway
→ Configuration → Accessories. This does not amend or create an
exception to MCD-01A — it applies the already-ratified hierarchy. The
supplier choice must occur before any option whose availability
depends on that supplier, including fabric or cellular collection,
colourway, operating configuration, profile or hardware options,
permitted dimensions, and accessories.

Confirm §12's existing proposed flow already reflects this ordering;
if it does not, correct it to match.

## 4. Correct the Version History gap

The document's own v0.1 Version History entry under-reported its
Decision Register — it named only DR-06, DR-07, DR-12, and DR-13 as
pending judgment calls, omitting DR-01. Correct this so the Version
History accurately represents what the original document actually
contained. Do not rewrite the v0.1 entry's substance — add a
corrective note (or amend the specific listing of pending items) so a
future reader does not repeat the same miscount that delayed this
promotion.

## 5. Confirm DR-06, DR-07, DR-12, DR-13 remain applied as previously ratified

No changes needed to these — confirm they still read exactly as
applied in commit `9935838`. Do not re-open or re-word them.

Note explicitly for the promotion decision: **DR-07 remaining an
expressly documented evidence limitation does not block promotion**,
provided the specification preserves the conservative restriction and
does not present the alternative measurement route as verified. This
was true at the prior commit and remains true now — DR-01 was the only
blocker.

## 6. Re-run verification and promotion gate

Run the full supplier-neutrality, protected-document, and repository
checks again (not just for the DR-01 additions — the whole document).

Review the complete Decision Register once more. Confirm every entry
is now either resolved/ratified or is a genuine supplier-data gap or
confirmed-treatment-of-an-open-supplier-question (DR-07's case) — not
an unresolved architectural or business decision. If, after this
review, no such blocker remains: promote. Update Status from "Working
Draft — Unverified" to "Approved Draft Baseline – Product
Specification", set Version to **1.0**, and add a version-history
entry naming the remaining open items by content (the same list
already prepared in commit `9935838`'s version-history entry, since
that content remains accurate — DR-07's underlying supplier question,
motorisation evidence gap, and the other Open Evidence Items).

If any other genuine blocker is found during this final review that
was not previously identified: do not promote. Report exactly what it
is instead, the same way DR-01 was reported rather than silently
worked around.

## Verification

* Confirm DR-01 reads "confirmed by Nazmil Ghany, 29 Jul 2026" in full
  (all three parts) and no longer says "pending ratification."
* Confirm the Version History correction is present and accurately
  reflects what the original v0.1 document actually contained.
* Confirm DR-06, DR-07, DR-12, and DR-13 are unchanged from commit
  `9935838`.
* Confirm §12's advisor-facing sequence matches the ratified DR-01(c)
  ordering.
* Confirm no supplier names, trademarks, product names, or codes were
  introduced anywhere in the document.
* Confirm MCD-01A, MCD-01B-01 through MCD-01B-08, MCD-01B-08B, and
  MCD-04 remain byte-for-byte unchanged.
* Confirm the promotion decision (or lack thereof) matches what this
  final Decision Register review actually found.
* Commit and push to the existing branch. Do not open a pull request
  or merge — that remains a manual step.
