Please update MCD-01B-02.md only. Do not modify MCD-01A or MCD-01B-01.

Apply the following Phase 1 content corrections.

---

## 1. Product Configuration Summary — Installation Height

Installation Height is an advisor-facing Survey Requirement in §6 but is
missing from the Product Configuration Summary in §21.

Add Installation Height to the measurement/survey step alongside:
- Recess / Exact Fit
- Width
- Drop

The Product Configuration Summary must include every advisor-facing
question required by the detailed workflow.

---

## 2. Wand workflow clarification — confirmed business rule

This is a confirmed product/business decision (not an open architectural
question): for Wand operation, control position and stack direction are
physically coupled by the headrail design.

Add an explicit rule in §6 (Dynamic Configuration Workflow) and §21
confirming:
- Wand Left = wand positioned left and blind stacks left.
- Wand Right = wand positioned right and blind stacks right.
- Split Draw = centre split; Supplier Capability determines whether the
  system uses one central wand or two wands.

Do not introduce separate Control Side and Draw Configuration questions
for Wand operation. Retain the existing separate Control Side and Draw
Configuration questions for Cord & Chain operation, unchanged.

---

## 3. Accessories reconciliation — Control Type

Add a reconciliation paragraph in §16 explaining:

Control Type is a Configuration-layer selection. It determines which
control-related Accessory Engine items become eligible:
- Wand operation enables the compatible wand components.
- Cord & Chain operation enables compatible cord and chain components.
- Motorised Tilt enables the compatible motor-control accessories.

The advisor selects the Control Type; the Accessory Engine and Supplier
Capability Engine determine the eligible physical components.

---

## 4. Accessories reconciliation — Chain Type

Add a reconciliation paragraph in §16 explaining:

Chain Type is a Configuration-layer selection shown only when Cord &
Chain operation is selected. It determines which compatible physical
chain item is supplied:
- Standard white plastic chain.
- Optional steel chain.

The advisor selects the chain type; the Accessory Engine and Supplier
Capability Engine resolve the compatible product/SKU and pricing.

---

## 5. Terminology standardisation — "Bottom Chain" (confirmed business
   decision, resolves the §15 open item)

This resolves the Decision Register entry in §15 currently marked
"pending confirmation by Nazmil Ghany" (the terminology-reconciliation
row). It is no longer pending — the following is the confirmed product
definition:

- **Bottom Weights** — the plastic weights inserted into every vane.
  These always exist. Advisor Selection: White (Standard) or Black
  (Optional Upgrade).
- **Bottom Chain** — the chain joining the bottom weights together.
  Advisor Selection: White, Black, or No Chain.
  - If **No Chain** is selected, the manufacturer does not simply
    remove the chain — a different bottom weight system designed for
    chainless operation is used instead. The advisor never chooses the
    weight type in this case; the substitution is a Derived Default,
    resolved automatically by the Supplier Capability Engine.

**Remove "Bottom Stabilising Chain" as internal terminology throughout
the document.** Standardise on "Bottom Chain" everywhere (§6, §15, §16,
§18, §21, and the Decision Register). Do not use "Bottom Stabilising
Chain" except when directly quoting supplier literature, if that ever
occurs.

Update the §15 Decision Register entry to reflect this as a confirmed
decision (not an open item): the terminology is standardised on "Bottom
Chain," and this entry should now read as resolved, raised/confirmed by
Nazmil Ghany, rather than "pending confirmation."

---

## 6. Pricing Inputs consistency

Separate the Bottom Chain pricing inputs into distinct entries:
- Bottom Chain Presence
- Bottom Chain Colour

Keep Bottom Weight Colour as its own separate input, unchanged.

Do not invent prices or supplier values.

---

## 7. Product Configuration Summary — Louvre Width

Remove Louvre Width as a numbered workflow step.

Instead, record it as an unnumbered system-default note near the
beginning of §21:

"Sales MVP applies 89mm louvre width as a system default. It is not an
advisor-facing workflow step. The deliberate exclusion of 127mm is
documented in §4, §8, and the Decision Register."

---

## 8. Verification

After editing:
- Confirm every advisor-facing Survey Requirement in §6 appears in §21.
- Confirm no separate Control Side question appears under Wand operation.
- Confirm the two new reconciliation paragraphs are present in §16
  (Control Type; Chain Type).
- Confirm "Bottom Stabilising Chain" does not appear anywhere in the
  document outside a direct supplier-literature quotation (if any).
- Confirm Louvre Width is no longer presented as a numbered advisor step.
- Confirm the §15 Decision Register entry now reads as resolved, not
  pending.
- Add a version-history entry describing these corrections.
- Commit and push the updated file on the current branch.

Do not alter any unresolved supplier-data items or substantive product
rules beyond the changes above.
