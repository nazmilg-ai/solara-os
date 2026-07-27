Use the following as the controlled research-stage findings for:
MCD-01B-08B — FITtoFRAME Venetian Blind

Create or update the product document as Working Draft — Unverified.
Record verified supplier rules separately from provisional
interpretations and unresolved evidence items.

Important controls:

* Use FITtoFRAME Venetian Blind as the advisor-facing product name.
* Keep Cruze FITtoFRAME Alumitex as an internal supplier or
  construction-system reference only.
* Use 250mm as the provisional controlled minimum width, but clearly
  record the conflict with the 200mm minimum shown in the measuring
  guide.
* Do not mark folding-handle or handle-free options as currently
  available until further ordering evidence confirms this.
* Do not prepare a Claude Code implementation brief.
* Do not convert unresolved evidence into application validation
  rules.
* Preserve all open evidence items for further review.
* Make no assumptions beyond the supplied evidence.

The document must remain open until the supplier conflicts,
installation-route rules, handle options, warranty, lead time, and
remaining compatibility requirements have been reviewed.

This is a research-stage handover only. Do not:

* finalise the product specification;
* prepare the Claude Code implementation brief;
* build validation logic into the application;
* treat the 250mm minimum width as permanently resolved;
* activate folding-handle or handle-free options.

It is suitable only for:

* creating the initial MCD-01B-08B working draft;
* recording verified rules;
* adding the evidence conflict register;
* structuring open questions;
* keeping the product status as Working Draft — Unverified.

---

## Research findings

### 1. Product identity

Advisor-facing product name: FITtoFRAME Venetian Blind

Internal supplier/system reference: Cruze FITtoFRAME Alumitex

"Alumitex" should remain an internal supplier or construction-system
reference. It should not replace the familiar product name in the
sales or survey workflow.

### 2. Verified product classification

| Classification field | Controlled value | Status |
|---|---|---|
| Product family | Venetian Blind | Verified |
| Installation family | FITtoFRAME | Verified |
| Slat material | Aluminium | Verified |
| Slat width | 25mm | Verified |
| Operation | Manual | Verified |
| Raising configuration | Tensioned Bottom Up | Verified |
| Headrail | Fixed top profile/headrail | Verified |
| Slat control | Tilt rod | Verified |
| Raising/lowering control | Handle on moving bottom profile | Verified |
| Pull cords or chains | None used by customer | Verified |
| Installation route 1 | Beading brackets/clips | Verified |
| Installation route 2 | Adhesive tape | Verified |
| Ordering measurement methods | Glass size or Glass (hidden seal) | Verified |
| Manufacturing tolerance | ±3mm width and drop | Verified |
| Maximum area | 3m² | Verified |

The specification confirms a tensioned Bottom Up blind with a fixed
headrail and screw-free installation routes. The leaflet confirms
handle operation, a Venetian tilt rod, beading-bracket or
adhesive-tape fixing, and no customer-operated pull cords.

### 3. Size-rule conflict identified

There is a genuine supplier-document conflict.

Specification document: Minimum width 250mm; Maximum width 1,500mm;
Minimum drop 150mm; Maximum drop 2,300mm; Maximum area 3m². The
specification also states the blind must not exceed the maximum
permitted area.

Marketing leaflet: agrees with the specification — Width 250-1,500mm;
Drop 150-2,300mm.

Measuring instructions: instead state Minimum width 200mm; Maximum
width 1,500mm; Minimum drop 150mm; Maximum drop 2,300mm; Maximum area
3m².

Therefore: the 200mm minimum width must not be implemented yet. The
safer controlled value remains 250mm, because it is supported by both
the dedicated product specification and the later product leaflet,
while only the measuring document says 200mm.

Evidence register entry:

| Evidence issue | Current controlled treatment |
|---|---|
| Minimum width: 200mm or 250mm | Use 250mm provisionally |
| Reason | Supported by product specification and leaflet |
| Open action | Obtain supplier clarification before closing research |
| Implementation status | Block 200-249mm unless supplier confirms otherwise |

### 4. Coupled maximum-size restrictions

The measuring guide contains two important restrictions not included
in the opening evidence:

* A width of 1,500mm is only available up to a maximum drop of
  2,000mm.
* A drop of 2,300mm is only available up to a maximum width of
  1,300mm.

These must become validation rules rather than simple information
text (once the document leaves research stage).

Proposed rules:

```
Base width range: 250-1,500mm
Base drop range: 150-2,300mm
Maximum area: 3.00m²

Coupled dimension rules:
If width > 1,300mm, drop must not exceed 2,000mm.
If drop > 2,000mm, width must not exceed 1,300mm.
```

The two coupled statements are logically equivalent around the same
restricted size zone, but both should remain traceable to the
supplier wording. The system should validate all three conditions: (1)
width and drop are inside their basic ranges; (2) width × drop does
not exceed 3m²; (3) the coupled width/drop restriction is satisfied.

### 5. Measurement method

Standard glass measurement: the surveyor measures width at the top,
middle, and bottom; drop at three positions across the glass; the
smallest measurement is ordered; beading and rubber seals are not
included in the standard visible-glass measurement.

Gasket rule — controlled decision rule:

```
Rubber gasket protrusion onto glass < 2mm → Glass (hidden seal)
Rubber gasket protrusion onto glass >= 2mm → Glass size
```

This must be treated as a measurement-method selector, not an
automatic product rejection.

The original specification says square-frame windows should have at
least 2mm of rubber bead protruding onto the glass, while the newer
measuring guide explains how to order where less than 2mm is present.
The newer measuring guidance therefore refines the earlier statement.
It demonstrates that less than 2mm is not necessarily a failed survey.

### 6. Handle clearance

The measuring guide requires at least 35mm between the glass
depth/reference and an obstruction such as a window handle.

Advisor-facing field: Glass-to-handle clearance: ___mm

Validation: 35mm or greater → Pass; below 35mm → Product compatibility
warning/failure.

However, the supplier wording is slightly awkward and refers both to
the edge of the beading and the depth of the glass. The exact
measurement datum should be visually confirmed from the guide before
finalising the survey illustration and implementation wording.

### 7. Profile dimensions

| Component | Width | Height |
|---|---|---|
| Side guide | 14mm | 8mm |
| Bottom profile | 22mm | 22mm |
| Fixed top profile | 25mm | 24mm |

These are verified internal construction dimensions. They should be
retained for obstruction checks, survey guidance, installation
documentation, technical support, and future graphical diagrams. They
do not need to appear in the basic sales workflow unless required by
a compatibility check.

### 8. Profile colours

Verified profile colours: White, Black, Anthracite, Grey, Nobel. The
default profile colour is White unless another colour is specified.

Verified RAL references: Anthracite — RAL7016; Nobel — RAL7022. Other
components are described as closely matched to the profile colour.
This wording matters — the system should not promise that every
component is an exact RAL match.

### 9. Handle rules discovered

Standard Cruze handle supplied. Clear folding handle available at
additional surcharge. No-handle ordering option available. Up to
1,200mm width: one handle per moving profile. Over 1,200mm width: two
handles. Handles consist of a handle and an insert.

Profile-to-handle matching:

| Profile colour | Standard handle colour |
|---|---|
| White | White |
| Grey | Clear |
| Nobel | Clear |
| Anthracite | Anthracite |
| Black | Black |

These should eventually create: a standard-handle default; a
folding-handle surcharge option; a no-handle option; automatic handle
quantity based on width; automatic standard handle colour based on
profile colour.

Evidence caution: the leaflet states that folding and handle-free
options are available, but also displays "Coming Soon" near that
content. Therefore, availability of the folding-handle and no-handle
options must remain an open evidence item until current ordering or
price-book evidence confirms they are live.

### 10. Initial controlled product-rule structure

```
Platform category: Bi-Fold Door / FITtoFRAME
Advisor-facing product: FITtoFRAME Venetian Blind
Product family: Venetian Blind
Construction system: Cruze FITtoFRAME Alumitex
Supplier: Decora
Material: Aluminium
Slat size: 25mm
Operation: Manual
System configuration: Tensioned Bottom Up
Headrail: Fixed
Slat control: Tilt rod
Blind movement: Handle-operated moving bottom profile

Fixing methods:
- Beading clips/brackets
- Adhesive tape

Measurement methods:
- Glass size
- Glass (hidden seal)

Basic size limits:
- Minimum width: 250mm provisional
- Maximum width: 1,500mm
- Minimum drop: 150mm
- Maximum drop: 2,300mm
- Maximum area: 3m²

Coupled restrictions:
- Width above 1,300mm limits drop to 2,000mm
- Drop above 2,000mm limits width to 1,300mm

Obstruction requirement:
- Minimum glass-to-handle clearance: 35mm

Manufacturing tolerance:
- Width: ±3mm
- Drop: ±3mm
```

## Open evidence register

The following items must be resolved before the product is closed:

1. Minimum width conflict: 200mm versus 250mm.
2. Folding handle availability: live option or still "coming soon".
3. Handle-free availability: live option or still "coming soon".
4. Exact 35mm clearance measurement datum.
5. Whether adhesive tape and beading-clip routes are advisor-selectable
   or factory/system-determined.
6. Window and bead compatibility requirements for each fixing route.
7. Whether square, shaped, rounded, or unusual glazing beads are
   restricted.
8. Whether tilt-and-turn and bi-fold suitability requires additional
   clearance checks.
9. Whether every listed 25mm slat colour is currently orderable in
   FITtoFRAME.
10. Current pricing, surcharges, and supplier ordering codes.
11. Warranty and lead time.
12. Any exclusions relating to glass type, frame type, vents, or
    seals.

The product should remain Working Draft — Unverified until these
matters are checked.
