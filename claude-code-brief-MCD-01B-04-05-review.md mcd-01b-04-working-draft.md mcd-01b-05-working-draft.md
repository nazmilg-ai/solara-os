Update MCD-01B-05.md only, on branch claude/mcd-01b-04-05-venetian-review.
Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, MCD-01B-03, or MCD-04.

This corrects two things left over from the previous pass on this branch.

## 1. §49 still names a supplier

The Open supplier-data items section currently includes "Beverley Home
Creations motor compatibility" as a list item. This is the same
category of supplier-neutrality violation as the removed §41 — just
smaller. Replace it with a generic item:

"unconfirmed supplier-range motor compatibility"

Do not name any supplier anywhere in this list. If any other item in
this section names a supplier, range, or specific product, generalise
it the same way.

## 2. §41 must be fully deleted, not left as a marked placeholder

If the previous pass left §41 present with an inline marker (e.g.
"[SUPPLIER-NEUTRALITY VIOLATION]" or similar bracketed annotation)
rather than actually removing the section, delete the entire section
now, including the marker text itself. The reference working-draft
file (mcd-01b-05-working-draft.md) intentionally kept that marker
visible for your reference during the redraft — it was never meant to
survive into MCD-01B-05.md itself. Renumber all subsequent sections
so the document has no gap and no leftover annotation.

## 3. Confirm Part 1 (MCD-01B-04) received equivalent treatment

Before this branch is considered ready for the next stage, confirm
MCD-01B-04.md has the same rigor already applied to MCD-01B-05.md:
Decision Register with real Shared Service Profile reasoning (not a
provisional table), Version History, no self-declared approval
sections, and a full supplier-name sweep. If any of this is
incomplete for MCD-01B-04.md, complete it now using the same standard
already applied to MCD-01B-05.md in the prior pass on this branch.

## Verification

- Confirm zero supplier names, trademarks, or specific colour names
  appear anywhere in MCD-01B-05.md — full sweep including §49 and any
  section not explicitly named above (grep for Beverley, Home
  Creations, Embassy, Forestwood, Decora, Arena, Somfy, and the twelve
  colour names from the original violation).
- Confirm the same sweep on MCD-01B-04.md.
- Confirm no bracketed violation-marker text remains anywhere in
  MCD-01B-05.md.
- Confirm section numbering in MCD-01B-05.md is continuous with no
  gap where §41 was removed.
- Confirm both documents have a complete Decision Register (with
  documented Shared Service Profile reasoning, not a provisional
  table) and Version History.
- Confirm neither document's Status line claims Approved Draft
  Baseline — both remain Working Draft — Unverified pending explicit
  ratification.
- Report a diff summary.
- Commit and push to the existing branch. Do not open a pull request
  or merge.
