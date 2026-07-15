Create a new branch from main: claude/mcd-04-structured-technical-value

Update MCD-04.md only. Do not modify MCD-01A, MCD-01B-01, MCD-01B-02,
or MCD-01B-03.

## Part 1 — Schema enhancement

Add a reusable block type to MCD-04's Record Structure (§5), called
"Structured Technical Value." This generalizes and replaces the
earlier weight-only convention — it must represent weight, length,
count, dimensional deductions, and load limits without a separate
near-identical block per data type. State explicitly that this is an
MCD-04 schema enhancement applicable to all future product families
(Roller tube/fabric weights, Vertical stack/control formulas, Curtain
fullness/track-load rules, Shutter panel/frame limits, motor
torque/load thresholds, bracket-spacing formulas), not a Roman-only
addition.

Each Structured Technical Value entry contains these fields:
Metric, Value, Unit, Basis, Applies To, Calculation Rule, Input
Variables, Minimum, Maximum, Evidence Status, Source Reference, Notes.

Add one more field beyond the original design: Value Type, with
allowed values: Weight, Length, Area, Count, Torque, Voltage, Time,
Percentage, Boolean, Text Rule. This exists so automated interpretation
doesn't have to infer type from the Metric name alone.

Allowed Basis values: Fixed, Per Square Metre, Per Metre Width,
Per Metre Drop, Per Component, Per Fold, Per Lift Cord, By Drop Band,
By Width Band, Formula, Percentage of Calculated Value,
Supplier-Stated Maximum, Construction-Specific.

Include these five worked examples in the schema documentation itself
(not just this brief), using the exact field values below:

1. Lining weight — Metric: Material Weight; Value: 135; Unit: g/m²;
   Value Type: Weight; Basis: Per Square Metre; Applies To: Premier
   Lining; Calculation Rule: Value x finished lining area; Evidence
   Status: Supplier Confirmed.

2. Standard/No-Drill/Cassette chain length — Metric: Control Chain
   Length; Unit: mm; Value Type: Length; Basis: Formula; Applies To:
   Standard Headrail (also No-Drill Headrail, Cassette Headrail —
   confirm from source whether identical or create one entry per
   construction if the source shows any variation); Calculation Rule:
   Installation Height minus 1500; Input Variables: Installation
   Height; Minimum: 200mm; Notes: Fallback rule — two-thirds of blind
   drop when installation height is unavailable; Evidence Status:
   Supplier Confirmed.

3. Breakaway chain length — Metric: Control Chain Length; Unit: mm;
   Value Type: Length; Basis: Formula; Applies To: Breakaway
   configuration; Calculation Rule: Installation Height minus 600;
   Input Variables: Installation Height; Minimum: 200mm; Notes:
   Fallback rule — two-thirds of blind drop when installation height
   is unavailable; Evidence Status: Supplier Confirmed.

4. Rod count — Metric: Rod Count; Unit: count; Value Type: Count;
   Basis: By Drop Band; Applies To: Roman Blind body; Calculation
   Rule: supplier drop-band table (represent the actual band
   boundaries and counts in Notes, since this block type has no
   native multi-row table — use a compact inline format); Input
   Variables: Finished Drop; Evidence Status: Supplier Confirmed.

5. No-Drill finished-weight limit — Metric: Maximum Finished Weight;
   Value: 10; Unit: kg; Value Type: Weight; Basis: Supplier-Stated
   Maximum; Applies To: No-Drill construction; Evidence Status:
   Supplier Confirmed.

## Part 2 — Populate confirmed Roman supplier data

Using this schema, add Structured Technical Value entries to a new
Vertical Blinds-parallel section for Roman Blinds (Roman Blinds ->
Standard Headrail / Breakaway / No-Drill Headrail / Cassette Headrail,
matching MCD-01B-03's construction classification) for the following,
all confirmed from primary supplier technical documentation (name the
supplier and cite the specific source document by title in each
entry's Source Reference field — this is MCD-04, where that's expected
and required):

- Lining weights: Premier 135 g/m², Satin 200 g/m² (+/-5%), Blockout
  140 g/m², Bonded 400 g/m², Blockout Bonded 333 g/m² — include width
  and composition for each in Notes.
- Construction-specific dimensional limits (min/max width x drop) for
  all four constructions.
- No-Drill maximum finished weight: 10kg.
- Recess deductions: Width -10mm, Drop -10mm (confirm whether this
  applies uniformly across all four constructions per the source, or
  varies).
- Manufacturing tolerance: +/-5mm.
- Chain-length formulas per worked examples 2 and 3 above.
- Rod count and cord count tables by drop band, per construction.
- Motor specifications for the three named motors found (torque,
  voltage, width/drop range, battery life, warranty) — full named
  detail belongs here, not in MCD-01B-03.
- Fabric widths and compositions: do NOT create one record per
  individual fabric/colourway combination — the source table has
  roughly 100 rows and that level of granularity belongs in the
  pricing/fabric table system, out of scope for MCD-04 capability
  records. Instead, record summary-level facts useful to Product
  Engine logic (observed fabric width range across the collection,
  e.g. 1140mm-3000mm; composition variety exists per range; price
  bands A-D exist) and reference the source document by title for the
  complete range list.
- Face fabric weight (GSM): explicitly record as Value: Not Provided,
  Evidence Status: Supplier data required — do not leave this silently
  absent; state clearly that composition and width were found for
  every fabric range but weight was not, despite a direct targeted
  search, and that the confirmed next step is asking the supplier
  directly.

## Verification

- Confirm the Structured Technical Value block type and its Value Type
  field are documented in MCD-04's schema section, generically,
  before any Roman-specific data.
- Confirm no fabric-level GSM value is fabricated — the "Not Provided"
  entry must be explicit, not omitted.
- Confirm named suppliers and source document titles appear freely in
  this document (expected here, unlike MCD-01B-03).
- Confirm MCD-01A, MCD-01B-01, MCD-01B-02, and MCD-01B-03 are
  untouched.
- Add a version history entry summarizing this as the schema
  generalization plus the first Roman data population pass.
- Commit and push to the new branch. Do not open a pull request or
  merge.
