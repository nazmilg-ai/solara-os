Update MCD-01B-04.md and MCD-01B-05.md, on branch
claude/mcd-01b-04-05-final-review (base this off the current tip of
that branch, commit d395a32 — do NOT branch from main; that branch
does not contain these documents, as established in the prior task on
this same branch).

Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, MCD-01B-03, or MCD-04.

---

## 1. Ratify MCD-01B-04's reference-implementation-role Decision Register entry

Locate the Decision Register entry in MCD-01B-04.md for the
Venetian-family reference-implementation role (the one still marked
"pending ratification by Nazmil Ghany"). Update it to reflect explicit
ratification, using this reasoning verbatim as the ratified content
(replacing or supplementing the existing reasoning — preserve the
existing reasoning as prior analysis if useful, but the entry must now
read as confirmed, not proposed):

Decision: Wooden Venetian Blinds are the Venetian-family reference
implementation.

Reasoning: Wooden Venetian provides the most complete reusable
Venetian configuration model — slat size; ladder cord and decorative
tape; tilt and lift controls; control-side arrangements; valance
treatment; stack height; alignment across multiple blinds; manual,
tilt-only and tilt-and-lift motorisation; bracket and accessory rules;
dimensional capability matrices; child-safety handling. Faux Wood and
Metal Venetian specifications inherit applicable shared concepts and
explicitly document their material, construction and operation
differences. Reference status is architectural only and does not
establish commercial priority or universal capability.

Raised By: confirmed by Nazmil Ghany, 16 Jul 2026.

## 2. Promote MCD-01B-04

With both Decision Register entries now ratified (the Shared Service
Profile reasoning, ratified in the prior task on this branch, and the
reference-implementation role, ratified in step 1 above), confirm no
other entry remains an open architectural or business-decision
question — only genuine supplier-data gaps and the standing MCD-00A
note should remain. If that holds, promote: update Status from
"Working Draft — Unverified" to "Approved Draft Baseline – Product
Specification", set Version to 1.1, and add a version-history entry
naming the remaining open items by content (matching the standard set
by MCD-01B-05's own promotion entry from the prior task).

## 3. Fix MCD-01B-05's now-stale Reference Document note

MCD-01B-05.md's header currently states that MCD-01B-04 is "Working
Draft — Unverified as of this promotion; its Venetian-family
reference-implementation role remains a proposal pending ratification
— that single unratified business decision is why MCD-01B-04 was not
promoted alongside this document." This is now inaccurate once step 2
promotes MCD-01B-04. Update this line to accurately reflect
MCD-01B-04's new status (Approved Draft Baseline, reference role
ratified). Add a short version-history entry to MCD-01B-05.md noting
this correction, since it's a factual update to an already-promoted
document, not a new promotion.

## Verification

* Confirm MCD-01B-04's reference-implementation-role entry reads
  "confirmed by Nazmil Ghany, 16 Jul 2026" and no longer says "pending
  ratification."
* Confirm MCD-01B-04's Status line reads "Approved Draft Baseline –
  Product Specification" and Version reads "1.1" — but only if no
  other open architectural/business item was found in step 2; if one
  was found, do not promote and report exactly what's blocking it
  instead, the same way the prior task withheld promotion.
* Confirm MCD-01B-05's Reference Document line is updated and no
  longer describes MCD-01B-04 as unpromoted, if MCD-01B-04 was in fact
  promoted in step 2.
* Confirm no supplier names, trademarks, or specific colour names were
  introduced anywhere in either document.
* Confirm MCD-01A, MCD-01B-01, MCD-01B-02, MCD-01B-03, and MCD-04
  remain unmodified.
* Commit and push to the existing branch. Do not open a pull request
  or merge — that remains a manual step.
