# Claude Code Brief — MCD-01B-03 Roman Blinds Product Specification

## Branch

Create a new branch from current `main`:

```text
claude/mcd-01b-03-roman-blinds
```

## Read before writing

Read these documents in full:

* `MCD-01A_v1.5_for_Claude_Code.md`
* `MCD-01B-01.md`
* `MCD-01B-02.md`
* `MCD-04.md`

Use MCD-01B-01 and MCD-01B-02 as structural and governance precedents.
Pay particular attention to how MCD-01B-02 applied the Construction /
Configuration / Accessory three-test model (its §3, on Curved Track vs.
Configuration) and how it resolved the Restricted-granularity question
(its §23 Decision Register, Questions A and B) — this brief asks you
to apply that same standard of documented reasoning to Roman Blinds,
not to carry over Roller's or Vertical's conclusions by default.

Do not modify any existing MCD document.

---

## Objective

Create `MCD-01B-03.md` — Title: "MCD-01B-03 — Roman Blinds Product
Specification". Initial status: Draft – Product Specification.
Initial version: v1.0.

This must be a supplier-independent Product Specification governed by
MCD-01A. Supplier names, trademarks, part numbers, supplier URLs, and
supplier-specific motor models must not appear anywhere in this
document — including its Decision Register, Open Evidence Items, and
Version History. This applies to meta-sections as strictly as it does
to operative rules; a sentence that names a supplier while stating the
supplier-independence rule is itself a violation of that rule. Where
this brief's own supporting notes below reference supplier evidence
generically, use category-level language only ("primary supplier
evidence," "secondary supplier evidence," "supplier technical
documentation") — never name the supplier.

Supplier-specific evidence and capabilities belong in MCD-04.

**All required architectural assessments (§2's Configured-vs-Extended
reasoning, §4a's construction classification, and §7a's Same Room
ownership question) must be recorded inside `MCD-01B-03.md` itself —
principally in the Decision Register, and reflected in whatever
operative section each conclusion affects. A conversational
explanation in your chat response does not satisfy this requirement.
If your response says "I assessed this as Configured" or similar, the
document must independently show the same reasoning and conclusion,
not just the resulting classification.**

---

# 1. Product Scope

Roman Blinds are a Standard Blinds product family within the MCD-01A
product architecture.

The Product Specification must support:

* Manual Roman Blinds
* Motorised Roman Blinds
* Standard concealed-headrail construction
* Breakaway-headrail construction
* No-drill construction
* Cassette construction
* Cascade style
* Stacked style
* Fabric and colourway selection
* Lining selection
* Stitch-method selection
* Pattern matching
* Same Room grouping
* Fabric-join warnings
* Recess and Exact measurement
* Child-safety configuration
* Construction-specific dimensional and clearance validation
* Supplier Capability-driven manufacturing and motor selection

Do not create supplier-named products or construction variants. Use
neutral construction names such as: Standard Headrail, Breakaway
Headrail, No-Drill Headrail, Cassette Headrail — but see §4a below;
these four names are a starting point for analysis, not a pre-approved
list of four independent constructions.

---

# 2. Shared Service Profile — provisional, subject to your own assessment

The table below is a **starting point for analysis, not an approved
classification**. Two rows in particular — Validation Engine and
Recommendation Engine, both marked Extended — must not be accepted as
given. Apply MCD-01A's actual test for Extended: *"implementing this
product requires a change to the shared platform service itself."*
Being more complex than Roller's or Vertical's use of a service, or
requiring more parameters, does not meet that test — Configured means
using existing capabilities via selection and parameterisation, however
elaborate; Extended means the shared service itself would need new
capability it doesn't already have.

Before finalising this table, write out your reasoning for Validation
Engine and Recommendation Engine specifically: does area validation
(Width × Drop against a threshold), fabric-join width checking, and
construction-eligibility validation require the Validation Engine
itself to gain new capability, or are these ordinary parameterised uses
of dimension/compatibility rules the engine already provides (compare
to how MCD-01B-02 handled Vertical's stack-width and chain-length
rules at Configured)? Does Roman's Recommendation Engine content
(room suitability, join warnings, fabric/motor suggestions) require new
recommendation-engine capability, or is it the same advisor-overridable
suggestion pattern Roller and Vertical both used at Configured? Report
your conclusion and reasoning in the Decision Register before treating
either row as final — do not silently implement the provisional table.

| Shared Platform Service    | Provisional Status | Roman-specific application (subject to your review) |
| --------------------------- | ------------------- | ----------------------------------------------------------------------------------------------------- |
| Survey Engine               | Configured          | Recess/Exact, obstructions, clearance, installation height, no-drill eligibility, motor battery access |
| Measurement Engine          | Configured          | Width, drop, recess/exact, three-point measuring guidance                                              |
| Validation Engine           | **Reassess**        | Dimensions, area, fabric joins, system clearance, construction eligibility, motor compatibility        |
| Operation Engine            | Configured          | Manual or Motorised; construction determines operation availability                                    |
| Motor Engine                | Configured          | Supplier Capability selects compatible motor according to construction, dimensions and load            |
| Child Safety Engine         | Configured          | P-clip, breakaway control and rear-cord safety mappings                                                |
| Pricing Engine              | Configured          | Fabric band, lining uplift, construction uplift, motorisation and accessories                          |
| Accessory Engine            | Configured          | Brackets, cassette finish, controls, chargers, remotes and related accessories                         |
| Supplier Capability Engine  | Configured          | Construction, dimensions, motor, fabric, lining and manufacturing limits                                |
| Recommendation Engine       | **Reassess**        | Fabric joins, room suitability, blackout expectations, wide-width recommendations                      |
| Document Generation Engine  | Configured          | Customer-facing warnings and supplier-order instructions                                               |
| Audit & Compliance Engine   | Configured          | Join acknowledgement, child safety, Same Room grouping and exceptions                                  |

Do not classify an entire service as Restricted merely because one
supplier or construction excludes an option (see MCD-01B-02 §23
Question A for the precedent on why a single excluded value doesn't
warrant a whole-service Restricted classification).

---

# 3. Core Configuration Fields

The Product Builder must include:

1. Room
2. Window/item reference
3. Measurement type: Recess or Exact
4. Width
5. Drop
6. Construction (see §4a for the required classification analysis
   before finalising this list)
7. Roman style: Cascade (default) or Stacked
8. Fabric collection
9. Fabric range
10. Colourway
11. Fabric property
12. Lining
13. Stitch method
14. Operation: Manual or Motorised
15. Control side, where applicable: Right (default) or Left
16. Chain/control finish, where applicable
17. Installation height
18. Same Room Option (see §7a for the required ownership analysis)
19. Same Room Group
20. Pattern matching
21. Bracket/fitting type
22. Cassette finish, when applicable
23. Advisor/customer acknowledgement where fabric joins are required

The interface must remain advisor-first and must not ask irrelevant
questions.

---

# 4. Construction Rules

The four constructions below (Standard, Breakaway, No-Drill, Cassette)
are a starting point. Before finalising them as independent
Construction Variants, complete the analysis required in §4a.

## 4.1 Standard Headrail

Supports: Manual; Motorised, subject to Supplier Capability; Cascade
or Stacked; Recess or Exact; Top fix or face fix. Motorised Standard
Headrail has one compatible motor family per supplier construction —
the advisor does not choose between unrelated motor models.

## 4.2 Breakaway Headrail

Supports: Manual operation only unless a future supplier capability
explicitly confirms motorisation; Breakaway control mechanism;
Cascade or Stacked; Recess or Exact.

## 4.3 No-Drill Headrail

Supports: Recess measurement only; Manual operation unless separately
confirmed; Firm-backed recess surfaces only; Maximum finished-weight
validation; Construction-specific minimum recess depth and clearance;
Manufacturer deductions applied from recess measurements. No-Drill
must be blocked for: hollow plasterboard; surfaces without firm
structural backing; unsuitable recess geometry; weights or dimensions
exceeding Supplier Capability.

## 4.4 Cassette Headrail

Supports: Manual; Motorised; Covered or uncovered cassette where
supported; Cascade or Stacked; Recess or Exact; Top fix or face fix.
Cassette dimensions and front-clearance requirements are validated
through Supplier Capability.

## 4a. Required construction classification analysis

For each of the four candidate constructions above, apply MCD-01A's
three-test model (Construction test → Configuration test → Accessory
test, in order — see MCD-01A §3, and MCD-01B-02 §3's worked example on
Curved Track vs. Configuration for the documentation standard
expected) and record your reasoning in the Decision Register before
finalising §4 and §1's construction list.

**Breakaway Headrail is the one most likely to fail the Construction
test.** Specifically assess whether it is genuinely a separate
Construction System, or whether it is more accurately: **Standard
Headrail + a breakaway safety/control configuration** — i.e. the same
underlying headrail construction as §4.1, with a breakaway safety
mechanism as a Configuration-layer or Accessory-layer selection, not a
different manufacturing route. If your analysis concludes Breakaway is
a configuration of Standard rather than an independent construction,
restructure §1, §3, and §4 accordingly rather than leaving the
provisional four-construction list in place.

No-Drill and Cassette are more likely to pass the Construction test,
since they plausibly change mounting method, physical assembly,
eligibility, and validation in ways that meet MCD-01A's test — but
this must still be reasoned through and documented, not assumed by
analogy to how obviously they differ from Standard.

---

# 5. Fabric and Lining Model

Fabric property and lining are separate fields. Fabric properties may
include: Sheer, Dimout, Blockout face fabric, Standard furnishing
fabric. Lining options may include, according to Supplier Capability:
Unlined, Standard lining, Premier lining, Satin lining, Blockout
lining, Bonded lining, Bonded blockout lining, Interlining. Do not
treat a blockout face fabric and blockout lining as the same
selection. The system must filter lining and stitch options according
to the selected fabric and supplier capability.

---

# 6. Fabric Join Rule

Each fabric record must include: usable fabric width; maximum blind
width without joins; whether joined manufacture is permitted; maximum
joined width; join arrangement where known.

As soon as the selected blind width exceeds the selected fabric's
usable no-join width, display:

```text
Fabric joins required
This Roman Blind exceeds the selected fabric's usable width and will be manufactured with visible vertical joins. Please explain this to the customer before proceeding.
```

The advisor must record: "Customer informed that visible fabric joins
will be present." The warning must occur during configuration, before
quotation acceptance, and before supplier-order submission if not
already acknowledged. Where possible, the Recommendation Engine may
suggest a wide-width fabric that avoids joins — it must advise, not
force.

---

# 7. Same Room Option

The Same Room Option links separate Roman Blind items. When enabled,
the advisor must either add the item to an existing Same Room Group or
create a new one. All grouped items must use the same fabric, the same
colourway, compatible construction, compatible lining and stitch
method where required, and the same supplier pattern-matching
instruction. The system must warn or block grouping where fabric or
colourway differs.

Supplier order instruction: "Pattern-match all Roman Blind items in
the same Same Room Group using the same fabric and colourway.
Coordinate the pattern consistently across the grouped items, subject
to supplier manufacturing tolerances."

Same Room Option is distinct from pattern matching within a single
blind. Retain supplier-specific tolerances, such as permitted drop
variation for fold alignment, in MCD-04.

## 7a. Required architectural ownership question — do not implement silently

Same Room Option does not obviously belong to any single one of
MCD-01A's twelve Shared Platform Services. It is a cross-item grouping
concept — it links separate configured items together — which is
different in kind from the per-item Construction / Configuration /
Accessory classification the three-test model was designed for.

Before implementing this feature, assess and report in the Decision
Register:

1. Does an existing Shared Platform Service plausibly own cross-item
   grouping (e.g. is this a Survey Engine responsibility, a Document
   Generation Engine concern, or something else)? If so, which, and
   why?
2. Or does this expose something MCD-01A's twelve services don't
   currently have a home for — a genuine architectural gap, in the
   same spirit as the Restricted-granularity question logged in
   MCD-01B-02 §23 Question B?
3. If it's a gap: do not propose an MCD-01A amendment. Log this as an
   evidence-tracking item the same way Question B was logged — a
   candidate for future clarification if the same need recurs in
   other product families (Roller/Vertical items don't currently
   need cross-item grouping, but Curtains or Shutters might).

Implement Same Room Option in MCD-01B-03 regardless of the answer —
describe it as required Roman product behaviour independent of the
ownership conclusion. Do not assign it to a specific Shared Platform
Service in §2's profile unless your assessment actually supports that
conclusion. Where ownership remains unresolved, record it as cross-item
product behaviour in the operative sections and log the architectural
gap in the Decision Register — do not leave it implicitly attributed
to whichever service happens to be nearest in the document (e.g.
Audit & Compliance Engine, per the provisional §2 table) without that
attribution being the actual conclusion of your analysis.

---

# 8. Pattern Matching

Where pattern matching is selected: patterns should be aligned
consistently at the top of grouped blinds; pattern centralisation
should be requested where supported; additional material and pricing
may apply; exact pattern alignment remains subject to supplier
tolerance; side seams across separate blinds may not align unless
expressly confirmed.

---

# 9. Measurement Rules

Roman Blinds support Recess and Exact. For Recess: advisor records the
recess size; supplier/manufacturing deductions are applied through
Supplier Capability; the Product Specification does not hard-code one
universal deduction. For Exact: advisor records required finished
blind size.

Survey guidance must retain: measure width at top, middle and bottom;
record the smallest relevant recess width; measure drop at left,
centre and right; record the smallest relevant recess drop; identify
handles, tiles, radiators, sills and other obstructions; verify front
clearance against selected construction.

Outside-recess recommendation guidance may include: lateral overlap;
top overlap; bottom termination around sills and radiators.
Supplier-specific overlap figures belong in MCD-04 or survey guidance
records.

---

# 10. Dimensional and Area Validation

Validation must check independently: minimum width; maximum width;
minimum drop; maximum drop; maximum total area; maximum finished
weight; fabric no-join width; construction clearance; operation
limits; motor minimum width; supplier live-ordering limits.

The system must not assume the first price-table cell is the minimum
manufacturable size. Price tables may begin at a larger chargeable
bracket than the technical minimum.

Where a supplier documents a maximum-area rule, calculate: Area =
Width × Drop. A blind can fail area validation even when width and
drop pass separately. Maximum-area values belong to Supplier
Capability records, not a universal Roman rule unless later adopted as
a Solara-wide business policy.

---

# 11. Motorisation

## 11.1 General rule

Motorisation is construction-dependent. The advisor selects: Manual or
Motorised; compatible construction; control requirements. The
Supplier Capability Engine determines: compatible motor family;
minimum motor width; maximum dimensions; power arrangement; suitable
control accessories; load suitability. Supplier-specific motor names
must not appear in MCD-01B-03.

## 11.2 Standard Headrail

For a motorised Standard Headrail: one compatible motor family is
automatically assigned; no advisor motor-model choice is presented; if
the configuration exceeds the motorised construction limit, block or
refer.

## 11.3 Cassette Headrail

Cassette motorisation may have lower-capacity and higher-capacity
motors. **Do not encode a specific dimensional threshold (e.g. a
width or drop figure in mm) as an operative rule.** An earlier draft
of this brief included a provisional 1500mm boundary; that figure came
from advisor risk-management judgement, not supplier evidence, and has
been removed rather than merely labelled provisional — encoding it as
an operative threshold would violate §11.4's own rule against
inventing thresholds where evidence is missing, and it is not settled
whether Solara business policy may substitute for missing technical
evidence in a supplier-neutral Product Specification (this is itself
an open governance question pending MCD-00A).

Instead, where motor-capacity selection between lower- and
higher-capacity options cannot yet be determined from Supplier
Capability data, the system must defer entirely:

```text
Motor selection subject to Supplier Capability confirmation.
```

Log the removed 1500mm figure in the Decision Register as a candidate
future Solara Business Rule, contingent on MCD-00A settling whether
business policy may govern motor selection ahead of complete supplier
load-chart evidence. Do not implement it as a rule in this draft.

The system must never downgrade a configuration already confirmed to
require a higher-capacity motor once evidence establishes that
requirement.

## 11.4 Load model

The architecture must support future calculated-load validation using:
estimated lifted load = face fabric weight + lining weight +
interlining or bonded-layer weight + rods + bottom bar + cord and
pocket allowance + joined-panel allowance.

Do not invent fabric weights or motor-load thresholds. Where evidence
is missing, use: "Motor selection subject to Supplier Capability
confirmation."

---

# 12. Child Safety

Manual looped-chain systems must support: installation height;
chain-length calculation; P-clip or equivalent safety device;
breakaway control where configured; rear lift-cord breakaway clips.
The exact chain formula and safety device mapping must come from
Supplier Capability and the Child Safety Engine. Motorised operation
removes the manual chain question. Breakaway Headrail must not also
display incompatible fixed-loop safety questions (subject to §4a's
analysis — if Breakaway is reclassified as a configuration of
Standard, restate this rule accordingly).

---

# 13. Installation and Survey Guidance

Retain the following as structured survey guidance for later
placement: construction-specific front clearance; window and door
handle clearance; battery-pack access; charging access; firm substrate
requirement for No-Drill; brackets positioned away from obstructions;
additional brackets evenly spaced; top-fix or face-fix suitability;
cassette removal access; customer expectations around creasing,
steaming and dressing; rear-cord clip inspection where a blind raises
unevenly.

Do not decide yet whether every guidance item appears directly in the
sales workflow, Survey Engine, Solara Academy, or installation
instructions. Log this as a Decision Register item.

---

# 14. Advisor Recommendations

The Recommendation Engine should support: Roman blinds in kitchens may
absorb odours, grease and moisture; blackout lining does not create a
total-blackout system because edge light remains; street-facing
windows may lose daytime privacy when the blind is raised; large
patterned fabrics may require joins; wide-width fabrics may avoid
joins; Same Room grouping should be used where coordinated pattern
placement is required; heavy fabric and lining combinations may
require stronger motor capability; cassette construction requires
greater front clearance than a standard headrail.

Recommendations advise rather than block unless the configuration is
technically invalid.

---

# 15. Pricing Inputs

Roman pricing may depend on: fabric price band; width/drop price cell;
minimum chargeable bracket; lining uplift; stitch-method uplift;
construction uplift; cassette uplift; breakaway mechanism;
motorisation; remote and control accessories; charger or power pack;
pattern matching; joined manufacture; supplier delivery or service
charges. Supplier prices and named pricing bands belong in MCD-04 or
the Pricing Engine's supplier records. MCD-01B-03 defines only the
inputs and behaviour.

---

# 16. Customer Documents

Customer quotes and invoices must not show: measurements; supplier
names; motor model numbers; internal fabric-width calculations;
internal motor-load calculations; supplier cost breakdown.
Customer-facing documents may include: room; Roman Blind description;
fabric and colourway; lining; style; manual or motorised operation;
cassette or no-drill description where relevant; visible fabric-join
disclosure; Same Room pattern-matching note; total price.

---

# 17. Advisor Workflow

Recommended sequence: Room and item reference; Measurement type; Width
and drop; Construction; Fabric and colourway; Lining; Stitch method;
Roman style; Fabric-join validation; Same Room Option; Manual or
Motorised; Conditional control questions; Installation height;
Bracket/fitting choice; Construction-clearance validation; Motor
compatibility; Customer warnings and acknowledgements; Price;
Duplicate/add another item.

Conditional questions must disappear where not applicable.

---

# 18. Supplier Capability Dependencies

Reference MCD-04 for: supplier construction names; fabric widths;
fabric weights; pattern repeats; maximum no-join widths; lining
compatibility; stitch compatibility; dimensions; area limits; weight
limits; manufacturing deductions; motor models; torque; motor load
limits; remotes; chargers; cassette finishes; chain colours; lead
times; portal restrictions; live supplier-ordering behaviour.

---

# 19. Decision Register

Include entries for (using generic evidence-category language only —
no supplier names, per this brief's Objective section):

1. Roman construction systems remain supplier-neutral in MCD-01B-03.
2. Fabric property and lining are separate configuration fields.
3. Fabric joins trigger an immediate advisor warning and customer
   acknowledgement.
4. Same Room Option groups separate blind items for coordinated
   pattern matching.
5. Standard motorised headrail uses one automatically assigned
   compatible motor family.
6. Cassette motorisation supports lower- and higher-capacity motor
   capability; specific dimensional thresholds are not encoded pending
   supplier load-chart evidence (see §11.3).
7. The 1500mm motor-selection figure from an earlier draft was removed
   rather than retained as a provisional rule, since it originated
   from advisor judgement rather than supplier evidence; logged as a
   candidate future Solara Business Rule pending MCD-00A's resolution
   of whether business policy may govern selection ahead of complete
   technical evidence.
8. Maximum-area validation is supported as a supplier capability
   field.
9. Survey and installation guidance has been retained without yet
   deciding final UI placement.
10. Construction classification reasoning for Standard, Breakaway,
    No-Drill, and Cassette (§4a) — record your three-test analysis and
    conclusion here, including whether Breakaway was reclassified.
11. Same Room Option architectural ownership assessment (§7a) — record
    your conclusion here: which service (if any) owns cross-item
    grouping, or whether this is logged as an evidence-tracking
    architectural question.
12. Validation Engine and Recommendation Engine Configured-vs-Extended
    assessment (§2) — record your reasoning and final classification
    here.
13. Supplier-specific evidence (referenced only by category, not by
    name) belongs in MCD-04.
14. MCD-00A remains referenced but is not present in the repository,
    following existing document precedent.

Use: Date | Decision | Reasoning | Raised By.

---

# 20. Open Evidence Items

Log these honestly, using category-level language only — no supplier
names:

* Supplier motor-load thresholds for Roman constructions
* Fabric weight per square metre for each collection
* Lining and interlining weights
* Rod and bottom-bar weight calculation
* Roman-specific motor selection charts
* Confirmed supplier maximum-area rule(s)
* Live-portal motor filtering logic
* Current supplier motor models and load rules
* Supplier-specific Same Room tolerances
* Complete no-join width data for all fabrics
* Construction-specific bracket counts and spacing formulas
* MCD-00A repository dependency

These do not prevent creation of the v1.0 Draft.

---

# 21. Version History

Create: "v1.0 — Initial Roman Blinds Product Specification draft
created from primary and secondary supplier evidence, advisor trade
knowledge, and the approved MCD-01A architecture."

---

# Review Requirements

Before committing:

* Confirm the reasoning for §2, §4a, and §7a is written into
  `MCD-01B-03.md` itself (Decision Register plus the relevant
  operative section) — not only present in your chat response.
* Confirm no supplier names appear anywhere in the document, including
  the Decision Register, Open Evidence Items, and Version History.
* Confirm no motor trademarks or model numbers appear.
* Confirm the 1500mm figure (or any other unevidenced dimensional
  threshold) does not appear as an operative rule anywhere.
* Confirm §4a's construction classification reasoning is documented in
  the Decision Register, with an explicit conclusion on Breakaway
  Headrail's classification.
* Confirm §7a's Same Room ownership assessment is documented in the
  Decision Register.
* Confirm §2's Validation Engine and Recommendation Engine
  classifications are backed by documented reasoning against MCD-01A's
  actual Extended test, not carried over from the provisional table.
* Confirm Same Room Option is a grouping rule across separate items.
* Confirm fabric joins trigger an immediate advisor warning.
* Confirm fabric property and lining remain separate.
* Confirm construction determines motor compatibility.
* Confirm supplier-specific evidence is directed to MCD-04 by category
  reference only.
* Confirm existing MCD files remain untouched.
* Commit and push to the feature branch.
* Do not merge or open a pull request until review is complete.

This gets Roman moving without waiting for every remaining
supplier-data field to be complete — but it asks Claude Code to reason
through the genuinely unsettled architectural questions rather than
implement a provisional table or an unevidenced threshold as if they
were already decided.
