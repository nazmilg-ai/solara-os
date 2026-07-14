Document ID: MCD-04
Document Title: Product Library & Supplier Management
Status: Draft Skeleton
Version: 0.1
Last Updated: 14 July 2026 (v0.1)

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
└── Future Entries
      ├── Roller Blinds
      ├── Roman Blinds
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

### 7.3 Future Entries (other product families)

Roller Blinds, Roman Blinds, Curtains, Pleated Blinds, Perfect Fit Systems, and Shutters have no populated records yet. These will be added as their own supplier capability evidence is gathered, following the same document architecture established here.

## 8. Decision Register

Maintained in accordance with MCD-00A conventions as established in MCD-01B-01 §17 and MCD-01B-02 §23 (MCD-00A itself was not available in the repository at time of writing — see the row below). Format: Date | Decision | Reasoning | Raised By.

| Date | Decision | Reasoning | Raised By |
|---|---|---|---|
| 14 Jul 2026 | MCD-04 is established as the deliberate exception to Constraint 2 (Product Specification supplier-independence): supplier names, trademarks, brand names, part numbers, model numbers, and source URLs are expected and required in this document, not a violation of Solara's supplier-independence principle. | Product Specifications (MCD-01B-xx) must stay supplier-neutral so quotations/customer-facing behaviour and internal engine logic never leak commercial specifics; that neutrality is only sustainable if the supplier-specific evidence it depends on is recorded somewhere authoritative. MCD-04 is that somewhere. Stated explicitly here, in MCD-04's own Scope (§2), so a future review pass does not mistakenly "clean up" this document the way MCD-01B-02 was cleaned up. | Design brief (claude-code-brief-MCD-04.md) |
| 14 Jul 2026 | Only one record is populated in this first draft (Vertical Blinds → Vogue → Motorised Tilt Operation). All other nodes in §7 and §6 are left as empty Future Entries rather than populated with placeholder or speculative content. | The document architecture should grow from real, evidence-backed records added over time, not be speculatively designed now. An empty node accurately represents "not yet gathered"; a placeholder record would misrepresent it as "gathered but thin." | Design brief (claude-code-brief-MCD-04.md) |
| 14 Jul 2026 (open) | MCD-00A (Project Development Standards) was not present in the repository when this document was drafted. | MCD-04's own Dependencies and Governance sections both require MCD-00A. Governance, versioning, and Decision Register format conventions were instead inherited from their established use in MCD-01B-01 and MCD-01B-02 (which themselves cite MCD-00A for these same conventions), rather than fabricated. If MCD-00A's actual content differs from the inherited conventions once available, this document's §8 format and version-history style may need reconciliation. | Claude Code — flagged for Nazmil Ghany; not a content defect, a missing-dependency note |

## 9. Version History

| Version | Summary |
|---|---|
| 0.1 Draft Skeleton | Initial MCD-04 document architecture established per the design brief (claude-code-brief-MCD-04.md): Purpose, Scope (with the Constraint 2 exception stated explicitly), Relationship to MCD-01A/MCD-01B-xx, Governance, Record Structure (seven fields), and Document Organisation (product-architecture-first tree). Populated exactly one record — Vertical Blinds → Vogue → Motorised Tilt Operation — matching the resolved MCD-01B-02 §23 Decision Register entry, including the confirmed 3m/200mm limits and the supplier-capability-vs-Solara-restriction distinction on louvre width (89mm Solara restriction vs. supplier support for both 89mm and 127mm). All other Construction Variants and product families left as empty Future Entries. MCD-01A, MCD-01B-01, and MCD-01B-02 were not modified. |
| 0.1 Draft Skeleton | Corrected the MCD-01B-02 dependency reference from Draft v1.2 to v1.3 Approved Draft Baseline, reflecting its promotion after this document was first drafted. |
