Create a new branch from main: claude/mcd-01b-03-final-review

Read before writing:


MCD-01A_v1.5_for_Claude_Code.md
MCD-01B-01.md (Roller — precedent for reaching Approved Draft Baseline)
MCD-01B-02.md (Vertical — precedent for reaching Approved Draft Baseline)
MCD-01B-03.md (Roman — the document under review)
MCD-04.md (the populated Roman capability records)


Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, or MCD-04 in this task.


Objective

Perform the final consistency review of MCD-01B-03, matching the
review standard used before MCD-01B-02 (Vertical) was promoted to
Approved Draft Baseline, then make a promotion decision.

1. Reconcile against MCD-04's now-populated Roman records

When MCD-01B-03 was first drafted, several items in §9 (Dimensional
and Area Validation) and the Open Evidence Items section were marked
"not yet specified" because no supplier data existed yet. MCD-04 now
contains real, evidenced Roman capability records. Go through §9 and
the Open Evidence Items section line by line against MCD-04's actual
content and update accordingly:


Items now resolved in MCD-04 (Standard Headrail's dimensional
limits; the chain-length formula, confirmed shared across Standard/
No-Drill/Cassette with Breakaway's distinct formula; rod count and
cord count tables per construction; lining weights for all five
lining types; recess deductions; manufacturing tolerance) should be
updated to reference the specific MCD-04 record rather than say "not
yet specified" — state the fact and point to MCD-04, do not duplicate
the full figures into MCD-01B-03 (which must remain supplier-neutral;
referencing "see MCD-04" is sufficient, consistent with how §18
already handles this).
Items still genuinely absent from MCD-04 (No-Drill and Cassette's
own dimensional limits; face fabric weight/GSM; motor specifications
and load thresholds; a confirmed maximum-area rule; Same Room
tolerances; complete fabric no-join width data; bracket spacing
formulas) must remain marked as open — do not imply they're resolved
just because other items in the same section now are.


This reconciliation is expected to touch §9 and the Open Evidence
Items section; it should not require changes to the Decision Register
entries already ratified by Nazmil Ghany (§3/§4a Breakaway, §7a Same
Room, §2 Configured-vs-Extended) — those are settled and out of scope
for this task.

2. Full Decision Register review

Confirm every Decision Register entry is either resolved or is a
genuine supplier-data gap — not an unresolved architectural or
business-decision question. If anything reads as an open architectural
or business question rather than a data gap, flag it clearly rather
than resolving or hiding it, the same standard applied to MCD-01B-02's
equivalent review.

3. Readiness assessment

Based on the reconciliation and the Decision Register review, assess
whether MCD-01B-03 is ready for the same "Approved Draft Baseline –
Product Specification" status MCD-01B-01 and MCD-01B-02 both reached.
Both reached that status while still carrying honestly-logged open
supplier-data items — remaining data gaps are not a blocker, provided
no architectural or business-decision item remains open.

4. Promotion

If ready: update the Status line from "Draft – Product Specification"
to "Approved Draft Baseline – Product Specification", bump the version
number, and add a version-history entry that explicitly names the
remaining open items by content (not just "see Decision Register" or
"see Open Evidence Items") — the same standard MCD-01B-02's v1.3
promotion entry and MCD-01B-01's B5 both used.

If not ready: do not change the Status line or version. Report exactly
what's blocking promotion instead.

Verification


Confirm §9 and Open Evidence Items accurately reflect MCD-04's
actual current content — spot-check at least three reconciled items
against the real MCD-04 record, not just against this brief's list.
Confirm no supplier names, trademarks, or part numbers were
introduced into MCD-01B-03 during the reconciliation — references to
MCD-04 must stay at "see MCD-04" level, not reproduce supplier
specifics.
Confirm the three already-ratified Decision Register entries are
unchanged.
Confirm MCD-01A, MCD-01B-01, MCD-01B-02, and MCD-04 are unmodified.
Commit and push to the new branch. Do not open a pull request or
merge — that's a manual step after review.
