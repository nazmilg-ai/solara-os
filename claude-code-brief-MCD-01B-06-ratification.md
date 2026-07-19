Update MCD-01B-06.md on branch claude/mcd-01b-06-metal-venetian
(base this off the current tip of that branch, commit d5ad78d — do
NOT branch from main, which does not contain this document).

Do not modify MCD-01A, MCD-01B-01 through MCD-01B-05, or MCD-04.

---

## 1. Ratify the four Decision Register entries

Locate each of the following entries in MCD-01B-06.md's Decision
Register and update their "Raised By" / status language from "pending
ratification by Nazmil Ghany" (or equivalent) to "confirmed by Nazmil
Ghany, 16 Jul 2026." Preserve the existing reasoning in each entry —
this is a ratification-status update, not a rewrite. Where useful,
append the additional reasoning below as supporting confirmation
alongside the existing analysis, the same way MCD-01B-04's
reference-implementation-role entry preserved its prior analysis
when ratified.

**Entry 1 — Slat-size grouping (Required Classification Question 1):**
Ratified as concluded: Narrow-Slat (Wand) and Wide-Slat (Cord) are
separate Construction Variants, with slat size as Configuration within
each variant. Supporting reasoning: selecting the group changes
several linked physical characteristics at once — tilt mechanism,
headrail profile and dimensions, bracket system, control arrangement,
dimensional limits, and motorisation eligibility. The advisor is not
independently choosing wand or cord; the mechanism is inherent to the
construction selected through the slat family. Treating this as one
construction would force too many hidden dependencies into ordinary
configuration logic.

**Entry 2 — Specialist construction classifications (Required
Classification Question 2):** Ratified as concluded for all five:
Side Guide Tilt, Side Guide Roof, Partition, and Double Glazing as
Construction Variants; Mixed Colours as Configuration/Colourway.
Supporting reasoning: the four specialist systems are not ordinary
accessories added to a standard blind — Side Guide Tilt changes how
the blind is retained and operated on an inclined opening; Side Guide
Roof uses a guide-wire system intended to hold the blind at a
significantly greater angle; Partition replaces the normal operating
arrangement with a flexible, usually tilt-only mechanism; Double
Glazing uses a torsion rod and Bowden cable and is designed as an
enclosed-glazing system. Each changes the physical build, operating
method, installation context, or available functionality, and should
therefore generate distinct manufacturing and validation paths. Mixed
Colours does not alter the mechanism or installation system, so
Configuration/Colourway is correct.

**Entry 3 — Shared Service Profile (Motor Engine and Supplier
Capability Engine):** Ratified as concluded: both Configured, not
Extended. Supporting reasoning: the platform already supports
operation eligibility, supplier and construction filtering, supported
versus prohibited motorisation, and quoting disabled where technical
data is insufficient — the Metal Venetian evidence creates new data
combinations, not a new kind of Motor Engine behaviour. The existing
Supplier Capability model can already represent supplier and range,
Construction Variant, slat-size eligibility, reseller route,
unresolved identity, evidence status, and technical restrictions — the
records are more detailed than prior products, but do not require a
fundamentally new platform capability.

**Entry 4 — Motorisation asymmetry policy:** Ratified as concluded:
the fully-evidenced supplier route may be quoted only within its
verified construction and dimensional limits; the category-level-only
route remains unavailable for quoting until slat-size-specific
technical evidence is obtained. Supporting reasoning: category-level
confirmation proves that motorised Venetian blinds exist in that
supplier's range, but does not establish eligible slat sizes,
compatible Construction Variants, operation mode, motor type, power
supply, minimum or maximum dimensions, or weight limits — enabling
quoting on that basis would require assumptions, which conflicts with
the project's core rule against inventing unevidenced capability.

## 2. Final open-item check

Review the full Decision Register. Confirm every entry is now either
resolved (including the four ratified above) or is a genuine
supplier-data gap — not an unresolved architectural or business
decision. Expected remaining open items are supplier-data gaps only:
real dimensional envelopes and exact slat-size thresholds per
Construction Variant; the category-level-only route's motor model,
torque, and slat-size eligibility; the second sibling collection's
identity; supplier, collection, and source-document identity for the
whole product family; and the standing MCD-00A dependency note. If
anything else reads as an open architectural or business question,
flag it clearly and do not promote — report exactly what's blocking
promotion instead, the same way MCD-01B-04's first ratification pass
correctly withheld promotion pending a second unratified entry.

## 3. Promotion

If the check in Part 2 confirms no other open architectural/business
item remains: update Status from "Working Draft — Unverified" to
"Approved Draft Baseline – Product Specification", set Version to 1.1,
and add a version-history entry naming the remaining open items by
content (matching the standard set by MCD-01B-04 and MCD-01B-05's own
promotion entries) — not just "see Decision Register."

## Verification

* Confirm all four ratified entries read "confirmed by Nazmil Ghany,
  16 Jul 2026" and no longer say "pending ratification."
* Confirm the promotion decision matches what Part 2's check actually
  found — do not promote if any non-data-gap item remains open.
* Confirm no supplier names, trademarks, part numbers, or specific
  collection/colour names were introduced anywhere in the document.
* Confirm MCD-01A, MCD-01B-01 through MCD-01B-05, and MCD-04 remain
  unmodified.
* Commit and push to the existing branch. Do not open a pull request
  or merge — that remains a manual step.
