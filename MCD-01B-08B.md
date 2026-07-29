Document ID: MCD-01B-08B
Document Title: Side-Guide Window-Mounted Aluminium Venetian Blind
Status: Working Draft — Unverified
Version: 0.2 (research stage — partial ratification, not promoted)
Parent Document: MCD-01A — Sales MVP Product Engine Architecture
Family Document: MCD-01B-08 — Frame-Mounted and Window-Mounted Blind Systems (Side-Guide Window-Mounted System Construction Group)
Base Product Specification: MCD-01B-06 — Metal Venetian Blinds
Last Updated: 28 July 2026 (v0.2)

## Dependencies
- MCD-00 — Executive Charter
- MCD-00A — Project Development Standards (not present in repository at time of writing — see Decision Register)
- MCD-01A — Sales MVP Product Engine Architecture (v1.5, Approved Draft Baseline)
- MCD-01B-06 — Metal Venetian Blinds Product Specification (v1.1, Approved Draft Baseline – Product Specification), the base product specification this document inherits its Aluminium Venetian technology rules from and does not duplicate, per MCD-01B-08 §5's own Blind-Technology routing table ("Aluminium Venetian → references MCD-01B-06 (Metal Venetian)")
- MCD-01B-08 — Frame-Mounted and Window-Mounted Blind Systems, Family Architecture (v1.0, Approved Draft Baseline – Product Specification), the family document this document inherits its Side-Guide Window-Mounted System Construction Group from, and whose ratified "Perfect Fit" controlled-reference precedent (19 Jul 2026) this document applies to its own supplier system by the same reasoning
- MCD-01B-08A — Side-Guide Window-Mounted Pleated & Cellular Blind (v0.1, Working Draft — Unverified), the sibling variant under the same Construction Group and the same supplier system; referenced for consistency of treatment, **not modified by this task**
- MCD-04 — Product Library & Supplier Management (v0.8, Draft Skeleton) — the designated home for this construction's exact supplier system, company, product, and code detail. **Not modified by this task** — see Decision Register (DR-09) for the MCD-04 follow-up this research stage now requires.

## Research-Stage Scope Statement

**This document is a research-stage working draft. It is not a finalised product specification.**

It was created from `mcd-01b-08b-research-handover.md`, which is explicitly a research-stage handover and not an implementation brief. Per that handover's own controlling instruction, this document deliberately does **not**:

- finalise the product specification;
- constitute, contain, or prepare a Claude Code implementation brief;
- define application validation logic, or convert any unresolved evidence into an application validation rule;
- treat the 250mm minimum width as permanently resolved;
- activate the folding-handle or handle-free options.

Everything recorded below is separated into three deliberately distinct registers, and that separation is the primary purpose of this draft:

1. **§4 Verified Supplier Rules** — supplier-confirmed facts, recorded as verified.
2. **§5–§8 Provisional Interpretations and Controlled Treatments** — reasonable working positions that are explicitly *not* confirmed and must not be implemented as-is.
3. **§9 Evidence Conflict Register** and **§10 Open Evidence Register** — unresolved conflicts and open questions, preserved in full.

Nothing in §5–§8 is a rule the application may act on. Where the handover proposes future validation behaviour, it is recorded here as *proposed and inactive*, attributed to the handover, and explicitly marked as requiring resolution of the underlying evidence before it could ever become a rule.

This document must remain **Working Draft — Unverified** until the supplier conflicts, installation-route rules, handle options, warranty, lead time, and remaining compatibility requirements have been reviewed.

## Documentation Conventions: Advisor Selection / Derived Default / Supplier Capability

Consistent with every other product specification in this project, the following three terms are used throughout this document as **documentation conventions only** — they are not new architectural layers and do not modify MCD-01A §3:

- **Advisor Selection** — a value the advisor actively chooses. Architecturally, this is the Configuration layer (or, where the choice changes construction, the Construction/System layer).
- **Derived Default** — a value the system determines automatically from an Advisor Selection, without a separate question. Architecturally, this is the Accessory Engine and/or Supplier Capability Engine resolving a compatible component or value from an existing Configuration selection.
- **Supplier Capability** — the actual data (dimensions, weights, compatibility, pricing, availability) that makes a Derived Default resolvable. Architecturally, this is the Supplier Capability Engine (MCD-01A §5.9) and the Supplier Capability Library, maintained in MCD-04.

## Neutral Document Identity Statement

This is a Product Specification governed by MCD-01A. The exact recognisable supplier system name, supplier construction-system name, and supplier company name for this construction do not appear anywhere in this document — not as its title, not as neutral construction or operation terminology, not in the Decision Register, not in the Evidence Conflict Register, not in Open Evidence Items, not in Version History. They are recorded exclusively in MCD-04.

This applies MCD-01B-08's own ratified (19 Jul 2026) "Perfect Fit" controlled-reference precedent, and its sibling MCD-01B-08A's identical application of that precedent to this same supplier system, by the same reasoning: a supplier system name may be referenced in a neutral document only when naming an excluded or separately governed family (e.g. "Perfect Fit," "INTU," already permitted throughout this project as controlled references to excluded families) or when cross-referencing where the real capability is governed (MCD-04) — never as the document's own identity or as neutral construction terminology. No alternative supplier-adjacent label, close variant, or respacing is substituted either.

**The research handover asked for the opposite on this specific point.** That conflict is genuine, is not silently resolved here, and is recorded in full in the Decision Register (DR-01), including the distinction between a governance document's identity and a separate advisor-facing display name — which is itself recorded here as a real requirement, with only the name string held in MCD-04.

---

## 1. Product Definition

This product is a screw-free, window-mounted Aluminium Venetian blind using a fixed top profile, a moving bottom profile, and independent side guides, with the blind tensioned and raised from the bottom up. Slat angle is controlled by a tilt rod; raising and lowering is controlled by a handle on the moving bottom profile. No pull cords or chains are operated by the customer.

It is not: a complete joined perimeter frame (that is the Full-Frame Bead-Mounted System, a different Construction Group under MCD-01B-08); a conventional recess- or face-fixed Metal Venetian blind (that is MCD-01B-06, this document's base specification); an INTU or Micro INTU system; a Pleated or Cellular product (that is the sibling variant MCD-01B-08A, a different Blind Technology under the same Construction Group).

## 2. Document Classification and Family Position

This is a **Product Specification**, not a Construction Group definition and not a family architecture document.

- **Construction Group:** Side-Guide Window-Mounted System — inherited from MCD-01B-08 §2, already ratified 19 Jul 2026. This document does not re-litigate that classification, and does not restate its three-test reasoning.
- **Blind Technology:** Aluminium Venetian — the orthogonal axis defined in MCD-01B-08 §5, which routes explicitly to MCD-01B-06 (Metal Venetian) as the base specification. This document inherits MCD-01B-06's Aluminium Venetian technology rules and records only what the side-guide window-mounted construction itself changes or adds.
- **Sibling variant:** MCD-01B-08A (Pleated & Cellular) sits alongside this document under the same Construction Group and the same supplier system, with a different Blind Technology and a different base specification. MCD-01B-08A §4 and its DR-04 already reserved Aluminium Venetian for this document specifically. That reservation is now taken up. **MCD-01B-08A is not modified by this task** — see DR-06 and DR-09 for two findings that affect it and are flagged rather than applied.

## 3. Advisor-Facing Product Naming

The research handover specifies that this product carries a **distinct advisor-facing display name**, different from this document's neutral governance title, and that a separate internal supplier construction-system reference also exists which must *not* replace the familiar name in the sales or survey workflow.

Both of those are recorded here as **verified requirements**:

- A distinct advisor-facing display name exists for this product and is what advisors see in the sales and survey workflow.
- A separate internal supplier construction-system reference exists, and is an internal engineering/supplier reference only — it must not surface as the advisor-facing name.

The **name strings themselves** are supplier trademarks and are held in MCD-04, not here, per the Neutral Document Identity Statement above. This is the same distinction MCD-01B-08A §12 already drew: advisor-facing supplier display is a legitimate internal UI concern, and is unaffected by — and does not require loosening — the governance documents' supplier-neutrality rule. See Decision Register (DR-01).

## 3A. Application Contexts (Not a Platform Category)

Ratified per Decision Register (DR-03): this document distinguishes four separate things, and none of them substitutes for another.

- **Product:** aluminium Venetian blind.
- **Construction Group:** side-guide window-mounted system (MCD-01B-08 §2, ratified).
- **Application contexts:** bi-fold doors, tilt-and-turn windows, and other compatible glazed frames. An application context describes where and to what the product is fitted — it is not a platform or family classification, and it does not change this document's Construction Group or Blind Technology classification (§2).
- **Supplier or commercial family name:** managed separately in MCD-04, not recorded here.

"Bi-fold door," specifically, is an application context only. It must not be read, here or elsewhere in this document, as this product's governing platform category.

---

## 4. Verified Supplier Rules

Everything in this section is recorded by the research handover as supplier-verified. Nothing in this section is provisional.

### 4.1 Verified Product Classification

| Classification field | Controlled value |
|---|---|
| Product family | Venetian Blind |
| Installation family | Side-Guide Window-Mounted System (see naming note below) |
| Slat material | Aluminium |
| Slat width | 25mm |
| Operation | Manual |
| Raising configuration | Tensioned Bottom Up |
| Headrail | Fixed top profile / headrail |
| Slat control | Tilt rod |
| Raising/lowering control | Handle on moving bottom profile |
| Pull cords or chains | None used by the customer |
| Installation route 1 | Beading brackets / clips |
| Installation route 2 | Adhesive tape |
| Ordering measurement methods | Glass size, or Glass (hidden seal) |
| Manufacturing tolerance | ±3mm width and drop |
| Maximum area | 3m² |

*Naming note:* the handover's "Installation family" value is the supplier system name. The neutral equivalent recorded here is the Construction Group name already ratified in MCD-01B-08 §2; the supplier system name for that same family is in MCD-04.

### 4.2 Verified Base Dimensional Limits

| Metric | Value |
|---|---|
| Maximum width | 1,500mm |
| Minimum drop | 150mm |
| Maximum drop | 2,300mm |
| Maximum area | 3m² |
| Manufacturing tolerance | ±3mm, width and drop |

Minimum width is **not** listed here — it is disputed between source documents and is recorded in §5.1 and §9 instead.

### 4.3 Verified Profile Dimensions

| Component | Width | Height |
|---|---|---|
| Side guide | 14mm | 8mm |
| Bottom profile | 22mm | 22mm |
| Fixed top profile | 25mm | 24mm |

These are verified internal construction dimensions, retained for obstruction checks, survey guidance, installation documentation, technical support, and future graphical diagrams. They are not required in the basic sales workflow unless a compatibility check calls for them.

### 4.4 Verified Profile Colours

Verified profile colours: **White, Black, Anthracite, Grey, Nobel.** Default profile colour is **White** unless another colour is specified.

Verified RAL references: **Anthracite — RAL7016; Nobel — RAL7022.**

**Controlled wording caution (verified, and material):** other components are described by the supplier as *closely matched* to the profile colour. The system must not represent every component as an exact RAL match. This wording distinction is itself part of the verified evidence and must survive into any customer- or advisor-facing text.

### 4.5 Verified Measurement Method

Standard glass measurement: the surveyor measures width at the top, middle, and bottom; drop at three positions across the glass; **the smallest measurement is ordered**; beading and rubber seals are not included in the standard visible-glass measurement.

### 4.6 Verified Handle Facts

The following handle facts are verified. **Availability of two of the options is not** — see §7 and §10.

- A standard handle is supplied as the default.
- A folding handle exists, at an additional surcharge (availability unconfirmed — §7).
- A no-handle ordering option exists (availability unconfirmed — §7).
- Handle quantity: up to 1,200mm width, one handle per moving profile; over 1,200mm width, two handles.
- Handles consist of a handle and an insert.

Verified profile-to-standard-handle colour matching:

| Profile colour | Standard handle colour |
|---|---|
| White | White |
| Grey | Clear |
| Nobel | Clear |
| Anthracite | Anthracite |
| Black | Black |

### 4.7 Verified Obstruction Clearance

At least **35mm** is required between the glass depth/reference and an obstruction such as a window handle.

The 35mm figure is verified. The **exact measurement datum is not** — the supplier wording refers both to the edge of the beading and to the depth of the glass. See §5.4 and §10 item 4.

---

## 5. Provisional Interpretations and Controlled Treatments

**Nothing in this section is confirmed. Nothing in this section may be implemented as an application rule.** Each item records a controlled working position and the specific evidence that must be obtained before it could be resolved.

### 5.1 Minimum Width — Provisional 250mm

**Provisional controlled value: 250mm minimum width. Not permanently resolved.**

Reasoning as supplied: 250mm is supported by both the dedicated product specification and the later product leaflet, while only the measuring instructions state 200mm. The 250mm figure is therefore the safer controlled value at research stage.

**The 200mm minimum width must not be implemented.** Equally, the 250mm value must not be treated as settled: it is a provisional control pending supplier clarification, not a verified limit. The 200–249mm band is treated as unavailable at research stage, on the strength of the provisional control only — this is a holding position, not a validated restriction.

See §9 for the full conflict record and §10 item 1 for the open action.

### 5.2 Coupled Maximum-Size Restrictions — Proposed, Not Active

The measuring guide records two coupled restrictions:

- A width of 1,500mm is only available up to a maximum drop of 2,000mm.
- A drop of 2,300mm is only available up to a maximum width of 1,300mm.

The handover proposes that these eventually become validation rules rather than information text, **once this document leaves research stage**. They are therefore recorded here as **proposed and inactive**, attributed to the handover, and are not written as rules this document imposes.

**A discrepancy was found inside the handover's own material and is not smoothed over here.** The supplier wording above constrains specific endpoint values (a *1,500mm* width; a *2,300mm* drop). The handover's own proposed rule text instead constrains ranges — "if width > 1,300mm, drop must not exceed 2,000mm." These are not equivalent, and the handover's claim that the two coupled statements are "logically equivalent around the same restricted size zone" does not hold at the boundary. A worked counter-example: width 1,400mm × drop 2,100mm is 2.94m² (inside the 3m² maximum), is not a 1,500mm width, and is not a 2,300mm drop — so the supplier wording does not clearly exclude it, while the handover's proposed rule does. Which reading is correct materially changes the available size envelope. See Decision Register (DR-05) and §10 item 13.

**Ratified controlled treatment, per `claude-code-brief-MCD-01B-08B-ratification.md` — a confirmed treatment of an unresolved question, not a resolution of the question itself.** Two distinct statuses apply here and must not be conflated:

1. **Confirmed treatment:** the two supplier statements are recorded in **endpoint form only**, exactly as written, and no other form:
   - a width of 1,500mm is only available up to a maximum drop of 2,000mm;
   - a drop of 2,300mm is only available up to a maximum width of 1,300mm.
   The broader interpreted rule (width above 1,300mm → maximum drop 2,000mm; drop above 2,000mm → maximum width 1,300mm) **must not be implemented as verified logic** — it is a stricter reading than the supplier's literal wording supports.
2. **Still open:** the underlying supplier ambiguity itself is **not resolved** by recording the endpoint-only treatment. The intermediate boundary region — width above 1,300mm and below 1,500mm, **and** drop above 2,000mm and below 2,300mm — remains unresolved pending supplier clarification. **No automatic pass or fail rule may be inferred for that region** from either supplier statement without further supplier evidence. This is recorded explicitly so a future implementation pass cannot mistake the endpoint statements for a complete rule set.

### 5.3 Gasket Rule as a Measurement-Method Selector — Provisional

The handover records a controlled decision rule treating rubber-gasket protrusion onto the glass as a **selector between two measurement methods**, not as an automatic product rejection:

- protrusion below 2mm → the "Glass (hidden seal)" ordering method;
- protrusion of 2mm or more → the "Glass size" ordering method.

The reasoning supplied: the original specification states that square-frame windows should have at least 2mm of rubber bead protruding onto the glass, while the newer measuring guide explains how to order where less than 2mm is present. The newer guidance therefore refines the earlier statement, and demonstrates that less than 2mm is not necessarily a failed survey.

This is recorded as a **provisional interpretation**, not a verified rule, because it is a reading of how two supplier documents of different vintages relate to one another rather than a single explicit supplier statement.

**This materially affects the sibling document MCD-01B-08A, which is not modified by this task.** See Decision Register (DR-06).

### 5.4 35mm Clearance Datum — Provisional

The 35mm value is verified (§4.7). The **datum it is measured from is not**: the supplier wording refers both to the edge of the beading and to the depth of the glass, which are different reference points and would yield different survey outcomes on the same window.

Provisional treatment: capture the clearance as an advisor-facing survey value, and treat the datum as unresolved. The datum must be visually confirmed from the guide before any survey illustration, advisor wording, or compatibility behaviour is finalised. See §10 item 4.

### 5.5 Fixing Routes — Selectability Unresolved

Two installation routes are verified to exist (beading brackets/clips; adhesive tape). What is **not** established is whether the route is an Advisor Selection, or is determined by the factory/system from the survey data.

This is a genuine architectural question, not merely a data gap: it determines whether the fixing route is a Configuration-layer selection presented to the advisor at all. It is deliberately **not** answered here, because the evidence to answer it does not exist yet. See §10 items 5 and 6.

Note for whoever resolves it: MCD-01B-08A DR-09 concluded, for the sibling Pleated/Cellular variant, that the two fixing routes are Configuration-layer rather than Construction-defining. That conclusion is about the *classification layer*, not about who chooses — it does not answer this question and must not be treated as having answered it.

---

## 6. Controlled Product-Rule Structure — Research Snapshot

Recorded as a **research snapshot for review**, not as an implementable rule set. Provisional and unresolved values are marked inline.

- Product family: Venetian Blind
- Construction Group: Side-Guide Window-Mounted System (MCD-01B-08 §2, ratified)
- Blind Technology: Aluminium Venetian → base specification MCD-01B-06
- Advisor-facing display name / internal construction-system reference / supplier company: **held in MCD-04** (§3, DR-01, DR-09)
- Material: Aluminium — *verified*
- Slat size: 25mm — *verified*
- Operation: Manual — *verified*
- System configuration: Tensioned Bottom Up — *verified*
- Headrail: Fixed — *verified*
- Slat control: Tilt rod — *verified*
- Blind movement: Handle-operated moving bottom profile — *verified*
- Fixing methods: beading clips/brackets; adhesive tape — *verified that both exist; selectability unresolved (§5.5)*
- Measurement methods: Glass size; Glass (hidden seal) — *verified*
- Minimum width: 250mm — **PROVISIONAL, disputed (§5.1, §9)**
- Maximum width: 1,500mm — *verified*
- Minimum drop: 150mm — *verified*
- Maximum drop: 2,300mm — *verified*
- Maximum area: 3m² — *verified*
- Coupled restrictions — **PROPOSED, INACTIVE, and internally inconsistent in the source material (§5.2)**
- Minimum glass-to-handle clearance: 35mm — *verified value; datum unresolved (§5.4)*
- Manufacturing tolerance: ±3mm width and drop — *verified*

**Platform category discrepancy, ratified as an application context (DR-03):** the handover's own rule-structure block assigns this product to a platform category pairing a door type with the supplier system name. That does not match the Construction Group already ratified in MCD-01B-08 §2, under which this document sits, and no supporting evidence for the pairing was supplied. It is **not** adopted as this document's classification. Ratified treatment: "bi-fold door" is an application context — see §3A — alongside tilt-and-turn windows and other compatible glazed frames, not a platform or family classification. This document's classification remains the ratified Construction Group.

---

## 7. Options Explicitly Not Activated

The following exist in supplier material but are **not available** and must not be presented, quoted, or configured:

| Option | Status | Reason |
|---|---|---|
| Folding handle (surcharge) | **Not activated** | Leaflet states availability but also displays "Coming Soon" adjacent to the content — availability is contradicted within a single source |
| Handle-free / no-handle ordering | **Not activated** | Same contradiction, same source |

The standard handle remains the only handle treatment carried forward at research stage. Neither option may be activated until current ordering or price-book evidence confirms it is live. See §10 items 2 and 3.

The handle-quantity and handle-colour-matching facts in §4.6 are verified and are unaffected by this — they describe the standard handle, which is not in question.

---

## 8. Shared Service Profile — Deliberately Deferred

No Shared Service Profile is drafted in this document.

This is a deliberate omission, not a gap. The research handover's controlling instruction lists exhaustively what this stage is suitable for — creating the initial working draft, recording verified rules, adding the evidence conflict register, structuring open questions, and holding the status at Working Draft — Unverified. Drafting a twelve-service profile would require settled positions on measurement method selection, fixing-route selectability, handle availability, and dimensional validation, **all four of which are unresolved above**. Producing Configured/Extended conclusions on top of disputed inputs would manufacture exactly the false settledness this stage exists to avoid.

The Shared Service Profile is therefore reserved for the specification stage, once the Open Evidence Register is closed. Recorded as §10 item 14.

---

## 9. Evidence Conflict Register

| # | Conflict | Sources in disagreement | Controlled treatment | Open action |
|---|---|---|---|---|
| C-1 | **Minimum width: 200mm or 250mm** | Product specification: 250mm. Product leaflet: 250mm. Measuring instructions: 200mm. | Use **250mm provisionally** — supported by two of three sources, including the dedicated product specification. Treat 200–249mm as unavailable at research stage. Do **not** implement 200mm. Do **not** treat 250mm as permanently resolved. | Obtain supplier clarification before closing research |
| C-2 | **Folding-handle and handle-free availability** | Leaflet states both are available; the same leaflet displays "Coming Soon" adjacent to that content. | Both options **not activated** (§7). | Confirm against current ordering or price-book evidence |
| C-3 | **Coupled size restriction — endpoint values vs. ranges** | Supplier wording constrains 1,500mm width / 2,300mm drop specifically; the handover's own proposed rule constrains width > 1,300mm / drop > 2,000mm. These are not equivalent at the boundary (§5.2). | **Treatment confirmed by Nazmil Ghany, 26 Jul 2026:** record the endpoint-only statements as the controlled treatment; the broader range-based rule must not be implemented as verified logic. **Underlying ambiguity remains open, not resolved by that treatment:** the intermediate boundary region (width 1,300–1,500mm **and** drop 2,000–2,300mm) has no confirmed pass/fail rule. | Obtain supplier clarification for the intermediate boundary region before any pass/fail rule is inferred for it |
| C-4 | **35mm clearance datum** | Supplier wording refers both to the edge of the beading and to the depth of the glass. | Value verified; datum unresolved (§5.4). | Visually confirm the datum from the measuring guide |
| C-5 | **2mm gasket protrusion — compatibility gate or measurement-method selector** | The original specification frames 2mm as a square-frame requirement; the newer measuring guide explains how to order below 2mm. | Provisionally treated as a **measurement-method selector**, not an automatic rejection (§5.3). | Confirm the refinement is intended, and reconcile with MCD-01B-08A's own treatment (DR-06) — without modifying MCD-01B-08A as a side effect |

---

## 10. Open Evidence Register

All items from the research handover are preserved. Items 13 and 14 were identified during this drafting pass and are added rather than folded into existing items.

1. Minimum width conflict: 200mm versus 250mm.
2. Folding handle availability: live option, or still "coming soon".
3. Handle-free availability: live option, or still "coming soon".
4. Exact 35mm clearance measurement datum.
5. Whether adhesive tape and beading-clip routes are advisor-selectable or factory/system-determined.
6. Window and bead compatibility requirements for each fixing route.
7. Whether square, shaped, rounded, or unusual glazing beads are restricted.
8. Whether tilt-and-turn and bi-fold suitability requires additional clearance checks.
9. Whether every listed 25mm slat colour is currently orderable in this construction.
10. Current pricing, surcharges, and supplier ordering codes.
11. Warranty and lead time.
12. Any exclusions relating to glass type, frame type, vents, or seals.
13. **(Added during drafting; treatment confirmed 26 Jul 2026, underlying ambiguity still open — two distinct statuses, not to be conflated.)** Treatment confirmed: the coupled size restriction is recorded in endpoint-only form (§5.2), and the broader range-based reading must not be implemented as verified logic. Still open: which rule, if any, governs the intermediate boundary region (width 1,300–1,500mm and drop 2,000–2,300mm) — the supplier's endpoint wording does not itself state a rule for that region, and none may be inferred without further supplier evidence.
14. **(Added during drafting)** The Shared Service Profile, deliberately deferred to the specification stage (§8).

Also standing, and recorded separately below rather than as product evidence items: the MCD-04 population follow-up (DR-09), the MCD-01B-08A cross-impact finding (DR-06), the advisor-facing naming ratification (DR-01), and the MCD-00A repository dependency.

**This product remains Working Draft — Unverified until these matters are checked.**

---

## 11. Decision Register

| Date | Decision | Reasoning | Raised By |
|---|---|---|---|
| 28 Jul 2026 (confirmed by Nazmil Ghany, 26 Jul 2026) | **DR-01 — Document identity: this document is supplier-neutral, contrary to the research handover's explicit instruction. Flagged, not silently applied either way.** The handover instructs that the supplier system name be used as the advisor-facing product name, names a supplier construction-system reference, and names the supplier company. Following that literally would put all three into a governance Product Specification. That directly contradicts (a) the project-wide supplier-neutrality rule for MCD-01B-xx documents, (b) MCD-01B-08's ratified (19 Jul 2026) "Perfect Fit" controlled-reference rule, and (c) this document's own direct sibling MCD-01B-08A, which applied that precedent to **this same supplier system** and was verified clean of it — including the deliberate removal of the name even from quoted source-document filenames. Two sibling variants of one Construction Group and one supplier system cannot coherently apply opposite naming rules. **Resolution applied:** this document is neutral; the name strings live in MCD-04. **What is preserved from the handover, rather than discarded:** the requirement that a distinct advisor-facing display name exists, and that the internal construction-system reference must not replace it in the sales or survey workflow, are both recorded as verified requirements in §3 — only the *strings* are relocated. This distinction is already established: MCD-01B-08A §12 treats advisor-facing supplier display as an internal UI concern that neutrality does not restrict. The handover was almost certainly written to capture supplier research rather than to revisit ratified naming governance, but the conflict is real and is not resolved unilaterally in either direction. **If Nazmil Ghany ratifies the handover's naming instead, this document's title and §3 change and MCD-01B-08A must change with it — the two must not diverge.** **Ratified, per `claude-code-brief-MCD-01B-08B-ratification.md`, with the following supporting confirmation appended alongside the analysis above:** the neutral drafting is confirmed — the governance document remains supplier-neutral, titled "Side-Guide Window-Mounted Aluminium Venetian Blind." The research handover's earlier instruction to place the supplier system name directly into this neutral governance document as the advisor-facing product name is **formally withdrawn**: it conflicted with the ratified supplier-neutrality rule, with MCD-01B-08's ratified controlled-reference precedent, and with MCD-01B-08A, which had already applied that rule to this same supplier system. Two sibling variants of one Construction Group cannot run opposite naming rules. The following remain recordable in this document as verified product requirements — this is what the withdrawn instruction was correctly protecting, and it survives intact: (a) the application must provide a distinct advisor-facing product name; (b) the internal construction-system reference must not replace that familiar advisor-facing name in the sales or survey workflow; (c) the actual supplier-facing and advisor-facing name strings belong in MCD-04, not in the neutral product specification. | The handover's naming instruction conflicts with a ratified project rule and with the sibling document governing the same supplier system; per this project's standing practice, a brief/rule conflict is flagged and reasoned, never silently obeyed or silently ignored — Claude Code | Claude Code — raised and reasoned; **confirmed by Nazmil Ghany, 26 Jul 2026** |
| 28 Jul 2026 | **DR-02 — Document classification and family position.** Product Specification under the Side-Guide Window-Mounted System Construction Group (MCD-01B-08 §2, ratified 19 Jul 2026), with Aluminium Venetian as the Blind Technology routing to MCD-01B-06 as base specification. This is not a new judgment: MCD-01B-08 §5's own Blind-Technology table already states "Aluminium Venetian → references MCD-01B-06 (Metal Venetian)," and MCD-01B-08A DR-04 already reserved Aluminium Venetian for this document specifically, on the grounds that it inherits from a materially different base specification than Pleated/Cellular. This document takes up that reservation without re-litigating either conclusion. | Both the Construction Group and the Blind-Technology routing were already ratified elsewhere; confirming rather than re-testing them | Research handover (mcd-01b-08b-research-handover.md); MCD-01B-08 §5; MCD-01B-08A DR-04 |
| 28 Jul 2026 (confirmed by Nazmil Ghany, 26 Jul 2026) | **DR-03 — Platform category discrepancy recorded, not adopted; ratified as an application context.** The handover's controlled rule-structure block assigns this product to a platform category pairing a door type with the supplier system name. No supporting evidence for that pairing was supplied anywhere in the handover, and it does not correspond to the Construction Group already ratified in MCD-01B-08 §2. Adopting it would introduce an unevidenced classification axis into a research-stage draft. Recorded in §6 as a discrepancy for review; this document's classification remains the ratified Construction Group. **Ratified, per `claude-code-brief-MCD-01B-08B-ratification.md`, with the following supporting confirmation appended alongside the analysis above:** the door-type/supplier-system pairing is **demoted from platform category to application context**, and does not define this product's neutral platform classification. The document distinguishes four separate things, which must not be collapsed into one another: **Product** — aluminium Venetian blind; **Construction Group** — side-guide window-mounted system; **Application contexts** — bi-fold doors, tilt-and-turn windows, and other compatible glazed frames; **Supplier or commercial family name** — managed separately in MCD-04. A bi-fold door describes an application the product is fitted to, not the product's governing category. See §3A, where the application contexts are recorded on that ratified basis. | Per this project's standing discipline: a classification asserted in a brief without supporting evidence, and inconsistent with ratified architecture, is recorded and flagged rather than adopted | Claude Code — raised and reasoned; **confirmed by Nazmil Ghany, 26 Jul 2026** |
| 28 Jul 2026 | **DR-04 — Minimum width held provisionally at 250mm; explicitly not resolved.** Recorded per the handover's instruction, with its reasoning (250mm supported by both the product specification and the later leaflet; 200mm by the measuring instructions alone). The 200–249mm band is treated as unavailable at research stage as a holding position only. **This is deliberately not written as a validation rule**, per the handover's instruction not to convert unresolved evidence into application validation rules and not to treat 250mm as permanently resolved. **Observation offered as a lead, explicitly not as evidence and not as a basis for resolving the conflict:** the sibling Pleated/Cellular variant records a 200mm minimum width, and this construction's minimum drop, maximum drop, maximum area, manufacturing tolerance, and handle clearance figures are all identical to that sibling's. Whether the measuring instructions' 200mm figure is that sibling's figure appearing in shared measuring documentation is a **question to put to the supplier**, not a finding, and must not be used to close the conflict without supplier confirmation. | Required by the handover's own instruction; the observation is recorded as a question rather than an inference, per the handover's "make no assumptions beyond the supplied evidence" control | Research handover (mcd-01b-08b-research-handover.md); observation raised by Claude Code as a supplier question only |
| 28 Jul 2026 (confirmed by Nazmil Ghany, 26 Jul 2026 — treatment only; underlying ambiguity remains open) | **DR-05 — Internal inconsistency found in the handover's own coupled-restriction material; both readings preserved, neither adopted.** The handover states the supplier restrictions in endpoint terms (a *1,500mm* width caps drop at 2,000mm; a *2,300mm* drop caps width at 1,300mm), then proposes rule text in range terms (width > 1,300mm caps drop at 2,000mm; drop > 2,000mm caps width at 1,300mm), and asserts the two are "logically equivalent around the same restricted size zone." They are not equivalent at the boundary: width 1,400mm × drop 2,100mm = 2.94m², inside the 3m² maximum, is neither a 1,500mm width nor a 2,300mm drop, so the supplier wording does not clearly exclude it while the proposed rule does. The difference is material to the available size envelope, so it is neither smoothed over nor resolved by choosing the more conservative reading — the handover explicitly requires both statements remain traceable to the supplier wording. Recorded as proposed and inactive (§5.2), logged as conflict C-3 and open item 13. **Ratified, per `claude-code-brief-MCD-01B-08B-ratification.md`, with the following supporting confirmation appended alongside the analysis above — a confirmed treatment of an unresolved question, not a resolution of the question itself:** the finding is confirmed correct — the two supplier statements are not logically equivalent, and the worked boundary example is correct. The two supplier statements are recorded exactly as written, in endpoint form only. The broader interpreted rule must not be implemented as verified logic, being a stricter reading than the supplier's literal wording supports. The intermediate boundary region (width above 1,300mm and below 1,500mm, **and** drop above 2,000mm and below 2,300mm) remains explicitly unresolved pending supplier clarification, with no automatic pass or fail rule inferred for it. | Per this project's standing discipline against silently reconciling a discrepancy inside a brief's own material — the same pattern applied to the measuring-instructions filename suffix discrepancy in MCD-04's 26 Jul 2026 register | Claude Code — raised and reasoned; treatment **confirmed by Nazmil Ghany, 26 Jul 2026**; the underlying supplier ambiguity remains open |
| 28 Jul 2026 (confirmed by Nazmil Ghany, 26 Jul 2026) | **DR-06 — The gasket-rule refinement materially affects MCD-01B-08A; flagged for separate follow-up, and MCD-01B-08A deliberately not modified.** This handover treats gasket protrusion below 2mm as selecting an alternative ordering measurement method rather than as a compatibility failure. MCD-01B-08A's own DR-07 reached a different position for the sibling variant, characterising the square-profile eligibility scheme as a "conservative operational restriction" built on the 2mm figure, with non-square/insufficient-gasket cases routed to Physical Assessment or Supplier Confirmation Required — a treatment that is itself still pending ratification there. If the refinement recorded here is confirmed, MCD-01B-08A DR-07's characterisation is likely too restrictive and its §7.3 eligibility policy would need revisiting. **MCD-01B-08A is not edited as a side effect of this research-stage task** — that would resolve a pending judgment call in a ratified-status-pending sibling document on the strength of provisional evidence in a different Blind Technology. Recorded here, and as conflict C-5, for a separate and deliberate follow-up. **Ratified, per `claude-code-brief-MCD-01B-08B-ratification.md`, with the following supporting confirmation appended alongside the analysis above:** confirmed as a deliberate cross-document review action, to be handled as its own controlled review, not silently changed during this work package. The decision not to apply it automatically was correct. | Per the standing instruction that a sibling specification's open items are not closed as a side effect of another document's task — the same discipline applied to the profile-colour finding in MCD-04's 26 Jul 2026 register | Claude Code — raised and reasoned; **confirmed by Nazmil Ghany, 26 Jul 2026**; requires a separate follow-up task against MCD-01B-08A |
| 28 Jul 2026 | **DR-07 — Folding-handle and handle-free options recorded as not activated.** Both exist in supplier material; the same leaflet that states their availability also displays "Coming Soon" adjacent to that content, so the source contradicts itself internally. Neither is presented, quoted, or configurable (§7). The verified handle-quantity and colour-matching rules are unaffected, since they concern the standard handle, whose availability is not in question. | Required by the handover's explicit instruction not to activate either option until current ordering or price-book evidence confirms them | Research handover (mcd-01b-08b-research-handover.md) |
| 28 Jul 2026 | **DR-08 — Shared Service Profile deliberately deferred, recorded as an omission by design rather than a gap.** The handover's controlling instruction gives an exhaustive list of what this stage is suitable for, and a Shared Service Profile is not among them. Substantively, four of its inputs are unresolved (measurement-method selection, fixing-route selectability, handle availability, dimensional validation), so Configured/Extended conclusions drawn now would rest on disputed premises and would manufacture false settledness. Deferred to the specification stage; logged as open item 14. | Per the handover's own scope limits, and per this project's precedent that a deliberate deferral is stated explicitly rather than left as a silent absence (MCD-01B-08 deferred supplier capability records the same way) | Claude Code — scope assessment against the handover's controlling instruction |
| 28 Jul 2026 (confirmed by Nazmil Ghany, 26 Jul 2026) | **DR-09 — MCD-04 population follow-up required and flagged; MCD-04 deliberately not modified by this task.** This handover discloses supplier detail that MCD-04 does not currently hold: the supplier **company** name for this construction system (MCD-04 §7.15 currently records it as "Not Provided"), the internal construction-system reference, the advisor-facing display name, and this construction's verified profile dimensions, colour set, and handle facts. MCD-04 §7.15's own 20 Jul 2026 revision note already reserves the Aluminium Venetian implementation for this work package. That population is nonetheless **not** performed here: the task scope is the creation of MCD-01B-08B, this is a research-stage handover rather than an MCD-04 enrichment brief, and populating a supplier record from research-stage material — including a company-name attribution that would resolve a standing "Not Provided" field — warrants its own deliberate pass. Flagged for a separate follow-up. **Ratified, per `claude-code-brief-MCD-01B-08B-ratification.md`, with the following supporting confirmation appended alongside the analysis above:** confirmed as a deliberate cross-document review action, to be handled separately, not during this work package. The neutral product document must not expose supplier identities; MCD-04 may hold supplier-specific display names or mappings where operationally required, but that disclosure must remain governed and must not leak back into supplier-neutral documents. | Task scope is MCD-01B-08B; the same separation applied in the 26 Jul 2026 MCD-04 enrichment, where a finding affecting another document was flagged rather than applied | Claude Code — raised and reasoned; **confirmed by Nazmil Ghany, 26 Jul 2026**; a separate MCD-04 enrichment task is required |
| 28 Jul 2026 (open) | MCD-00A (Project Development Standards) was not present in the repository when this document was drafted. | This document's own Dependencies require MCD-00A. Governance, versioning, and Decision Register format conventions were instead inherited from their established use in every other product specification in this project, rather than fabricated. | Claude Code — flagged for Nazmil Ghany; not a content defect, a missing-dependency note |

---

## 12. Version History

| Version | Summary |
|---|---|
| 0.1 (pre-review, research stage) | Initial Side-Guide Window-Mounted Aluminium Venetian Blind working draft created from `mcd-01b-08b-research-handover.md`, taking up the Aluminium Venetian variant that MCD-01B-08 §5 routes to MCD-01B-06 and that MCD-01B-08A DR-04 explicitly reserved for a later work package. Created at **Working Draft — Unverified** and deliberately held there. Per the handover's controlling instruction, this draft does not finalise the specification, does not constitute or prepare an implementation brief, defines no application validation logic, does not treat the 250mm minimum width as permanently resolved, and does not activate the folding-handle or handle-free options. Verified supplier rules (§4), provisional interpretations (§5), the evidence conflict register (§9), and the open evidence register (§10) are kept in separate, explicitly labelled registers, which is this draft's primary purpose. Twelve open evidence items preserved from the handover; two added during drafting (the coupled-restriction reading, and the deliberately deferred Shared Service Profile). Five evidence conflicts recorded, including two discrepancies found inside the handover's own material rather than supplied by it: the coupled size restriction stated in endpoint terms but proposed as range-based rules, which are not equivalent at the boundary (DR-05), and a platform-category assignment inconsistent with the ratified Construction Group and unsupported by any supplied evidence, recorded but not adopted (DR-03). **The one decision requiring attention before this draft proceeds (DR-01):** the handover instructs that the supplier system name be used as the advisor-facing product name and names the supplier company and construction-system reference; applying that literally would contradict the ratified supplier-neutrality rule and would put this document in direct conflict with its own sibling MCD-01B-08A, which applied that rule to the same supplier system. This draft is therefore supplier-neutral, with the requirement that a distinct advisor-facing display name exists preserved as a verified requirement (§3) and only the name strings relocated to MCD-04 — flagged for ratification rather than resolved unilaterally, and reversible if ratified the other way, in which case the sibling document must change with it. Two cross-document findings are flagged rather than applied: this handover's gasket-rule refinement likely affects MCD-01B-08A's own pending DR-07 (DR-06), and its newly disclosed supplier company name would resolve a standing "Not Provided" field in MCD-04 §7.15 (DR-09). Neither document was touched. This document is not promoted by this task and must not be — it remains Working Draft — Unverified until the supplier conflicts, installation-route rules, handle options, warranty, lead time, and remaining compatibility requirements have been reviewed. MCD-01A, MCD-01B-01 through MCD-01B-08, MCD-01B-08A, and MCD-04 were not modified. |
| 0.2 (research stage — partial ratification, not promoted) | **Partial ratification pass**, per `claude-code-brief-MCD-01B-08B-ratification.md`. Four Decision Register entries now read "confirmed by Nazmil Ghany, 26 Jul 2026," each carrying the ratification brief's supporting reasoning appended alongside the existing analysis, not replacing it: (1) **DR-01** — the neutral drafting is confirmed; the handover's earlier instruction to place the supplier system name directly into this governance document as the advisor-facing product name is formally withdrawn, while the underlying requirement for a distinct advisor-facing display name is preserved as a verified requirement (§3), with the name strings held in MCD-04. (2) **DR-03** — the door-type/supplier-system platform-category pairing is demoted to an application context, not a platform or family classification; a new §3A records the ratified distinction between Product, Construction Group, Application Contexts, and Supplier/commercial family name, and §6's discrepancy note was updated to match. (3) **DR-06** and (4) **DR-09** — both confirmed as deliberate cross-document review actions requiring their own separate, later tasks against MCD-01B-08A and MCD-04 respectively; the decision not to apply either automatically during this work package was confirmed correct. **Open item 13 and its corresponding Evidence Conflict Register entry (C-3) now explicitly carry two distinct, non-conflated statuses**, per the ratification brief's own instruction: the endpoint-only treatment of the coupled size restriction is a **confirmed treatment** (record the two supplier statements in endpoint form only — 1,500mm width capped at 2,000mm drop, 2,300mm drop capped at 1,300mm width — and do not implement the broader range-based reading as verified logic), while the underlying supplier ambiguity for the intermediate boundary region (width 1,300–1,500mm **and** drop 2,000–2,300mm) **remains open**, with no automatic pass/fail rule inferred for it pending supplier clarification. **This document was explicitly not promoted.** The Status line remains Working Draft — Unverified; the version increment (0.1 → 0.2) is a research-stage increment only, not a promotion. No Claude Code implementation brief was prepared. The document remains open because: the 200mm-versus-250mm minimum-width conflict is unresolved (open item 1); the coupled-restriction intermediate boundary region is unresolved (open item 13, underlying ambiguity); folding-handle and handle-free availability remain unconfirmed against live ordering/price-book evidence (open items 2–3); and the remaining Open Evidence Register items (4–12, 14) are all still open. MCD-01A, MCD-01B-01 through MCD-01B-08A, and MCD-04 were not modified. |
