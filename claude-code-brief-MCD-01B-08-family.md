# Claude Code Brief — MCD-01B-08 Frame-Mounted and Window-Mounted Blind Systems (Family Architecture)

## Branch

Create a new branch from current main: claude/mcd-01b-08-family-architecture

## Read before writing

* MCD-01A_v1.5_for_Claude_Code.md
* MCD-01B-01.md through MCD-01B-07.md (governance precedent — especially how MCD-01B-04 established itself as the Venetian family's reference implementation, and how MCD-01B-05/06 each referenced it rather than duplicating it)
* MCD-04.md

Do not modify any of the above documents. This brief produces one new document only: MCD-01B-08.md. It does not create any variant specification (those are separate, later briefs) and does not populate any specific supplier capability record in MCD-04 (those are populated when each variant is drafted, not now).

---

## Scope of this document — read carefully before drafting

MCD-01B-08 is a **family architecture document**, not a full product specification. It defines only what is genuinely shared across every frame-mounted and window-mounted blind system, regardless of which blind technology (Roller, Pleated, Cellular, Aluminium Venetian, Wooden Venetian, Softshade, Pleated Night & Day) is inserted into it. It does NOT contain:

* Blind-Technology-specific rules (these belong in separate variant specifications — MCD-01B-08A onwards — to be drafted later, each referencing this document and its own underlying base specification, e.g. a future Frame-Mounted Wooden Venetian spec would reference both this document and MCD-01B-04).
* Populated supplier capability records (Arena's specific products, Decora's specific systems, Beverley's specific routes) — these are populated in MCD-04 when each variant is actually drafted, not pre-loaded here. This document defines the organisational-role *schema* those records will use, not the records themselves.

This mirrors exactly how MCD-01B-04 (Wooden Venetian) became the Venetian family's reference implementation before Faux Wood and Metal Venetian were drafted, each referencing it rather than duplicating its content — apply the same discipline here, one level up (family architecture, then variants).

---

## Document Status

Status: Working Draft — Unverified (matching every other pre-review document in this project — this must NOT be created as "Approved Draft Baseline." Promotion only happens after independent review, resolution of findings, explicit ratification of every Decision Register judgment by Nazmil Ghany, a promotion commit, and merge verification on main — the same sequence used for all seven prior product specifications.)
Document type: Family Architecture Document
Architecture: Must comply with MCD-01A
Supplier neutrality: Required — applies to the Decision Register, Open Evidence Items, and Version History as strictly as it applies to operative sections. This has recurred as a real problem multiple times in this project (Roman's Decision Register; MCD-01B-05's §41/§49) and must not recur here. Even where this brief's own supporting notes below reference real evidence, transcribe them into MCD-01B-08.md using neutral language only — see the Supplier-Neutrality Boundary section below.
No assumptions rule: unsupported combinations must be blocked rather than inferred. Where evidence is missing, use "Not Provided" or "Supplier Confirmation Required" — do not convert missing evidence into a restriction unless a source specifically states the option is unavailable.

---

## 1. Scope Statement

This document governs blind systems that mount directly to an individual window or door sash through either:

1. a complete surrounding frame secured through glazing-bead brackets; or
2. top and bottom profiles with independent side guides secured to the window through brackets or adhesive.

The system normally moves with the opening window or door sash. This document governs the mounting-system architecture and its interaction with the inserted blind technology. It does not replace the underlying technical specification for Roller, Pleated, Cellular, Aluminium Venetian, or Wooden Venetian products (MCD-01B-01 through MCD-01B-07) — it adds only the rules caused by the frame-mounted/window-mounted construction itself.

## 2. Required Classification Question — apply MCD-01A's three-test model, do not accept as pre-decided

Two mounting-system groups are proposed based on real evidence of materially different physical architecture:

* A system contained within a complete surrounding frame that attaches to the glazing area through compatible glazing-bead brackets (four-sided frame, no wall or recess fixing for the main frame, blind and frame move with the opening sash).
* A system using reinforced top and bottom profiles with independent side guides rather than a complete four-sided surrounding frame (tensioned operation, guided by side rails, beading-bracket or adhesive installation).

Apply the Construction test → Configuration test → Accessory test (MCD-01A §3/§4) to confirm these genuinely warrant two separate Construction Groups rather than one construction with mounting method as a Configuration-layer selection. Real evidence supports a materially different physical fixing and guiding architecture between the two (complete perimeter frame vs. top/bottom profile with side guides) — but document the actual reasoning in the Decision Register rather than restating this evidence as a conclusion. If confirmed, use neutral names only:

* **Full-Frame Bead-Mounted System**
* **Side-Guide Window-Mounted System**

Do not use any supplier trademark, product name, or system name as the neutral classification title.

## 3. Blind Technology — a separate axis, not a Construction Group

The inserted blind technology (Roller, Softshade, Pleated, Cellular, Pleated Night & Day, Aluminium Venetian, Wooden Venetian) is not itself a Construction Group under this document — it is a separate controlled axis that activates the applicable rules from the existing MCD-01B-01 through MCD-01B-07 specifications. Document this relationship structurally (e.g. "Blind Technology: Roller → references MCD-01B-01") without drafting the Blind-Technology-specific rules themselves here — those belong in each variant specification.

## 4. Exclusions

Explicitly exclude from this family and all its future variants: INTU; Micro INTU; roof-window systems; skylight systems; lantern-roof systems; shaped roof blinds; gable systems; specialist angled roof/side-window systems (a separate specialist product line, out of scope here — consistent with the standing project decision that Perfect Fit-equivalent specialist roof systems sit outside standard product families); ordinary free-hanging blinds; ordinary tensioned blinds outside this family; total-blackout cassette systems; any shutter-lite or shutter product (belongs under a future Shutters specification); standard recess-mounted or face-fixed Roller, Venetian, or Pleated blinds (already covered by their own existing specifications).

## 5. Supplier-Neutrality Boundary — read carefully

This document must describe mounting architecture using neutral language only. Do not use supplier trademarks, product names, system names, or product codes anywhere in MCD-01B-08.md, including the Decision Register, Open Evidence Items, and Version History. Use descriptions such as:

* "a complete perimeter frame secured through glazing-bead fixings" (not any specific trademarked system name)
* "top and bottom profiles with independent side guides" (not any specific trademarked system name)
* "a tensioned handle-operated Venetian insert" / "a chain-operated Roller insert" (describing function, not naming a supplier's product)

All exact supplier terminology, trademarks, product codes, and named organisations belong exclusively in MCD-04, populated when each variant specification is drafted — not in this document, and not yet, since no variant is being drafted in this task.

## 6. Organisational Role Schema (for MCD-04 — define the schema here, do not populate records)

Real evidence shows the supplier relationships in this product family are more complex than any prior product in this project — a single named organisation can hold multiple distinct roles simultaneously (e.g. one organisation may be both an ordering supplier and a reseller of a different organisation's finished product; another may be a system inventor/patent holder without being an active finished-goods supplier at all). Define, as a schema only (not populated with real organisation names in this task), the following distinct roles MCD-04 must be able to represent for this family:

* System Owner
* Patent Holder
* Component Manufacturer
* Licence Holder
* Finished-Blind Manufacturer
* Ordering Supplier
* Reseller
* Fabric Supplier
* Commercial Route
* Technical Source

State explicitly in this document that a single organisation may hold several of these roles simultaneously, or none at all for a given product route (e.g. a system inventor that licenses its technology to manufacturers without itself supplying finished goods to Solara). This schema will be populated with real organisation names and evidence when each variant specification is drafted.

### Required Classification Question — does this richer role model require Supplier Capability Engine to be Extended?

The Supplier Capability Engine has, in every prior product in this project, been concluded Configured — richer records were still parameterisation of an existing Supplier → Range → Construction hierarchy. This family's evidence includes a ten-role organisational model, genuinely richer than anything modelled before (the prior richest case, Vertical/Metal Venetian's reseller relationships, used three roles: Original Owner, Ordering Supplier, Commercial Route). Test this specifically and document your reasoning — do not assume Configured by precedent alone, and do not assume Extended merely because the model is richer (MCD-01A §2 explicitly excludes "more complex" or "more parameters" from the Extended test). The real question is whether representing multiple simultaneous roles per organisation, and roles with no active finished-goods route at all, requires new platform capability the existing hierarchy cannot express, or whether it is a deeper but still-ordinary use of the same Supplier → Range → Construction structure.

## 7. Shared Survey and Measurement Fields

Define, at the family level only (not tied to any specific blind technology), the survey and measurement fields common to all frame-mounted and window-mounted systems:

* Measurement basis (e.g. glass size vs. supplier-specific product size — do not enable recess or exact measurement automatically unless a future variant's supplier system explicitly uses them).
* Handle clearance (window-handle position, vent position, clearance to glass, obstruction conflict).
* Bead and bracket survey (bead type/profile, bead depth, rubber bead protrusion, bracket compatibility, frame obstruction, handle obstruction, seal condition, window material, opening type).
* Frame group and frame colour (as Configuration-layer fields, supplier-capability controlled — do not create one universal colour list; colour and frame-group availability will always be filtered by the exact variant/supplier product once populated).
* Fixing method (Glazing-Bead Bracket / Beading-Bracket Side Guide / Adhesive Side Guide — supplier-capability controlled).

## 8. Validation Principles (family level)

Document the following as family-wide validation principles, without populating specific numeric limits (those belong to each variant's supplier capability records):

* A product can only be quoted when Construction Group, exact supplier system, size, area, frame group, frame colour, bracket/fixing method, operation, fabric/slat compatibility, control, and window compatibility all match a confirmed supplier capability record.
* No cross-supplier inheritance: sizes, bracket depths, component capability, frame colours, motorisation, and fabric limits must never be inherited from one supplier's evidence into another supplier's or another product's record.
* Pricing-grid values (first/last entries in a price table) are not automatically technical limits — store "Minimum/Maximum Priced Band" separately from "Technical Minimum/Maximum," and only populate the technical fields where a specification explicitly confirms them.
* Where a supplier states that a dimensional limit depends on fabric thickness or fabric choice, require fabric selection before final validation and apply the fabric-specific limit where available; otherwise mark "Supplier Confirmation Required" rather than allowing the advisor to assume a table maximum.

## 9. Motorisation Principle (family level)

Do not enable motorisation globally across this family. Real evidence indicates that at least one system-owning organisation has a named manufacturing system with motorisation capability at the technology-platform level, without a confirmed active made-to-measure finished-blind quoting route through any current supplier. Record the general principle: a manufacturing-system-level motor capability existing at the system-owner level does not by itself establish an active quoting route — quoting must remain blocked until a specific supplier's specific product is confirmed to support motorisation. The specific system name and evidence belong in MCD-04 when the relevant variant is drafted, not in this document.

## 10. Child Safety (family level)

Apply the existing Child Safety Shared Service. State the family-level principle: do not assume every framed or window-mounted system is automatically Safe by Design — classification depends on the exact control mechanism of the inserted blind technology (handle-operated tensioned systems may be Safe by Design where evidence confirms this; chain-operated systems require the appropriate safety device; wand and cord systems require applicable controls). The specific classification per blind technology and supplier product happens in each variant specification.

## 11. Customer-Document and Audit Rules

Apply the existing project-wide rules: customer documents show product description, fabric/slat and colour, frame colour, operation, total price, lead time, and warranty where applicable; they must not show internal component codes, supplier costs, reseller relationships, manufacturing deductions, bracket calculations, measurements, technical evidence statuses, or internal capability notes. The audit record must preserve ordering supplier, finished-blind manufacturer, system owner, exact supplier system/product, Construction Group, Blind Technology, fabric/slat details, frame details, bracket/fixing selection, operation, control side, applied limits, source document/version, advisor overrides, supplier-confirmation items, and pricing/reseller route where applicable.

## 12. Shared Service Profile — required reasoning, not a checklist

Do not accept a pre-decided all-Configured table. Apply MCD-01A §7's actual Extended test to each of the twelve services independently, with particular scrutiny required for: **Supplier Capability Engine** (see the Required Classification Question in §6 above); **Validation Engine** (does the multi-axis eligibility model — Construction Group × Blind Technology × exact supplier product × dimensions × frame/colour × fixing method — require new capability, or is it parameterisation, consistent with every prior product's Configured conclusion for comparably complex conditional validation?); **Measurement Engine**; **Survey Engine**; **Pricing Engine**; **Operation Engine**; **Motor Engine**; **Audit & Compliance Engine**. Do not skip the remaining four services — reason through all twelve and record the conclusions in the Decision Register.

## 13. Evidence Discipline

Any fact in this brief without a clearly identified source document, or an expressly labelled operational-knowledge source, must not be transcribed into MCD-01B-08.md as confirmed — mark it "Supplier Confirmation Required" or "Not Provided." This document should contain almost no supplier-specific facts at all, since it is family architecture only — but where any evidence-based statement is unavoidable (e.g. describing that a role-model complexity exists), do not name the source in MCD-01B-08.md itself; if a source needs naming for MCD-04 schema-design purposes, name it only in MCD-04.

## 14. Decision Register, Version History, and Open Evidence Items

MCD-01B-08.md must include a numbered Decision Register (Date | Decision | Reasoning | Raised By), a Version History section (v0.1, recorded as the initial Working Draft — Unverified), and an Open Evidence Items section, matching the format used in every prior document in this project. At minimum, log in the Decision Register:

1. The Required Classification Question conclusion (§2) — two Construction Groups or one with Configuration-layer mounting method.
2. The Supplier Capability Engine Required Classification Question conclusion (§6).
3. The Shared Service Profile reasoning for all twelve services (§12).
4. Confirmation that Blind Technology is a separate axis, not a Construction Group, and why.
5. Confirmation of the exclusions (§4).
6. The standing MCD-00A missing-dependency note, consistent with every other document in this project.

Mark entries representing genuine judgment calls as pending ratification by Nazmil Ghany, matching the pattern used for every prior product.

Open Evidence Items should note, at minimum, that populated supplier capability records for every organisation and product in this family remain entirely undone — they are deliberately deferred to each variant specification's own drafting process, not a gap in this document.

## Verification

* Confirm zero supplier names, trademarks, product names, part numbers, or system names appear anywhere in MCD-01B-08.md — full sweep, including the Decision Register, Open Evidence Items, and Version History.
* Confirm this document contains no Blind-Technology-specific rules and no populated supplier capability records — only shared family architecture and the organisational-role schema.
* Confirm the two Required Classification Questions (§2, §6) are reasoned in the Decision Register with actual three-test/Extended-test analysis shown, not asserted.
* Confirm the Shared Service Profile reasoning is documented for all twelve services.
* Confirm MCD-01A and MCD-01B-01 through MCD-01B-07 remain unmodified.
* Confirm the document's Status line reads "Working Draft — Unverified," not "Approved Draft Baseline."
* Report: branch name; files created; summary of the architecture implemented; the two Construction Group names (or the corrected structure if the classification question concludes differently); Shared Service Profile with reasoning; Decision Register entries; Open Evidence Items; any conflict with frozen architecture; any place the brief could not be implemented without assumption; confirmation that no merge was performed.
* Commit and push to the new branch. Do not open a pull request or merge.
