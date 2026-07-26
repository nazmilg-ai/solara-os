Update MCD-04.md only. Do not modify MCD-01B-08A.md, MCD-01A, or
MCD-01B-01 through MCD-01B-08. This is a supplier-record evidence
enrichment task, not a new product-specification work package — no
status promotion, no merge, no architectural change.

Work on a new branch from current main
(e.g. claude/mcd-04-side-guide-pleated-cellular-enrichment).

---

## Scope

Update only the existing §7.15 supplier-capability record for the
Pleated/Cellular side-guide window-mounted system (the record created
alongside MCD-01B-08A). Replace "Not Provided" or "Supplier
Confirmation Required" fields only where the two source documents
below now provide direct evidence. Do not touch any other MCD-04
section, and do not touch MCD-01B-08A.md at all — every fact below is
supplier-specific detail that belongs in MCD-04 only, consistent with
MCD-01B-08A's own established supplier-neutrality boundary.

Source documents (cite the exact filename against every fact added):

* `SPEC70 Cruze Pleated Cellular Specification - Issue V7 - 17.06.2026.pdf`
* `MEAS005 - Cruze Pleated Cellular FITtoFRAME Measuring Instructions - Issue V2 - 02.07.2025 (1).pdf`

---

## Confirmed fields to add

From SPEC70:

* Cellular cell size: 25mm.
* Pleated pleat size: 20mm.
* Manufacturing tolerance: ±3mm width and drop.
* Recess width deduction: 10mm (note: the source states this for
  width specifically — do not assume an equivalent drop deduction
  unless the source states one separately; if none is stated, record
  drop deduction as Not Provided rather than assuming it matches).
* Installation/fixing routes: CZP09 = beading brackets connecting into
  the side guide; CZP10 = high-strength adhesive tape affixing the
  side guide to the window.
* Bracket/component codes: CZP106, CZP107 (beading brackets, window-
  bead mounting); CZP109, CZP110 (side guide brackets, window-bead
  mounting); CZP124, CZP125 (side guide brackets, taped mounting);
  CZP108 (side guide clip, as required).
* Standard control handle codes: CZP128 (white), CZP129 (black), CZP130
  (anthracite), CZP131 (clear).
* Folding handle code: CZP151 (clear), recorded as an additional
  surcharge item, distinct from the standard handle codes.
* Handle quantity rule: one handle per moving profile up to 1,200mm
  width; two handles above 1,200mm width.
* End-cap codes (FITtoFRAME-specific): CZP033 (white), CZP034
  (anthracite), CZP035 (black), CZP036 (grey), CZP037 (nobel).
* Profile/end-cap/handle colour-matching rules, as given in the source
  (e.g. White profile → White end cap → White handle; Anthracite →
  Anthracite → Anthracite; Grey/Nobel → Grey/Nobel end cap → Clear
  handle; Black → Black → Black).
* Anthracite colour reference: RAL7016.
* Nobel colour reference: RAL7022.
* Bowery fabric exclusion — re-confirm with the exact source wording
  ("Not available with Bowery fabric"), citing SPEC70 directly, since
  this exclusion was already recorded but should now carry a precise
  source citation rather than a general one.

From MEAS005 V2 (confirms, does not add new facts beyond what's
already recorded from the design brief — cite it as the confirming
source for the following, since it independently corroborates the
same figures from a second document):

* Visible glass measurement method (three-point width and drop,
  smallest-of-three, excluding beading/rubber seals).
* Minimum/maximum dimensions and the linked width/drop restriction
  (1,500mm width available only up to 2,000mm drop; 2,300mm drop
  available only up to 1,300mm width).
* 35mm handle clearance from the depth of the window glass.
* The 2mm square-frame rubber-bead-protrusion rule, confirmed with
  matching wording.

## Fields that must remain open — do not resolve them

* Motorisation — no mention found in either source document for this
  construction; keep as Not Provided.
* Chamfered-bead eligibility — not addressed in either source; keep
  as Supplier Confirmation Required.
* Ovolo/curved-bead eligibility — not addressed in either source; keep
  as Supplier Confirmation Required.
* Maximum acceptable gasket thickness or projection, or any rule
  beyond the confirmed minimum 2mm gasket protrusion — not addressed;
  keep open.
* The second, differently-titled measuring-instructions document
  ("MEAS005 - Cruze FITtoFRAME Measuring Instructions - Issue V4 -
  06.05.2026.pdf", originally flagged in the MCD-01B-08A design brief
  as possibly applicable to this work package or possibly Aluminium-
  Venetian-specific) must be recorded as:

  "Not located in the available SharePoint source library after
  repeated targeted searches."

  Do not describe it merely as inaccessible, and do not infer its
  contents from SPEC70, MEAS005 V2, or any other similarly named
  document. Its applicability to this construction, or to a future
  Aluminium Venetian work package, remains genuinely unresolved.

Do not resolve any Decision Register entry, Open Evidence Item, or
judgment call in MCD-01B-08A.md as a result of this task — this task
only enriches the MCD-04 supplier record. If any of MCD-01B-08A.md's
existing Open Evidence Items are now factually resolved by this new
evidence (e.g. items that were phrased as needing exactly this kind of
supplier data), do not edit MCD-01B-08A.md to close them — flag this
in your report instead, so a separate, explicit follow-up can update
the product specification's own Decision Register deliberately, rather
than have it change as a side effect of an MCD-04-only task.

---

## Required report

Report explicitly:

* The exact MCD-04 file section changed (confirm it is §7.15 only).
* Every field replaced, with its new value and source citation.
* Every field left unresolved, with its recorded status (Not
  Provided / Supplier Confirmation Required / the specific "not
  located" wording for the V4 document).
* Source provenance confirmed for each new fact — confirm no fact was
  added without a named source document.
* Verification that MCD-01B-08A.md and all other MCD documents (MCD-
  01A, MCD-01B-01 through MCD-01B-08) are byte-for-byte unchanged.
* Branch name and commit hash.
* Any MCD-01B-08A.md Open Evidence Item that this new evidence now
  factually resolves, flagged for separate follow-up rather than
  edited directly.

Commit and push to the new branch. Do not open a pull request or
merge.
