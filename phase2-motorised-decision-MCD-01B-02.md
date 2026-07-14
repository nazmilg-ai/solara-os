Please update MCD-01B-02.md only. Do not modify MCD-01A or MCD-01B-01.

---

## 1. Close the Motorised (Tilt Only) Decision Register item

Replace the existing open Decision Register entry regarding the Motorised
(Tilt Only) draw mechanism with the following resolved entry:

> **Decision:** For Slimline Vogue® vertical blind systems, motorisation
> controls louvre tilt only; traversing (draw) remains manual and is
> performed using the operating wand.
>
> **Evidence:**
> 1. Louvolite Commercial's Vertical Blind Systems webpage states:
>    "MOTORISED: Compatible with Slimline Vogue® vertical blinds
>    only... Use wand operation to draw open or draw closed."
>    (louvolitecommercial.com/discover/vertical-blinds)
> 2. Louvolite's technical brochure ("Slimline Vogue® Vertical Blind
>    System — Side Draw with Wand Operation") documents the Vogue
>    Channel with Tilt Rod (part 1019) and the One Touch® Vogue motor
>    pack (part 1140) as components of the standard Vertical Blind
>    system.
> 3. Confirmed by Nazmil Ghany's own trade knowledge: based on Nazmil
>    Ghany's trade knowledge and experience with the Louvolite product
>    range, the first motorised implementation of the Slimline Vogue
>    headrail was introduced for the standard Vertical Blind System.
>    Around six years later, Louvolite developed Allusion®, which
>    adopted the existing Vogue headrail platform rather than
>    introducing a new operating system. Therefore, the Allusion®
>    reference within the technical brochure should not be interpreted
>    as meaning motorisation is exclusive to Allusion — Allusion is
>    another product that utilises the same Vogue headrail and
>    motorisation platform. This is also consistent with Louvolite's
>    current Vertical Blind Systems webpage, which explicitly lists
>    Motorised (Vogue only) as a feature of the Vertical Blind System,
>    while separately marketing Allusion as a different product
>    family.
>
> **Classification:** This is Supplier Capability, not an Advisor
> Selection or Derived Default. The supplier does not manufacture a
> motorised-tilt-with-cord-draw variant, so there is no alternative to
> choose or derive from — the constraint is a manufacturing fact, not
> a configuration choice.
>
> **Applied rule:** When Control Type = Motorised (Tilt Only) and
> Construction Variant = Vogue, Draw Mechanism = Wand automatically.
> No advisor configuration is required or presented.
>
> Raised By: Confirmed by Nazmil Ghany, supported by Louvolite
> Commercial technical documentation (Phase 2 review).

Update the Shared Service Profile (§5) Operation Engine and/or Motor
Engine row notes if they currently reference this as an open item, so
they reflect the resolved rule instead.

Update the Configuration Workflow (§6) and Product Configuration
Summary (§21) Motorised branches to state the locked Wand draw rule
explicitly, replacing any "open item" language.

---

## 2. Add two confirmed supplier data points (from the same brochure)

Add to the Validation Rules (§8) and/or Supplier Capability Requirements
(§20), attributed to the same Louvolite technical brochure:

- Maximum width for Motorised (Tilt Only) operation on Vogue: 3m.
- Minimum blind width with open cassette (motorised): 200mm.

State clearly that these apply specifically to Motorised operation on
Vogue — do not apply them as general Vogue width limits, since the
brochure does not state they apply to manual (Wand or Cord & Chain)
operation.

---

## 3. Verification

- Confirm no "open item" or "pending" language remains referring to
  the Motorised draw mechanism anywhere in the document.
- Confirm the resolved Motorised (Tilt Only) rule is implemented
  consistently across the Decision Register, Shared Service Profile,
  Configuration Workflow, Product Configuration Summary, Validation
  Rules, and Supplier Capability Requirements, with no contradictory
  behaviour remaining elsewhere in the document.
- Confirm the three evidence sources are distinguishable in the
  Decision Register entry (manufacturer webpage, manufacturer
  brochure, advisor trade knowledge) rather than blended together.
- Add a version-history entry describing this as the Phase 2 closure.
- Commit and push to the current branch.
