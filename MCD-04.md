Document ID: MCD-04
Document Title: Product Library & Supplier Management
Status: Draft Skeleton
Version: 0.2
Last Updated: 14 July 2026 (v0.2)

## Dependencies
- MCD-00 — Executive Charter
- MCD-00A — Project Development Standards (not present in repository at time of writing — see Decision Register)
- MCD-01A — Sales MVP Product Engine Architecture (v1.5, Approved Draft Baseline)
- MCD-01B-01 — Roller Blinds Product Engine Specification (v1.5, Approved Draft Baseline – Product Specification)
- MCD-01B-02 — Vertical Blinds Product Engine Specification (v1.3, Approved Draft Baseline – Product Specification)

This is a new document. It is not an extension of MCD-01A, MCD-01B-01, or MCD-01B-02, and none of those documents are modified by its introduction.

## 1. Purpose

MCD-04 is the permanent, authoritative record of supplier capabilities for the Solara product range — what specific suppliers can actually manufacture, supply, and support, with the evidence behind each claim. Product Specifications (MCD-01B-xx) reference capabilities defined here; they do not embed supplier-specific detail themselves.

## 2. Scope

**Critical scope boundary — MCD-04 is the deliberate exception to Constraint 2.** Product Specifications (MCD-01B-xx) must remain supplier-independent — no supplier names, trademarks, part numbers, or URLs anywhere in them. MCD-04 is the opposite: it is *specifically* the place where supplier names, trademarks, brand names, part numbers, model numbers, and source URLs belong and are expected to appear throughout.

Unlike Product Specifications (MCD-01B-xx), which must remain supplier-independent per MCD-01A §3/§9 and their own design briefs, this document is the designated location for supplier-specific detail. Naming suppliers, brands, trademarks, part numbers, and source URLs here is expected and required, not a violation of Solara's supplier-independence principle. Do not apply Product Specification supplier-neutrality rules to this document.

This is important: without stating it plainly, a future review pass could mistakenly try to "clean up" MCD-04 the same way MCD-01B-02 was cleaned up, which would defeat the document's purpose.

This document covers supplier capability records for all Solara product families as they are developed — Vertical Blinds now; Roller, Roman, Curtains, Shutters, Perfect Fit, and others as their own supplier capability evidence is gathered.

## 3. Relationship to MCD-01A and MCD-01B-xx

MCD-01A defines the Supplier Capability Engine as one of the twelve Shared Platform Services (§5.9) and requires that Product Specifications reference Supplier Capability rather than embed it. MCD-04 is the document that Supplier Capability Engine rows in each Product Specification's Shared Service Profile point to.

A Product Specification's Decision Register should cite evidence by category only ("supplier technical documentation," "advisor trade knowledge") and reference "see MCD-04" for the underlying detail, once this document exists — matching the precedent set in MCD-01B-02 §23's resolved Motorised (Tilt Only) entry.

## 4. Governance

MCD-04 follows the same conventions as MCD-01B-01 and MCD-01B-02: Decision Register format (Date | Decision | Reasoning | Raised By), version history, and status labelling (Draft Skeleton for this first version).

Consistent with prior documents in this repo, MCD-00A (Project Development Standards) is referenced but not yet present in the repository. Its conventions are inherited from how MCD-01B-01 and MCD-01B-02 already apply them, rather than fabricated; this is logged as a Decision Register entry below rather than silently assumed.

## 5. Record Structure

Each Supplier Capability Record contains the following fields:

- **Capability** — a short name for what this record documents (e.g. "Motorised Tilt Operation").
- **Business Rule** — the Solara-terminology rule this capability supports or constrains, expressed exactly as it appears (or should appear) in the relevant Product Specification's Decision Register.
- **Technical Specification** — the underlying technical facts: dimensions, performance parameters, tolerances, compatible components, part numbers, colours, and similar detail.
- **Evidence** — the specific source material supporting the Business Rule and Technical Specification: named suppliers, brochures, webpages, URLs, direct quotations (kept short and clearly marked as quotations), and advisor trade knowledge, clearly attributed.
- **Source References** — direct citations: document titles, URLs, brochure identifiers, and the date each source was accessed, published, or confirmed. This date is included for every source listed, not just where convenient — it is what lets a later reviewer judge whether a record has gone stale.
- **Validation Status** — e.g. Confirmed, Awaiting Supplier Confirmation, Superseded, Under Review.
- **Revision History** — dated log of changes to this specific record (not the whole document), noting what changed and why (e.g. "supplier revised specification," "additional evidence obtained").

### Structured Technical Value (generalized block type)

This block type generalizes the earlier weight-only convention used within a record's Technical Specification field. It represents any single quantifiable technical fact — weight, length, count, dimensional deduction, tolerance, or load limit — without requiring a separate near-identical block per data type. **This is an MCD-04 schema enhancement applicable to all future product families**, not a Roman-only addition: for example, Roller tube/fabric weights, Vertical stack/control formulas, Curtain fullness/track-load rules, Shutter panel/frame limits, motor torque/load thresholds, and bracket-spacing formulas across any product family may all be represented using this block type.

Each Structured Technical Value entry contains:

- **Metric** — the name of the fact being recorded (e.g. "Material Weight," "Control Chain Length," "Rod Count").
- **Value** — the numeric or textual value, where a single fixed value applies.
- **Unit** — the unit of measure (e.g. g/m², mm, count, Nm, V).
- **Value Type** — one of: Weight, Length, Area, Count, Torque, Voltage, Time, Percentage, Boolean, Text Rule. Exists so automated interpretation does not have to infer type from the Metric name alone.
- **Basis** — one of: Fixed, Per Square Metre, Per Metre Width, Per Metre Drop, Per Component, Per Fold, Per Lift Cord, By Drop Band, By Width Band, Formula, Percentage of Calculated Value, Supplier-Stated Maximum, Construction-Specific.
- **Applies To** — the construction, product family, or component the value applies to.
- **Calculation Rule** — the formula or method, where Basis = Formula or a similarly derived basis.
- **Input Variables** — the named inputs a Calculation Rule depends on.
- **Minimum** — a floor value, where applicable (e.g. a formula's result never falls below this).
- **Maximum** — a ceiling value, where applicable.
- **Evidence Status** — e.g. Supplier Confirmed, Supplier data required, Awaiting Supplier Confirmation.
- **Source Reference** — the specific supplier document or evidence category this value comes from.
- **Notes** — supplementary detail, including compact inline representations of multi-row supplier tables (this block type has no native multi-row table).

**Worked examples** (illustrating the schema; items 2, 3, and 5 are also populated as real Roman Blinds data in §7):

1. **Lining weight** — Metric: Material Weight; Value: 135; Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Premier Lining; Calculation Rule: Value × finished lining area; Evidence Status: Supplier Confirmed.
2. **Standard/No-Drill/Cassette chain length** — Metric: Control Chain Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To: Standard Headrail (also No-Drill Headrail, Cassette Headrail — see §7 for whether the source confirms this as identical across all three or shows variation); Calculation Rule: Installation Height minus 1500; Input Variables: Installation Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind drop when installation height is unavailable; Evidence Status: Supplier Confirmed.
3. **Breakaway chain length** — Metric: Control Chain Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To: Breakaway configuration; Calculation Rule: Installation Height minus 600; Input Variables: Installation Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind drop when installation height is unavailable; Evidence Status: Supplier Confirmed.
4. **Rod count** — Metric: Rod Count; Unit: count; Value Type: Count; Basis: By Drop Band; Applies To: Roman Blind body; Calculation Rule: supplier drop-band table; Input Variables: Finished Drop; Notes: illustrative inline format for a compact drop-band table — e.g. "Drop band 1: n rods; Drop band 2: n rods; Drop band 3: n rods." **This example shows the schema pattern only** — the actual Roman band boundaries and counts were not included in the material provided to Claude Code, so they are not asserted as Supplier Confirmed here; the real Roman entry is recorded as Not Provided in §7 rather than invented to complete this illustration (see Decision Register).
5. **No-Drill finished-weight limit** — Metric: Maximum Finished Weight; Value: 10; Unit: kg; Value Type: Weight; Basis: Supplier-Stated Maximum; Applies To: No-Drill construction; Evidence Status: Supplier Confirmed.

## 6. Document Organisation

Records are organised by Solara product architecture first, supplier second — never the reverse:

```
Supplier Capability Records
│
├── Vertical Blinds
│     ├── Vogue
│     │     └── Motorised Tilt Operation   [populated — see §7]
│     ├── Slimline                          [Future Entries — empty for now]
│     ├── Cruze                             [Future Entries — empty for now]
│     ├── Nova                              [Future Entries — empty for now]
│     ├── Curved                            [Future Entries — empty for now]
│     └── Sloping                           [Future Entries — empty for now]
│
├── Roman Blinds
│     ├── Standard Headrail                 [populated — see §7]
│     ├── Breakaway Control                 [populated — see §7; Configuration-layer feature, not a Construction Variant — see MCD-01B-03 §3]
│     ├── No-Drill Headrail                 [partially populated — see §7]
│     ├── Cassette Headrail                 [partially populated — see §7]
│     └── General                           [partially populated — see §7; lining, fabric, recess deduction, tolerance, rod/cord count, motor]
│
└── Future Entries
      ├── Roller Blinds
      ├── Curtains
      ├── Pleated Blinds
      ├── Perfect Fit Systems
      └── Shutters
```

Supplier relationships (which supplier provides which capability) are metadata attached to each record, not the organising structure of the document. A future Supplier Mapping appendix (Decora, Louvolite, Arena, Beverley, Santa Fe, Temposhade, and others) may cross-reference records by supplier for convenience, but is not the primary structure and is not required for this first draft.

## 7. Supplier Capability Records

### 7.1 Vertical Blinds → Vogue → Motorised Tilt Operation

- **Capability:** Motorised Tilt Operation (Vogue Construction Variant, Vertical Blinds)
- **Business Rule:** When Control Type = Motorised (Tilt Only) and Construction Variant = Vogue, Draw Mechanism = Wand automatically. No advisor configuration of draw mechanism is presented for this combination. (Matches the resolved "Motorised (Tilt Only) Draw Mechanism" Decision Register entry in MCD-01B-02 §23 — identified by name here as well as by section number, since section numbers may move in later revisions.)
- **Technical Specification:** Motorisation is compatible with the Slimline Vogue® headrail system specifically. The motor controls louvre tilt only (0°, 45°, 90°, 135°, 180° positions); traversing (draw) remains manual via wand. Maximum width for motorised operation: 3m. Minimum blind width with open cassette: 200mm. Available Vogue headrail colours: white, black, brown, anthracite grey, brushed aluminium, champagne gold.

  **Supplier capability vs. Solara restriction — kept distinct:** the underlying supplier system supports both 89mm and 127mm louvre widths. Solara's Sales MVP exposes 89mm only; this is a Solara business restriction governed by MCD-01B-02 (§4), not a supplier manufacturing limitation. This restriction must not be read as something the supplier itself cannot support.
- **Evidence:** Louvolite Commercial's Vertical Blind Systems webpage states that motorisation is compatible with Slimline Vogue® vertical blinds specifically, is tilt-only, and that wand operation performs the draw. A Louvolite technical brochure ("Slimline Vogue® Vertical Blind System — Side Draw with Wand Operation") documents the Vogue Channel with Tilt Rod (part 1019) and the One Touch® Vogue motor pack (part 1140) as components of the standard Vertical Blind system, including performance parameters (rated torque, RPM, motor diameter, voltage, power, current, IP rating) and the bunching/stacking distance table by louvre width and draw type. Advisor trade knowledge (Nazmil Ghany) confirms that motorised tilt was introduced for the standard Vertical Blind System on the Vogue headrail before Louvolite's separate Allusion® product line was developed roughly six years later, adopting the same Vogue headrail and motorisation platform — ruling out an alternative reading in which motorisation might be exclusive to Allusion® rather than available on standard Vertical Blinds.
- **Source References:**
  - Louvolite Commercial, Vertical Blind Systems page (louvolitecommercial.com/discover/vertical-blinds) — accessed 14 July 2026.
  - Louvolite technical brochure "2025_LL_SLIMLINE-VOGUE-VERTICAL-BLINDS_SIDE-DRAW-WITH-WAND-CONTROL.pdf" — 2025 edition, reviewed 14 July 2026.
  - Advisor trade knowledge — confirmed by Nazmil Ghany on 14 July 2026.
- **Validation Status:** Confirmed.
- **Revision History:** 14 Jul 2026 — record created, evidence gathered and confirmed during MCD-01B-02 Phase 2 review.

### 7.2 Vertical Blinds → Other Construction Variants

Slimline, Cruze, Nova, Curved, and Sloping have no populated records yet — Future Entries, empty for now. Populating them requires the same evidence-gathering standard applied in §7.1, not placeholder or speculative content.

### 7.3 Roman Blinds → Standard Headrail

- **Capability:** Dimensional Limits and Control Chain Length (Standard Headrail, Roman Blinds)
- **Business Rule:** Standard Headrail's finished-width and finished-drop ranges, and its Manual-operation control chain length formula, are Supplier Capability facts referenced by MCD-01B-03 §4.1, §9, and §17 rather than embedded there.
- **Structured Technical Value — Finished Width Range:** Metric: Finished Width Range; Unit: mm; Value Type: Length; Basis: Construction-Specific; Applies To: Standard Headrail; Minimum: 350; Maximum: 2600; Evidence Status: Supplier Confirmed.
- **Structured Technical Value — Finished Drop Range:** Metric: Finished Drop Range; Unit: mm; Value Type: Length; Basis: Construction-Specific; Applies To: Standard Headrail; Minimum: 250; Maximum: 4000; Evidence Status: Supplier Confirmed.
- **Structured Technical Value — Control Chain Length:** Metric: Control Chain Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To: Standard Headrail; Calculation Rule: Installation Height minus 1500; Input Variables: Installation Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind drop when installation height is unavailable; Evidence Status: Supplier Confirmed.
- **Evidence:** Primary supplier technical documentation.
- **Source Reference:** Not provided to Claude Code — supplier name and specific source document title pending from Nazmil Ghany (see Decision Register).
- **Validation Status:** Confirmed (dimensional and chain-length values); Source Reference outstanding.
- **Revision History:** 14 Jul 2026 — record created during MCD-01B-03 breakaway-note review.

### 7.4 Roman Blinds → Breakaway Control

**Note:** this is a technical-data grouping node, not an assertion that Breakaway is a Construction Variant. Breakaway Control is a Configuration-layer, Manual-only safety mechanism per MCD-01B-03 §3/§4a (Decision Register #10) — it still needs a home for its own supplier-derived technical parameters (dimensional eligibility, chain-length formula), which is what this node holds.

- **Capability:** Dimensional Limits and Control Chain Length (Breakaway Control, Roman Blinds)
- **Business Rule:** Breakaway Control's finished-width and finished-drop ranges, and its distinct control chain length formula, are Supplier Capability facts referenced by MCD-01B-03 §3, §9, and §17 rather than embedded there.
- **Structured Technical Value — Finished Width Range:** Metric: Finished Width Range; Unit: mm; Value Type: Length; Basis: Construction-Specific; Applies To: Breakaway configuration; Minimum: 400; Maximum: 2400; Evidence Status: Supplier Confirmed.
- **Structured Technical Value — Finished Drop Range:** Metric: Finished Drop Range; Unit: mm; Value Type: Length; Basis: Construction-Specific; Applies To: Breakaway configuration; Minimum: 300; Maximum: 2500; Evidence Status: Supplier Confirmed.
- **Structured Technical Value — Control Chain Length:** Metric: Control Chain Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To: Breakaway configuration; Calculation Rule: Installation Height minus 600; Input Variables: Installation Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind drop when installation height is unavailable; Evidence Status: Supplier Confirmed.
- **Evidence:** Primary supplier technical documentation.
- **Source Reference:** Not provided to Claude Code — supplier name and specific source document title pending from Nazmil Ghany (see Decision Register).
- **Validation Status:** Confirmed (dimensional and chain-length values); Source Reference outstanding.
- **Revision History:** 14 Jul 2026 — record created during MCD-01B-03 breakaway-note review.

### 7.5 Roman Blinds → No-Drill Headrail

- **Capability:** Maximum Finished Weight, Dimensional Limits, and Control Chain Length (No-Drill Headrail, Roman Blinds)
- **Business Rule:** No-Drill Headrail's maximum finished-weight limit is a Supplier Capability fact referenced by MCD-01B-03 §4.2 and §9 rather than embedded there.
- **Structured Technical Value — Maximum Finished Weight:** Metric: Maximum Finished Weight; Value: 10; Unit: kg; Value Type: Weight; Basis: Supplier-Stated Maximum; Applies To: No-Drill construction; Evidence Status: Supplier Confirmed.
- **Structured Technical Value — Finished Width/Drop Range:** Not Provided. Value: Not Provided; Evidence Status: Supplier data required; Notes: No-Drill-specific dimensional limits were not included in the material provided to Claude Code, despite Standard's and Breakaway's ranges being available. Not assumed to match either.
- **Structured Technical Value — Control Chain Length:** Metric: Control Chain Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To: No-Drill Headrail; Calculation Rule: Installation Height minus 1500 (same formula as Standard Headrail, per the brief's grouping); Input Variables: Installation Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind drop when installation height is unavailable. **Not independently verified** — the material provided to Claude Code grouped No-Drill with Standard's formula but did not confirm from source documentation whether this is genuinely identical or varies; recorded provisionally rather than asserted as independently confirmed. Evidence Status: Supplier Confirmed for Standard's formula; Awaiting Supplier Confirmation that No-Drill shares it.
- **Evidence:** Primary supplier technical documentation (weight limit only).
- **Source Reference:** Not provided to Claude Code — supplier name and specific source document title pending from Nazmil Ghany (see Decision Register).
- **Validation Status:** Confirmed (weight limit only); dimensional limits and chain-length-formula-sharing outstanding.
- **Revision History:** 14 Jul 2026 — record created during MCD-01B-03 breakaway-note review.

### 7.6 Roman Blinds → Cassette Headrail

- **Capability:** Dimensional Limits and Control Chain Length (Cassette Headrail, Roman Blinds)
- **Business Rule:** Cassette Headrail's dimensional limits and chain-length formula are Supplier Capability facts referenced by MCD-01B-03 §4.3 and §9 rather than embedded there.
- **Structured Technical Value — Finished Width/Drop Range:** Not Provided. Value: Not Provided; Evidence Status: Supplier data required; Notes: Cassette-specific dimensional limits were not included in the material provided to Claude Code, despite Standard's and Breakaway's ranges being available. Not assumed to match either.
- **Structured Technical Value — Control Chain Length:** Metric: Control Chain Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To: Cassette Headrail; Calculation Rule: Installation Height minus 1500 (same formula as Standard Headrail, per the brief's grouping); Input Variables: Installation Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind drop when installation height is unavailable. **Not independently verified** — same caveat as No-Drill Headrail (§7.5): grouped with Standard's formula but not confirmed from source documentation whether identical or varying. Evidence Status: Supplier Confirmed for Standard's formula; Awaiting Supplier Confirmation that Cassette shares it.
- **Evidence:** None yet for dimensional limits; formula-sharing unconfirmed.
- **Source Reference:** Not provided to Claude Code — supplier name and specific source document title pending from Nazmil Ghany (see Decision Register).
- **Validation Status:** Awaiting Supplier Confirmation.
- **Revision History:** 14 Jul 2026 — record created during MCD-01B-03 breakaway-note review.

### 7.7 Roman Blinds → General (cross-construction facts)

- **Capability:** Lining Weights, Recess Deductions, Manufacturing Tolerance, Fabric Range Summary, Rod/Cord Count, Motor Specifications (Roman Blinds, not construction-specific)

  **Lining weights** — five Structured Technical Value entries:
  - Metric: Material Weight; Value: 135; Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Premier Lining; Calculation Rule: Value × finished lining area; Evidence Status: Supplier Confirmed; Notes: width and composition not included in the material provided to Claude Code — recorded as Not Provided rather than invented.
  - Metric: Material Weight; Value: 200 (±5%); Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Satin Lining; Calculation Rule: Value × finished lining area; Evidence Status: Supplier Confirmed; Notes: width and composition Not Provided.
  - Metric: Material Weight; Value: 140; Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Blockout Lining; Calculation Rule: Value × finished lining area; Evidence Status: Supplier Confirmed; Notes: width and composition Not Provided.
  - Metric: Material Weight; Value: 400; Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Bonded Lining; Calculation Rule: Value × finished lining area; Evidence Status: Supplier Confirmed; Notes: width and composition Not Provided.
  - Metric: Material Weight; Value: 333; Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Blockout Bonded Lining; Calculation Rule: Value × finished lining area; Evidence Status: Supplier Confirmed; Notes: width and composition Not Provided.

  **Recess deductions** — two Structured Technical Value entries: Metric: Recess Width Deduction; Value: -10; Unit: mm; Value Type: Length; Basis: Fixed; Applies To: Roman Blind body; Evidence Status: Supplier Confirmed; Notes: source did not specify whether this applies uniformly across all four constructions or varies per construction — recorded as given, not assumed uniform. Metric: Recess Drop Deduction; Value: -10; Unit: mm; Value Type: Length; Basis: Fixed; Applies To: Roman Blind body; Evidence Status: Supplier Confirmed; same uniformity caveat.

  **Manufacturing tolerance** — Metric: Manufacturing Tolerance; Value: ±5; Unit: mm; Value Type: Length; Basis: Fixed; Applies To: Roman Blind body; Evidence Status: Supplier Confirmed.

  **Fabric range summary** (not a per-fabric record — per this brief's explicit instruction not to transcribe the ~100-row fabric range table): observed fabric width range across the collection is 1140mm–3000mm; composition variety exists per range; price bands A–D exist. The complete fabric/colourway range list belongs in the pricing/fabric table system, not here. Source Reference: Not provided to Claude Code — supplier name and specific source document title pending from Nazmil Ghany (see Decision Register); reference by title once supplied.

  **Face fabric weight (GSM)** — explicitly recorded as absent, not silently omitted: Metric: Face Fabric Weight; Value: Not Provided; Unit: g/m²; Value Type: Weight; Basis: Per Square Metre; Applies To: Roman Blind face fabric (all ranges); Evidence Status: Supplier data required; Notes: composition and width were found for every fabric range but weight was not, despite a direct targeted search; confirmed next step is asking the supplier directly.

  **Rod count and cord count by drop band** — explicitly recorded as absent, not silently omitted: Metric: Rod Count; Value: Not Provided; Unit: count; Value Type: Count; Basis: By Drop Band; Applies To: Roman Blind body; Input Variables: Finished Drop; Evidence Status: Supplier data required; Notes: actual drop-band boundaries and rod counts were not included in the material provided to Claude Code (see §5's Structured Technical Value worked example 4, which shows the intended schema pattern without inventing figures to fill it). Metric: Cord Count; Value: Not Provided; Unit: count; Value Type: Count; Basis: By Drop Band; Applies To: Roman Blind body; Input Variables: Finished Drop; Evidence Status: Supplier data required; same treatment.

  **Motor specifications** — explicitly recorded as absent, not silently omitted: the design brief refers to "the three named motors found," but no motor names, torque, voltage, width/drop range, battery life, or warranty figures were included in the material provided to Claude Code. Metric: Motor Specification (torque, voltage, width/drop range, battery life, warranty); Value: Not Provided; Value Type: Text Rule; Applies To: Roman Blinds (all motorised constructions); Evidence Status: Supplier data required; Notes: three motors were referenced as found per the design brief, but their names and specifications were not supplied to Claude Code for transcription. Full named detail belongs here (not in MCD-01B-03) once supplied.

- **Evidence:** Primary supplier technical documentation (lining weights, recess deductions, tolerance, fabric range summary); none yet for face fabric weight, rod/cord count, or motor specifications.
- **Source Reference:** Not provided to Claude Code — supplier name and specific source document title pending from Nazmil Ghany (see Decision Register).
- **Validation Status:** Confirmed (lining weights, recess deductions, tolerance, fabric range summary); Supplier data required (face fabric weight, rod/cord count, motor specifications); Source Reference outstanding throughout.
- **Revision History:** 14 Jul 2026 — record created during MCD-04 structured technical value population.

### 7.8 Future Entries (other product families)

Roller Blinds, Curtains, Pleated Blinds, Perfect Fit Systems, and Shutters have no populated records yet. These will be added as their own supplier capability evidence is gathered, following the same document architecture established here.

## 8. Decision Register

Maintained in accordance with MCD-00A conventions as established in MCD-01B-01 §17 and MCD-01B-02 §23 (MCD-00A itself was not available in the repository at time of writing — see the row below). Format: Date | Decision | Reasoning | Raised By.

| Date | Decision | Reasoning | Raised By |
|---|---|---|---|
| 14 Jul 2026 | MCD-04 is established as the deliberate exception to Constraint 2 (Product Specification supplier-independence): supplier names, trademarks, brand names, part numbers, model numbers, and source URLs are expected and required in this document, not a violation of Solara's supplier-independence principle. | Product Specifications (MCD-01B-xx) must stay supplier-neutral so quotations/customer-facing behaviour and internal engine logic never leak commercial specifics; that neutrality is only sustainable if the supplier-specific evidence it depends on is recorded somewhere authoritative. MCD-04 is that somewhere. Stated explicitly here, in MCD-04's own Scope (§2), so a future review pass does not mistakenly "clean up" this document the way MCD-01B-02 was cleaned up. | Design brief (claude-code-brief-MCD-04.md) |
| 14 Jul 2026 | Only one record is populated in this first draft (Vertical Blinds → Vogue → Motorised Tilt Operation). All other nodes in §7 and §6 are left as empty Future Entries rather than populated with placeholder or speculative content. | The document architecture should grow from real, evidence-backed records added over time, not be speculatively designed now. An empty node accurately represents "not yet gathered"; a placeholder record would misrepresent it as "gathered but thin." | Design brief (claude-code-brief-MCD-04.md) |
| 14 Jul 2026 (open) | MCD-00A (Project Development Standards) was not present in the repository when this document was drafted. | MCD-04's own Dependencies and Governance sections both require MCD-00A. Governance, versioning, and Decision Register format conventions were instead inherited from their established use in MCD-01B-01 and MCD-01B-02 (which themselves cite MCD-00A for these same conventions), rather than fabricated. If MCD-00A's actual content differs from the inherited conventions once available, this document's §8 format and version-history style may need reconciliation. | Claude Code — flagged for Nazmil Ghany; not a content defect, a missing-dependency note |
| 14 Jul 2026 | The Structured Technical Value block type (§5) generalizes the earlier weight-only convention into a single reusable block covering weight, length, count, dimensional deductions, and load limits, with a new Value Type field added beyond the original design. | Prevents a proliferation of near-identical, data-type-specific blocks as more product families are added; explicitly stated as applicable to all future product families (Roller, Vertical, Curtains, Shutters, motor and bracket-spacing data generally), not a Roman-only addition, per the design brief (claude-code-brief-MCD-04-structured-technical-value.md). | Design brief (claude-code-brief-MCD-04-structured-technical-value.md) |
| 14 Jul 2026 | Worked example 4 (Rod count) in §5 does not carry "Evidence Status: Supplier Confirmed" with fabricated band boundaries, despite the brief's literal field-value instruction. | The brief supplied real figures for worked examples 1, 2, 3, and 5 (135 g/m², the two chain-length formulas, 10kg) but not for Rod Count's actual drop-band boundaries and counts — only the schema pattern. Asserting invented numbers as "Supplier Confirmed" would violate this project's standing discipline against inventing unevidenced thresholds (the same discipline that removed the 1500mm Cassette motor-capacity figure from MCD-01B-03 §13.3). The schema pattern is documented; the real Roman rod/cord-count data is recorded as Not Provided in §7.7 instead. | Claude Code — flagged for Nazmil Ghany; a deliberate deviation from a literal instruction, not an oversight |
| 14 Jul 2026 | Roman Blinds (§7.3–§7.7) is populated using real confirmed values supplied in this brief and the prior breakaway-note brief (dimensional limits for Standard and Breakaway, No-Drill's 10kg weight limit, both chain-length formulas, five lining weights, recess deductions, manufacturing tolerance, and the fabric range summary). No supplier name or specific source document title was supplied anywhere in either brief's text, so every record's Source Reference field reads "Not provided to Claude Code" rather than a fabricated name or title. | Per this project's standing discipline against inventing evidence: real given values are transcribed faithfully; fields for which no real value was supplied are marked Not Provided rather than filled with a plausible-sounding placeholder. This applies even though MCD-04 is the designated location where supplier names and document titles are expected to appear freely — the exception permits naming a real supplier, it does not permit inventing one. | Claude Code — flagged for Nazmil Ghany; source attribution for all Roman entries is an open item pending supply of the actual supplier name and document title(s) |
| 14 Jul 2026 (open) | No-Drill and Cassette Headrail dimensional limits (§7.5, §7.6), No-Drill/Cassette's sharing (or not) of Standard's chain-length formula, lining width and composition detail per lining type (§7.7), face fabric weight in GSM (§7.7), rod and cord count by drop band (§7.7), and motor specifications for the three motors referenced in the brief (§7.7) are recorded as explicit Not Provided / Supplier data required entries rather than silently omitted or invented. | Neither brief supplied these specific values; the brief's own explicit instruction for face fabric weight ("do not leave this silently absent; state clearly") is applied consistently to every other value gap found during this population pass, not just the one item explicitly flagged. | Claude Code — awaiting Nazmil Ghany |

## 9. Version History

| Version | Summary |
|---|---|
| 0.1 Draft Skeleton | Initial MCD-04 document architecture established per the design brief (claude-code-brief-MCD-04.md): Purpose, Scope (with the Constraint 2 exception stated explicitly), Relationship to MCD-01A/MCD-01B-xx, Governance, Record Structure (seven fields), and Document Organisation (product-architecture-first tree). Populated exactly one record — Vertical Blinds → Vogue → Motorised Tilt Operation — matching the resolved MCD-01B-02 §23 Decision Register entry, including the confirmed 3m/200mm limits and the supplier-capability-vs-Solara-restriction distinction on louvre width (89mm Solara restriction vs. supplier support for both 89mm and 127mm). All other Construction Variants and product families left as empty Future Entries. MCD-01A, MCD-01B-01, and MCD-01B-02 were not modified. |
| 0.1 Draft Skeleton | Corrected the MCD-01B-02 dependency reference from Draft v1.2 to v1.3 Approved Draft Baseline, reflecting its promotion after this document was first drafted. |
| 0.2 Draft Skeleton | Schema generalization plus first Roman data population pass, per claude-code-brief-MCD-04-structured-technical-value.md. Part 1: added the Structured Technical Value block type to §5 (Metric, Value, Unit, Value Type, Basis, Applies To, Calculation Rule, Input Variables, Minimum, Maximum, Evidence Status, Source Reference, Notes) as a generalized, product-family-agnostic schema enhancement, with five worked examples. Part 2: populated Roman Blinds (§7.3–§7.7, matching MCD-01B-03's construction classification, with Breakaway Control explicitly labelled a Configuration-layer grouping node rather than a Construction Variant) with confirmed dimensional limits for Standard and Breakaway, No-Drill's 10kg weight limit, both chain-length formulas, five lining weights, recess deductions, manufacturing tolerance, and a fabric range summary (per this brief's own instruction, not a per-fabric transcription of the ~100-row range table). No supplier name or source document title was supplied in either brief, so every Roman record's Source Reference reads "Not provided to Claude Code" rather than a fabricated attribution. Face fabric weight, rod/cord count by drop band, motor specifications, No-Drill/Cassette dimensional limits, and No-Drill/Cassette's chain-length-formula sharing are recorded as explicit Not Provided / Supplier data required entries, extending the brief's own face-fabric-weight disclosure discipline consistently rather than silently omitting other gaps. MCD-01A, MCD-01B-01, MCD-01B-02, and MCD-01B-03 were not modified. |
