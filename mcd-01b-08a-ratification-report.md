# MCD-01B-08A Ratification Review — Report Only

Prepared per `claude-code-brief-MCD-01B-08A-ratification-review.md`. **This is a report. No document was edited to produce it.** See Verification at the end for the explicit no-modification confirmation.

Scope discipline observed throughout: no new product specification started; the Full-Frame Bead-Mounted variant numbering question is out of scope and not addressed.

---

## 1. DR-06 — Visible Glass Measurement

**Current wording** (MCD-01B-08A §6):
> "The ordering measurement basis is **Visible Glass Size**. Required capture: glass width at top, middle, and bottom; smallest width used; glass drop at left, centre, and right; smallest drop used; bead and rubber seals are not included in the measurement. The measuring guide confirms visible-glass measurement and smallest-of-three ordering."

**Current wording** (Decision Register DR-06, conclusion only):
> "Applying MCD-01A §7's objective Extended test directly... **Conclusion: Configured.**"

**Evidence reviewed:**
- MCD-01B-08A §6 and DR-06 (as above)
- MCD-01A §5.2 (Measurement Engine Responsibilities: Width, Height, Recess, Exact fit, Bay windows, Tolerances, Validation; Extension Point: "Product-specific measurements") and §7 (objective Extended test)
- MCD-01B-07 §12.4 (top/middle/bottom width, left/centre/right drop, smallest-of-three, for Recess — the precedent DR-06 cites)
- MCD-01B-08 (family-level Shared Service Profile, ratified 19 Jul 2026, already concluding Configured for "glass size... or supplier-specific product size" as a measurement basis)
- MCD-04 §7.15 (current, on `main`) — Structured Technical Value — Measurement Basis: **one** method recorded ("Visible Glass Size"), Evidence Status "Supplier Confirmed (SPEC70; independently corroborated by MEAS005 V2, same method)"
- MCD-01B-08B §4.1 and §4.5 — the sibling variant's own **verified** ordering methods are a pair: "Glass size, or Glass (hidden seal)"

**Recommended decision:** Ratify DR-06's Configured conclusion. The Extended-test reasoning is sound and directly supported by MCD-01A §5.2's named reference-point modes plus the Extension Point, and by the multi-point/smallest-of-three method precedent already established for Recess in MCD-01B-07 §12.4. No defect found in the existing reasoning.

**On the brief's requested separation** (neutral concept / supplier ordering labels / gasket-condition selector): §6 as currently written does not contain any supplier ordering terminology — "Visible Glass Size" is used as a neutral measurement-basis name throughout, and MCD-04 §7.15 is where the concrete label lives. This check passes cleanly with no violation to correct.

However, **08B now records two named ordering methods** for its own Blind Technology ("Glass size" and "Glass (hidden seal)"), selected by a gasket-condition test. 08A's own MCD-04 record shows only **one** method, and MEAS005 V2 corroborates the Pleated/Cellular 2mm figure "with matching wording" rather than introducing a second method. Recommend adding an explicit clarifying sentence to §6 — not because of an error, but to pre-empt future conflation with 08B now that a second named method exists for the sibling variant.

**Proposed replacement wording** (append to §6, after the existing paragraph):
> "This is a single, neutral measurement concept. Any supplier-specific ordering field names used to capture or transmit it belong in MCD-04 as an external supplier mapping, not in this document. This construction's own supplier evidence (MCD-04 §7.15) confirms one ordering method only; it does not establish a second, gasket-condition-selected ordering method — see Decision Register (DR-07) for why that finding, present in the sibling Aluminium Venetian variant (MCD-01B-08B), is not adopted here."

**Confidence level:** High for ratifying Configured (well-supported, multiple independent precedents). Medium for the specific added wording (a clarity improvement, not a correction — would be raised to High by an editorial pass confirming it reads naturally alongside DR-07's own wording below, since the two are cross-referenced).

**Remaining open evidence:** None specific to this decision. The measurement basis itself is fully evidenced.

---

## 2. DR-07 — Square-Profile Policy

**Current wording** (MCD-01B-08A §7.3):
> "Eligible by default: square-profile bead/frame; minimum 2mm rubber-gasket protrusion onto glass; gasket capable of allowing the brackets or side guides to seat correctly; all other clearances passed. Not automatically eligible: chamfered bead; ovolo or curved bead; unknown profile; thick, raised, or distorted gasket; unsuitable or insufficient seating surface. These conditions trigger: **Physical Assessment or Supplier Confirmation Required**."

**Current wording** (Decision Register DR-07, conclusion):
> "It is best characterised as a **conservative operational restriction**... Evidence status: the 2mm square-profile figure — Confirmed Operational Supplier Knowledge; the default-eligibility/Physical-Assessment-Required policy for other profiles — conservative operational restriction, pending ratification."

**Evidence reviewed** (per the brief's §2 discipline — 08A's own evidence tested independently before considering 08B's finding at all):
- MCD-01B-08A §7.2, §7.3, and DR-07 (as above)
- MCD-04 §7.15 (current, on `main`), specifically: "Square-profile bead/gasket: minimum 2mm rubber-gasket protrusion onto glass required. Evidence Status: Confirmed Operational Supplier Knowledge — supported by comparative supplier evidence... **independently corroborated with matching wording** by `MEAS005 - Cruze Pleated Cellular FITtoFRAME Measuring Instructions - Issue V2 - 02.07.2025 (1).pdf`." and "Chamfered bead, ovolo/curved bead, unknown profile: eligibility Not Confirmed — checked against SPEC70 and MEAS005 V2 during the 26 Jul 2026 enrichment pass; neither addresses these profiles."
- MCD-01B-08B §5.3 and Evidence Conflict Register C-5 (the finding being tested for transferability) — the sibling variant's own gasket-rule reading, itself explicitly recorded there as "a **provisional interpretation**, not a verified rule, because it is a reading of how two supplier documents of different vintages relate to one another rather than a single explicit supplier statement," and derived from a different Blind Technology's evidence base (Aluminium Venetian, MCD-01B-06)
- MCD-01B-08B DR-06 (its own explicit finding that this materially affects 08A's DR-07 and must not be copied across automatically)

**Analysis:** 08A's own second source document (MEAS005 V2) is checked directly: MCD-04 §7.15 records it as corroborating the 2mm figure "with matching wording" — the same fact, restated, not a refinement introducing an alternate measurement route below 2mm. Nowhere in 08A's own MCD-04 record does a second ordering method, a "hidden seal" route, or any statement that sub-2mm protrusion is handled differently appear. The chamfered/ovolo/unknown-profile gap was explicitly re-checked against both of 08A's own source documents during the 26 Jul enrichment pass and remains unaddressed by either. **08A's own evidence base does not independently support the less-than-2mm alternative-measurement-route interpretation.**

**Recommended decision:** Classify as **unresolved for Pleated & Cellular pending supplier confirmation**. Do not copy 08B's finding into 08A. Retain DR-07's existing "conservative operational restriction" characterisation unchanged — it remains the accurate description of what 08A's own evidence supports.

**A classification-framing imprecision, flagged rather than fixed:** the brief offers three categories, one of which is "verified only for the Aluminium Venetian variant (i.e. 08B)." Strictly, 08B's own document does not describe its gasket-rule reading as *verified* either — MCD-01B-08B §5.3 explicitly labels it a provisional interpretation, and MCD-01B-08B DR-06 (now ratified) confirms only that this is "a deliberate cross-document review action," not that the underlying reading is settled even for 08B. Selecting "unresolved for Pleated & Cellular" is still the correct answer for 08A, but it would misstate 08B's own status to describe the alternative as "verified" there. The more precise framing: *the alternative-measurement-route interpretation is unconfirmed for both variants; 08A's own evidence provides no independent support for it and does not adopt it.*

**Proposed replacement wording** — no change to §7.3's existing text; append to DR-07:
> "**Cross-variant check performed, per this project's standing discipline against generalising an unconfirmed finding from a sibling document covering a different Blind Technology.** MCD-01B-08B (Aluminium Venetian, a different base specification) independently proposed that sub-2mm gasket protrusion may select an alternative measurement route rather than fail eligibility — but that reading is itself recorded there as provisional, not verified, derived from a different evidence base. This document's own second source document (the corroborating measuring-instructions document, cited in MCD-04 §7.15) restates the 2mm figure with matching wording; it does not introduce an alternate route. This document's own evidence therefore does not independently support adopting that interpretation. The existing conservative-operational-restriction characterisation stands, unchanged, pending direct supplier confirmation for this construction specifically."

**Confidence level:** High. The evidentiary comparison is clean — 08A's own corroborating source document is on record as restating, not refining, the 2mm figure. What would raise confidence further (though it is already high): independent access to the actual source PDFs rather than MCD-04's summarised citations — the same standing limitation across this entire project, not specific to this finding.

**Remaining open evidence:** Unchanged from 08A's existing Open Evidence Items — compatible bead profiles beyond square; maximum acceptable gasket thickness/projection; whether the eligibility scheme is a confirmed rule.

---

## 3. Profile Colours (Open Evidence Item)

**Current wording** (MCD-01B-08A §20):
> "Exact profile-colour availability."

**Evidence reviewed:**
- MCD-01B-08A §20 (as above)
- MCD-04 §7.15 (current, on `main`, post-26-Jul-2026 enrichment): "**Profile colours:** White, Anthracite, Black, Grey, Nobel — as implied by the profile/end-cap/handle colour-matching rules below... Evidence Status: **Supplier Confirmed**. Source Reference: `SPEC70 Cruze Pleated Cellular Specification - Issue V7 - 17.06.2026.pdf`."
- MCD-04's own 26 Jul 2026 Decision Register entry, which already flagged this exact resolution and deferred editing MCD-01B-08A as a side effect

**State:** Fully resolved. The colour set and its evidence status are Supplier Confirmed, not partial.

**Recommended decision:** Close the open item. Per the brief's explicit instruction, do not transcribe the colour names or RAL mappings into the neutral product specification — record the governance requirement and point to the controlled mapping location.

**Proposed replacement wording** — remove the §20 bullet "Exact profile-colour availability," and add to the Decision Register:
> "**DR-15 — Profile-colour open item resolved by external supplier mapping.** The profile-colour availability question (formerly an Open Evidence Item) is fully resolved: current supplier evidence confirms a defined set of profile colours for this construction, with an associated colour-matching rule and RAL references, recorded at MCD-04 §7.15 (Supplier Confirmed). This document does not transcribe the colour names or the mapping itself — per the Neutral Document Identity Statement, that detail belongs exclusively in MCD-04. Advisors are shown the confirmed colour options via the Supplier Capability Engine (§18), which resolves them from MCD-04 at configuration time; nothing further is required in this document's own text."

**Confidence level:** High. This is a direct evidence-status read, not a judgment call.

**Remaining open evidence:** None for this item.

---

## 4. DR-12 — Motor Engine

The brief requires these answered as two separate questions. They are kept fully separate below and must not be read as informing one another.

### (a) Motorisation availability — product-capability evidence question

**Current wording** (MCD-01B-08A §5.1):
> "Current evidence supports manual operation only. Motorisation is recorded as **Not Provided** unless a current supplier-issued specification confirming motorisation for this specific construction is found."

**Evidence reviewed:** MCD-04 §7.15 (current, on `main`): "**Motorisation:** Not Provided for this specific construction. Not inferred from Pleated, Cellular, or other framed systems' own motorisation evidence. Checked against SPEC70 and MEAS005 V2 during the 26 Jul 2026 enrichment pass; neither mentions motorisation for this construction."

**Finding:** Both of 08A's own source documents were re-checked specifically for motorisation content during the 26 Jul 2026 MCD-04 enrichment pass, and neither mentions it. This is not an untested gap — it is a checked absence. Motorisation availability for this construction is not: available and advisor-selectable; available but factory-selected; supplier-dependent; or restricted to certain configurations. None of those states has any supporting evidence. It is correctly the remaining category: **unsupported by current evidence.**

**Recommended decision:** Confirm motorisation availability remains **Not Provided**; quoting stays disabled. No change.

### (b) Motor Engine Shared Service status — architectural classification question

**Current wording** (Decision Register DR-12, conclusion):
> "**Conclusion: Configured** — the product's relationship to the Motor Engine remains an ordinary capability-based eligibility gate... with the current evidence state (Not Provided) keeping the specific capability hidden and unquotable until a supplier confirms it — an evidence gate, not an SSP status change."

**Evidence reviewed:**
- MCD-01A §5.5 (Motor Engine Responsibilities: Motor compatibility, Weight calculations, Tube compatibility, Power options, Smart Home compatibility) and §7 (Shared Service Status Definitions, objective Extended test)
- MCD-01B-06 §Decision Register (17 Jul 2026, ratified 16 Jul 2026), which tested the identical question for a harder case (an intermediate "Category-Level Availability Confirmed / Quoting Status: Disabled" evidence state) and concluded Configured, explicitly because "representing degrees of evidence confidence is a data/schema question... not a question of whether the engine's own matching/eligibility logic must change"
- MCD-01B-08 §8 (family-level Motorisation Principle, ratified 19 Jul 2026): "the motorisation quoting gate... is a data-availability gate, not a deliberate Solara exclusion of an available capability" — i.e. Configured, not Restricted, as a standing family-level rule this variant inherits

**Finding:** DR-12's existing reasoning tests Full, Restricted, and Not Applicable individually against their MCD-01A §7 definitions and rejects each correctly: Full fails because no motorised variant is currently evidenced at all (so there is nothing to "use as defined"); Restricted fails because nothing shows an available capability being deliberately withheld — the evidence is simply absent; Not Applicable fails because MCD-01B-07 §11 already treats motorisation as potentially available across Tensioned constructions generally, so there is no structural incapability specific to this construction. This reasoning is not stated by analogy — it is tested against each definition directly, exactly as MCD-01A §19 (per the design brief) required. It also matches, rather than merely resembles, two separately ratified precedents (MCD-01B-06's Motor Engine Configured conclusion; MCD-01B-08's family-level data-availability-gate-is-Configured rule) that this variant is entitled to inherit rather than re-derive.

**Reviewed for genuine defect:** none found. The reasoning does not rest on the *thinness* of the evidence about (a) — it rests on the *architecture* of what an evidence gap means for SSP classification, which is exactly the distinction the brief requires.

**Recommended decision:** Ratify DR-12 as-is. **Configured.** No wording change needed beyond removing "pending ratification" and appending a ratification-confirmation note (see Proposed replacement wording).

**Proposed replacement wording** — append to DR-12 (do not replace existing analysis):
> "**Reviewed for ratification, per `claude-code-brief-MCD-01B-08A-ratification-review.md`. Recommendation: ratify as Configured.** Motorisation availability (a genuine evidence-availability question) and Motor Engine's Shared Service status (an architectural classification question) are confirmed as two separate questions, per MCD-01A §7 and this project's own precedent (MCD-01B-06's Evidence Status / Quoting Status two-field model; MCD-01B-08's family-level data-availability-gate rule). Motorisation availability for this construction was re-checked against both of this document's own source documents during MCD-04's 26 Jul 2026 enrichment pass and remains genuinely absent from both — Not Provided, quoting disabled. This evidence state does not itself change, and must not be read as changing, the Motor Engine's Configured classification, which rests on the engine's unchanged eligibility-gating architecture, not on how much motorisation evidence currently exists."

**Confidence level:** High for both (a) and (b) independently. What would raise (a) specifically: a supplier document that actually addresses motorisation for this construction, either way. Nothing would or should raise (b), since it is not evidence-dependent by design.

**Remaining open evidence:** Current motorisation availability for this specific construction (already listed in §20).

---

## 5. DR-13 — Shared Service Profile (all twelve services, reviewed individually)

Each service below is assessed against its MCD-01A §5.x Responsibilities and the objective Extended test (MCD-01A §7), not assigned by analogy to the existing all-Configured table.

| # | Service | Proposed status | Evidence / governing precedent | Level | Unresolved dependency |
|---|---|---|---|---|---|
| 1 | Survey Engine | Configured | MCD-01A §5.1 Extension Point ("Product-specific questions"); field categories already Configured at family level, MCD-01B-08 §6 | Construction-Group-level fields, product-specific content | None architectural. Some field values (bead profile eligibility beyond square) remain open evidence, which is a content gap, not an SSP-status question. |
| 2 | Measurement Engine | Configured | MCD-01A §5.2 (Recess, Exact fit named as reference-point modes; Extension Point for product-specific measurements); MCD-01B-07 §12.4 multi-point/smallest-of-three precedent; MCD-01B-08 family-level glass-size conclusion | Product-specific reference point; method inherited from base spec | None. See DR-06 above — recommend the added clarifying sentence, not a status change. |
| 3 | Validation Engine | Configured | MCD-01A §5.3 ("Dimension validation," "Compatibility"); MCD-01B-07 §12.3 width-dependent-max-drop precedent; MCD-01B-06 multi-factor eligibility-matrix precedent | Product-specific parameterisation | The non-square-profile eligibility *content* (DR-07) is an open evidence item — this affects what the Validation Engine currently validates, not whether its classification is Configured. Flagged explicitly here so the two are not conflated, mirroring the brief's own DR-12(a)/(b) discipline. |
| 4 | Operation Engine | Configured | MCD-01A §5.4 ("Manual Only" is one of four defined modes); §7 worked example explicitly confirms selecting existing modes is Configured | Product-specific selection of an existing mode | None. |
| 5 | Motor Engine | Configured | See DR-12(b) above in full | Product-specific evidence-gate application of an unchanged engine | See DR-12(a) — evidence gap, not an SSP question. |
| 6 | Child Safety Engine | Configured | MCD-01A §5.6 (BS EN 13120 compliance; Extension Point: "product-specific implementation, e.g. safety device mappings per construction"); MCD-01B-08 §9 family-level principle that classification depends on the inserted Blind Technology's control mechanism | Product-specific control-route classification | Technology-specific child-safety classification beyond the initial independent assessment (§20) is an open evidence item — again a content gap, not a status question. Flagged explicitly for the same reason as row 3. |
| 7 | Pricing Engine | Configured | MCD-01A §5.7 (Dimensions, Supplier costs, Margins, Discounts, VAT, Commercial pricing, Accessories; Extension Point: "additional pricing inputs") | Product-specific inputs (fixing-route and profile-colour surcharges) | None. |
| 8 | Accessory Engine | Configured | MCD-01A §5.8 (Extension Point: "real accessories, not generic placeholders") | Product-specific named accessory groups | None. |
| 9 | Supplier Capability Engine | Configured | MCD-01A §5.9 (Available constructions/fabrics/motors, Lead times, Manufacturing limits; Extension Point: "Supplier Library provides the implementation"); MCD-01B-08's own ratified ten-role schema precedent, a harder case than this document's five-key lookup | Product-specific data model, schema inherited/precedented | None architectural. |
| 10 | Recommendation Engine | Configured | MCD-01A §5.10 ("Rank compatible alternatives," "Explain the reasoning behind recommendations"; Extension Point: product-specific rules/exclusions) | Product-specific application | None. |
| 11 | Document Generation Engine | Configured | MCD-01A §5.11 and §5.7's Customer-Facing Documentation Rule; MCD-01B-08 §10 family-level Customer-Document Rules | Inherited rule, product-specific exclusion list content | None. |
| 12 | Audit & Compliance Engine | Configured | MCD-01A §5.12 (User history, Decision history, Product changes, Compliance logs, Approval records) | Inherited pattern, product-specific record fields | None. |

**No service qualifies for Extended:** applying MCD-01A §7's objective test service-by-service (would implementing this product require a change to the shared service itself?) — no. Every row above parameterises an existing, named Responsibility or Extension Point.

**No service qualifies for Restricted or Not Applicable:** every gated/unconfirmed state in this document (motorisation, non-square-profile eligibility, Dual-Fabric availability, child-safety classification beyond the initial assessment) is an evidence-availability gate on *content*, not a deliberate Solara exclusion of an available capability and not a structural irrelevance. This is the same distinction DR-12 already draws for Motor Engine specifically, and it is confirmed here to hold identically for Validation Engine (row 3) and Child Safety Engine (row 6) — the two other rows where an open evidence item could be mistaken for an SSP-status question if the two were conflated.

**Recommended decision:** Ratify the existing all-Configured table (§18) and DR-13 as-is. Recommend appending the explicit row-3/row-6 clarification above (evidence gap ≠ status change) to DR-13's text, since the existing DR-13 makes this distinction explicitly only for Motor Engine.

**Confidence level:** High across all twelve. What would raise confidence further for rows 3 and 6 specifically: closing the underlying open evidence items (which would not change their SSP status, only their content completeness).

**Remaining open evidence:** As already listed in §20 — none of it bears on any SSP status.

---

## 6. Cross-Variant Consistency

Compared strictly at the shared Side-Guide Construction Group level, per the brief's instruction not to assume a rule verified for one variant applies to the other.

- **Construction Group principles (shared, MCD-01B-08):** both 08A and 08B correctly inherit the Side-Guide Window-Mounted System classification without re-litigating MCD-01B-08's own ratified three-test reasoning. Consistent.
- **Pleated & Cellular variant rules (08A):** measurement basis (single method), square-profile 2mm figure (corroborated, not refined, by its own second source), dimensional limits (200mm–1,500mm width; 150mm–2,300mm drop), fixing routes (Configuration-layer, per DR-09), full Shared Service Profile drafted and reasoned.
- **Aluminium Venetian variant rules (08B):** two named ordering methods, a *different and lower* provisionally-controlled minimum width (250mm, disputed against a 200mm figure in its own measuring instructions), a gasket-rule reading that is itself provisional, no Shared Service Profile (deliberately deferred).
- **Supplier-specific capabilities (MCD-04):** §7.15 holds the Pleated/Cellular record only, fully populated per the 26 Jul enrichment; the Aluminium Venetian record is explicitly reserved and not yet populated (MCD-01B-08B DR-09, confirmed 26 Jul 2026).

**Inconsistencies found, flagged and not fixed:**

1. **Minimum width mismatch between the two variants' own dimensional figures.** 08A's confirmed minimum width is 200mm (§10, Supplier Confirmed in MCD-04 §7.15, independently corroborated by both of 08A's own source documents). 08B's *disputed* minimum width figures are 200mm (per its measuring instructions) or 250mm (per its product specification and leaflet, currently the provisional control). MCD-01B-08B's own DR-04 already raises, as a bare *question to the supplier* rather than a finding, whether the 200mm figure in 08B's measuring instructions might actually be 08A's own figure appearing in shared documentation — given the two variants' minimum drop, maximum drop, maximum area, manufacturing tolerance, and handle clearance are all otherwise identical between them. This review does not resolve that question (it is explicitly out of scope, and DR-04 itself declines to resolve it) but confirms it remains open and worth flagging in the same place a future supplier clarification would land.
2. **DR-07 / 08B-C-5 classification imprecision**, already flagged in full under §2 above: the brief's own three-option classification for the gasket-rule finding does not have a clean slot for "provisional in the source variant too" — worth tightening if this classification scheme is reused for a future cross-variant question.

No other inconsistency was found between 08A, 08B, MCD-01B-08, or MCD-04 during this review.

---

## 7. Where the Evidence Does Not Support a Recommendation

- **DR-07's underlying eligibility scheme** (which non-square profiles, if any, are compatible) remains genuinely unresolved for 08A. What is missing: any supplier statement — from either of 08A's own two source documents — addressing chamfered, ovolo/curved, or unknown profiles at all. This was actively re-checked (not merely re-asserted) during MCD-04's 26 Jul 2026 enrichment pass and confirmed still absent.
- **Motorisation availability** (DR-12(a)) remains Not Provided for the same reason: actively re-checked against both source documents, confirmed absent.
- **Minimum-width cross-variant question** (§6 above): a real observation exists, but nothing in either document's own evidence resolves it — it requires a supplier answer, not further internal analysis.

---

## Verification

- **No existing document was modified.** Confirmed via `git diff origin/main` and `git status` (see below) — MCD-01B-08A.md, MCD-01B-08B.md, MCD-04.md, MCD-01A, and MCD-01B-01 through MCD-01B-08 are byte-for-byte unchanged. The only addition is this report file, `mcd-01b-08a-ratification-report.md`.
- **No status was promoted or changed.** All recommendations above are proposed text for a future, separately-authorised edit; nothing in MCD-01B-08A.md's actual Status line, Decision Register, or Open Evidence Items has been altered by this task.
- **No supplier names, trademarks, system names, or document codes appear in any proposed replacement wording** intended for the neutral product specification (§1, §2, §3, §5's proposed text). Where a source document is referenced, it is described generically ("this document's own second source document," "the corroborating measuring-instructions document") — the same discipline the documents under review already apply to themselves.
- **Every proposed Shared Service status uses only the six approved MCD-01A values** (Full, Configured, Extended, Restricted, Not Applicable, Future) — every status recommended above is Configured; no out-of-vocabulary status ("Unresolved" or otherwise) is proposed anywhere, including for DR-12(b).
- **This report file is the only file added.** No pull request opened, nothing merged.

**Delivery:** created as a new file, `mcd-01b-08a-ratification-report.md`, on branch `claude/mcd-01b-08a-ratification-review` (branched from `main`, not from either product-specification branch, since this is a report-only task with no dependency on their branch state).
