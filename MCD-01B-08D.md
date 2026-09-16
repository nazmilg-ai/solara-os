Document ID: MCD-01B-08D
Document Title: Full-Frame Bead-Mounted Pleated & Cellular Blind
Status: Approved Draft Baseline – Product Specification
Version: 1.0
Parent Document: MCD-01A — Sales MVP Product Engine Architecture
Family Document: MCD-01B-08 — Frame-Mounted and Window-Mounted Blind Systems (Full-Frame Bead-Mounted System Construction Group)
Base Product Specification: MCD-01B-07 — Pleated & Cellular Blinds Product Specification
Reference Implementation Referenced: MCD-01B-08C — Full-Frame Bead-Mounted Roller Blind (Construction-Group-wide conventions)
Owner: Nazmil Ghany
Last Updated: 16 September 2026 (v1.0)

## Dependencies
- MCD-00 — Executive Charter
- MCD-00A — Project Development Standards (not present in repository at time of writing — see Decision Register)
- MCD-01A — Sales MVP Product Engine Architecture (v1.5, Approved Draft Baseline)
- MCD-01B-07 — Pleated & Cellular Blinds Product Specification (v1.1, Approved Draft Baseline – Product Specification), the base blind-technology specification this document inherits from and does not duplicate
- MCD-01B-08 — Frame-Mounted and Window-Mounted Blind Systems, Family Architecture (v1.0, Approved Draft Baseline – Product Specification), the family document this document inherits its Full-Frame Bead-Mounted System Construction Group from
- MCD-01B-08C — Full-Frame Bead-Mounted Roller Blind (v1.0, Approved Draft Baseline – Product Specification), the reference implementation for Full-Frame Bead-Mounted construction-layer conventions this document inherits from where genuinely applicable, and does not transfer automatically where not (§3)
- MCD-04 — Product Library & Supplier Management — not modified by this document; population of real organisation, product, and technical-value records against the schema referenced here is explicitly deferred to a future task (Open Evidence Item)

## Documentation Conventions: Advisor Selection / Derived Default / Supplier Capability

Consistent with every other product specification in this project, the following three terms are used throughout this document as **documentation conventions only** — they are not new architectural layers and do not modify MCD-01A §3:

- **Advisor Selection** — a value the advisor actively chooses. Architecturally, this is the Configuration layer (or, where the choice changes construction, the Construction/System layer).
- **Derived Default** — a value the system determines automatically from an Advisor Selection, without a separate question. Architecturally, this is the Accessory Engine and/or Supplier Capability Engine resolving a compatible component or value from an existing Configuration selection.
- **Supplier Capability** — the actual data (dimensions, weights, compatibility, pricing, availability) that makes a Derived Default resolvable. Architecturally, this is the Supplier Capability Engine (MCD-01A §5.9) and the Supplier Capability Library, maintained in MCD-04.

## Neutral Document Identity Statement

This is a Product Specification governed by MCD-01A. The recognisable supplier trademark for a screw-free, full-frame, glazing-bead-mounted blind system does not appear anywhere in this document — not as its title, not as a neutral classification, not as a source of technical rules, not in the Decision Register, not in Open Evidence Items, not in Version History. This applies MCD-01B-08's own ratified controlled-reference rule together with MCD-01B-08A's and MCD-01B-08C's extension of it to a document whose subject matter *is* the construction the trademark describes — the excluded/related-family exception does not apply here. Following MCD-01B-08C's own precedent (zero occurrences achieved), the term is not used at all in this document, including as a controlled reference. Every supplier organisation name, product-line name, fabric name, and supplier document/product code is likewise absent from this document's body and meta-sections, and is recorded exclusively in MCD-04, deferred to a future task. Where this document must distinguish between two independently evidenced commercial routes to the same construction, it does so using the Organisational Role Schema roles already defined in MCD-01B-08 §5 (e.g. Finished-Blind Manufacturer, Fabric Supplier, Ordering Supplier), matching MCD-01B-08C's own Route 1/Route 2 convention exactly.

---

## 1. Purpose

This document defines the Full-Frame Bead-Mounted Pleated & Cellular Blind implementation of the Sales MVP Product Engine: Pleated and Cellular blinds (base construction and operation logic per MCD-01B-07) inserted into the Full-Frame Bead-Mounted System Construction Group (per MCD-01B-08 §2), following MCD-01B-08C's construction-layer conventions where genuinely applicable.

It implements the architecture defined in MCD-01A, the family architecture defined in MCD-01B-08, and the base blind-technology rules defined in MCD-01B-07. It shall not redefine any Shared Platform Service, any MCD-01B-08 family-level rule, or any MCD-01B-07 base rule. **MCD-01B-08C is used as the reference implementation for Full-Frame Bead-Mounted construction-layer conventions, but its Roller-specific rules do not transfer automatically** (§3) — every convention carried over from MCD-01B-08C in this document is one this construction's own evidence independently confirms applies to the construction layer (frame, beading, brackets, fixing holes, clearance, handle inserts, frame colour), not one assumed by analogy to Roller-blind technology.

No dimension, control limit, colour, bracket size, or compatibility rule in this document has been added, inferred, or generalised beyond what the supplied evidence states. Where the evidence itself conflicts, is silent, or is internally inconsistent, that conflict or gap is recorded rather than resolved by assumption. This document was promoted to **Approved Draft Baseline – Product Specification**, version 1.0, by Nazmil Ghany on 16 September 2026 (Decision Register DR-01).

## 2. Inheritance Statement

> MCD-01B-08D inherits blind-technology rules from MCD-01B-07, family/construction-group rules from MCD-01B-08, and uses MCD-01B-08C as the reference implementation for Full-Frame Bead-Mounted construction-layer conventions.

**Roller-specific rules in MCD-01B-08C do not transfer automatically.** Every rule carried over from MCD-01B-08C in this document is one that applies to the construction layer itself (frame, beading, brackets, fixing holes, handle-related clearance, frame colour) rather than to Roller-blind technology specifically. Concretely, this construction's own evidence (§9) **independently confirms** the following MCD-01B-08C Construction-Group-wide conventions apply here too, rather than assuming they do: glass-size measurement basis (§7); the 1,100 mm-drop fixing-hole trigger (§9.2); the 4-under/6-over-1,100 mm-drop fixing-bracket-quantity convention (§9.2); frame colour as a mandatory field distinct from every other colour field (§10). This construction's own evidence **does not** confirm the 2 mm/6 mm handle-packer convention for both routes — only Route 2 evidences it (§9.5) — and this document does not assume Route 1 shares it. Anything else from MCD-01B-08C not explicitly confirmed by this construction's own evidence is not assumed to transfer.

## 3. Product Scope

**Included**
- Pleated and Cellular blinds fitted entirely within a Full-Frame Bead-Mounted System frame, in the two constructions confirmed by this construction's evidence: Bottom Up and Top Down Bottom Up (§5).

**Excluded — not covered by this document, cross-referenced**
- Free-hanging and tensioned Pleated & Cellular constructions outside a Full-Frame Bead-Mounted frame — already fully covered by MCD-01B-07.
- Side-Guide Window-Mounted Pleated & Cellular constructions — a different Construction Group under the same family document, covered by MCD-01B-08A.
- Skylight and roof-window Pleated/Cellular constructions — excluded per MCD-01B-08 §4 and MCD-01B-07 §2/§28; this construction's own evidence separately and independently confirms a skylight-specific Pleated/Cellular product exists outside this document's scope, adjacent to but not part of this construction.
- Other Full-Frame Bead-Mounted child products — MCD-01B-08C (Roller, drafted) and the remaining four future siblings (Day & Night, Aluminium Venetian, Wooden Venetian, Lite Shutters) named in MCD-01B-08C §3, none drafted or anticipated by content in this document.
- Dual-Fabric Pleated/Cellular within this Construction Group — not evidenced for this construction (§17).
- INTU, Micro INTU, roof/skylight/lantern/shaped-roof/gable systems, specialist angled roof/side-window systems, ordinary free-hanging/tensioned blinds outside this family, total-blackout cassette systems, and shutter-lite/shutter products — all excluded per MCD-01B-08 §4, not restated in full here.

**Future**
- Confirmation of open items §22; the remaining four Full-Frame Bead-Mounted child products.

## 4. Pleated vs Cellular Distinction

Pleated and Cellular are covered in this single document, consistent with MCD-01B-07 §3 (which already treats both as sharing one base specification) and MCD-01B-08A's own precedent of covering both technologies in one Construction-Group child document. **They remain technically distinct within it:**

- **Pleat size 20 mm width (Pleated) vs. cell width 25 mm (Cellular)** — confirmed structural distinction, stated for the whole range this construction belongs to, not merely a general industry figure.
- **Separate fabric collections** — this construction's evidence confirms two genuinely separate, real fabric collections exist for Route 1, one for Cellular and one for Pleated, each with its own real fabric names, colours, compositions, widths, and price bands. Real fabric names are not reproduced in this neutral document (§21) — recorded in MCD-04 only.
- **A confirmed fabric-eligibility difference:** at least one fabric in Route 1's Cellular collection is explicitly restricted to two other, non-full-frame constructions within the same range and is therefore **not available** for this construction specifically — a real, confirmed exclusion, not generalised to any other fabric.
- **A genuinely unresolved classification question, not resolved here:** whether Route 2's own range (named "pleated" by Route 2 itself) is actually Pleated, Cellular, or both is **open** — see DR-08 (§23).

Neither technology is treated as a separate Construction Group or Product Family; both remain within the single Full-Frame Bead-Mounted System Construction Group per MCD-01B-08 §2, consistent with MCD-01B-07 §3.

## 5. Construction Classification

Applying MCD-01A §3's three-test model to this construction's own open questions (the Construction Group itself is already settled by MCD-01B-08 §2 and MCD-01B-07's Bottom Up/TDBU classification is not re-litigated, only re-applied to this specific construction — see below):

**5.1 Bottom Up and Top Down Bottom Up are Construction-layer capability, not separate Blind Technologies or Product Families (DR-04).** MCD-01B-07's own Required Classification Question 2 (Decision Register, ratified 18 Jul 2026) already establishes, for Pleated & Cellular generally, that Bottom Up and Top Down Bottom Up pass Test 1 (a genuine assembly difference — TDBU requires "a second, independently-mechanised rail beyond the baseline Bottom Up construction") and are therefore Construction-layer, not Configuration. **This construction's own evidence independently corroborates that same conclusion at the specific full-frame level, rather than merely inheriting it by citation:** Route 1's own technical specification states the Bottom Up construction uses a Standard top profile and a Reinforced bottom profile, while the Top Down Bottom Up construction uses a Reinforced top profile and a Reinforced bottom profile — a genuine physical hardware difference (different top-profile component) between the two, not a configuration toggle on identical hardware. Test 1 passes on this construction's own evidence, not only by citation of MCD-01B-07. **Conclusion: Construction-layer capability**, confirming MCD-01B-07's own ruling rather than reopening it. Neither is treated as a separate Blind Technology or Product Family.

**5.2 Control options (Handle / No Handle / Folding Handle) are Configuration, not Construction.** Test 1: does selecting Handle, No Handle, or Folding Handle change this construction's frame, profile, bracket, or fixing-hole convention? Route 1's evidence shows identical frame, profile, and bracket data regardless of which control option is selected for either Bottom Up or Top Down Bottom Up — only the handle component (or its absence) differs. Test 1 fails; Test 2 passes (a control option must be resolved, even if the resolution is "no handle," for the blind to be ordered correctly). **Conclusion: Configuration**, matching MCD-01B-08C's own Control System reasoning in shape.

**5.3 Route 2's build styles (named by Route 2 as "Standard," "Dual Pull," and "Dual Meet") are recorded as supplier-named options, not classified against Bottom Up/Top Down Bottom Up.** Route 2's own evidence names these three styles without stating which corresponds to Bottom Up, which to Top Down Bottom Up, or whether "Dual Pull"/"Dual Meet" are a third, different movement style entirely. Applying the three-test model to an unmapped label is not possible without inventing the mapping — this document does not attempt it. **Recorded as Open Evidence Item, not resolved — see DR-09 (§23).**

**Operational block (DR-09).** Route 2's build styles named "Standard," "Dual Pull," and "Dual Meet" must not be mapped, automated, validated, or quoted as Bottom Up or Top Down Bottom Up until supplier evidence confirms the mapping. Until then, no Product Engine, Survey Engine, Validation Engine, Pricing Engine, or Supplier Capability Engine behaviour may treat any of these three build styles as equivalent to either construction defined in §5.1.

## 6. Shared Service Profile

| Shared Platform Service | Status | Notes |
|---|---|---|
| Survey Engine | Configured | Standard survey workflow configured with this construction's questions (§16): construction (Bottom Up/TDBU), control option, route/supplier selection, glass width/drop, frame colour, headrail colour (Route 2), bracket size, handle insert colour and position, profile colour, obstruction/handle clearance, fabric selection |
| Measurement Engine | Configured | Glass-size measurement basis (§7) — a parameterisation of the shared engine's existing width/height/reference-point capture, matching MCD-01B-08C's own already-Configured conclusion and this construction's own confirming evidence |
| Validation Engine | Configured | Route-specific dimensional eligibility (§8); Priced-Band vs. Technical-Limit field separation applied to Route 2's unconfirmed drop minimum (§8.2); no cross-route inheritance; fabric-eligibility exclusion (§4) applied as a compatibility check |
| Operation Engine | Configured | Supports Manual only, using the existing shared mode; Handle/No Handle/Folding Handle are Configuration-layer control options (§5.2), not separate Operation Engine modes; no Motorised mode is evidenced for this construction |
| Motor Engine | Configured | Suppresses motor options given the current absence of motorisation evidence for this construction on either route (Not Provided) — the same evidence-gate pattern as MCD-01B-08C DR-08 and MCD-01B-08A DR-12, not inherited from free-hanging/tensioned Pleated & Cellular's own motorised capability (MCD-01B-07 §11) or from any adjacent construction |
| Child Safety Engine | Configured | No cord- or chain-operated control is evidenced for this construction on either route — only Handle/No Handle/Folding Handle (Route 1) and a route-named handle-based option set (Route 2). Provisionally consistent with MCD-01B-08 §9's "may be Safe by Design where evidence confirms this" pattern; recorded as provisional, not settled (DR-13, §23) |
| Pricing Engine | Configured | This construction's pricing inputs (§19): fabric/fabric band, frame colour, construction, control option, bracket size, accessories, route; Priced-Band vs. Technical-Limit separation for Route 2's grid-only drop-minimum evidence |
| Accessory Engine | Configured | Named accessory groups confirmed by this construction's evidence (§20): frame, fixing brackets (9 sizes, Route 1; 9 sizes, Route 2, separately confirmed), handle insert (Route 1), window packing piece (Route 2), folding handle (both routes, existence only), handle rebate (Route 2, existence only) |
| Supplier Capability Engine | Configured | Applies MCD-01B-08's ten-role Organisational Role Schema to two independently evidenced routes for this construction, including the same multi-role-per-organisation case already tested and concluded Configured in MCD-01B-08C DR-04, applied fresh to this construction's own real (but unnamed) evidence rather than assumed to transfer by citation alone (DR-10, §23) |
| Recommendation Engine | Configured | No Full-Frame-Bead-Mounted-specific recommendation content is separately evidenced yet; where applicable, this construction inherits base Pleated & Cellular's general construction/movement-style/fabric recommendation logic (MCD-01B-07 §20) without assuming supplier- or route-specific figures not evidenced here |
| Document Generation Engine | Full | Standard implementation; no construction-specific exception to the Customer-Facing Documentation Rule (MCD-01A §5.7/§5.11) |
| Audit & Compliance Engine | Configured | Preserves route, organisational role, construction/control/bracket selection, and evidence-source detail per MCD-01B-08 §10's audit-field list — the same reasoning MCD-01B-08 and MCD-01B-08C both applied (richer field content within existing engine responsibilities, not new engine capability) |

This profile complies with MCD-01A §6 and §7. No service is classified Extended: every application above parameterises a responsibility the relevant shared service already has per MCD-01A §5, none requires the platform itself to change. A high volume of route-specific and construction-specific rules is parameterisation, not by itself grounds for Extended, per MCD-01A §2 and MCD-01B-07's own standing governance clarification (Decision Register, 18 Jul 2026). No service is classified Restricted: every gated state in this document (motorisation, the unconfirmed Route 2 drop minimum, the provisional Child Safety classification) is an evidence-availability gate, not a deliberate Solara exclusion of an available capability.

## 7. Measurement

Glass size (glass width, glass drop) is the confirmed measurement basis for this construction — Route 1's own evidence states sizing is "based on glass size." Do not use Recess or Exact measurement for this construction — no evidence supports either being required here. This confirms, rather than merely inherits, MCD-01B-08C §5.1's Construction-Group-wide measurement basis for this construction specifically.

## 8. Capability Envelopes

The shared Validation Engine performs validation. This construction's evidence provides two independently evidenced routes; per MCD-01B-08 §7's no-cross-supplier/no-cross-route-inheritance principle, neither route's figures are applied to the other, and neither is applied to any other Full-Frame Bead-Mounted sibling or to free-hanging/tensioned Pleated & Cellular (MCD-01B-07).

**8.1 Route 1 (a Finished-Blind Manufacturer providing a confirmed technical specification for this construction) — Technical Limits, both constructions identical:**
- Minimum width: 200 mm. Minimum drop: 150 mm. Maximum width: 1,500 mm. Maximum drop: 2,300 mm. Maximum area: 3 m².
- Manufacturing tolerance: ±3 mm (width and drop), stated for the wider range this construction belongs to.
- Square-frame guidance: a 5 mm deduction from width and drop is this route's own stated recommendation for component clearance, not a universal Full-Frame Bead-Mounted rule (matching MCD-01B-08C §7.1's identical caveat for its own Route 1).
- No width-dependent maximum-drop restriction is evidenced for this construction (unlike some other constructions in this project) — not assumed.

**8.2 Route 2 (a second Finished-Blind Manufacturer, manufacturing this construction in-house) — mixed Technical Limit and Priced Band, per the source documents' own conflicting figures:**
- The specification page states: minimum width 80 mm; maximum width 1,400 mm; maximum drop 2,400 mm. Recorded as **Technical Limit**.
- The pricing grid separately shows a width range starting at 0.400 m (400 mm) and a drop range starting at 0.400 m (400 mm). Per MCD-01B-08 §7's explicit field-separation principle (applied identically in MCD-01B-08C DR-07), the pricing grid's start point is **not** automatically a technical minimum — recorded as a **Priced Band** start, not a Technical Minimum.
- **No technical minimum drop is separately stated anywhere in Route 2's evidence.** Recorded as **Not Provided**, distinct from the 400 mm Priced Band start — must not be presented to an advisor as a confirmed technical drop minimum.
- Route 2's own build styles (Standard, Dual Pull, Dual Meet — §5.3) share this same width/drop envelope in the evidence; no per-build-style size difference is stated. Subject to the §5.3 operational block (DR-09).

**8.3 No universal Full-Frame Bead-Mounted Pleated & Cellular limit should be created from either route's values — each stays route-specific**, consistent with MCD-01B-08 §7 and MCD-01B-08C §7.3.

## 9. Construction-Layer Components

**9.1 Frame (Route 1, confirmed).** Aluminium, 7 colours: White, Beige, Anthracite, Brown, Golden Oak, Mahogany, Black. **This differs from MCD-01B-08C §9.1's own Route 1 frame-colour list for the Roller construction, which confirms only 6 colours (White, Brown, Golden Oak, Mahogany, Anthracite, Black) and does not include Beige.** The difference is recorded, not resolved — this construction's own evidence is not assumed to match a different Blind Technology's evidence on the same route merely because both are Route 1, and MCD-01B-08C is not corrected or reconciled by this document. Logged as a new Open Evidence Item (§22) and DR-15 (§23). **No frame-colour default is stated for this construction.** (A document-wide default is stated for *profile* colour — White, §9.3 — but that is a separate field, §10; the frame-colour default remains unconfirmed and is logged as an Open Evidence Item, §22, not assumed to be White by analogy to the profile-colour default.)

**9.2 Fixing brackets, clips, and side-frame fixing holes (Route 1, confirmed).**
- **9 confirmed sizes: 18, 20, 22, 24, 26, 28, 30, 32, and 38 mm**, colours White, Brown, Anthracite, Black. Real product codes exist per size/colour combination — not reproduced here, recorded in MCD-04 only.
- **Bracket quantity by drop: 4 brackets under 1,100 mm drop, 6 brackets from 1,101–2,300 mm drop** — this construction's own evidence independently confirms MCD-01B-08C §5.4's Construction-Group-wide convention rather than assuming it transfers.
- **Fixing-hole convention: two holes standard, a third hole added over 1,100 mm drop** — likewise independently confirmed by this construction's own evidence, further corroborating the drop-trigger convention MCD-01B-08C §5.4 already established and flagged as conflicting with a different (not-yet-drafted) sibling's width-trigger evidence. That conflict is not resolved here, and this construction's own evidence does not bear on it either way beyond adding a further drop-trigger confirmation.
- **Route 2's own bracket sizes are separately confirmed, not assumed to match Route 1's:** 9 sizes, 18–38 mm (same numeric range as Route 1, independently stated by Route 2 rather than inherited). Colours: White, Unpainted, Brown, **Anthracite Grey**, Black. **One colour in this list carries an asterisk in the source (Anthracite Grey\*), and the source page does not state what the asterisk means.** Recorded neutrally as given; the asterisk's meaning is logged as a new Open Evidence Item (§22), not guessed.
- **Route 2's bracket-quantity-by-drop rule, fixing-hole rule, handle-quantity rule, and clearance rule are not stated anywhere in Route 2's own evidence.** Recorded as **Not Provided** for each — not borrowed from Route 1.

**9.3 Profile.** This construction's own profile is confirmed distinct from the standard (22 mm wide × 16.4 mm high) and reinforced (22 mm wide × 22 mm high) profiles used elsewhere in Route 1's range: **38 mm wide × 26.4 mm high**. Default profile colour is White unless otherwise specified (a document-wide statement in Route 1's evidence, not scoped only to this construction, but applicable to it as stated).

**9.4 Handle clearance (Route 1, confirmed).** 25 mm of clearance is required between handles and/or vents and the glass — stated twice in Route 1's own evidence, for both the frame generally and the handle insert specifically.

**9.5 Window packing piece / handle packer (Route 2 only, confirmed).** Available in 2 mm and 6 mm — this construction's own evidence (Route 2 only) confirms MCD-01B-08C §5.3's Construction-Group-wide 2 mm/6 mm handle-packer convention (including the earlier withdrawn 3 mm reference, which is not reintroduced here either). **Route 1's evidence does not mention a handle packer or window packing piece at all for this construction** — this is a genuine silence, not a contradiction, and is not read as either confirming or excluding the convention for Route 1. Colours listed for Route 2's packing piece: White, Brown, Tan, Light Grey, Brown, Anthracite — **the source repeats "Brown" in this list**, recorded exactly as given; the duplicate is logged as an Open Evidence Item (§22), not silently corrected.

**9.6 Frame and headrail (Route 2, confirmed).** The source text states: "Special Frames: Golden Oak & Mahogany" and "Standard Frames: White, Black, Brown, Anthracite Grey, Matt Grey" — seven named colours in total, matching the expected list exactly. **A genuine text-vs-image inconsistency in the source itself, recorded rather than resolved:** the colour-swatch image shown alongside this same text labels seven swatches as White, Black, Brown, Anthracite, Grey, Golden Oak, Mahogany — treating "Anthracite" and "Grey" as two separate swatches rather than the text's single combined "Anthracite Grey," and showing no "Matt" qualifier on the Grey swatch at all. Both readings are recorded; neither is treated as authoritative over the other. Logged as a new Open Evidence Item (§22) and DR-16 (§23). Route 2 organises these frame colours into **two commercial pricing tiers** — a tier for Golden Oak and Mahogany, and a tier for the remaining confirmed colours — a pricing/commercial distinction only, following MCD-01B-08C §9.4's identical pattern for the same underlying business structure; no technical (dimensional, material, or capability) difference between the tiers is stated on this page. **Headrail colours: White, Silver, Black, Brown, Anthracite Grey, Tan** — six colours, matching the expected list exactly, no discrepancy found. **No frame-colour default is stated anywhere on this page for Route 2** — confirmed absence, not assumed.

## 10. Colour Fields

Frame colour (§9.1, §9.6), profile colour (§9.3), headrail colour (§9.6), handle colour (§11), and handle-insert colour (§11) are each confirmed as separate fields — this construction's own evidence directly corroborates MCD-01B-08C §5.2's Construction-Group-wide principle that these must be stored separately rather than assumed to share a name.

**Profile-colour → frame-colour → frame-corner-colour mapping (Route 1, confirmed; recommended, not exact, per the source's own wording):**

| Profile Colour | Frame Colour | Frame Corner Colour |
|---|---|---|
| Dark Oak | Brown | Brown |
| Golden Oak | Golden Oak | Tan |
| Oak | Golden Oak | Tan |
| Mahogany | Mahogany | Brown |
| White | White | White |
| Cream | Beige | Beige |
| Grey | White | White |
| Anthracite | Anthracite | Anthracite |
| *(a further profile colour — name uncertain, see Open Evidence Item, §22)* | Anthracite | Anthracite |
| Black | Black | Black |
| Brown | Brown | Brown |
| Walnut | Brown | Brown |

The source states explicitly: profile and frame colours "will not be an exact match," and when a beige frame is required, a white profile is the recommended (not exact) match — both carried forward here rather than smoothed into a false one-to-one mapping. **One profile-colour name in this table's source row is generalised rather than reproduced** — it did not clearly read as a plain descriptive colour term (unlike White, Black, Brown, Grey, Anthracite, Mahogany, Golden Oak, all already used freely elsewhere in this project's neutral documents) and may be a proprietary/branded finish name; per this document's own naming-governance discipline (Neutral Document Identity Statement; DR-12), it is not reproduced, and its status is logged as a new Open Evidence Item (§22) rather than guessed at.

## 11. Controls

**Route 1 (confirmed):** a standard handle supplied as standard, in White, Black, Anthracite, or Clear; a folding handle available as an additional surcharge option, Clear only (existence only, no amount recorded); handle quantity — 1 per moving profile up to 1.2 m width, 2 above 1.2 m width; handles are supplied as two pieces (a handle and an insert); the blind can also be ordered with no handle. Handle insert: 6 colours — White, Tan, Brown, Grey, Anthracite, Black; position in the frame must be specified at order.

**Route 2 (confirmed, existence only):** a folding handle surcharge option and a handle-rebate surcharge option both exist — no amounts recorded. Dual Pull and Dual Meet build styles carry an additional width-dependent component cost — existence only, no amount recorded. No handle colour set, handle quantity rule, or handle-insert equivalent is stated anywhere in Route 2's evidence — recorded as Not Provided, not borrowed from Route 1.

Cord/ladder colour-matching for this specific construction is **not confirmed**: Route 1's document-wide "additional information" list states cord colour is chosen closest to the fabric colour for three named system types, and full-frame ("this construction") is not among the three named there; a separate, unscoped footnote elsewhere in the same document states cords are chosen to the closest fabric colour generally, without naming which system types it covers. This is a genuine internal inconsistency in the source, not resolved here — logged as an Open Evidence Item (§22).

## 12. Organisational Role Schema Application

Two independently evidenced commercial routes exist for this construction, described using MCD-01B-08's ten-role schema, matching MCD-01B-08C's own convention:

- **Route 1** plays the Finished-Blind Manufacturer and Technical Source roles for its own output — it provides a confirmed technical specification and manufactures its own complete branded product for this construction.
- **Route 2** plays the Finished-Blind Manufacturer, Ordering Supplier, and Commercial Route roles for its own output — this construction's evidence confirms Route 2 manufactures the finished blind in-house, using fabric sourced from a separate organisation rather than reselling a finished product.
- **A genuinely novel-per-this-document structural fact, tested rather than assumed:** this construction's own evidence indicates the organisation behind Route 1 is the fabric-sourcing organisation for Route 2 — i.e. the same multi-role-per-organisation pattern (one organisation holding a Finished-Blind Manufacturer role for its own route while holding only a Fabric Supplier role toward the other route) that MCD-01B-08C DR-04 already tested and concluded Configured for the Roller construction. See DR-10 (§23) for why that conclusion is applied here rather than re-derived from first principles, and why applying a prior conclusion to a new, real instance is not the same as assuming it transfers without testing.

## 13. Supplier Capability Engine Application

The engine resolves a selected construction (Bottom Up or Top Down Bottom Up), control option, and route to the applicable capability record. Route 1 and Route 2 capability envelopes (§8) are **not merged** — the engine determines valid combinations per route independently, consistent with MCD-01B-08 §7's no-cross-route-inheritance principle. No "most generous of the two systems" rule applies to this construction (see DR-05, §23) — the Day & Night (MCD-01B-09) treatment was a product-specific business ruling for that product only, not a project-wide precedent, and is not applied here or to any other Full-Frame Bead-Mounted sibling without its own explicit business decision. Subject to the §5.3 operational block (DR-09).

## 14. Recommendation Rules

Recommendations are provided by the shared Recommendation Engine. No Full-Frame-Bead-Mounted-specific recommendation content is separately evidenced for this construction; where applicable, this construction may inherit base Pleated & Cellular's general construction/movement-style/fabric recommendation logic (MCD-01B-07 §20), always advisor-overridable and never asserting a supplier- or route-specific figure this document does not itself evidence.

## 15. Supplier Capability Requirements

Supplier/route documents shall define: available frame colours; profile colours and the profile-to-frame colour mapping; bracket sizes and compatible colours; confirmed technical width/drop ranges (distinct from any pricing-grid range); construction and control-option availability; fabric collections and price bands, with fabric-level construction eligibility; accessory availability; lead times; organisational role (per MCD-01B-08 §5) for each evidenced route.

Supplier capability shall remain independent of Product Engine behaviour, per MCD-01A §9.

## 16. Survey Requirements

The shared Survey Engine shall be used. This construction's questions include: route/supplier selection; construction (Bottom Up/Top Down Bottom Up, §5.1); control option (Handle/No Handle/Folding Handle, §5.2); glass width; glass drop; frame colour; profile colour; headrail colour (Route 2, §9.6); handle insert colour and position (Route 1); bracket size; bracket colour; window-packing-piece size (Route 2); handle/vent/obstruction clearance; fabric selection; colourway. Subject to the §5.3 operational block (DR-09).

No survey logic already owned by the shared Survey Engine, MCD-01B-08 §6, or MCD-01B-07 §12 is duplicated here.

## 17. Operation

Operation behaviour is defined by the shared Operation Engine.

**This construction supports:** Manual only, via the confirmed control options (§5.2, §11): Handle, No Handle, or Folding Handle (Route 1); a route-named set of surcharge-based handle options (Route 2).

**This construction does not support (not evidenced):** Manual or Motorised (Advisor Selection); Manual or Motorised (Factory Selection); Motorised Only; Dual-Fabric Pleated/Cellular. This is a genuine absence of evidence for this specific construction, not inferred to be present because free-hanging/tensioned Pleated & Cellular (MCD-01B-07 §11) supports motorisation for other constructions, because MCD-01B-08A evidences motorisation questions for a different Construction Group, or because MCD-01B-08C evidences a different Blind Technology's own separate absence of motorisation. Per MCD-01B-08 §8's family-level Motorisation Principle, a capability existing elsewhere in the same Blind Technology does not by itself establish an active quoting route for this construction.

Operation modes are not redefined.

## 18. Child Safety

The shared Child Safety Engine implements BS EN 13120 compliance (MCD-01A §5.6). This construction's own implementation:

- **No cord- or chain-operated control is evidenced for this construction on either route** — Route 1 offers Handle, No Handle, or Folding Handle only; Route 2's evidence likewise shows only handle-related options (folding handle, handle rebate), with no cord or chain option stated.
- This is provisionally consistent with MCD-01B-08 §9's stated pattern that handle-operated systems "may be Safe by Design where evidence confirms this," matching the same provisional reasoning MCD-01B-08C applied to its own tensioned-spring control. **Recorded as provisional, not settled** (DR-13, §23) — full confirmation is a genuine Open Evidence Item, not assumed from the absence of a cord option in the evidence reviewed.
- Chain or cord length is not applicable given no such control is evidenced; not restated as a formula here.

## 19. Pricing Inputs (structure only — no commercial values)

Pricing calculations are provided by the shared Pricing Engine. This construction's pricing parameters include: route/supplier; construction (Bottom Up/Top Down Bottom Up); fabric collection; fabric price band; frame colour; profile colour; control option; bracket size; accessories (§20); glass width; glass drop; headrail colour (§9.6); Route 2's commercial frame-tier structure (§9.6 — see DR-06, §23, for why it is recorded as a pricing-structure fact only, not a technical restriction). Subject to the §5.3 operational block (DR-09).

Commercial pricing behaviour, actual price bands, and actual monetary values are excluded from this document per MCD-01A §5.7/§9 and MCD-01B-07 §21 — they belong in MCD-04 and the Pricing Engine. No construction-specific exception exists to the Customer-Facing Documentation Rule (MCD-01A §5.7/§5.11): quotations and invoices show total price only.

## 20. Accessories

The shared Accessory Engine manages compatibility. This construction's confirmed accessory groups include:
- Frame (aluminium, both routes)
- Fixing brackets (9 sizes, Route 1; 9 sizes, Route 2, separately confirmed — §9.2)
- Handle insert (Route 1 only, §11)
- Window packing piece (Route 2 only, 2 mm/6 mm, §9.5)
- Folding handle (both routes, existence only)
- Handle rebate (Route 2 only, existence only)

Real product codes and confirmed colour options per accessory belong in MCD-04, not this document.

## 21. Fabric

Two separate, real fabric collections exist for Route 1 — one for Cellular, one for Pleated — each with real fabric names, colours, compositions, widths, and price bands (§4). Route 2 evidences two further real, separate fabric names, each with a corresponding blockout/dimout variant, mapped to two price bands. **None of these real fabric names are reproduced anywhere in this document, including Open Evidence Items and the Decision Register** — they are recorded exclusively in MCD-04. Where this document must refer to a specific named fabric to record a genuine finding (§4, §23 DR-08), it does so without naming the fabric, describing only the structural fact.

## 22. Open Evidence Items — Unresolved / Supplier Confirmation Required / Do Not Automate or Expose

1. **Route 2 nomenclature (DR-08, §23).** Whether Route 2's own range, which it names "pleated," is actually Pleated, Cellular, or both is unconfirmed — at least one fabric name in Route 2's own range also appears, identically, in Route 1's own Cellular (not Pleated) fabric table, and Route 2's own adjacent, non-full-frame range for the same general product family is headed as a cell-fabric-only construction. Not reclassified here.
2. **Route 2 build-style mapping (DR-09, §23).** Whether "Standard" = Bottom Up, and how "Dual Pull" and "Dual Meet" map to Bottom Up/Top Down Bottom Up (or are a third, different movement style), is not evidenced. No mapping assumed. Subject to the §5.3 operational block (DR-09).
3. **Route 2 window-packing-piece colour duplicate (§9.5).** The colour list repeats "Brown." Recorded as given, not silently corrected.
4. **Route 2's true technical minimum drop (§8.2).** Not stated anywhere in Route 2's evidence; only a 400 mm pricing-grid start point exists, recorded as a Priced Band, not a Technical Limit.
5. **Whether Route 2's commercial frame tiers (§19) carry any genuine technical difference beyond price.** No technical difference is stated in the evidence reviewed; not assumed to exist or not exist beyond what is stated.
6. **One profile-colour name in Route 1's profile-to-frame mapping table (§10)** could not be confidently neutralised as a plain descriptive colour term and may be a proprietary/branded finish name. Not reproduced; not guessed at.
7. **The asterisk against one bracket colour in Route 2's evidence (§9.2, "Anthracite Grey\*").** The source page does not state what it means. Logged, not guessed.
8. **Cord/ladder colour-matching scope for this construction (§11).** Route 1's own document-wide statement names three system types the rule applies to, and this construction's system type is not among them; a separate, unscoped footnote elsewhere in the same document restates the rule generally. Genuine internal source inconsistency, not resolved here.
9. **Frame-colour default for this construction (§9.1).** Not stated; only the separate profile-colour default (White) is stated, and is not assumed to apply to frame colour.
10. **Route 2's bracket-quantity-by-drop rule, fixing-hole rule, handle-quantity rule, and clearance rule (§9.2).** Not stated anywhere in Route 2's evidence; recorded as Not Provided for each, not borrowed from Route 1.
11. **Full confirmation of the Safe-by-Design child-safety classification (§18).** Currently provisional, based on the absence of an evidenced cord/chain option, not an explicit confirmation.
12. **MCD-04 enrichment for this construction's Route 1 and Route 2 capability envelopes and commercial tiers.** Separate controlled task, not performed here.
13. **MCD-00B Product Register entry for MCD-01B-08D.** Separate controlled task after this document is reviewed — MCD-00B-Product-Register.md is not edited by this task.
14. **The carried-forward Full-Frame Bead-Mounted fixing-hole width-vs-drop discrepancy** (MCD-01B-08C §5.4, concerning a different, not-yet-drafted sibling). This construction's own evidence adds a further drop-trigger confirmation but does not resolve the underlying conflict — not treated as settled by that corroboration.
15. Any route beyond the two evidenced here.
16. The standing MCD-00A repository dependency (consistent with every other document in this project).
17. **Route 1 frame-colour list differs from MCD-01B-08C's own Route 1 frame-colour list for the Roller construction (§9.1, DR-15).** This construction's evidence confirms 7 colours including Beige; MCD-01B-08C confirms 6 colours for a different Blind Technology on the same route, without Beige. Recorded, not resolved; MCD-01B-08C is not corrected by this document.
18. **Route 2 frame-colour list: text-vs-swatch-image inconsistency in the source (§9.6, DR-16).** The text names "Anthracite Grey" and "Matt Grey" as two of seven colours; the swatch image on the same page labels the same colours as separate "Anthracite" and "Grey" swatches with no "Matt" qualifier. Both readings recorded; neither resolved.

## 23. Decision Register

Maintained in accordance with this project's established convention (MCD-00A itself is not present in this repository — see the equivalent standing note in MCD-01B-08 §13/MCD-01B-08A §21/MCD-01B-08C §19). Format: Date | Decision | Reasoning | Raised By.

| Date | Decision | Reasoning | Raised By |
|---|---|---|---|
| 16 Sep 2026 (ratified by Nazmil Ghany, 16 Sep 2026) | **DR-01 — Document number MCD-01B-08D and title "Full-Frame Bead-Mounted Pleated & Cellular Blind" are proposed, not final.** Follows the naming pattern already used for MCD-01B-08A/08B/08C (Construction Group child, lettered under the family document MCD-01B-08). Consistent with MCD-01B-08C's own DR-01 precedent, this stays open pending explicit ratification rather than assumed final because it was the first document drafted. Conclusion: ratified. | Nazmil Ghany — ratified 16 Sep 2026 |
| 16 Sep 2026 (confirmed by Nazmil Ghany, 16 Sep 2026, pre-drafting direction) | **DR-02 — One document, two technologies (Pleated, Cellular), kept technically distinct.** Full reasoning in §4. Confirmed by this construction's own evidence: a real 20 mm/25 mm pleat/cell structural distinction, two genuinely separate real fabric collections, and a confirmed fabric-eligibility exclusion affecting only one technology's collection. | Pre-drafting direction (Nazmil Ghany) — confirmed, corroborated by this construction's own evidence during drafting — Claude Code |
| 16 Sep 2026 (confirmed by Nazmil Ghany, 16 Sep 2026, pre-drafting direction) | **DR-03 — Inheritance chain and non-transfer of Roller-specific rules.** Full reasoning in §2. This construction's own evidence was checked against every MCD-01B-08C Construction-Group-wide convention individually rather than assumed to transfer wholesale — confirmed independently for measurement basis, fixing-hole trigger, and bracket-quantity convention; confirmed only for Route 2 (not assumed for Route 1) for the handle-packer convention; not confirmed at all for frame-colour default. | Pre-drafting direction (Nazmil Ghany) — confirmed; transfer/non-transfer tested individually during drafting, not assumed — Claude Code |
| 16 Sep 2026 (confirmed by Nazmil Ghany, 16 Sep 2026, pre-drafting direction) | **DR-04 — Bottom Up and Top Down Bottom Up are Construction-layer capability for this construction, not separate Blind Technologies or Product Families.** Full reasoning in §5.1. Applies MCD-01B-07's own Required Classification Question 2 ruling (ratified 18 Jul 2026: TDBU requires "a second, independently-mechanised rail beyond the baseline Bottom Up construction," a genuine Test-1 assembly difference) and independently corroborates it with this construction's own evidence: Bottom Up uses a Standard top profile, Top Down Bottom Up uses a Reinforced top profile — a real physical hardware difference on this specific construction, not only a citation of the base ruling. | Pre-drafting direction (Nazmil Ghany) — confirmed; formal three-test corroboration performed against this construction's own evidence, not assumed by citation alone — Claude Code |
| 16 Sep 2026 (confirmed by Nazmil Ghany, 16 Sep 2026, pre-drafting direction) | **DR-05 — Route 1 and Route 2 capability envelopes are not merged; the Day & Night "most generous of the two systems" ruling is not a project-wide precedent.** Full reasoning in §8, §13. This construction's evidence shows genuinely different figures between the two routes (200 mm vs. 80 mm minimum width; a confirmed 2,400 mm technical maximum drop for Route 2 against 2,300 mm for Route 1; no confirmed technical minimum drop for Route 2 at all) — no single "most generous" figure is asserted; each route's figures are recorded and kept separate. The MCD-01B-09 Day & Night ruling was a specific business decision for that product, not a classification precedent applicable here. | Pre-drafting direction (Nazmil Ghany) — confirmed, stated explicitly not to treat Day & Night as a precedent — Claude Code |
| 16 Sep 2026 (confirmed by Nazmil Ghany, 16 Sep 2026, pre-drafting direction) | **DR-06 — Route 2's commercial frame tiers (Special/Standard) are a pricing distinction, not a technical one; Frame Colour remains mandatory and separate from every other colour field.** Full reasoning in §10, §19. Route 2's evidence confirms two named tiers (a tier for two specific colours; a tier for the remaining confirmed colours) with different prices at equivalent sizes, but no technical (dimensional, material, bracket, or capability) difference is stated between the tiers anywhere in the evidence reviewed — recorded as a pricing-structure fact only. If a technical difference is found later, it is a new Open Evidence Item, not assumed absent forever. | Pre-drafting direction (Nazmil Ghany) — confirmed; evidence checked specifically for a technical difference and none found, not assumed absent by default — Claude Code |
| 16 Sep 2026 (confirmed by Nazmil Ghany, 16 Sep 2026, pre-drafting direction) | **DR-07 — Motorisation is recorded as Not Provided for this construction on both routes; not inherited from any adjacent construction.** Full reasoning in §17. Neither route's evidence for this specific construction mentions a motorised control option — Route 1 offers Handle/No Handle/Folding Handle only; Route 2's evidence shows only handle-related surcharge options. Not inferred from MCD-01B-07's own general Pleated & Cellular motorisation evidence (a different, non-full-frame context), from MCD-01B-08A (a different Construction Group), or from MCD-01B-08C (a different Blind Technology). | Pre-drafting direction (Nazmil Ghany) — confirmed, corroborated by direct evidence check during drafting — Claude Code |
| 16 Sep 2026 (open) | **DR-08 — Route 2 nomenclature (Pleated vs. Cellular) is recorded as unresolved, not reclassified.** Route 2 names its range "pleated." This construction's own review of Route 1's evidence found at least one fabric name common to both routes' ranges classified by Route 1 under its Cellular (not Pleated) fabric table — a genuine, specific, evidenced basis for uncertainty, not a speculative flag. Route 2's own adjacent, non-full-frame range for the same general product family is headed as covering cell fabric only, cited here solely as further context for this same uncertainty, not as Route 2 full-frame evidence (which it is not — see §3, §8). No reclassification is made; the advisor-facing construction should not be presented as confirmed Pleated-only or Cellular-only until this is resolved. | Claude Code — recorded, not resolved; genuine cross-route evidence found and logged during drafting, not merely restated from the working draft |
| 16 Sep 2026 (open) | **DR-09 — Route 2's build-style names (Standard, Dual Pull, Dual Meet) are not mapped to Bottom Up/Top Down Bottom Up.** No supplier evidence states this mapping; inventing one would misrepresent Route 2's own capability. Recorded as three supplier-named options pending confirmation. Operational block applies — see §5.3. | Claude Code — recorded, not resolved |
| 16 Sep 2026 (ratified by Nazmil Ghany, 16 Sep 2026) | **DR-10 — Route 2's multi-role Organisational Role Schema test.** Full reasoning in §12. This construction's own evidence indicates the same multi-role-per-organisation pattern MCD-01B-08C DR-04 already tested for the Roller construction (one organisation holding a Finished-Blind Manufacturer role for its own route while holding only a Fabric Supplier role toward the other route). Applying MCD-01A §7's objective Extended test: does representing this pattern for a second construction require the Supplier Capability Engine's own resolution logic to change, or only the data it operates on? The engine's actual job (resolving a product configuration to a currently orderable capability record) is unchanged by which construction is being resolved or how many times the same organisational pattern recurs across constructions — this is a second real instance of an already-tested pattern, not a new pattern requiring re-derivation from first principles. **Conclusion: Supplier Capability Engine remains Configured for this application, applying MCD-01B-08C DR-04's conclusion to this construction's own evidence rather than assuming it transfers without testing.** No organisation is named to make this point, consistent with this document's Neutral Document Identity Statement. Conclusion: ratified. | Claude Code — ratified by Nazmil Ghany, 16 Sep 2026 |
| 16 Sep 2026 (ratified by Nazmil Ghany, 16 Sep 2026) | **DR-11 — No cassette or second-enclosure construction applies within this Construction Group for this construction; the frame itself is the sole enclosure.** Compare MCD-01B-08C DR-05 (Roller): the same reasoning is retested, not assumed, for this construction. Test 1: does a cassette-equivalent split exist? No evidence shows an open/enclosed sub-split for either route of this construction — the aluminium frame described in §9.1 is the sole enclosing structure evidenced for both Bottom Up and Top Down Bottom Up, on both routes. No second, cassette-style enclosure option is evidenced. **Conclusion: no cassette/enclosure construction applies**, matching MCD-01B-08C's own conclusion for a different Blind Technology, reached here by independently retesting this construction's own evidence rather than assuming the conclusion transfers. Conclusion: ratified. | Claude Code — ratified by Nazmil Ghany, 16 Sep 2026 |
| 16 Sep 2026 | **DR-12 — Naming governance and neutrality sweep result.** A case-insensitive, word-boundary sweep was run across the whole document — including the Decision Register, Open Evidence Items, and Version History, not only the operative body — for every supplier and organisation name, every brand/system/product name, every document and product code, every price indicator, and every fabric name appearing in either route's evidence. The sweep returned zero matches. Following MCD-01B-08C's own precedent (zero occurrences), the frame system's trademark is not used at all in this document, including as a controlled reference. | Claude Code — neutrality verification |
| 16 Sep 2026 (ratified by Nazmil Ghany, 16 Sep 2026) | **DR-13 — Provisional Safe-by-Design child-safety classification.** Full reasoning in §18. No cord- or chain-operated control is evidenced for this construction on either route. Applying MCD-01B-08 §9's own stated pattern ("handle-operated tensioned systems may be Safe by Design where evidence confirms this") by analogy to this construction's own handle-based control set: the absence of an evidenced cord option supports a provisional Safe-by-Design classification, but the evidence reviewed does not contain an explicit supplier confirmation of this classification (as opposed to a simple absence of any cord-option mention) — recorded as provisional pending that confirmation, not asserted as settled, matching MCD-01B-08C DR-09's identical treatment of its own tensioned-spring control. Conclusion: ratified as provisional. Safe-by-Design remains provisional pending explicit supplier confirmation; Open Evidence Item 11 remains open. | Claude Code — ratified by Nazmil Ghany, 16 Sep 2026 |
| 16 Sep 2026 (ratified by Nazmil Ghany, 16 Sep 2026) | **DR-14 — Cord/ladder colour-matching scope check performed; genuine internal source inconsistency found and logged, not resolved.** Full reasoning in §11, Open Evidence Item 8 (§22). A document-wide list in Route 1's evidence names three system types cord colour-matching applies to, and this construction's system type is not among them; a separate, unscoped footnote in the same source restates the rule without naming which system types it covers. Neither statement is treated as controlling over the other; both are recorded, and the question of whether the colour-matching rule applies to this construction specifically is left open. Conclusion: ratified as logged and unresolved; Open Evidence Item 8 remains open. | Claude Code — ratified by Nazmil Ghany, 16 Sep 2026 |
| 16 Sep 2026 (open) | **DR-15 — Route 1 frame-colour list for this construction differs from MCD-01B-08C's own Route 1 frame-colour list for the Roller construction; recorded, not resolved.** Full detail in §9.1, Open Evidence Item 17 (§22). This construction's own evidence confirms 7 frame colours (including Beige) on Route 1; MCD-01B-08C §9.1 confirms only 6 (no Beige) for the same route on a different Blind Technology. Both routes being labelled "Route 1" across two documents does not itself imply the same organisation offers an identical colour range for every construction it manufactures — a real Blind-Technology-specific difference is at least as plausible as a documentation gap in either document, and this document does not assume either explanation. MCD-01B-08C is not edited or reconciled as a side effect of this correction pass. | Correction-pass instruction to verify this specific claim against MCD-01B-08C's actual content rather than assume it — Claude Code, found and corrected during verification |
| 16 Sep 2026 (open) | **DR-16 — Route 2 frame-colour list: a text-vs-swatch-image inconsistency found in the source itself, recorded rather than resolved.** Full detail in §9.6, Open Evidence Item 18 (§22). The source's own text and the colour-swatch image on the same page do not agree on whether "Anthracite Grey" and "Matt Grey" are two colours or whether "Anthracite" and "Grey" are two separate, unqualified colours. This is an inconsistency within one source document, not a conflict between two different sources — both readings are recorded and neither is treated as controlling, matching the same discipline already applied to the cord/ladder colour-matching inconsistency (DR-14). | Correction-pass instruction to read Route 2's printed page 39 visually and log any difference found — Claude Code, found during that reading |
| 16 Sep 2026 (open) | MCD-00A (Project Development Standards) was not present in the repository when this document was drafted. | This document's own Dependencies require MCD-00A. Governance, versioning, and Decision Register format conventions were instead inherited from their established use in every other product specification in this project, rather than fabricated. | Claude Code — flagged for Nazmil Ghany; not a content defect, a missing-dependency note |

## 24. Version History

| Version | Summary |
|---|---|
| 0.1 | Initial Full-Frame Bead-Mounted Pleated & Cellular Blind Product Specification, drafted per `claude-code-brief-MCD-01B-08D-drafting.md`. Two independently evidenced commercial routes are described neutrally via the Organisational Role Schema: Route 1 (a confirmed full-frame bead-mounted specification, read visually for its dedicated section plus fabric tables) and Route 2 (a page-numbered evidence set, printed pages 37–39, read visually, with pages 35–36 cited only as neutral context for DR-08). Applies MCD-01A's three-test classification model and mirrors MCD-01B-08C's structure throughout, with every conflict, silence, or internal source inconsistency found (including cord/ladder colour-matching scope, DR-14) recorded rather than resolved by assumption. This document's own number (MCD-01B-08D) is proposed, not final (DR-01, pending ratification); DR-10, DR-11, DR-13, and DR-14 are pending ratification; DR-08 and DR-09 are recorded open, not resolved. Status: **Working Draft — Partially Verified**, version 0.1 — not promoted. No other file was modified by this task. |
| 0.1.1 | Correction pass: cross-reference fixes (§2, §3), MCD-01B-08C frame-colour comparison corrected (§9.1), Route 2 frame/headrail evidence added (§9.6), process-artefact references removed (§10, DR-12, §24). |
| 1.0 | Promoted to **Approved Draft Baseline – Product Specification** by Nazmil Ghany, 16 Sep 2026. DR-01, DR-10, DR-11, and DR-14 ratified; DR-13 ratified as provisional only. DR-08, DR-09, DR-15, and DR-16 remain open; a new DR-09 operational block was added (§5.3), barring Product/Survey/Validation/Pricing/Supplier Capability Engine treatment of Route 2's unmapped build styles as Bottom Up or Top Down Bottom Up until supplier evidence confirms the mapping. No open evidence item was resolved by inference. No other file was modified by this task. |
