# Claude Code Brief – MCD-01B-02 Vertical Blinds

Pull latest `main`.

Read the following documents before making any changes:
- MCD-00A (Approved)
- MCD-01A v1.5 (Approved Draft Baseline)
- MCD-01B-01 Roller Blinds v1.5 (Approved Draft Baseline)

Roller Blinds is the structural template only. Vertical Blinds has significantly more dynamic behaviour and supplier capability and should not be forced to match Roller where the product requires a richer model.

---

## Objective

Produce the first complete draft of **MCD-01B-02 – Vertical Blinds Product Specification**, maintaining the same document structure and writing standard as MCD-01B-01.

Produce this draft while preserving the architectural boundaries established by MCD-01A v1.5. Where a design decision appears to expose a potential architectural ambiguity, document it within MCD-01B-02 rather than modifying or extending MCD-01A.

---

## Architectural Constraints

Before writing MCD-01B-02, the following constraints apply:

1. The Product Specification shall remain supplier-independent.
2. Named suppliers belong only in the Supplier Capability Library — never in MCD-01B-02 itself.
3. Derived Defaults are a documentation pattern only, not a new architectural layer.
4. Advisor Selection / Derived Default / Supplier Capability are documentation conventions only, not a new architectural layer.
5. Deliberate business restrictions (e.g. 89mm-only louvre width) shall be reflected in the Shared Service Profile using the appropriate Shared Service Status rather than implied by omission — subject to the Architectural Review Question below.

---

## Product Scope

**Construction Variants:**
- Slimline
- Nova
- Cruze
- Vogue
- Curved Vertical
- Sloping Vertical

Curved and Sloping are specialist construction variants.

Supplier availability for Curved and Sloping is defined within the Supplier Capability Library. (Do not name suppliers in this document — see Architectural Constraints above.)

---

## Louvre Width

Sales MVP supports 89mm only. 127mm shall not appear in normal advisor workflow. Retain only as Legacy/Future capability.

Reason: very low market demand; declining supplier fabric availability.

See the Architectural Review Question below for how this should be classified in the Shared Service Profile.

---

## Control Types

There are only three control types:
- Wand
- Cord & Chain
- Motorised (Tilt Only)

Do not introduce additional terminology such as "Wand & Cord," "Split Wand," or "Mono Control." These are supplier implementations, not Product Engine terminology.

### Dynamic Configuration Workflow

**Wand** — if selected, display: Wand Left / Wand Right / Split Draw. Supplier Capability determines whether Split Draw is manufactured using a single centre wand or two wands. The advisor does not choose this.

**Cord & Chain** — if selected, display Control Side (Left / Right), then a separate Draw Configuration (Left Stack / Right Stack / Split Draw). These are separate selections.

**Motorised** — applies only to louvre tilt, not traversing. Display: Motor Left / Motor Right. No motorised draw.

---

## Headrail Systems

Headrail systems are: Slimline, Nova, Cruze, Vogue. Curved and Sloping remain specialist construction variants.

---

## Headrail Colours

Headrail Colour is a customer-facing selection. Available colours are determined by Supplier Capability.

Examples verified so far: Nova (White, Grey, Black); Vogue (White, Grey, Anthracite, Brown, Black, Brushed Aluminium, Champagne Gold). Do not hard-code supplier colour lists beyond examples already verified — remaining colour ranges (e.g. Cruze, Slimline) are determined by the Supplier Capability Library and shall not be named here.

### Derived Defaults

Selecting Headrail Colour shall automatically determine: Wand colour, Cord colour, Bracket colour, end caps, and other matching visible hardware. The advisor is never prompted separately for these. This is Product Engine behaviour; Supplier Capability provides the compatible components.

---

## Brackets

The advisor selects Bracket Type only (e.g. Face Fix, Top Fix, Extension Bracket). Bracket colour is automatically derived from Headrail Colour. Supplier Capability determines the correct physical bracket. The advisor never selects bracket colour.

---

## Chain

Only displayed for Cord & Chain operation. Options: White Plastic (Standard), Steel Chain (Optional Upgrade). Pricing supplied by Supplier Capability.

## Bottom Weights

Options: White (Standard), Black (Optional Upgrade). Pricing supplied by Supplier Capability.

## Bottom Stabilising Chain

Colour options: White (Standard), Black (Optional Upgrade). Pricing supplied by Supplier Capability.

## Bottom Chain

Options: Standard, No Chain. If No Chain is selected, do NOT simply remove the chain — Supplier Capability shall automatically substitute the standard chained bottom weight system with the supplier's compatible chainless bottom weight system. The advisor is not asked to choose bottom weight type.

---

## Automatic vs Advisor Selection

The specification shall clearly distinguish, throughout the document: Advisor Selections; System Derived Defaults; Supplier Capability. These concepts should remain separate throughout.

---

## Survey Rules

Vertical-specific survey includes: Construction Variant, Control Type, Draw Configuration, Headrail Colour, Bracket Type, Fabric, Colourway, Bottom Weight Colour, Bottom Chain Colour, Bottom Chain. Curved and Sloping introduce additional supplier-specific survey requirements.

## Measurement Rules

Do not duplicate MCD-01A. Reference the shared Measurement Engine. Only include Vertical-specific measurements such as: Stack clearance, Headrail projection, Bracket projection, Curved geometry, Sloping geometry, Specialist supplier dimensions.

## Validation Rules

Include validation for: Construction Variant compatibility, Control Type compatibility, Draw Configuration compatibility, Headrail Colour availability, Bracket compatibility, Supplier manufacturing limitations, Curved/Sloping validation.

## Child Safety

Follow the Roller pattern. Reference MCD-01A. Only include Vertical-specific implementation. Do not restate shared Child Safety responsibilities.

## Supplier Capability

Keep supplier implementation out of the Product Specification. Supplier Capability should own: headrail colours, component compatibility, bracket compatibility, motor compatibility, size limits, manufacturing limits, premium options, colour synchronisation, technical dimensions.

## Product Configuration Summary

Add a Product Configuration Summary section summarising the complete advisor workflow — this will become the implementation blueprint for the UI.

---

## Architectural Review Question

Do not modify MCD-01A. The following is an architectural review only.

Sales MVP deliberately exposes only 89mm vertical louvre width, while 127mm remains available as Legacy/Future capability. MCD-01A currently demonstrates Restricted status only using whole-engine examples (e.g. Operation Engine losing an entire operation mode). Please assess the following separately:

**A. Current Documentation**
How should this specific Product Specification document the deliberate exclusion of 127mm? Consider whether it should be:
- A documented Product Specification business rule.
- A note within an otherwise Configured Shared Service.
- Another approach consistent with MCD-01A.

Provide your reasoning.

**B. Architectural Assessment**
Does this reveal an ambiguity in the current definition of Shared Service Statuses within MCD-01A regarding the granularity of Restricted (whole-engine vs. a single configuration value within an otherwise Configured service)? If yes: explain why; explain whether this is likely to recur in future Product Specifications; and state whether it should simply be tracked for future evidence or whether it already justifies an architectural clarification.

Do not amend MCD-01A.

### Decision Register Requirement

Regardless of your conclusions, record the outcome within MCD-01B-02's Decision Register.

Future Product Specifications shall distinguish between the two review questions as follows:

- **Question A – Precedent.** If the same documentation question arises in a future Product Specification, reference this decision rather than reassessing it from first principles, unless the underlying architecture has changed.
- **Question B – Evidence Tracking.** If the same architectural ambiguity arises in a future Product Specification, create a new Decision Register entry describing the new occurrence and reference this earlier decision. Each occurrence should be logged independently so evidence can accumulate across products. When sufficient evidence exists that the same ambiguity affects multiple Product Specifications, it may justify a future clarification to MCD-01A. Until then, MCD-01A remains unchanged.

---

## Review Requirements

Before committing:
- Check for duplication against MCD-01A.
- Ensure only Vertical-specific logic remains.
- Ensure every advisor question is intentional.
- Ensure every automatic decision is documented as a derived default.
- Ensure supplier-specific implementation remains in Supplier Capability.
