# Claude Code Brief — MCD-01B-06 Metal Venetian Blinds

## Branch

Create a new branch from current main: claude/mcd-01b-06-metal-venetian

## Read before writing

* MCD-01A_v1.5_for_Claude_Code.md
* MCD-01B-01.md, MCD-01B-02.md, MCD-01B-03.md (governance precedent)
* MCD-01B-04.md (Venetian-family reference implementation — ratified)
* MCD-01B-05.md (Faux Wood Venetian — shows how a second Venetian family member inherited from MCD-01B-04 and documented only genuine differences)
* MCD-04.md

Do not modify any of the above documents. This brief produces one new document only: MCD-01B-06.md, plus additions to MCD-04.md per Part 3 below.

---

## Objective

Create MCD-01B-06.md — Title: "Metal Venetian Blinds Product Specification". Status: Working Draft — Unverified. Version: 1.0 (pre-review). This is a supplier-neutral Product Specification. Supplier names, trademarks, part numbers, model numbers, and URLs must not appear anywhere in this document, including its Decision Register, Open Evidence Items, and Version History — the same standard already enforced in MCD-01B-04 and MCD-01B-05.

## Relationship to the Venetian reference implementation

Metal Venetian Blinds inherit the shared Venetian architecture established in MCD-01B-04 (Recess/Exact measurement, control-side arrangement, bracket allocation, valance/pelmet treatment, stack height, hold-down brackets, bay-window grouping, alignment, child-safety validation, motorisation eligibility model, supplier-capability filtering, internal/customer-facing document rules). Include a "Relationship to the Venetian Reference Implementation" section stating this explicitly, matching MCD-01B-05's own equivalent section. Document only genuine Metal Venetian differences — do not duplicate MCD-01B-04's content wholesale.

---

## Part 1 — Product scope and required classification questions

Metal Venetian Blinds are made-to-measure aluminium Venetian blinds. Real supplier evidence (gathered across two supplier lines) shows genuine slat-size families exist, each with materially different headrail dimensions, bracket systems, dimensional limits, and — critically — a different tilt mechanism:

* **Narrow slat sizes (15/16mm and 25mm)** — tilt operated by wand. Slimmer headrails. Broader colour ranges observed. Larger maximum dimensions on the largest of these sizes (up to 4m x 4m for one supplier's 25mm).
* **Wider slat sizes (35mm and 50mm)** — tilt operated by cords (no wand option observed for these sizes in either supplier's evidence). Deeper/larger headrails. Narrower maximum dimensions (approx. 2.9-4m x 3-3.5m). One supplier's 35mm size cannot be motorised at all under any circumstance (confirmed hard restriction, not merely unconfirmed) — the only size across all evidence gathered where motorisation is definitively ruled out rather than simply not yet evidenced.

This wand-vs-cord split, tied to slat size, is corroborated independently by two unrelated suppliers, not a single supplier's idiosyncrasy — treat this as a genuinely confirmed cross-supplier pattern, not a provisional one.

### Required Classification Question 1 — slat-size groupings as Construction Variants

Apply MCD-01A's three-test model (Construction test → Configuration test → Accessory test) to determine whether the narrow-slat (wand) group and wide-slat (cord) group should be modelled as two separate Construction Variants (analogous to how MCD-01B-03 modelled Standard/No-Drill/Cassette as separate Roman constructions), or as a single construction with slat size as a Configuration-layer selection that determines eligible control mechanism.

Consider: the tilt mechanism itself (wand vs. cord) is not advisor-selectable independent of slat size — it is determined by which slat size is chosen, similar to how Vertical Blinds' Control Mechanism was Configuration-layer but was itself a free advisor choice within one construction. Here, by contrast, the mechanism is *tied to* a physical dimension choice (slat size) that also drives headrail, bracket, and dimensional-limit differences simultaneously. Document your reasoning and conclusion in the Decision Register before finalising §1's scope list and §4's construction rules — do not assume either answer.

### Required Classification Question 2 — specialist constructions

Supplier evidence includes four specialist mechanical constructions and one mutually exclusive colour configuration, found only at one supplier (evidence not yet found for the other):

* **Side Guide Tilt** — for windows that tilt open up to approximately 15° from vertical; all controls fitted on the same side; available only on narrow slat sizes.
* **Side Guide Roof** — for roof/skylight windows; a guide wire holds the slats at an angle up to approximately 45° from vertical; all controls same side; available only on the larger narrow slat size.
* **Partition** — uses a flexible tilt mechanism; can normally only be tilted, not raised or lowered (a genuine functional restriction, not a lesser variant of the standard construction); available on narrow and one wide slat size, not the largest wide size.
* **Double Glazing** — supplied with a tilt/torsion rod and a bowden cable; can be tilted, raised, and lowered; all controls same side; same slat-size availability as Partition.
* **Mixed Colours** — a colour-level option (different colour per slat within one blind); available only on the larger narrow slat size; explicitly incompatible with Side Guide Tilt, Side Guide Roof, Partition, and Double Glazing (mutual exclusivity, not a simple additive combination).

Apply the three-test model to each of Side Guide Tilt, Side Guide Roof, Partition, and Double Glazing individually. These involve genuinely different mechanisms (a guide wire holding the slat angle, a flexible tilt-only mechanism, a torsion rod and bowden cable) — this is the same shape of evidence that made Curved Track a Construction Variant for Vertical Blinds (MCD-01B-02 §3) and Breakaway a Configuration item for Roman (MCD-01B-03, after specific reasoning). Do not assume Construction Variant status merely because the mechanisms differ — apply the actual test and document the reasoning for each of the four separately, since they may not all classify the same way (Partition's "tilt-only, cannot lift" restriction in particular deserves its own scrutiny, as it may be more analogous to Roman's Breakaway — a configuration-layer functional restriction — than to a construction-defining mechanism). Mixed Colours, being a colour-level option with no mechanical difference, is very unlikely to be a Construction Variant — classify it explicitly rather than leaving it unaddressed, but this one is not expected to need extensive reasoning.

---

## Part 2 — Motorisation

Motorisation evidence is asymmetric across the two suppliers evidenced, and this asymmetry must be preserved precisely, not smoothed over:

* **One supplier's wider slat size**: motorisation confirmed available, both Tilt Only and Tilt & Lift, with specific minimum widths for each mode, a hard restriction that taped blinds can only use Tilt Only motorisation, and a hard restriction that one specific narrower wide-slat size cannot be motorised under any circumstance.
* **One supplier's narrower/wand slat size (the larger of the two)**: motorisation confirmed available, one mode only (Tilt & Lift), with specific width/drop limits, battery-powered.
* **The other supplier's entire Metal Venetian range**: motorisation is confirmed to exist at a category level only — their own technical documentation explicitly lists Venetian blinds (alongside Roller, Roman, Pleated) as a supported motorised product category, with Venetian-specific tilt/mid-point behaviour documented. However, no slat-size-specific eligibility, motor model, torque, voltage, or width/drop limit has been found for this supplier's Metal Venetian motorisation, despite a thorough search. This is a genuine intermediate evidence state — it is factually wrong to describe this supplier's motorisation as "not available," and equally wrong to enable any slat size for motorised quoting on this supplier's route without the missing detail.

The Product Specification must represent this precisely, using two separate fields already available within the Supplier Capability model rather than inventing a new Shared Service Status:

```
Evidence Status: Category-Level Availability Confirmed
Quoting Status: Disabled — Slat-Size Capability Not Provided
```

Use this pattern generally: distinguish Evidence Status (what is actually known) from Quoting Status (what the advisor can act on) as two separate fields, rather than collapsing them into one combined label. The full distinction to support:

| Evidence state | Meaning | Quoting |
|---|---|---|
| Available | Complete capability evidence supports the configuration | Enabled |
| Not Available | Supplier explicitly prohibits it | Disabled |
| Not Confirmed | No reliable evidence either way | Disabled |
| Category-Level Confirmed | Supplier confirms the product category supports motorisation, but eligible construction, slat size, and technical limits are missing | Disabled |

Represent the category-level confirmation through these evidence and quoting-status fields already available within the Supplier Capability model. Do not create a new Shared Service Status unless analysis against MCD-01A actually proves the current platform cannot represent evidence confidence separately from quoting eligibility — this is expected to be an evidence-granularity issue, not an architectural gap, but confirm that conclusion through the Part 5 Motor Engine reasoning rather than assuming it here.

The likely conclusion for Motor Engine (to be tested and documented, not assumed) is **Configured**: the engine already supports capability-based eligibility and disabling unsupported or insufficiently evidenced configurations. The unusual element here is the evidence state, not a new type of motor operation.

Do not infer motor model, torque, size limits, or slat-size eligibility for the under-evidenced supplier from the other supplier's fully-evidenced figures, from component-code similarity, or from the general category-level confirmation. Log this explicitly as an Open Evidence Item.

---

## Part 3 — Supplier Capability structure for MCD-04

Update MCD-04.md with the following, using the same evidence-attribution and Structured Technical Value conventions already established (name suppliers, brands, and part numbers freely here — this is the deliberate exception to Product Spec supplier-neutrality):

### 3a. Reseller layer

One supplier's 25mm Metal Venetian offering has been confirmed as a reseller relationship: its specialist-construction rules (wording, surcharges, slat-size restrictions) are identical to the other supplier's own published rules, even referencing slat sizes the reselling supplier does not itself stock — strong evidence the technical content was republished, not independently authored. Its actual prices differ from the original supplier's own table, confirming a genuinely separate commercial layer. Record this using the three-layer model already established for Vertical Blinds' Arena/Beverley relationship: Original Product Owner/Technical Source → Ordering Supplier/Reseller → Commercial Route. Do not duplicate the technical capability record for the reselling supplier's 25mm range — reference the original owner's record and add only the reselling supplier's own commercial fields (pricing, ordering route, lead time).

### 3b. Two sibling collections at one supplier

One supplier has two named collections for Metal Venetian: a standard collection (fully evidenced across two slat-size specifications) and a second, separately-branded collection. The second collection is confirmed to exist as a distinct named system (its own specification document, its own price-list files split by slat size, its own component-code prefix), but:

* The only full specification document found for this second collection describes its Perfect Fit construction specifically — out of scope for this Product Specification.
* Evidence for its standard (free-hanging) variant is limited to price-list fragments and a partial components file (16mm only), which shows a colour palette and control-type vocabulary closely overlapping with the standard collection's own 16mm-available options — complicating rather than confirming that it is a fully separate technical system.
* Internal notes in this supplier's own discount-preparation materials show unresolved uncertainty about which trade-book items some of this second collection's branded line items actually correspond to, across multiple unrelated product categories (not just Metal Venetian) — this is the supplier's own documented confusion, not something to resolve by inference.

Record this second collection in MCD-04 as a provisional identity record only: confirmed to exist as a named system, standard/free-hanging technical capability (dimensions, controls, brackets, child safety, motorisation) marked Not Provided across the board, explicitly not merged into the standard collection's record, and explicitly not populated as if it were a complete separate record. Include the framed supplier question for future use (not to block this task): "Is [collection name] a technically separate free-hanging aluminium Venetian collection, or is the naming a pricing, component-coding, or historic branding distinction? Please provide the current standard specification if it remains active." Do not name the actual collection name from this brief in the framed question if it would violate the Product Spec's own neutrality — this question belongs in MCD-04, where naming is fine.

### 3c. Motorisation capability records

Record the fully-evidenced supplier's motorisation data completely (motor models, torque, voltage, protocol, width/drop limits, per slat size, per operation mode). For the other supplier, create a record explicitly marked with the category-level-only status from Part 2 above, citing the specific source document, and listing exactly what remains missing (slat-size eligibility, motor model, torque, limits) rather than leaving the gap implicit.

### 3d. Provenance

Every technical fact in every new MCD-04 record must cite its specific source document by name. Do not create records with unattributed figures.

---

## Part 4 — Decision Register requirements

MCD-01B-06's Decision Register must include, at minimum:

1. The classification conclusion and reasoning for Required Classification Question 1 (slat-size groupings as Construction Variants or Configuration).
2. The classification conclusion and reasoning for each of Side Guide Tilt, Side Guide Roof, Partition, and Double Glazing individually (Required Classification Question 2), plus Mixed Colours.
3. The Shared Service Profile reasoning (see Part 5 below) for all twelve services — do not accept a provisional all-Configured table without documented reasoning, matching the standard set in MCD-01B-04/05.
4. The motorisation asymmetry — record the distinction between the fully-evidenced supplier route and the category-level-only supplier route explicitly, and state plainly that quoting is blocked for the latter pending further evidence.
5. The second-collection identity ambiguity from Part 3b, logged as unresolved, not merged, not assumed.
6. Confirmation that Perfect Fit constructions (all found across both suppliers) are excluded from this specification.
7. The standing MCD-00A missing-dependency note, consistent with every other document in this project.

All Decision Register entries should be marked pending ratification by Nazmil Ghany where they represent a genuine judgment call (classification questions, motorisation policy), following the same pattern as MCD-01B-04/05.

---

## Part 5 — Shared Service Profile

Do not accept an all-Configured table without reasoning. Apply MCD-01A's actual Extended test (a shared service needs new capability the platform doesn't already have — not "more complex" or "more parameters") to each of the twelve services, with particular attention to:

* **Validation Service** — does validating the wand/cord split, the five specialist constructions' slat-size eligibility, and the mutual-exclusivity rules (e.g. Mixed Colours incompatible with the other four specialist constructions) require new platform capability, or is this parameterisation of existing dimension/compatibility/eligibility rules (compare to how MCD-01B-03 and MCD-01B-05 both concluded Configured for comparably complex validation)?
* **Motor Engine** — does the category-level-only motorisation status for one supplier require new Motor Engine capability, or is "capability confirmed to exist but insufficient detail to enable quoting" simply a data-availability gate the existing Configured pattern already handles (compare to MCD-01B-02's and MCD-01B-05's Motor Engine reasoning for unconfirmed motorisation)?
* **Supplier Capability Engine** — does representing two sibling collections at one supplier, a reseller relationship at another, and a provisional/unresolved identity record require new schema capability, or does the existing Supplier → Range → Material/Construction hierarchy already accommodate it?

Reason through all twelve services and record the conclusions in the Decision Register.

---

## Part 6 — Exclusions

Confirm the document excludes: Wooden Venetian Blinds, Faux Wood Venetian Blinds, Perfect Fit Metal Venetian Blinds (all Perfect Fit / framed no-drill constructions found across both suppliers' evidence), shutters, and any product not evidenced in this research. State that Perfect Fit Metal Venetian is a separate construction-system family per the standing project decision, not a sub-configuration of this product.

---

## Verification

* Confirm zero supplier names, trademarks, part numbers, model numbers, or URLs appear anywhere in MCD-01B-06.md — full sweep, including the Decision Register, Open Evidence Items, and Version History.
* Confirm the reasoning for both Required Classification Questions is written into the Decision Register, not just asserted as a conclusion.
* Confirm the Shared Service Profile reasoning is documented for all twelve services.
* Confirm the motorisation asymmetry is represented accurately — the category-level-only supplier's motorisation must not read as "unavailable," and no slat size for that supplier may be enabled for quoting.
* Confirm the second-collection identity record in MCD-04 is provisional only — not merged into the standard collection, not fully populated as if resolved.
* Confirm the reseller layer (Part 3a) does not duplicate technical capability.
* Confirm every new MCD-04 fact cites a specific source document.
* Confirm MCD-01A, MCD-01B-01 through MCD-01B-05 remain unmodified.
* Add a Version History entry naming all open items by content (motorisation granularity gap, second-collection identity, specialist-construction classification pending ratification, standing MCD-00A note).
* Commit and push to the new branch. Do not open a pull request or merge.
