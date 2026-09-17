Document ID: MCD-00B
Document Title: Solara OS Product Specification Register
Status: Living Document — Updated per change
Last Updated: 17 September 2026

**Purpose:** This is the single source of truth for MCD-01A/MCD-01B document numbers, statuses, and the construction-group hierarchy — it supersedes any prose status report for that purpose. It sits alongside MCD-00/MCD-00A conceptually but, unlike the frozen MCD-00A governance convention, is a live tracking document expected to change every time a document's status, number, or hierarchy position changes.

---

## 1. All MCD-01A/01B Documents

| Document Number | Title | Status | Version | Branch (if not on main) | One-line Description | Reference Implementation? |
|---|---|---|---|---|---|---|
| MCD-01A | Sales MVP Product Engine Architecture | Approved Draft Baseline | 1.5 | — (main) | Platform architecture: three-test classification model, twelve Shared Platform Services, six-status Shared Service Profile, Product Taxonomy | N/A (architecture doc, not a product) |
| MCD-01B-01 | Roller Blinds Product Engine Specification | Approved Draft Baseline – Product Specification | 1.5 | — (main) | Standard/Cassette Roller Blind | **Y** — reference implementation for Standard Blinds generally |
| MCD-01B-02 | Vertical Blinds Product Engine Specification | Approved Draft Baseline – Product Specification | 1.3 | — (main) | Vertical louvre blinds, incl. Curved/Sloping geometry and Vogue motorised-tilt route | N |
| MCD-01B-03 | Roman Blinds Product Specification | Approved Draft Baseline – Product Specification | 1.1 | — (main) | Standard/No-Drill/Cassette/Breakaway Roman constructions | N |
| MCD-01B-04 | Wooden Venetian Blinds Product Specification | Approved Draft Baseline – Product Specification | 1.1 | — (main) | Wooden Venetian Blind | **Y** — ratified reference implementation for the Venetian sub-family |
| MCD-01B-05 | Faux Wood Venetian Blinds Product Specification | Approved Draft Baseline – Product Specification | 1.1 | — (main) | Faux wood/PVC Venetian, referencing MCD-01B-04 | N |
| MCD-01B-06 | Metal Venetian Blinds Product Specification | Approved Draft Baseline – Product Specification | 1.1 | — (main) | Aluminium Venetian, incl. specialist window-fit/guide-mounted constructions | N |
| MCD-01B-07 | Pleated & Cellular Blinds Product Specification | Approved Draft Baseline – Product Specification | 1.1 | — (main) | Free-hanging/tensioned Pleated and Cellular fabric blinds | N |
| MCD-01B-08 | Frame-Mounted and Window-Mounted Blind Systems — Family Architecture | Approved Draft Baseline – Product Specification | 1.0 | — (main) | Family architecture for two Construction Groups (Full-Frame Bead-Mounted System, Side-Guide Window-Mounted System); no populated product content | N/A (family architecture doc, not a product) |
| MCD-01B-08A | Side-Guide Window-Mounted Pleated & Cellular Blind | Approved Draft Baseline – Product Specification | 1.0 | — (main) | Pleated/Cellular under the Side-Guide Window-Mounted Construction Group | N (child of MCD-01B-08) |
| MCD-01B-08B | Side-Guide Window-Mounted Aluminium Venetian Blind | Working Draft — Unverified | 0.2 (research stage — partial ratification, not promoted) | `claude/mcd-01b-08b-side-guide-aluminium-venetian` | Aluminium Venetian under the Side-Guide Window-Mounted Construction Group | N (child of MCD-01B-08) |
| MCD-01B-08C | Full-Frame Bead-Mounted Roller Blind | Approved Draft Baseline – Product Specification | 1.0 | — (main) | Roller under the Full-Frame Bead-Mounted Construction Group | **Y** — ratified reference implementation for the Full-Frame Bead-Mounted Construction Group |
| MCD-01B-08D | Full-Frame Bead-Mounted Pleated & Cellular Blind | Approved Draft Baseline – Product Specification | 1.1 | — (main) | Pleated and Cellular under the Full-Frame Bead-Mounted Construction Group | N (child of MCD-01B-08) |
| MCD-01B-09 | Day & Night Blind | Working Draft — Partially Verified | v0.3 | — (main) | Free-hanging Day & Night (alternating sheer/opaque band) blind, standard family | N |
| MCD-04 | Product Library & Supplier Management | Draft Skeleton | 0.11 | — (main) | Supplier capability library (dimensions, codes, pricing) underlying all product specifications above | N/A (supplier library, not a product spec) |

**Not present anywhere in the repository:** MCD-00 (Executive Charter) and MCD-00A (Project Development Standards) — both are referenced as Dependencies by every document above, but no file for either exists on any branch. Long-standing, universally-acknowledged gap, not new.

---

## 2. Full-Frame Bead-Mounted Construction Group Hierarchy

| Child Product | Document Number | Status |
|---|---|---|
| Roller | MCD-01B-08C | Promoted — Approved Draft Baseline v1.0 (reference implementation) |
| Day & Night | Not yet established | Not started |
| Pleated | MCD-01B-08D | Promoted — Approved Draft Baseline v1.1 (Pleated and Cellular covered together in one document) |
| Cellular | MCD-01B-08D | Promoted — Approved Draft Baseline v1.1 (Pleated and Cellular covered together in one document) |
| Aluminium Venetian | Not yet established | Not started |
| Wooden Venetian | Not yet established | Not started |
| Lite Shutters | Not yet established | Not started |

---

## 3. Side-Guide Window-Mounted Construction Group Hierarchy

| Child Product | Document Number | Status |
|---|---|---|
| Pleated & Cellular | MCD-01B-08A | Promoted — Approved Draft Baseline v1.0 |
| Aluminium Venetian | MCD-01B-08B | Working Draft — Unverified, v0.2 (research stage — partial ratification, not promoted); on branch `claude/mcd-01b-08b-side-guide-aluminium-venetian`, not on main; no PR ever opened |

No other Side-Guide Window-Mounted children are currently planned or referenced anywhere in the repository — MCD-01B-08's own Blind-Technology routing table names only these two as the confirmed constructions for this group.

---

## 4. Cross-Document Open Items

| Item | Documents Affected | Status |
|---|---|---|
| Fixing-hole trigger stated by width (not drop) for one construction, versus the drop-trigger convention confirmed elsewhere in the Full-Frame Bead-Mounted family | MCD-01B-08C and MCD-01B-08D (both confirm the drop-trigger convention for their own constructions); the not-yet-drafted Aluminium Venetian child of that same Construction Group (source of the width-trigger discrepancy) | Open — carried forward in MCD-01B-08C's and MCD-01B-08D's Open Evidence Items, not resolved |
| Blackout-fabric availability for Day & Night: MCD-04 §7.20 logged this as "conflicts with MCD-01B-09 §10.2, flagged not resolved" (1 Aug 2026); MCD-01B-09's own later corrections pass (2 Aug 2026) removed the blackout-fabric listing from §10.2 | MCD-04, MCD-01B-09 | Likely resolved on the MCD-01B-09 side, but MCD-04's Decision Register narrative was never updated to reflect this — the two documents currently tell inconsistent stories about the same fact |
| Cruze/Softshade drop-minimum figure: MCD-04 §7.16 logged a conflict with MCD-01B-09 §7.2's then-existing 500mm minimum-drop figure (1 Aug 2026); MCD-01B-09's later corrections pass (2 Aug 2026) recorded and resolved a related SPEC71-vs-SPEC72/75/76 conflict on this same figure | MCD-04, MCD-01B-09 | Likely resolved on the MCD-01B-09 side, but MCD-04's Decision Register narrative was never updated — same live inconsistency as above |
| Gasket-rule refinement (sub-2mm protrusion selecting an alternative ordering measurement route rather than failing eligibility), found in MCD-01B-08B's research evidence, likely affects MCD-01B-08A's own DR-07 "conservative operational restriction" characterisation | MCD-01B-08B (source), MCD-01B-08A (potentially affected) | Open — flagged in MCD-01B-08B DR-06 (treatment confirmed by Nazmil Ghany, 26 Jul 2026, as requiring its own separate follow-up task); MCD-01B-08A not modified |
| Supplier company name, internal construction-system reference, advisor-facing display name, and verified profile/colour/handle facts disclosed in MCD-01B-08B's research evidence would resolve MCD-04 §7.15's standing "Not Provided" supplier-company field | MCD-01B-08B (source), MCD-04 (target) | Open — flagged in MCD-01B-08B DR-09 (treatment confirmed by Nazmil Ghany, 26 Jul 2026, as requiring its own separate MCD-04 enrichment task); MCD-04 not modified |
| MCD-01B-08B exists as a substantial partially-ratified working draft but sits unmerged on its own branch, with no PR ever opened — not visible from `main` alone | MCD-01B-08, MCD-01B-08A (its declared sibling/family context), MCD-01B-08B | Open — no PR exists to track promotion or merge; status only discoverable by checking the branch directly |
| Route 1 frame-colour list differs between Full-Frame Bead-Mounted constructions: 7 colours including Beige for Pleated & Cellular, 6 colours without Beige for Roller | MCD-01B-08D (DR-15, source of the finding), MCD-01B-08C (not modified) | Open for MCD-01B-08C only — Beige confirmed operational for MCD-01B-08D on both routes (16 Sep 2026); whether MCD-01B-08C's Route 1 Roller list is complete remains unconfirmed; MCD-01B-08C not modified |
| Day & Night Open-cassette drop: MCD-04 §7.16 still flags its 2,300 mm pricing grid as conflicting with MCD-01B-09 §7.1's 1,900 mm Open-cassette maximum; the business resolution is that the 2,300 mm figure is Closed-cassette data mislabelled as Open | MCD-04, MCD-01B-09 | Open — for pricing-row re-attribution only: MCD-04 §7.16 was corrected 17 Sep 2026 (PR #27); MCD-01B-09 was correct throughout; the affected Open-configuration pricing rows above 1,900 mm drop are flagged in MCD-04 but not yet re-attributed, which remains a separate task |
| Day & Night child-safety device: MCD-01B-09 records that the same child-safety device applies regardless of fascia system; MCD-04 §7.16 records a single device from one source only and does not state this decision | MCD-04, MCD-01B-09 | Closed — MCD-04 §7.16 now cross-references MCD-01B-09 §7.2.3 as of 17 Sep 2026 (PR #27) |
| MCD-00B was not updated in the same commit as MCD-01B-08D's promotion and merge (PR #24), contrary to this register's own "How to keep this current" rule; corrected by a separate follow-up commit | MCD-00B, MCD-01B-08D | Closed — register brought up to date 16 Sep 2026; process note recorded for future promotions |
| Centre-Meet movement style (two fabric sections meeting within the glass) is defined in MCD-01B-08D §5.4 (Route 2 only) but not in the base Pleated & Cellular specification | MCD-01B-08D (source, DR-18), MCD-01B-07 (not modified) | Open — MCD-01B-07 may need a separate controlled update to define it as a base movement style |
| MCD-04 §7.21 and §7.22 now supply MCD-01B-08D's Route 1 (Decora) and Route 2 (Beverley) supplier records | MCD-04, MCD-01B-08D | Closed — both records added 17 September 2026 |

---

## How to keep this current

This file must be updated in the same commit as any change to a document's status, version, number, or hierarchy position — never as a separate follow-up task.
