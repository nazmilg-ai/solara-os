Please update MCD-01B-02.md only. Do not modify MCD-01A or MCD-01B-01.

This replaces any prior version of this fix document. If a previous
version already led to partial changes in MCD-01B-02.md (e.g. a
Decision Register entry containing supplier names, trademarks, part
numbers, or a URL), those need to be corrected to match this version,
not merely added to.

---

## 1. Close the Motorised (Tilt Only) Decision Register item

Replace the existing Decision Register entry regarding the Motorised
(Tilt Only) draw mechanism — including any interim version already
written — with the following resolved entry. This entry must not
contain any supplier name, trademark, brand name, part number, model
number, or URL. Evidence is cited by category only.

> **Decision:** For the Vogue Construction Variant, motorisation
> controls louvre tilt only; traversing (draw) remains manual and is
> performed using the operating wand.
>
> **Evidence:** This decision is supported by supplier technical
> documentation and by advisor trade knowledge and experience with the
> relevant supplier's product range. The supplier's documentation
> confirms that motorisation is compatible with the Vogue Construction
> Variant, tilt only, with draw performed via wand. Advisor trade
> knowledge confirms that motorised tilt was introduced for the
> standard Vertical Blind System before being adopted by a separate,
> later product line that shares the same headrail platform — this
> rules out an alternative reading in which motorisation might be
> exclusive to that later product line rather than available on
> standard Vertical Blinds.
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
> **Detailed evidence:** The underlying supplier documentation, brand
> and part references, and source URLs are retained by Nazmil Ghany
> outside this Product Specification. They will be maintained in MCD-04
> Product Library & Supplier Management once that document is
> introduced into the repository. This Product Specification records
> only the rule and the evidence category, consistent with
> MCD-01B-01's B3 precedent and Constraint 2.
>
> Raised By: Nazmil Ghany, Phase 2 review.

Update the Shared Service Profile (§5) Operation Engine and/or Motor
Engine row notes if they currently reference this as an open item, so
they reflect the resolved rule instead — using Solara terminology only
(e.g. "Vogue Construction Variant"), no supplier names.

Update the Configuration Workflow (§6) and Product Configuration
Summary (§21) Motorised branches to state the locked Wand draw rule
explicitly, replacing any "open item" language, using Solara
terminology only.

---

## 2. Add two confirmed supplier data points

Add to the Validation Rules (§8) and/or Supplier Capability Requirements
(§20), attributed to "supplier technical documentation" only — no
supplier name, brand, or document title:

- Maximum width for Motorised (Tilt Only) operation on the Vogue
  Construction Variant: 3m.
- Minimum blind width with open cassette (Motorised operation on
  Vogue): 200mm.

State clearly that these apply specifically to Motorised operation on
Vogue — do not apply them as general Vogue width limits, since the
source documentation does not state they apply to manual (Wand or
Cord & Chain) operation.

---

## 3. Verification

- Confirm no supplier name, trademark, brand name, part number, model
  number, or URL appears anywhere in MCD-01B-02.md, including the
  Decision Register — this is a hard requirement, not a preference.
- Confirm no "open item" or "pending" language remains referring to
  the Motorised draw mechanism anywhere in the document.
- Confirm the resolved Motorised (Tilt Only) rule is implemented
  consistently across the Decision Register, Shared Service Profile,
  Configuration Workflow, Product Configuration Summary, Validation
  Rules, and Supplier Capability Requirements, with no contradictory
  behaviour remaining elsewhere in the document.
- Confirm the Decision Register entry distinguishes the two evidence
  categories (supplier technical documentation; advisor trade
  knowledge) without naming individual suppliers or documents.
- Add a version-history entry describing this as the Phase 2 closure.
- Commit and push to the current branch.
