# Claude Code Brief – MCD-04 Product Library & Supplier Management

Create a new branch from main: claude/mcd-04-supplier-capability-library

Read before writing:
- MCD-01A_v1.5_for_Claude_Code.md (Approved Draft Baseline)
- MCD-01B-01.md (Approved Draft Baseline – Product Specification)
- MCD-01B-02.md (Draft v1.2 – Product Specification)

---

## Objective

Create MCD-04.md — Product Library & Supplier Management — as a Draft
Skeleton. This is a new document, not an extension of an existing one.

Do not attempt to design a complete supplier capability library today.
Establish the document architecture and one real, fully-populated
record only. The structure should grow from real records added over
time (Roller, Roman, Curtains, Shutters, and Vertical's own remaining
Construction Variants), not be speculatively designed now.

Do not modify MCD-01A, MCD-01B-01, or MCD-01B-02.

---

## Critical scope boundary — read this before writing anything else

**MCD-04 is the deliberate exception to Constraint 2.** Product
Specifications (MCD-01B-xx) must remain supplier-independent — no
supplier names, trademarks, part numbers, or URLs anywhere in them.
MCD-04 is the opposite: it is *specifically* the place where supplier
names, trademarks, brand names, part numbers, model numbers, and
source URLs belong and are expected to appear throughout.

State this explicitly in MCD-04's own Scope section, in these terms:
"Unlike Product Specifications (MCD-01B-xx), which must remain
supplier-independent per MCD-01A §3/§9 and their own design briefs,
this document is the designated location for supplier-specific detail.
Naming suppliers, brands, trademarks, part numbers, and source URLs
here is expected and required, not a violation of Solara's
supplier-independence principle. Do not apply Product Specification
supplier-neutrality rules to this document."

This is important: without stating it plainly, a future review pass
could mistakenly try to "clean up" MCD-04 the same way MCD-01B-02 was
cleaned up, which would defeat the document's purpose.

---

## Document Structure

### 1. Purpose

MCD-04 is the permanent, authoritative record of supplier capabilities
for the Solara product range — what specific suppliers can actually
manufacture, supply, and support, with the evidence behind each claim.
Product Specifications (MCD-01B-xx) reference capabilities defined
here; they do not embed supplier-specific detail themselves.

### 2. Scope

Include the critical scope boundary statement above. State that this
document covers supplier capability records for all Solara product
families as they are developed (Vertical Blinds now; Roller, Roman,
Curtains, Shutters, Perfect Fit, and others as their own supplier
capability evidence is gathered).

### 3. Relationship to MCD-01A and MCD-01B-xx

State plainly: MCD-01A defines the Supplier Capability Engine as one
of the twelve Shared Platform Services (§5.9) and requires that
Product Specifications reference Supplier Capability rather than
embed it. MCD-04 is the document that Supplier Capability Engine rows
in each Product Specification's Shared Service Profile point to. A
Product Specification's Decision Register should cite evidence by
category only ("supplier technical documentation," "advisor trade
knowledge") and reference "see MCD-04" for the underlying detail, once
this document exists — matching the precedent set in MCD-01B-02 §23's
resolved Motorised (Tilt Only) entry.

### 4. Governance

Follow the same conventions as MCD-01B-01 and MCD-01B-02: Decision
Register format (Date | Decision | Reasoning | Raised By), version
history, and status labelling (Draft Skeleton for this first version).
Note, consistent with prior documents in this repo, that MCD-00A
(Project Development Standards) is referenced but not yet present in
the repository — inherit its conventions from how MCD-01B-01 and
MCD-01B-02 already apply them, and log this as a Decision Register
entry rather than fabricating MCD-00A's content.

### 5. Record Structure

Each Supplier Capability Record contains the following fields:

- **Capability** — a short name for what this record documents (e.g.
  "Motorised Tilt Operation").
- **Business Rule** — the Solara-terminology rule this capability
  supports or constrains, expressed exactly as it appears (or should
  appear) in the relevant Product Specification's Decision Register.
- **Technical Specification** — the underlying technical facts:
  dimensions, performance parameters, tolerances, compatible
  components, part numbers, colours, and similar detail.
- **Evidence** — the specific source material supporting the Business
  Rule and Technical Specification: named suppliers, brochures,
  webpages, URLs, direct quotations (kept short and clearly marked as
  quotations), and advisor trade knowledge, clearly attributed.
- **Source References** — direct citations: document titles, URLs,
  brochure identifiers, and the date each source was accessed,
  published, or confirmed. Include this date for every source listed,
  not just where convenient — it is what lets a later reviewer judge
  whether a record has gone stale.
- **Validation Status** — e.g. Confirmed, Awaiting Supplier
  Confirmation, Superseded, Under Review.
- **Revision History** — dated log of changes to this specific record
  (not the whole document), noting what changed and why (e.g.
  "supplier revised specification," "additional evidence obtained").

### 6. Document Organisation

Organise records by Solara product architecture first, supplier
second — never the reverse. Structure:

```
Supplier Capability Records
│
├── Vertical Blinds
│     ├── Vogue
│     │     └── Motorised Tilt Operation   [populate this one now]
│     ├── Slimline                          [Future Entries — empty for now]
│     ├── Cruze                             [Future Entries — empty for now]
│     ├── Nova                              [Future Entries — empty for now]
│     ├── Curved                            [Future Entries — empty for now]
│     └── Sloping                           [Future Entries — empty for now]
│
└── Future Entries
      ├── Roller Blinds
      ├── Roman Blinds
      ├── Curtains
      ├── Pleated Blinds
      ├── Perfect Fit Systems
      └── Shutters
```

State explicitly: supplier relationships (which supplier provides
which capability) are metadata attached to each record, not the
organising structure of the document. A future Supplier Mapping
appendix (Decora, Louvolite, Arena, Beverley, Santa Fe, Temposhade, and
others) may cross-reference records by supplier for convenience, but
is not the primary structure and is not required for this first draft.

---

## First Populated Record

Populate exactly one record now: Vertical Blinds → Vogue → Motorised
Tilt Operation. Use the detail below (this is the appropriate document
for this level of supplier-specific detail):

- **Capability:** Motorised Tilt Operation (Vogue Construction
  Variant, Vertical Blinds)
- **Business Rule:** When Control Type = Motorised (Tilt Only) and
  Construction Variant = Vogue, Draw Mechanism = Wand automatically.
  No advisor configuration of draw mechanism is presented for this
  combination. (Matches the resolved "Motorised (Tilt Only) Draw
  Mechanism" Decision Register entry in MCD-01B-02 §23 — identified by
  name here as well as by section number, since section numbers may
  move in later revisions.)
- **Technical Specification:** Motorisation is compatible with the
  Slimline Vogue® headrail system specifically. The motor controls
  louvre tilt only (0°, 45°, 90°, 135°, 180° positions); traversing
  (draw) remains manual via wand. Maximum width for motorised
  operation: 3m. Minimum blind width with open cassette: 200mm.
  Available Vogue headrail colours: white, black, brown, anthracite
  grey, brushed aluminium, champagne gold.
  **Supplier capability vs. Solara restriction — keep these
  distinct:** the underlying supplier system supports both 89mm and
  127mm louvre widths. Solara's Sales MVP exposes 89mm only; this is a
  Solara business restriction governed by MCD-01B-02 (§4), not a
  supplier manufacturing limitation. Do not let a future reader
  interpret the 89mm-only restriction as something the supplier
  itself cannot support.
- **Evidence:** Louvolite Commercial's Vertical Blind Systems webpage
  states that motorisation is compatible with Slimline Vogue® vertical
  blinds specifically, is tilt-only, and that wand operation performs
  the draw. A Louvolite technical brochure ("Slimline Vogue® Vertical
  Blind System — Side Draw with Wand Operation") documents the Vogue
  Channel with Tilt Rod (part 1019) and the One Touch® Vogue motor
  pack (part 1140) as components of the standard Vertical Blind
  system, including performance parameters (rated torque, RPM, motor
  diameter, voltage, power, current, IP rating) and the bunching/
  stacking distance table by louvre width and draw type. Advisor trade
  knowledge (Nazmil Ghany) confirms that motorised tilt was introduced
  for the standard Vertical Blind System on the Vogue headrail before
  Louvolite's separate Allusion® product line was developed roughly
  six years later, adopting the same Vogue headrail and motorisation
  platform — ruling out an alternative reading in which motorisation
  might be exclusive to Allusion® rather than available on standard
  Vertical Blinds.
- **Source References:**
  - Louvolite Commercial, Vertical Blind Systems page
    (louvolitecommercial.com/discover/vertical-blinds) — accessed 14
    July 2026.
  - Louvolite technical brochure
    "2025_LL_SLIMLINE-VOGUE-VERTICAL-BLINDS_SIDE-DRAW-WITH-WAND-CONTROL.pdf"
    — 2025 edition, reviewed 14 July 2026.
  - Advisor trade knowledge — confirmed by Nazmil Ghany on 14 July
    2026.
- **Validation Status:** Confirmed.
- **Revision History:** 14 Jul 2026 — record created, evidence
  gathered and confirmed during MCD-01B-02 Phase 2 review.

---

## Review Requirements

Before committing:
- Confirm the critical scope boundary statement is present and clear.
- Confirm the document is organised by product architecture first,
  not by supplier.
- Confirm only one record is populated (Vogue Motorised Tilt) —
  do not add placeholder content for other capabilities beyond the
  empty Future Entries list.
- Confirm MCD-01A, MCD-01B-01, and MCD-01B-02 are unmodified.
- Add a version history entry (v0.1 Draft Skeleton).
- Commit and push to the new branch.

Do not open a pull request or merge to main — this stays on its own
branch pending review, the same discipline used for MCD-01B-02.
