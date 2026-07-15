Create a new branch from main: claude/mcd-01b-04-05-final-review

Read before writing:
* MCD-01A_v1.5_for_Claude_Code.md
* MCD-01B-01.md, MCD-01B-02.md, MCD-01B-03.md (promotion precedent)
* MCD-01B-04.md, MCD-01B-05.md (the documents under review)
* MCD-04.md

Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, MCD-01B-03, or MCD-04 in this task.

---

## Objective

Perform the final consistency review of MCD-01B-04 and MCD-01B-05, matching the review standard used before MCD-01B-03 (Roman) was promoted to Approved Draft Baseline, then make a promotion decision for each.

## 1. Update the two ratified Decision Register entries

Two judgment calls in each document's Shared Service Profile reasoning are now explicitly ratified by Nazmil Ghany (15 Jul 2026):

1. Motor Engine — unsupported/unverified motorisation remains Configured, with quoting disabled by a data-availability gate, not Restricted.
2. Validation Engine and Supplier Capability Engine — colour-specific size/heat/availability/motor rules remain Configured (deeper parameterisation of an existing hierarchical lookup), not Extended.

Locate the corresponding Decision Register entries in both MCD-01B-04.md and MCD-01B-05.md (the entries reasoning through the Shared Service Profile) and update their "Raised By" / status language from "pending ratification by Nazmil Ghany" (or equivalent) to "confirmed by Nazmil Ghany, 15 Jul 2026." Do not alter the reasoning text itself — this is a ratification-status update only.

## 2. Full Decision Register review, both documents

Confirm every Decision Register entry in both documents is either resolved or is a genuine supplier-data gap — not an unresolved architectural or business-decision question. If anything reads as an open architectural or business question rather than a data gap, flag it clearly rather than resolving or hiding it.

## 3. Reconcile against MCD-04's current content

Check both documents' Open Data Items / open-item sections against what MCD-04 actually contains right now (read MCD-04.md fresh, do not assume). Where MCD-04 already has a confirmed record that resolves an item currently marked open in either document (e.g. the Embassy/Forestwood colour governance in MCD-04 §7.9), update the reference to point at the MCD-04 record rather than leaving it as an unresolved open item. Where MCD-04 explicitly marks something "Evidence gathered — Independent verification pending" (e.g. §7.10's Arena Sherwood/Expressions, Home Creations motor compatibility), keep the corresponding item in MCD-01B-04/05 marked open — do not treat "evidence gathered" as equivalent to "confirmed."

## 4. Readiness assessment, each document independently

Assess whether MCD-01B-04 and MCD-01B-05 are each ready for "Approved Draft Baseline – Product Specification" status, matching the standard MCD-01B-01/02/03 all reached — remaining supplier-data gaps are not a blocker, provided no architectural or business-decision item remains open. Assess each document on its own; one may be ready while the other is not.

## 5. Promotion

For each document that is ready: update the Status line from "Working Draft — Unverified" to "Approved Draft Baseline – Product Specification", set the version appropriately (both are currently at 1.0 (pre-review) — promote to 1.1), and add a version-history entry that explicitly names the remaining open items by content, not just "see Decision Register" — matching the standard set by MCD-01B-01's B5 and MCD-01B-02/03's promotion entries.

For any document not ready: do not change its Status line. Report exactly what's blocking promotion instead.

If MCD-01B-05 is promoted, confirm its "Reference Document: MCD-01B-04" line accurately reflects MCD-01B-04's actual status at the time (Approved Draft Baseline if promoted alongside it, or still Working Draft if MCD-01B-04 was not ready).

## Verification

* Confirm both ratified Decision Register entries now read "confirmed by Nazmil Ghany, 15 Jul 2026" in both documents.
* Confirm no supplier names, trademarks, or specific colour names were introduced during this task — full sweep, both documents.
* Confirm MCD-04 references are accurate to MCD-04's actual current content, spot-checked directly against the file, not assumed.
* Confirm MCD-01A, MCD-01B-01, MCD-01B-02, MCD-01B-03, and MCD-04 remain unmodified.
* Commit and push to the new branch. Do not open a pull request or merge — that's a manual step after review.
