# Claude Code Brief — MCD-01B-07 Pleated & Cellular Blinds

## Branch

Create a new branch from current main: claude/mcd-01b-07-pleated-cellular

## Read before writing

* MCD-01A_v1.5_for_Claude_Code.md
* MCD-01B-01.md, MCD-01B-02.md, MCD-01B-03.md (governance precedent — especially MCD-01B-03's §4a-style documented three-test reasoning, and MCD-01B-06's specialist-construction classification treatment)
* MCD-01B-04.md, MCD-01B-05.md, MCD-01B-06.md
* MCD-04.md

Do not modify any of the above documents. This brief produces one new document only: MCD-01B-07.md, plus additions to MCD-04.md per the supplier-mapping sections below.

## Document Status

Status: Working Draft — Unverified (matching the standard used for every other pre-review product specification in this project — not "Draft for implementation")
Document type: Product Specification
Architecture: Must comply with MCD-01A
Product scope: Standard vertical-window pleated and cellular blinds only
Supplier neutrality: Required — this applies to the Decision Register, Open Evidence Items, and Version History as strictly as it applies to operative sections. A sentence stating the neutrality rule while naming a supplier is itself a violation — this has recurred multiple times across this project (Roman's Decision Register, MCD-01B-05's §41/§49) and must not recur here.
Supplier capabilities: Stored separately in MCD-04
No assumptions rule: Unsupported combinations must be blocked rather than inferred

---

## Required Classification Questions — apply MCD-01A's three-test model before finalising, do not accept these structures as pre-decided

The sections below describe Free-Hanging/Tensioned, Bottom Up/TDBU/Dual-Fabric, and Fixed Bottom Bar as if their classification were already settled. It is not. Apply the Construction test → Configuration test → Accessory test (MCD-01A §3/§4) to each of the following, and write your reasoning into the Decision Register before finalising the Product Structure in §3. This mirrors the treatment required for Roman's Breakaway (MCD-01B-03 §4a) and Metal Venetian's four specialist constructions (MCD-01B-06) — a confident, detailed presentation of a structure is not the same as a tested one.

**Question 1 — Free-Hanging vs. Tensioned.** Do these two genuinely pass the Construction test (different manufacturing/assembly route, different mechanism) as two Construction Variants, or could either be modelled as a Configuration-layer selection within a single construction? The brief's own §4.1/§4.2 content (different lifting mechanism, different mounting method, different suitability for doors/tilt-and-turn windows) is evidence to reason from, not a conclusion to restate.

**Question 2 — Bottom Up, Top Down Bottom Up, and Dual-Fabric Pleated/Cellular.** Are these three genuinely separate Construction Variants (each with its own manufacturing route — TDBU needs a second rail and independent positioning mechanism; Dual-Fabric needs two fabric sections and an intermediate rail), or is "movement style" better modelled as a Configuration-layer selection within Free-Hanging or Tensioned? Consider whether TDBU and Dual-Fabric could exist as Configuration options within either Construction Variant from Question 1, the same way Roman's four constructions each independently support Manual/Motorised rather than needing separate constructions per operation type.

**Question 3 — Fixed Bottom Bar.** Is this a third Construction Variant (alongside whatever Question 1 and 2 conclude), or a Configuration-layer variant of Tensioned specifically (since the brief's own §6 describes it as "these variants use a permanently fixed lower bar... rather than a freely moving lower profile" — a mechanism detail *within* Tensioned, not necessarily its own construction)?

Document all three conclusions in the Decision Register with the actual three-test reasoning shown, not just the classification stated. The Product Structure tree in §3 below should be treated as provisional pending this reasoning, and corrected if the reasoning concludes differently.

---

## 1. Product Definition

Pleated & Cellular Blinds are fabric blinds formed from either:

* a single pleated fabric layer; or
* a cellular/honeycomb fabric construction.

The product is intended primarily for conventional vertical windows and doors.
The product may be: free-hanging; tensioned; manually operated; motorised, where supported; single-fabric; dual-fabric.

The neutral product specification must not use supplier-specific product names as product categories.

## 2. Product Scope

**Included:** standard free-hanging pleated blinds; standard free-hanging cellular blinds; tensioned pleated blinds; tensioned cellular blinds; Bottom Up operation; Top Down Bottom Up operation; Dual-Fabric Pleated/Cellular systems; fixed-bottom-bar tensioned variants; manual operation; motorisation where supplier capability permits; pleated and cellular fabric eligibility; accessories, hardware and customer expectation warnings.

**Excluded:** Perfect Fit Pleated; Click Fit Pleated; Fit-to-Frame Pleated; INTU Pleated; Micro INTU; roof-window blinds; skylight blinds; rectangular roof blinds; shaped roof blinds; fixed roof blinds; roof-lantern blinds; gable-end blinds; total-blackout framed systems; any specialist screen or fly-screen systems. These belong under their respective Perfect Fit, Roof Blinds, or Specialist Blinds categories — consistent with the standing project decision that Perfect Fit is a separate construction-system family, not a sub-configuration of a standard product (established in MCD-01B-04/05/06).

## 3. Supplier-Neutral Product Structure (provisional — see Required Classification Questions above)

```text
Pleated & Cellular Blinds
├── Free-Hanging
│   ├── Bottom Up
│   ├── Top Down Bottom Up
│   └── Dual-Fabric Pleated/Cellular
│
└── Tensioned
    ├── Bottom Up
    ├── Top Down Bottom Up
    ├── Dual-Fabric Pleated/Cellular
    ├── Bottom Up — Fixed Bottom Bar
    └── Top Down Bottom Up — Fixed Bottom Bar
```

This tree reflects the brief author's working assumption. Correct it if your three-test reasoning above concludes differently (e.g. if movement style is Configuration rather than Construction, this tree collapses to two Construction Variants — Free-Hanging and Tensioned — each with movement style, dual-fabric, and fixed-bottom-bar as Configuration-layer selections).

## 4. Construction Systems

### 4.1 Free-Hanging

A free-hanging system is suspended from the headrail and is not permanently tensioned between the top and bottom of the window. It may use cord operation, dual cord control, motorisation where supported, and supplier-specific internal lifting mechanisms. Free-hanging systems may be suitable for standard windows, standard doors where movement and clearance permit, recess fitting, and exact fitting.

Supplier capability must determine: permitted size; permitted control; fabric eligibility; maximum area; whether motorisation is available; whether TDBU or Dual-Fabric is available.

### 4.2 Tensioned

A tensioned system is held under continuous tension using cords, wires, springs, or supplier-specific tensioning components. The neutral name is **Tensioned**. Do not use "Tab Freehang," "Tab Fit," "Tab Fix," or "Tension Freehang" as neutral construction names — those are supplier aliases and belong in MCD-04.

Tensioned systems may be appropriate for doors, tilt-and-turn windows, shallow or movable installations, applications where fabric movement must be restricted, Bottom Up or TDBU operation, and handle-operated systems.

Supplier capability must determine: tension method; cord or wire arrangement; fixed-point requirements; handle availability; maximum angle or deflection; side-wire availability; fabric compatibility; motorisation compatibility.

## 5. Movement and Operating Styles

### 5.1 Bottom Up

The blind opens from the bottom rail upward; the upper rail remains fixed. Applicable to free-hanging, tensioned, manual, and motorised (where supported).

### 5.2 Top Down Bottom Up

Approved neutral terminology: **Top Down Bottom Up** (may be shown internally as TDBU). The blind may be positioned from both the top and the bottom, allowing the fabric section to sit at different points in the window — providing upper privacy, lower daylight, central positioning, or flexible glare control.

The system must capture: upper rail position; lower rail position; control arrangement; whether top and bottom movement are independently controlled; whether the system is corded, handled, or motorised. Supplier capability must verify availability.

### 5.3 Dual-Fabric Pleated/Cellular

Approved supplier-neutral name: **Dual-Fabric Pleated/Cellular**. Definition: a system containing two separate fabric sections, normally one light-filtering and one blackout or dimout, connected by a movable intermediate rail.

Supplier aliases for this system exist across at least three suppliers — **all supplier alias names and supplier-specific fabric-order rules must remain in MCD-04, not in this document**, matching the treatment already given to §7.1/§7.2's known supplier examples and §11.6/§16's supplier-specific evidence elsewhere in this brief. Do not use "Day & Night" as the neutral name in this document, since it conflicts with zebra/alternating-strip roller blind terminology already established elsewhere in the project.

The system must capture: primary fabric; secondary fabric; upper fabric position; lower fabric position; intermediate rail; fabric pairing compatibility; rail colour; control type; fabric order; whether the fabric order is advisor-selectable; whether the supplier fixes the fabric order. Any specific supplier's fixed fabric-order behaviour (e.g. one supplier positioning the primary fabric at the top) is supplier-specific evidence for MCD-04 and must not become a universal neutral rule in this document.

## 6. Fixed Bottom Bar Variants

The neutral working terminology is "Bottom Up — Fixed Bottom Bar" and "Top Down Bottom Up — Fixed Bottom Bar" (subject to the Required Classification Question 3 above — this may need to be restructured as a Configuration-layer variant of Tensioned rather than named as if a peer-level construction). These variants use a permanently fixed lower bar or lower mounting point rather than a freely moving lower profile, and may be used where the lower edge must remain secured, the blind is installed on a door, increased stability is required, or the supplier provides a fixed-bottom-bar configuration.

Retain "Fixed Bottom Bar" as the working term unless a clearer supplier-neutral term is identified during drafting — log this as an Open Evidence Item either way, do not silently finalise the term without noting it was provisional.

Do not treat side-wire guidance as a separate product construction — side wires are an Accessory/guidance option (see §16).

## 7. Fabric Construction

### 7.1 Pleated Fabric

A single folded fabric layer. Fields: pleat size; fabric name; colourway; room-side colour; glass-side colour; plain; patterned; textured; light-filtering; dimout; blackout; pearl-backed; reflective-backed; fire-retardant; moisture suitability; cleaning method; fabric direction; supplier eligibility.

Known supplier pleat-size examples exist (approximately 20mm for one supplier) — these values must remain in MCD-04, not in this document.

### 7.2 Cellular / Honeycomb Fabric

A multi-layer cellular fabric forming internal air pockets. Fields: cell size; single-cell or double-cell, where supported; light-filtering; dimout; blackout; thermal rating, where evidenced; room-side colour; glass-side colour; fire-retardant; moisture suitability; reflective coating; fabric weight; supplier eligibility.

Known supplier cell-size examples exist (approximately 25mm for one supplier) — supplier-specific, must not be enforced globally, and must remain in MCD-04.

## 8. Fabric Performance Classification

The fabric layer must distinguish:

```text
Light Control
├── Light-Filtering
├── Dimout
└── Blackout Fabric
```

Important rule: **blackout fabric does not mean total blackout.** A blackout pleated or cellular blind can still allow light around the sides, top, bottom, control cords, rail junctions, or intermediate rails. Total-blackout solutions belong under Specialist Blinds, not this product.

## 9. Operation Modes

The product must support the standard MCD-01A operation model:

```text
Operation Mode
├── Manual Only
├── Manual / Motorised — Advisor Selection
├── Manual / Motorised — Factory Selection
├── Motorised Only
└── Not Supported
```

Supplier capability determines which status applies.

## 10. Manual Controls

Possible manual control types:

```text
Manual Control
├── Cord
├── Dual Cord
├── Handle
├── Wand
└── Crank, only where supplier-supported
```

**Cord** — fields: control side; cord colour; cord length; cord lock type; cleat or safety device; child-safety requirement; installation height; breakaway device where applicable.

**Dual Cord** — primarily relevant to TDBU and Dual-Fabric systems. Fields: left control function; right control function; cord side arrangement; rail controlled; supplier-defined operating logic.

**Handle** — primarily relevant to tensioned systems. Fields: handle colour; handle position; handle quantity; handle compatibility; accessibility at installation height.

**Wand** — only include where the supplier offers wand operation for a standard vertical-window construction. Do not assume wand availability globally.

**Crank** — not expected to be a common standard-window option; should only appear when enabled by supplier capability.

## 11. Motorisation

Motorisation must be included as an eligible operation but must not be presented as universally available.

```text
Pleated & Cellular Blind
→ Select Construction
→ Select Movement Style
→ Select Fabric
→ Select Operation
→ Supplier Capability Validation
→ Motor Eligibility
```

Motorisation must be validated against: supplier; construction; movement style; fabric; width; drop; area; weight; control protocol; power source.

### 11.1 Motorisation Eligibility

The system must not assume that motorisation is available for every supplier, every pleated construction, every cellular construction, TDBU, Dual-Fabric, tensioned systems, or fixed-bottom-bar systems. Each combination must be explicitly supported by supplier capability. Unsupported combinations must display: "This combination is not supported by the selected supplier."

### 11.2 Motor Selection Responsibility

```text
Motor Selection Responsibility
├── Advisor Selectable
├── Factory Selected
└── Supplier Predefined
```

For pleated and cellular systems, factory or supplier selection may often be appropriate because the motor depends on blind weight, rail type, fabric weight, size, movement type, and internal lifting system.

### 11.3 Power Options

```text
Power Type
├── Rechargeable Battery
├── External Battery Pack
├── Solar-Assisted Battery
├── 240V Mains
├── Low-Voltage Hardwired
└── Supplier-Specific
```

Only display power options supported by the selected motor and supplier. Capture: charger required; charging-port location; charging access; transformer required; transformer location; cable-exit position; cable length; solar-panel position; battery replacement access; estimated charge duration, only if supplier-evidenced.

### 11.4 Controls

```text
Motor Control
├── Handheld Remote
├── Wall Switch
├── Smart Hub
├── App Control
├── Voice Assistant
├── Group Control
└── Supplier-Specific Control
```

Capture: protocol; channel number; room grouping; individual blind channel; central control; smart-home compatibility; hub requirement.

### 11.5 Motor Position

```text
Motor Position
├── Left
├── Right
├── Internal / Not Selectable
└── Factory Determined
```

Do not display left/right selection unless the supplier permits it.

### 11.6 Supplier Motorisation Evidence

At least one supplier is known to support motorised pleated systems for some eligible constructions, with approximate dimensional limits gathered from current evidence. **These figures, the motor technology name, and the supplier identity are supplier-specific and must remain in MCD-04, not in this document.** Do not assume that any supplier supports motorised TDBU, motorised Dual-Fabric, motorised tensioned Bottom Up, or motorised fixed-bottom-bar variants unless those specific combinations are independently confirmed — log each as an Open Evidence Item where not yet confirmed.

## 12. Measurement Model

### 12.1 Measurement Type

```text
Measurement Type
├── Recess
└── Exact
```

Perfect Fit and frame-mounted measurement rules are excluded.

### 12.2 Required Measurements

Core fields: width; drop; measurement type; measurement unit; installation height; window orientation; opening type; handle projection; bead depth, where relevant; recess depth; sill projection; obstruction notes; photo evidence; advisor notes.

### 12.3 Width and Drop

Measurements must be recorded to the supplier-required precision. Supplier capability must determine minimum width; maximum width; minimum drop; maximum drop; maximum area; width-dependent maximum drop; fabric-dependent restrictions; control-dependent restrictions. The platform must not use one universal maximum size.

### 12.4 Recess Measurement

Capture: top width; middle width; bottom width; left drop; centre drop; right drop; smallest width; smallest drop; squareness warning; obstruction warning. The deduction method is supplier-specific — do not apply a universal deduction unless explicitly configured.

### 12.5 Exact Measurement

Capture: finished requested width; finished requested drop; overlap required; fixing surface; fixing clearance; handle or architrave obstruction; selected fixing type.

## 13. Window and Door Suitability

```text
Opening Type
├── Fixed Window
├── Casement Window
├── Tilt-and-Turn Window
├── Door
├── French Door
├── Sliding Door
└── Other
```

The recommendation engine may suggest tensioned construction for doors, tilt-and-turn windows, frequently opened windows, and applications where fabric movement is undesirable. This must remain a recommendation rather than a mandatory restriction unless supplier rules require it.

## 14. Hardware and Profile Options

Capture: headrail colour; intermediate rail colour; bottom rail colour; moving rail colour; handle colour; cord colour; bracket colour; end-cap colour; profile finish; supplier profile code; pleat matching (as a fabric-manufacture characteristic, not a same-room service — see the removal in the Same-Room note below); rail matching; fabric alignment.

The UI should only display values supported by the selected supplier.

## 15. Fixing and Installation

### 15.1 Fixing Position

```text
Fixing Position
├── Top Fix
├── Face Fix
├── Side Fix
└── Supplier-Specific
```

### 15.2 Fixing Surface

```text
Fixing Surface
├── uPVC
├── Timber
├── Plaster
├── Masonry
├── Metal
├── Tile
└── Other
```

### 15.3 Brackets

Capture: bracket type; standard bracket; extension bracket; fixing screw type; fixing quantity; bracket spacing; rail clearance; obstruction clearance. Bracket selection may be supplier-defined.

## 16. Side-Wire and Guidance Options

Side-wire guidance is an accessory or construction option, not a separate product. Fields: side wires required; wire colour; wire position; wire fixing method; maximum allowable deflection; bottom fixing type; wire-tension adjustment; supplier eligibility.

Known supplier evidence indicates side-wire availability on some fixed-bottom-bar tensioned models with an approximate maximum deflection angle — **this figure and the supplier identity belong in that supplier's capability record in MCD-04, not in this document.**

## 17. Duplication Rules

When duplicating a pleated/cellular blind item, the platform must copy: product construction; movement style; fabric type; fabric; colourway; operation; control; rail colour; handle colour; supplier; accessories; room grouping.

Differences must be highlighted where the duplicate varies by: width; drop; control side; movement style; fabric; operation; motor; power type; profile colour; supplier. The advisor must confirm any deviation.

## 18. Child Safety

Corded pleated and cellular blinds must comply with the shared Child Safety Service. Capture: corded control present; cord length; installation height; child-safety device; device fixing location; customer refusal; refusal reason; advisor acknowledgement; customer signature; date and time; GPS location, where platform policy requires; photographic evidence.

Motorised and handle-operated products may reduce cord-related risk but must not bypass other safety checks.

## 19. Customer Expectation Warnings

The system should display warnings where applicable:

* **Blackout Fabric Warning:** "This product uses blackout fabric, but light may remain visible around the sides, top or bottom of the blind. Blackout fabric does not create a total-blackout room."
* **Dual-Fabric Warning:** "Dual-fabric systems include a visible intermediate rail between the two fabric sections."
* **Cellular Fabric Warning:** "Cellular fabric may improve thermal comfort, but it does not replace insulated glazing or eliminate heat loss."
* **Tensioned-System Warning:** "Tension cords, wires or fixing points may remain visible depending on the selected system."
* **Pattern Warning:** "Patterned fabrics may not align identically across separate blinds unless the supplier specifically supports pattern matching."

## 20. Recommendation Engine Logic

The recommendation engine may suggest, for a standard window: Free-Hanging Bottom Up for straightforward windows; TDBU where privacy and daylight control are required; Dual-Fabric where separate daytime and blackout fabrics are desired; cellular fabric where improved thermal comfort is important.

For doors and tilt-and-turn windows: tensioned construction where the blind must remain controlled against the glazing.

For a blackout requirement: blackout cellular fabric for improved room darkening; a Specialist Total Blackout System where the customer requires significantly reduced perimeter light.

The engine must not describe blackout pleated/cellular blinds as total blackout.

## 21. Pricing Inputs

The neutral pricing engine must support: supplier base price; pricing table; price band; width; drop; next-size-up pricing; square-metre pricing; minimum charge; construction surcharge; TDBU surcharge; Dual-Fabric surcharge; fabric surcharge; blackout surcharge; motor surcharge; remote surcharge; charger surcharge; solar panel surcharge; profile-colour surcharge; side-wire surcharge; delivery; installation; margin; discount; VAT.

Supplier pricing structures belong in MCD-04.

## 22. Supplier Capability Record

Each supplier must have an independent capability record covering:

```text
Supplier Capability
├── Available Constructions
├── Available Movement Styles
├── Fabric Eligibility
├── Control Eligibility
├── Motorisation Eligibility
├── Minimum and Maximum Sizes
├── Maximum Area
├── Rail Colours
├── Handle Colours
├── Cord Colours
├── Side-Wire Availability
├── Pricing Method
├── Lead Time
├── Warranty
└── Supplier Aliases
```

## 23. Known Supplier Mapping (MCD-04 content only — do not include supplier names in MCD-01B-07.md)

**This entire section, including every supplier name, product name, and code below, must be transcribed only into MCD-04.md, never into MCD-01B-07.md.** MCD-01B-07.md's own operative sections must reference the neutral construction/movement-style names only (Free-Hanging, Tensioned, Bottom Up, TDBU, Dual-Fabric Pleated/Cellular, Fixed Bottom Bar). This mirrors the exact treatment already required for Metal Venetian's Arena/Decora/Beverley mappings and Wooden Venetian's Sunwood/Starwood/Timberlux ranges.

Known supplier terms exist across at least three suppliers, including construction-name aliases (e.g. one supplier's "Standard Cord Freehang," "Tab Freehang," "TriLite," "Transition," "Night & Day"), and a second supplier's own product-code series (a "CZP01" through "CZP08" range mapping to Free-Hanging/Tensioned Bottom Up, TDBU, and Dual-Fabric variants, with frame-mounted codes from CZP09 onwards correctly excluded as Perfect Fit-equivalent), and a third supplier's own naming ("Pleated Freehang," "Tension Freehang," "Standard Tensioned," "3 Bar Tensioned," "Duo Meet").

Populate MCD-04 with the full neutral-to-supplier mapping for all three suppliers using the Structured Technical Value / evidence conventions already established, citing the specific source for each mapping. Where a mapping is not yet confirmed (e.g. one supplier's "Transition" and "Night & Day" naming, which needs exact construction confirmation before mapping), record it as "Supplier confirmation required" rather than inferring the mapping — do not guess which neutral construction these correspond to.

## 24. Validation Rules

The system must validate: selected supplier supports selected construction; selected fabric supports selected construction; selected control supports selected construction; selected movement style is available; width is within supplier limits; drop is within supplier limits; area is within supplier limits; selected fabric is within its own limits; motor supports the blind size and weight; power type supports the motor; TDBU is allowed; Dual-Fabric is allowed; fixed-bottom-bar variant is allowed; side wires are allowed; profile colour is available; control side is selectable; motor position is selectable.

Validation outcomes:

```text
Validation Status
├── Valid
├── Warning
├── Supplier Confirmation Required
└── Blocked
```

## 25. Advisor Freedom

The platform must preserve advisor control. The system may recommend, explain, warn, compare, and validate supplier restrictions. The system must not unnecessarily force one fabric, one supplier, one control, one construction, or one recommendation. Only genuine technical, safety, or supplier restrictions should block a selection.

## 26. Required UI Sequence

```text
1. Room
2. Window / Door Type
3. Measurement Type
4. Width and Drop
5. Construction
6. Movement Style
7. Fabric Construction
8. Fabric
9. Colourway
10. Operation
11. Manual Control or Motor
12. Power
13. Control Device
14. Profile Colour
15. Accessories
16. Child Safety
17. Supplier
18. Validation
19. Price
20. Advisor Notes
21. Customer Expectation Acknowledgement
```

The exact order may be adjusted for usability, but supplier validation must occur before final pricing.

## 27. Final Product Boundaries

```text
Pleated & Cellular Blinds
= Standard vertical-window pleated and cellular systems
```

It must not absorb frame-mounted products, Perfect Fit systems, roof systems, lantern systems, gable systems, total-blackout systems, or supplier-branded specialist systems.

The product may share: Survey Service; Measurement Service; Validation Service; Motor Service; Child Safety Service; Pricing Service; Accessory Service; Supplier Capability Service; Recommendation Service; Document Generation Service; Audit Service — subject to the Shared Service Profile reasoning required below, not assumed.

## 28. Shared Service Profile — required reasoning, not a checklist

Do not simply list the twelve services as shared and move on. Apply MCD-01A §7's actual Extended test (a shared service needs new capability the platform doesn't already have — not "more complex" or "more parameters") to each of the twelve services, matching the standard already required for every other product spec in this project. Pay particular attention to:

* **Validation Service** — does validating the movement-style/construction combinations, the TDBU/Dual-Fabric/fixed-bottom-bar eligibility rules, and the width-dependent maximum-drop logic require new platform capability, or is this parameterisation of existing dimension/compatibility rules (compare to Roman's and Metal Venetian's Configured conclusions for comparably complex validation)?
* **Motor Engine** — does the motorisation-eligibility-by-combination logic (construction × movement style × fabric × dimensions) require new capability, or does the existing capability-based eligibility/disabling pattern already handle it (compare to Metal Venetian's Motor Engine reasoning)?
* **Supplier Capability Engine** — does representing three suppliers' differing construction/movement-style/fabric-order naming and mapping require new schema capability, or does the existing Supplier → Range → Construction hierarchy already accommodate it?

Record the conclusions and reasoning for all twelve services in the Decision Register.

## 29. Decision Register and Version History requirements

MCD-01B-07.md must include a numbered Decision Register (Date | Decision | Reasoning | Raised By) and a Version History section, matching the format used in every other product specification in this project. At minimum, log:

1. The three Required Classification Question conclusions and reasoning (Free-Hanging/Tensioned; Bottom Up/TDBU/Dual-Fabric; Fixed Bottom Bar).
2. The Shared Service Profile reasoning for all twelve services.
3. Confirmation that Perfect Fit, Click Fit, Fit-to-Frame, INTU, and all roof/lantern/gable/specialist systems are excluded.
4. Confirmation that Same-Room matching does not apply to this product and has been fully removed (see the dedicated section below).
5. The standing MCD-00A missing-dependency note, consistent with every other document in this project.

Mark Decision Register entries representing genuine judgment calls (the three classification questions, the Shared Service Profile conclusions) as pending ratification by Nazmil Ghany, matching the pattern used for every other product in this project.

## 30. Same-Room Matching — explicitly excluded, not merely omitted

Same-Room matching does not apply to Pleated & Cellular Blinds and must not appear anywhere in this specification as a product option, service, or capability. This is a confirmed correction, not an oversight to silently work around. Specifically, this document must NOT contain:

* A "Same-Room Options" section or equivalent.
* Pleat alignment as a selectable same-room service.
* Room grouping framed as implying a matching or alignment guarantee.
* Same-room surcharges.
* Same-room supplier capability fields.
* Same-room validation rules.
* Any customer warning framed around supplier-supported pleat alignment as a purchasable service.
* "Same-room option" or "pleat matching as a same-room service" or "rail matching as a same-room service" anywhere in the Hardware and Profile Options section (§14) — §14 above has already been corrected to remove these; confirm this correction is preserved.

Pleated blinds may still be grouped by room for ordinary quoting, ordering, and installation purposes — this is a normal room/location reference only, and must not imply any matching service or alignment guarantee. The confirmed governing principle: "Same-room matching does not apply to Pleated & Cellular Blinds and must not appear as a product option."

## 31. Open Items Requiring Confirmation

Claude must not invent answers for these items — mark each as "Supplier confirmation required" rather than completing them through assumption:

* One supplier's exact neutral mapping for its "Transition" and "Night & Day" naming.
* That supplier's motorisation eligibility for TDBU, Dual-Fabric, and tensioned constructions.
* A second supplier's standard-window motorisation availability.
* A third supplier's standard-window motorisation availability.
* Whether "Fixed Bottom Bar" will remain the final neutral term (see §6).
* Exact supplier control-side rules.
* Exact supplier fabric-order rules for Dual-Fabric systems.
* Current supplier lead times, warranties, and pricing.

## Verification

* Confirm zero supplier names, trademarks, product names, or part numbers appear anywhere in MCD-01B-07.md — full sweep, including the Decision Register, Open Evidence Items, and Version History. §23's supplier mapping content must be entirely in MCD-04, not here.
* Confirm the three Required Classification Questions are reasoned in the Decision Register with actual three-test analysis shown, and that §3's Product Structure tree reflects the actual conclusion, not the brief's provisional assumption, if they differ.
* Confirm the Shared Service Profile reasoning is documented for all twelve services, with particular attention to Validation Service, Motor Engine, and Supplier Capability Engine.
* Confirm Same-Room matching does not appear anywhere in the document in any form (§30's checklist).
* Confirm §5.3's supplier-alias content and §7.1/§7.2/§11.6/§16's supplier-specific figures are absent from MCD-01B-07.md and present in MCD-04 with proper source attribution instead.
* Confirm MCD-01A, MCD-01B-01 through MCD-01B-06 remain unmodified.
* Add a Version History entry naming all open items by content (the Open Items list, the classification questions pending ratification, the Shared Service Profile conclusions pending ratification, the standing MCD-00A note).
* Commit and push to the new branch. Do not open a pull request or merge.
