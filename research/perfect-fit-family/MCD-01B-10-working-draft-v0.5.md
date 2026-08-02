# MCD-01B-10 — Perfect Fit Blinds Family

**Status:** Working Draft — Partially Verified
**Version:** v0.5
**Prepared for:** Solara OS Product Engine
**Drafted from:** MCD-01B-10 Claude Handover v0.1 (2 August 2026), revised through v0.4 with real supplier evidence
**This draft:** family document only. No commercial pricing included. No code, commit, or PR generated. Nothing written to MCD-04.

---

## 1. Purpose

This document consolidates verified supplier evidence and user-confirmed operational rules for the **Perfect Fit Blinds** family into a single supplier-neutral family specification, with each child product kept structurally separate.

No dimension, control, colour, bracket size, or compatibility rule has been added, inferred, or generalised beyond what supplied evidence states.

---

## 2. Product Family Scope

1. Perfect Fit Roller Blind
2. Perfect Fit Day & Night Blind
3. Perfect Fit Pleated Blind
4. Perfect Fit Cellular Blind
5. Perfect Fit Aluminium Venetian Blind
6. Perfect Fit Wooden Venetian Blind
7. Perfect Fit Lite Shutters

Each is a separate child product under a shared Perfect Fit family layer. Shared rules live at family level; product-specific rules (controls, dimensions, materials, pricing structure, operating systems, supplier capability) stay at child-product level.

---

## 3. Shared Family Layer

### 3.1 Principle

Perfect Fit products are frame-mounted systems fitted to suitable glazed doors or windows without drilling or screwing into the window frame, using: an aluminium Perfect Fit frame; corner joints or corner caps; supplier-supported fixing brackets or clips; the selected blind/shutter product fitted within the frame; glass-size measurement; supplier-specific bead-depth and bracket compatibility.

The advisor/surveyor must not assume every window is suitable. Survey must verify: glass width, glass drop, bead depth, bead shape, seal condition, frame condition, handle position, handle projection and movement, air vents/obstructions, opening direction, panel/sash movement, available clearance, supplier-supported bracket size, any packer/rebate/shim/foam-tape requirement.

### 3.2 Measurement Rule

Perfect Fit products are measured using **glass size**. The system must record: glass width, glass drop, unit of measurement, window/door reference, room, quantity, bead depth, bead type/profile, selected supplier, selected product, selected bracket/clip size.

Do not use **Exact** or **Recess** measurement options unless a supplier specifically requires those terms for a particular Perfect Fit product. Any deduction from square-frame glass dimensions must remain supplier- and product-specific — never applied as a universal family rule.

### 3.3 Frame Colour

Frame colour is a mandatory Perfect Fit configuration field, selected by the advisor after supplier and product. It must remain a field distinct from fabric, slat, shutter, headrail, bottom-bar, corner-cap, bracket, wand, chain, and tab/handle colour. The system must only display colours supported by the selected supplier, product, and operating system.

Frame, corner-cap and bracket colour mappings must be stored separately, since visible components may not share the same named colour (e.g. a Golden Oak frame may pair with Tan corner caps and Brown brackets; a Mahogany frame with Brown corner caps and Brown brackets).

**Decora frame colours currently evidenced** (per-product, not a universal list):
- Perfect Fit Roller: White, Brown, Golden Oak, Mahogany, Anthracite, Black
- Perfect Fit Sunwood: White, Anthracite, Beige, Black, Brown, Golden Oak, Mahogany
- Perfect Fit Softshade / Day & Night: White, Anthracite, Mahogany, Black
- Perfect Fit Aluminium Venetian (SPEC40): White, Anthracite, Beige, Black, Golden Oak, Mahogany, Brown (7 colours)
- **Perfect Fit Pleated/Cellular (SPEC70)**: White, Beige, Anthracite, Brown, Golden Oak, Mahogany, Black (same 7-colour set as Aluminium Venetian)

**Real Decora Frame Colour → Corner Cap Colour → Bracket Colour mapping (Perfect Fit Roller, SPEC07)**:

| Frame Colour | Corner Cap Colour | Bracket Colour |
|---|---|---|
| White | White | White |
| Brown | Brown | Brown |
| Golden Oak | Tan | Brown |
| Mahogany | Brown | Brown |
| Anthracite | Anthracite | Anthracite |
| Black | Black | Black |

Chain control is not available with the Golden Oak frame option (Roller only).

**Real Decora Perfect Fit Pleated/Cellular profile-colour-to-frame-colour mapping (SPEC70)** — profile colours differ from frame colours since they come from a separate colour system; this is a stated recommended match, not an exact one:

| Profile Colour | Frame Colour | Frame Corner Colour |
|---|---|---|
| Dark Oak | Brown | Brown |
| Golden Oak | Golden Oak | Tan |
| Oak | Golden Oak | Tan |
| Mahogany | Mahogany | Brown |
| White | White | White |
| Cream | Beige | Beige |
| Grey | White | White |
| Anthracite | Anthracite | Anthracite |
| Nobel | Anthracite | Anthracite |
| Black | Black | Black |
| Brown | Brown | Brown |
| Walnut | Brown | Brown |

When a Beige Perfect Fit frame is wanted, Decora recommends a White pleated profile instead, since no exact beige match exists.

### 3.4 Handle Clearance, Handle Rebate and Accessories

**Handle packers**: 2 mm and 6 mm only (the earlier 3 mm reference is withdrawn). Used where a turning window handle rubs, slides against, or contacts the Perfect Fit frame, bringing the handle forward for clearance. Surveyor must confirm: handle remains securely fixed; locking mechanism operates correctly; window opens/closes correctly; handle clears the frame through full movement; packer does not create another obstruction. System should record: packer required (Y/N), packer size (2/6mm), quantity, handle position, final clearance confirmed.

**Handle rebate / handle insert**: a supplier-supported option where the frame needs to accommodate the window handle. Known positions: None, Left Centre, Right Centre, Left Offset, Right Offset, Bottom Centre. Supplier-specific systems may also support Top, Bottom, Left, Right, Centre, Custom, Rail handle rebate, Stile handle rebate. Handle position must not be assumed central.

- Beverley: left/right handles measured bottom-to-centre of handle; top/bottom handles measured left-to-centre of handle; measured from the glass, not the outer frame.
- Decora: handle-insert position must be supplied at point of order. On Perfect Fit Pleated/Cellular (SPEC70), 25mm clearance is specifically required between any window handle/vent and the glass.

**Shared accessory catalogue** (supplier-mapped availability only, none universal): 2mm/6mm handle packers, self-adhesive foam, clip shims/packing shims, clip covers, Perfect Fit Konnect magnetic strip, Konnect insert, handle insert, handle rebate, folding handle, alternative glide handle, split tiltrod/split tilt bar, side clips, extension/special clips where evidenced.

### 3.5 Fixing Brackets, Clips and Bead Depth

Bracket/clip size is selected from supplier-supported values only; not every product supports every size.

- Decora examples: 18, 20, 22, 24, 26, 28, 30, 32, 38 mm — confirmed with real product codes for Roller and for Perfect Fit Pleated/Cellular (e.g. 18mm White = PF018, Brown = PF032, Anthracite = PF052, Black = PF109; full code table exists for all 9 sizes × 4 colours)
- Beverley Perfect Fit Shutter Lite: 18, 20, 22, 24, 26, 28, 30, 32 mm

**Fixing-hole convention (side frames)**: two holes are punched into the side frames as standard. A third hole is added over 1100mm **drop** — confirmed identically across Decora Perfect Fit Roller (SPEC07), Softshade/Day & Night (SPEC73), Sunwood/Wooden Venetian (SPEC08), Shutter Lite (SPEC42), and now Pleated/Cellular (SPEC70). **Decora's Aluminium Venetian spec (SPEC40) is the sole exception**, stating a width-trigger instead of a drop-trigger for the third hole — flagged as an unresolved discrepancy, increasingly likely to be a source inconsistency given how consistently every other Decora Perfect Fit product uses drop (see §D.6).

**Fixing bracket quantity by drop**: 4 brackets under 1100mm drop, 6 brackets from 1101mm drop upward — confirmed across every Decora Perfect Fit product evidenced, including Roller and Pleated/Cellular.

Beverley also states: quadrant-type beading recommended; smaller beads can be accommodated with foam tape and a clip shim; packing shims sit behind the clip/frame to keep it square; foam tape and shims may combine for sub-20mm beads. These are supplier-specific methods, not generalised family rules.

---

## PART A — Perfect Fit Roller Blind

### A.1 Definition
A roller blind contained within a Perfect Fit frame, fitted to suitable glazed windows/doors. Kept separate from standard Roller Blind, Perfect Fit Day & Night, Perfect Fit Pleated/Cellular, and spring-operated standard Roller.

### A.2 Control Systems
Supplier- and system-dependent. Possible: chain control, tensioned spring system, tab/handle attached to spring system. Advisor must select supplier before control.

**Decora evidence** (`SPEC07`, V5, 11.03.2026): available as tensioned or chain-control system. Chain control NOT available with Golden Oak frame. Chain side: right or left. Tensioned operation uses a handle on the wrap-around bottom bar.

### A.3 Decora Perfect Fit Roller — Verified Technical Evidence
- Frame: aluminium, matching corner caps, 6 colours (White, Brown, Golden Oak, Mahogany, Anthracite, Black)
- Fabric sources: The Fabric Box; Excel Roller Collection
- Tube: 25mm aluminium
- Glass-size limits: Chain — width 200–1400mm; Spring — width 330–1400mm; Drop 300–1800mm (actual limit fabric-dependent)
- Square-frame guidance: Decora recommends 5mm deduction from width and drop (Decora-specific, not a universal Perfect Fit rule)
- Side-frame fixing: 2 holes per side (3 over 1100mm drop)
- Fixing brackets: 4 under 1100mm drop, 6 over
- Handle insert: available, position supplied at order, colours White/Tan/Brown/Anthracite/Black
- Frame/corner-cap/bracket colour mapping: see §3.3 table
- Real fabric list received, organised by max-drop bucket (up to 1000/1200/1400/1600/1800/2000/2200mm) — dozens of named fabrics (Aki, Odin, Lennox, Marlow, Rocha, Sisi, Uniview, etc.); too large to reproduce here, source PDF is authoritative
- **Restriction**: Golden Oak frame not available with chain control

### A.4 Required Configuration Fields
Supplier, control type, chain-control side (where applicable), chain colour (where applicable), tab/handle type and colour (where applicable), control restrictions linked to frame colour, child-safety device (where applicable).

### A.5 Pricing Rule (structure only — no values)
Driven by: supplier, selected fabric, supplier-assigned fabric price band, glass width, glass drop, frame colour/type, control system, accessories/surcharges. Advisor selects fabric/colourway; system retrieves price band automatically — price band should not normally be advisor-selected.

### A.6 Beverley Perfect Fit Roller — Verified Evidence (in-house manufactured)
**User-confirmed manufacturing relationship**: Beverley buys fabrics from both Decora and Louvolite, but manufactures the Perfect Fit Roller blind in-house themselves — Decora is a fabric source, not the blind manufacturer, for this route.

- Real fabric-band tables (pp.17–19) for THREE fabric sources: **Louvolite**, **Decora**, and **Eclipse** (Eclipse is a fabric source not seen elsewhere in this project) — each with fabric-name-to-band (A–E, or AAA/AA for Decora) and roll-width mappings
- "PF Roller Blinds Std Frame" and "PF Roller Blinds Special Frame" (pp.15–16): real pricing grids, Bands AAA/AA/A/B/C/D/E, width 0.610–1.400m
- **Confirmed frame-tier convention**: Special Frame = Golden Oak & Mahogany; Standard Frame = White, Anodised, Anthracite, Beige, Black, Brown
- Chain Operation available left or right on both frame tiers; only certain fabrics can be made to maximum drop (thicker fabric = smaller max drop)
- Real Konnect/accessory pricing: Konnect Magnetic Strip £3.00/mtr, Konnect Insert £0.66/mtr, Handle Rebate £3.77 each, 12mm Double Side Foam Tape £0.28/mtr, Window Handle Packer £0.14 each

### A.7 Evidence Gaps — Do Not Automate/Expose
- Other-supplier (beyond Decora/Beverley) size limits and control mappings
- Complete pricing grids transcribed into MCD-04
- Chain lengths and child-safety details for every supplier
- Whether Beverley's frame-tier convention applies identically across every fabric band

---

## PART B — Perfect Fit Day & Night Blind

### B.1 Definition
A Day & Night fabric system contained within a Perfect Fit frame. Supplier names may include Perfect Fit Softshade, Perfect Fit Day & Night, Perfect Fit Night & Day. **Advisor-facing name: Perfect Fit Day & Night Blind.**

### B.2 Control Systems
Supplier-dependent. Possible: chain control, spring-operated, tab control. No universal control assumed.

**Decora evidence** (`SPEC73`, V5, 04.03.2026): chain controlled only. This specification does not evidence a spring/tab system for Perfect Fit Softshade. Other manufacturers may support spring/tab, but must be mapped separately — not yet evidenced.

### B.3 Decora Perfect Fit Softshade — Verified Technical Evidence
- Frame: aluminium, 4 colours (White, Anthracite, Mahogany, Black)
- Fabric source: Softshade Roller collection
- Control: chain, right or left, 400mm continuous plastic chain, chain colour matches corner-cap colour, chain tidy = child-safety device
- Tube: 25mm
- Glass-size limits: width 200–1500mm; drop 500–2000mm (max drop fabric-dependent)
- Konnect: recommended max drop 1400mm
- Side-frame fixing: 2 holes per side (3 over 1100mm drop)
- Fixing brackets: 4 under 1100mm drop, 6 over
- Bracket sizes: 18/20/22/24/26/28/30/32/38mm
- Handle insert: White/Brown/Anthracite/Black, position supplied at order
- Fabric-dependent max drops visible in source: 1400/1500/1800/2000mm — must be mapped at fabric-colourway level, not replaced by the general 2000mm product max

### B.4 Required Fields
Supplier, control system, chain side/colour/length (where applicable), child-safety device, tab type/position (where applicable), frame colour, fabric, fabric price band, bracket size, handle insert or packer, Konnect option (where supported).

### B.5 Pricing Rule (structure only)
Driven by: supplier, fabric collection, fabric colourway, supplier-assigned fabric price band, glass width, glass drop, frame colour, control system, Konnect option, accessories/surcharges. Fabric band derived automatically.

### B.6 Evidence Gaps
- Spring/tab suppliers and exact system rules
- Full fabric-band mapping
- Non-Decora dimensions and controls
- Other-supplier chain and child-safety data
- Whether Beverley manufactures this product in-house too (confirmed for Roller and Pleated; not yet confirmed for Day & Night)

---

## PART C — Perfect Fit Pleated and Cellular Blinds

### C.1 Product Separation
Pleated and Cellular are **separate child products**. They may share frame system, fixing method, accessories, operating-style options, fabric-band pricing structure. They must retain separate fabric collections, technical limits, performance attributes, fabric thickness, construction, and supplier restrictions. **Do not merge these into one product.**

### C.2 Manufacturing Relationship — User-Confirmed
Beverley sells fabrics sourced from Decora but **manufactures the Perfect Fit Pleated blind in-house themselves** — the same in-house-manufacturing pattern confirmed for Perfect Fit Roller and Aluminium Venetian. Decora also produces its own complete Perfect Fit Pleated/Cellular product (the "Cruze" range, SPEC70) sold under its own name. Both are therefore live, independently-evidenced routes to market for this product, not a single supplier chain — kept as two separate technical/pricing profiles below rather than merged.

### C.3 Decora Perfect Fit Pleated/Cellular — Verified Technical Evidence (SPEC70, "Cruze" range, Issue V7, 17.06.2026)

**Scope note**: SPEC70 covers Decora's full Cruze Pleated & Cellular range — Free-Hanging, Tensioned, and FITtoFRAME™ system types exist in the source alongside Perfect Fit, but only the **Perfect Fit configuration (CZP11/CZP12)** is in scope for this family document; the other system types belong to a separate, non-Perfect-Fit Cruze product line.

- **CZP11 (Perfect Fit Bottom Up)**: Min Width 200mm, Min Drop 150mm, Max Width 1500mm, Max Drop 2300mm, Max Area 3m². Top Profile Standard, Bottom Profile Reinforced. Control Options: Handle/No Handle
- **CZP12 (Perfect Fit Top Down Bottom Up)**: same size limits as CZP11. Top Profile Reinforced, Bottom Profile Reinforced. Control Options: Handle/No Handle
- Mounting: under-glass beading with brackets (Top Fix Bracket, code CZP186, Chrome, 30mm×7mm×22mm; bracket quantity 2 up to 700mm width, 3 from 701–1300mm, 4 from 1301–1500mm)
- Frame: aluminium, 7 colours — White, Beige, Anthracite, Brown, Golden Oak, Mahogany, Black (same 7-colour set as Decora's Aluminium Venetian, SPEC40)
- 25mm clearance required between handles/vents and glass
- **Perfect Fit Profile** (system-specific, distinct from the Standard/Reinforced profiles used elsewhere in the Cruze range): Width 38mm, Height 26.4mm
- Side-frame fixing: 2 holes standard, 3 holes over 1100mm **drop** (matches the family-wide convention — see §3.5)
- Fixing brackets: 9 sizes (18–38mm), colours White/Brown/Anthracite/Black, real product codes for all size/colour combinations (e.g. 18mm White = PF018); bracket quantity 4 under 1100mm drop, 6 from 1101–2300mm
- Control handle: "Cruze Handle" standard (White/Black/Anthracite/Clear); Folding Handle available as a surcharge option (Clear only). Handle quantity: 1 per moving profile up to 1.2m width, 2 over 1.2m width. Handles are two pieces (handle + insert); can be ordered with no handle
- Handle insert: 6 colours (White, Tan, Brown, Grey, Anthracite, Black); position in frame must be specified at order
- Profile-colour-to-frame-colour mapping: see §3.3 table
- Cell width 25mm (Cellular) / Pleat size 20mm (Pleated) — the stated structural distinction between the two products, consistent with keeping them separate per §C.1
- Cords/ladders chosen to closest fabric colour; white ladder used if no match available

**Fabric collections (real, separate per product)**:
- **Cellular uses "Softcell" fabrics**: Astoria, Artezen, Blenheim, Bowery (CZP04/CZP06 only — non-Perfect-Fit system types), Hudson, Lexington, Soho, Tribeca — each mapped to colour, composition, width(cm), fabric properties (Dimout/Blockout/Voile/Texture/Water Resistant/FR), and price band A–E
- **Pleated uses a separate "Pleated Fabrics" collection** (~36 named fabrics: Addison, Akona, Aliz, Amos, Arlo, Aspinal, Astral, Bahama, Bask, Cecily, Equa, Essence, Evissa, Fusion, Glantus, Hamilton, Hovia, Hypno, Kana, Kimora, Loxton, Luqa, Mako, Mirabella, Mirari, Mythic, Noto, Nouveau, Oketo, Paradise, Scandi, Sylvan, Talia, Tropez, Vista, Xyla) with the same colour/composition/width/properties/price-band structure
- Both fabric tables are real and complete but too large to reproduce here in full; source PDF is authoritative

### C.4 Beverley Perfect Fit Pleated — Verified Evidence (in-house manufactured)
- "Pleated Free Hanging Cell fabric only" (p.35, non-Perfect-Fit): real pricing grids, Band VFM/VFM BO, width 0.400–2.000m × drop 0.600–3.500m; colours White/Silver/Black/Brown/Anthracite/Tan; build variants Standard, Tensioned (£2.00/Mtr surcharge), 3 Bar Tensioned (£3.25/Mtr surcharge)
- "Pleated Skylight Cell" (p.36, non-Perfect-Fit, rectangular only): Width 200–1400mm, Drop 200–3000mm
- **"Perfect Fit Pleated (Standard Frames)" (p.37) and "(Special Frames)" (p.38)**: real pricing grids, Band VFM/VFM BO, width 0.400–1.400m × drop 0.400–2.400m, for Standard Perfect Fit / Dual Pull Perfect Fit / Dual Meet Perfect Fit build styles; Special Frame prices genuinely higher than Standard Frame at equivalent cells; both carry Folding Handle £1.50 and Handle Rebate £1.16 surcharges; Dual Pull/Dual Meet carry an additional insert cost by width
- **"Perfect Fit Pleated Specifications" (p.39)** — real frame-tier mapping: **Special Frames = Golden Oak & Mahogany; Standard Frames = White, Black, Brown, Anthracite Grey, Matt Grey**. Head Rail Colours: White/Silver/Black/Brown/Anthracite Grey/Tan. Bracket sizes 18–38mm (9 sizes), Bracket Colours White/Unpainted/Brown/Anthracite Grey/Black. Size limits: Min Width 80mm–Max Width 1400mm, Max Drop 2400mm. Window packing piece 2mm & 6mm (colours White/Brown/Tan/Light Grey/Brown/Anthracite). Fabrics: Iverea/Iverea BO, Lexington/Lexington BO (Band VFM/VFM BO)

### C.5 Decora vs Beverley Perfect Fit Pleated — Supplier Comparison

| Rule | Decora (SPEC70, Cruze) | Beverley |
|---|---:|---:|
| Minimum glass width | 200 mm | 80 mm |
| Maximum glass width | 1500 mm | 1400 mm |
| Minimum glass drop | 150 mm | not separately stated (grid starts 0.400m) |
| Maximum glass drop | 2300 mm | 2400 mm |
| Max area | 3 m² | not stated |
| Frame colours | 7 (White, Beige, Anthracite, Brown, Golden Oak, Mahogany, Black) | Standard: White, Black, Brown, Anthracite Grey, Matt Grey; Special: Golden Oak, Mahogany |
| Standard/Special Frame tier | Not evidenced as a Decora pricing tier | Explicit tier — Special = Golden Oak & Mahogany |
| Bracket sizes | 18–38mm (9 sizes), White/Brown/Anthracite/Black | 18–38mm (9 sizes), White/Unpainted/Brown/Anthracite Grey/Black |
| Control | Handle/No Handle (Cruze Handle, Folding Handle surcharge option) | Folding Handle (£1.50 surcharge), Handle Rebate (£1.16 surcharge) |
| Operating styles | Bottom Up (CZP11), Top Down/Bottom Up (CZP12) | Standard, Dual Pull, Dual Meet Perfect Fit |
| Fabric collection | Pleated Fabrics (~36 named fabrics, price bands A–E) | Iverea, Lexington (price bands VFM/VFM BO) |
| Window packing/handle clearance | 25mm clearance stated; handle insert 6 colours | 2mm & 6mm window packing piece, 6 colours |
| Fixing-hole trigger | 3rd hole over 1100mm drop | Not separately stated in supplied evidence |

**No universal Pleated limit should be created from these values — each stays supplier-specific, and both remain live evidenced routes to market per §C.2.**

### C.6 Cellular-Specific Notes
Real Decora technical spec (CZP11/CZP12, same as Pleated) and the separate Softcell fabric collection are now evidenced (§C.3). No Beverley-specific Cellular evidence has been supplied yet — only Beverley Pleated evidence exists on the Beverley side. Do not assume Beverley's Pleated pricing/frame-tier structure applies identically to Cellular until confirmed.

### C.7 Pricing Rule (structure only)
Driven by: supplier, product type, operating style, frame type/colour, fabric collection, fabric colourway, supplier-assigned price band, glass width, glass drop, accessories/surcharges.

### C.8 Evidence Gaps — Unresolved / Supplier Evidence Required / Do Not Automate or Expose
- Beverley Cellular-specific technical spec and pricing (currently only Beverley Pleated evidence exists)
- Full price-band-to-fabric mapping transcription into MCD-04 for both suppliers
- Other-supplier (beyond Decora/Beverley) operating styles and limits
- Whether Decora's Perfect Fit Pleated/Cellular has its own Standard/Special Frame pricing tier (not evidenced in SPEC70, unlike Beverley's explicit tier)

### C.9 Blocking Rule
**No longer blocked on "zero technical extraction"** — real Decora (SPEC70) and Beverley technical/pricing evidence both now exist for Pleated. Cellular has real Decora technical evidence but no Beverley-specific evidence yet. Both products remain blocked on: full pricing transcription into MCD-04, and confirming Beverley's Cellular-specific position.

---

## PART D — Perfect Fit Aluminium Venetian Blind

### D.1 Required Fields
Supplier, frame colour, slat colour category, slat colour, glass width, glass drop, bracket size, handle insert or packer, wand side, wand length, bottom-bar colour, handle type, operating configuration, accessories.

### D.2 Slat Colour Categories
Standard and Special. Advisor selects category then exact colour. Special colours may affect price, lead time, availability — these effects are supplier-controlled, not assumed.

### D.3 Wand Fields
Wand side: Left/Right. Wand length: supplier-supported lengths only (none yet evidenced). Wand position must avoid interference with window handle and Perfect Fit frame.

### D.4 Primary Sales Channel — Arena Metal Venetian Perfect Fit, purchased via Beverley Blinds
**User-confirmed: Solara's primary route to market for Perfect Fit Aluminium Venetian is Arena-manufactured product, purchased through Beverley Blinds — not bought directly from Arena, and Decora is not the primary supplier for this product despite Decora's spec (SPEC40, §D.5) being the most detailed on file.**

Source: Arena trade price list, issued June 2026, pp.10–18. Real pricing grids exist for Standard Perfect Fit, Special Effects Perfect Fit, Golden Oak Frame Perfect Fit, and Tabbed (Standard + Special Effects) — **pricing itself excluded from this document, belongs in MCD-04.**

**Resolved**: Beverley has its own separate price list for Arena-manufactured Perfect Fit blinds — confirmed genuinely distinct from Arena's direct trade pricing (e.g. Standard Perfect Fit, 46cm width/61cm drop: Beverley Standard Frame £38.88 vs. Arena's own direct list ~£72 for the equivalent cell). **Beverley's own Perfect Fit price list is Solara's real cost basis, not Arena's direct list** — the Arena pricing evidence above should not be used as the pricing source for MCD-04; Beverley's tables supersede it once fully transcribed.

**Standard/Special Frame tier — strong inference, not yet directly confirmed for this product**: Given the identical Standard/Special Frame convention now independently confirmed for both Perfect Fit Roller and Perfect Fit Pleated (Special = Golden Oak & Mahogany, Standard = everything else — §A.6, §C.4), it's highly likely Aluminium Venetian's Standard/Special Frame split follows the same convention. This should be verified directly against Beverley's Aluminium Venetian evidence before being applied as fact in MCD-04.

- Slat widths: 15mm, 25mm, 35mm, 50mm (availability varies by finish/colour — see full colour specification, source-authoritative)
- Perfect Fit & Tabbed system limits: Max width 130cm, Max drop 200cm, Max area 2.2m², Min width 15.3cm, Min drop 8cm
- **Measurement types differ from the family's stated glass-size-only rule**: Arena defines Exact (exact area to cover) and Recess (recess width measured wall-to-wall in 3 places, drop measured recess-top-to-sill in 3 places; if a size falls between price-table sizes, the next larger size is charged) — flagged as a genuine supplier-specific exception to the family measurement rule, not resolved
- Operation: 15/25mm slats tilt by wand; 35/50mm tilt by two cords; raise/lower always by cords, side specified at order (left/right/separate)
- Side Guide Tilt: up to 15° from vertical, 15/25mm slats only, all controls same side
- Side Guide Roof: for Velux/roof windows, up to 45° from vertical, 25mm slats only, comes with a tilt-rod retainer at the side
- Partition blinds: flexible tilt mechanism, tilt only — cannot be raised or lowered
- Double Glazing blinds: tilt/torsion rod + bowden cable, can be tilted, raised, and lowered
- Headrail depth: 27mm×19mm (15/25mm blinds) vs. 40mm×40mm (35/50mm blinds); cord lock differs by headrail profile; 50mm blinds have an enclosed bottom rail
- Full colour specification received (~100 colours): each with slat finish, slat width availability, headrail colour, ladder/tape colour, and special-effects Y/N flag — too large to reproduce here in full; source document is authoritative

### D.5 Secondary / Comparison Evidence — Decora Perfect Fit Aluminium
Source: `SPEC40 - Perfect Fit Aluminium Collection - Issue V8 - 25.03.2026`. Slats: Alumitex 25mm Collection. Kept on file as comparison evidence — **not currently Solara's primary route for this product** (see §D.4). Three distinct systems evidenced — **Free Hanging**, **Privacy**, **Glide** — each with its own dimensional and control profile; must not be merged into one generic Aluminium Venetian configuration.

**Frame**: 7 colours (White default) — Anthracite, Beige, Black, Golden Oak, Mahogany, White, Brown. **Corner joints**: Nylon 6, colours White/Brown/Tan/Beige/Anthracite/Black. **Headrail**: steel, 24mm(W) × 25mm(H).

**Free Hanging** — no tension, blind free within frame, tilt wand + cord operation:
- Corner caps: White, Beige, Tan, Brown, Anthracite, Black
- Glass size: Width 220–2000mm (wavier to 2200mm); Drop 150–2200mm (wavier to 2400mm)
- Controls: Raise = Plastic Tassel; Tilt = Clear Wand. Control side: 220–455mm width → Standard or RH Tilt/LH Raise; 456mm+ → also Left or Right
- Handle insert: White/Tan/Brown/Anthracite/Black, position supplied at order (Top/Bottom measured from left-hand beading to spindle centre; Left/Right measured from top beading to spindle centre)
- Bottom bar: 11mm(H) × 25mm(W), colour matches slats/headrail

**Privacy** — tension system using the 25mm aluminium bottom bar, centre handle, hidden side cords:
- Corner caps: White, Beige, **Grey**, Brown, Anthracite, Black *(differs from Free Hanging's "Tan" — not yet confirmed whether intentional or a source inconsistency; flagged, not resolved)*
- Glass size: Width 220–1500mm; Drop 150–2000mm (no wavier stated)
- Controls: Raise = Plastic handle; Tilt = Clear Wand; Left (standard) or Right. Folding handle available for bi-fold doors (surcharge applies) — colours Anthracite/Black/Brown/Light Grey/Tan/White
- Blinds over 851mm wide: 2 handles, equally spaced
- Springs: Width 0–600mm/Drop 0–1500mm = Single; Width 1500mm+/Drop 1500mm+ = Double Spring

**Glide** — tension system, same dimensional profile as Privacy, different handle range:
- Glide Handle: plastic, colour-matched to bottom bar where applicable, Frost default otherwise — Anthracite/Black/White/Frost
- Same folding-handle option/colours as Privacy
- A "Pleated Bottom Bar" colour set also appears in this section of the source (14mm×22mm, Anthracite/Black/Brown/Silver/Tan/White, matched to frame, White default) — **not yet confirmed whether this is genuinely a Glide-system option or a cross-reference artifact in the source document; flagged, not acted on**

**Shared across all three systems**:
- Square-frame guidance: 5mm deduction from width/drop (Decora-specific rule, consistent with other Decora Perfect Fit products)
- Side-frame fixing: 2 holes per side; 3 holes over 1100mm **width** — *this differs from every other Decora Perfect Fit product evidenced across the family (Roller, Softshade, Sunwood, Shutter Lite, and now Pleated/Cellular), all of which trigger the 3rd hole over 1100mm **drop**. With Pleated/Cellular now also confirming the drop-trigger convention, this SPEC40 width-trigger looks increasingly like a genuine source inconsistency rather than a real product difference — still not directly confirmed either way*
- Fixing brackets: 4 under 1100mm drop, 6 over (matches other Decora Perfect Fit products)
- Bracket sizes: 18/20/22/24/26/28/30/32/38mm, colours White/Brown/Anthracite/Black
- Swivel brackets: standard steel, 1 per ladder
- Punch-hole spacing by width interval: ≤365mm=75mm/2 punch/2 ladders; 366–450mm=100mm/2/2; 451–850mm=150mm/2/2; 851–1400mm=150mm/3/2; 1401–1950mm=150mm/4/4; 1951–2500mm=150mm/5/3
- Full colour-coordination table: 100+ Alumitex slat colours, each mapped to Headrail/Bottom Bar colour, Cord/Ladder colour, and Glide Bottom Bar colour, with an (M)=matching or (R)=nearest-available flag per colour — too large to reproduce here in full; source document is authoritative
- Mixed slat finish available, £8.65 surcharge, waiver required for non-standard requests

### D.6 Evidence Gaps — Unresolved / Supplier Evidence Required / Do Not Automate or Expose
- Whether Arena's direct trade price list matches what Solara actually pays via Beverley, or whether Beverley pricing needs to be sourced separately (resolved — see §D.4)
- Whether the Standard/Special Frame tier (confirmed elsewhere) applies identically to this product — strong inference only, not directly confirmed
- Wand-length options (neither Arena nor Decora SPEC40 evidence states this)
- Pricing extraction into MCD-04 (structure known, real figures not yet transcribed)
- The three flagged Decora SPEC40 discrepancies (§D.5) — Privacy corner-cap colour, 1100mm width-vs-drop hole trigger, Glide "Pleated Bottom Bar" relevance — lower priority now that Decora is confirmed secondary, but still worth resolving eventually

### D.7 Blocking Rule
No longer blocked on "zero evidence" — real Arena (primary channel) and Decora (secondary) technical specifications now exist. Remains blocked on: confirming the Standard/Special Frame mapping for this specific product, and pricing extraction into MCD-04.

---

## PART E — Perfect Fit Wooden Venetian Blind

**Advisor-facing name: Perfect Fit Wooden Venetian.** Supplier collections (e.g. Sunwood) used internally only.

### E.1 Required Fields
Supplier, frame colour, wooden slat range, slat colour, colour category (where applicable), glass width, glass drop, bracket size, bottom-bar colour, handle insert or packer, wand side, wand length, operating configuration, accessories.

### E.2 Decora Perfect Fit Sunwood — Verified Technical Evidence
Source: `SPEC08 - Perfect fit Sunwood Collection - V6 - 11.03.2026`
- System: tensioned Glide; bottom bar raised/lowered via centre handle; clear wand for tilt
- Frame colours: Anthracite, Beige, Black, Brown, Golden Oak, Mahogany, White (White default unless specified)
- Headrail: steel, colour-coordinated to slats, 24mm width × 25mm height
- Glass-size limits: width 250–1200mm; drop 150–2200mm
- Square-frame guidance: 5mm deduction (Decora-specific)
- Bracket sizes: 20/22/24/26/28/30/32/38mm
- Fixing brackets: 4 under 1100mm drop, 6 over
- Raise control: standard plastic Glide handle; optional folding handle (bi-fold doors, surcharge applies)
- Tilt control: standard clear wand left; optional right
- Handle quantity: blinds over 851mm wide have two handles, equally spaced
- Handle insert: available, position supplied at order, colours White/Tan/Brown/Anthracite/Black
- Slat: 25mm Sunwood slat
- Colour coordination: cords/ladders colour matched where applicable; bottom bar may match slat colour, White as fallback default, or customer may match to frame
- Current Sunwood colour evidence (Essential range): Ash, Auburn, Carbon, Honey, Kalm, Kohl, Morena, Oregon, Perla, Polar, Pure

### E.3 Evidence Gaps — Unresolved / Supplier Evidence Required / Do Not Automate or Expose
- Full supplier list (only Decora/Sunwood evidenced)
- Exact wand-length options
- Full colour/range mapping beyond the Essential range shown
- Pricing grids
- Moisture and application limitations where relevant

---

## PART F — Perfect Fit Lite Shutters

### F.1 Definition
Shutter panels clipped directly to suitable glazed windows/doors via a Perfect Fit-style fixing system. **Not fabric blinds** — must not inherit fabric price-band logic, chain controls, Venetian wand controls, or Roller/Day & Night system rules. Requires its own panel, louvre, tiltrod, handle-rebate and multi-panel logic.

### F.2 Shared Shutter Lite Fields
Supplier, glass width, glass drop, panel quantity, calculated panel widths, louvre size, shutter colour, tiltrod side, split tiltrod, rail handle rebate, stile handle rebate, handle location, handle-centre measurement, bracket/clip size, handle packer, side brackets/clips, midrail (where required/recommended), air vent/obstruction clearance, astragal requirement, light-gap acknowledgement, pricing-grid result, surcharges.

### F.3 Decora Perfect Fit Shutter Lite — Verified Evidence
Source: `SPEC42 - Perfect Fit Shutter Lite Specification - Issue V3 - 18.03.2026`
- Construction: clips directly to frame, no drilling, no outer framework, removable for cleaning
- Panel size: overall panel 46mm larger than glass size (gives overlap onto frame); multi-panel openings — combined panel size remains 46mm larger than glass size, panels equally sized
- Pitch: variable, may vary up to 8mm depending on panel drop
- Side brackets: required over 900mm drop
- Handle rebate/tiltrod rule: if a panel has a stile handle rebate, tiltrod must be on the opposite side
- Midrail: recommended for glass size 1500mm and over
- Glass-size limits: Minimum 201×174mm (panel 247×220mm); Minimum recommended 201×229mm (panel 247×275mm); Maximum single panel 754×2154mm (panel 800×2200mm); Maximum opening 3000×2154mm, up to 5 panels butted
- Profile: louvre size 63mm, rail size 50mm
- Bracket sizes: 18/20/22/24/26/28/30mm — minimum 22mm required for louvres to fully clear the glass
- Tiltrod position: Right standard, Left optional
- Options: rail handle rebate, stile handle rebate, 6mm handle packer, split tiltrod
- Panel quantity by glass width: 1 panel 201–754mm; 2 panels 448–1554mm; 3 panels 695–2354mm; 4 panels 942–3000mm; 5 panels 1189–3000mm

### F.4 Beverley Perfect Fit Shutter Lite — User-Supplied Evidence
Source: Beverley Blinds Master 2026, screenshots pp.40–45
- Pricing grid structure: width columns 300/450/600/750mm; drop rows under-300 through 2100mm at 150mm increments — **actual figures not yet extracted, belong in MCD-04, not this document**
- Surcharges shown (commercial, belong in MCD-04): Handle rebate £3.50; Split tilt bar £2.00
- Glass-size limits: width 150–750mm; drop 155–2100mm
- Bracket sizes: 18/20/22/24/26/28/30/32mm
- Bead/clip guidance: quadrant-type beading recommended; sub-20mm beads via foam tape + unique clip shim; clip covers supplied; packing shims keep clips square; example shown 16mm bead depth using 20mm clip + 4mm shim + foam tape
- Tilt: Left or Right
- Handle insert: Centre default; Top/Bottom/Left/Right; custom supported. Measured Bottom/Top = left-to-centre; Left/Right = bottom-to-centre; always from glass. Tilt must be opposite side to handle insert
- Frame overlap: ~25mm from glass onto window frame; vents/handles/obstructions must be checked
- Wide windows: max individual panel width 750mm glass size; panel count selected so no panel exceeds 750mm (example: 1200mm window → four 300mm panels)
- Wide windows with central top/bottom handles: central rebate cannot cross two panels — odd panel count may be required so rebate falls within one panel
- Multi-panel finish: astragal covers gaps between panels
- Light limitation: **not blackout, must not be sold as blackout** — thinner top/bottom rails leave ~3mm gap against window, customer must be informed
- Clip quantity: standard 4 (2 top, 2 bottom); side rails over 1m — 1 additional side clip per side at centre

### F.5 Decora vs Beverley Shutter Lite — Supplier Comparison

| Rule | Decora | Beverley |
|---|---:|---:|
| Minimum glass width | 201 mm | 150 mm |
| Maximum single-panel glass width | 754 mm | 750 mm |
| Minimum glass drop | 174 mm | 155 mm |
| Maximum glass drop | 2154 mm | 2100 mm |
| Maximum opening width | 3000 mm | Multi-panel logic evidenced; full technical maximum not separately stated |
| Louvre size | 63 mm | Not confirmed in supplied screenshots |
| Bracket/clip sizes | 18–30 mm | 18–32 mm |
| Tilt side | Right standard / Left | Left / Right |
| Split tilt option | Yes | Yes |
| Handle rebate | Rail / Stile | Centre / Top / Bottom / Left / Right / Custom |
| Handle packer | 6 mm | Shims and foam-tape method evidenced |
| Midrail | Recommended from 1500 mm glass size | Not confirmed in supplied screenshots |
| Side support | Side brackets over 900 mm drop | Side clips where rails exceed 1 metre |
| Blackout | Not claimed | Explicitly not blackout |

**No universal Shutter Lite limit should be created from these values — each stays supplier-specific.**

### F.6 Evidence Gaps — Unresolved / Supplier Evidence Required / Do Not Automate or Expose
- Beverley original workbook extraction (screenshots only so far)
- Beverley shutter colour and louvre-size evidence
- Beverley maximum total opening dimensions
- Exact material specification
- Current warranty and lead time
- Decora and Beverley pricing extraction into MCD-04
- Any other supplier capability

---

## 4. Shared Pricing Architecture (structure only — no commercial values)

**Fabric products** (Roller, Day & Night, Pleated, Cellular) use supplier-assigned fabric price bands. Flow: select product → supplier → control/operating style → frame colour/type → fabric collection → fabric/colourway → system retrieves price band → apply width×drop grid → add frame/control/accessory surcharges → apply Solara mark-up/selling-price rules. Advisor should not normally choose price band manually.

**Venetian products** (Aluminium, Wooden): pricing may depend on Standard/Special slat colour, dimensions, frame colour, supplier range, wand/accessory selections, applicable surcharges.

**Shutter Lite**: pricing may depend on supplier, glass width, glass drop, panel quantity, handle rebate, split tiltrod, accessories, supplier-specific grid.

**Supplier wholesale figures must remain in MCD-04 or the pricing engine. No commercial price appears in this document.**

---

## 5. Required Solara OS Workflow

**Shared family workflow:**
Select Perfect Fit family → select child product → select supplier → enter glass width/drop → record bead depth/type → select compatible bracket/clip → select frame colour → check handle/obstruction clearance → select packer/rebate/insert/shim/foam tape where supported → select product-specific configuration → select control system → validate supplier limits → apply price grid/surcharges → save survey/order record

**Product-specific control steps:**
- *Roller / Day & Night*: select chain or spring/tab only after supplier; select control side where applicable; validate frame-colour restrictions; validate child safety
- *Pleated / Cellular*: select Bottom Up or Top Down/Bottom Up; select supplier (Decora or Beverley — each with distinct frame-tier and fabric-collection rules); derive fabric price band; validate fabric-specific limits
- *Aluminium / Wooden Venetian*: select slat category; select slat colour; select wand side; select wand length
- *Shutter Lite*: calculate panel quantity; calculate panel widths; select tiltrod side; apply opposite-side rule where handle rebate requires it; validate multi-panel handle position; validate obstruction overlap; display non-blackout warning

---

## 6. Blocking Rules

System should block or refer where: no compatible supplier bracket/clip available; bead depth/type unsupported; glass width/drop outside selected supplier/product limit; chosen control incompatible with frame colour; handle cannot clear frame; rebate/insert cannot be manufactured at measured position; panel configuration places a central handle rebate across two panels; selected fabric exceeds its individual maximum drop; Konnect exceeds recommended product limit; wand side conflicts with obstruction; required handle-centre measurements missing; required side brackets/clips/midrail rules not satisfied; unsupported accessory selected; technical evidence missing.

**Additional, per this draft**: Pleated and Cellular now have real technical/pricing evidence from both Decora and Beverley (Pleated) or Decora alone (Cellular) — no longer blocked on zero extraction, but still blocked on full MCD-04 pricing transcription and, for Cellular, Beverley-specific evidence. Aluminium Venetian has real technical evidence but remains blocked on pricing extraction and the Standard/Special Frame confirmation for this specific product.

---

## 7. Warning Rules

Warnings should appear where: customer expects blackout performance; Shutter Lite opening will have visible light gaps; frame overlap may obstruct an air vent/handle; square-frame deduction guidance applies; more than one panel required; louvre alignment may differ between opening windows of different heights; handle not central; special slat colour affects lead time/price; Golden Oak frame removes chain-control availability on Decora Perfect Fit Roller; folding handle required for bi-fold application; two raise handles fitted because width exceeds supplier threshold; supplier-specific shim/foam-tape method in use; selected frame and component colours are not exact matches.

---

## 8. Evidence Status Summary

### Verified from uploaded Decora documents
- Perfect Fit Roller (SPEC07): frame, controls, tube, size limits, bracket counts, handle insert, frame/corner-cap/bracket colour mapping, real fabric list
- Perfect Fit Sunwood/Wooden Venetian (SPEC08): frame, size limits, control arrangement, wand side, handle options, slat data
- Perfect Fit Softshade/Day & Night (SPEC73): frame, chain control, tube, size limits, child-safety device, fabric-dependent drops, Konnect limit
- Perfect Fit Shutter Lite (SPEC42): dimensions, panel rules, louvre size, tiltrod, rebates, packer, bracket rules
- Perfect Fit Aluminium Collection (SPEC40): three systems (Free Hanging/Privacy/Glide), frame/corner/bracket data, full colour-coordination table
- **Perfect Fit Pleated/Cellular, Cruze range (SPEC70)**: full CZP11/CZP12 technical spec, Perfect Fit Profile dimensions, bracket codes, handle rules, profile-colour-to-frame mapping, both Softcell and Pleated Fabrics collections

### User-confirmed operational rules
- Roller and Day & Night may use chain or spring/tab depending on manufacturer
- Handle packers are 2mm and 6mm
- Handle rebate is an available frame option
- Frame colour must be selected
- Venetian slat colours grouped as Standard or Special
- Pleated, Cellular, Roller, Day & Night pricing driven by fabric price bands
- Venetian and Wooden Venetian require wand side and wand length
- Lite Shutters form part of the Perfect Fit family
- **Beverley manufactures Perfect Fit Roller, Pleated, and Aluminium Venetian in-house, sourcing fabrics/components from Decora, Louvolite, Eclipse (Roller) or Arena (Aluminium Venetian) rather than reselling a finished blind from those suppliers**
- **Standard/Special Frame is a real Beverley pricing tier for Roller and Pleated (Special = Golden Oak & Mahogany); strongly inferred, not yet confirmed, for Aluminium Venetian**

### Supplied Beverley evidence
- Shutter Lite pricing-grid structure, min/max dimensions, handle-rebate/split-tilt-bar surcharges, bracket sizes, bead/shim guidance, handle-measurement method, tilt side, multi-panel logic, overlap/obstruction rule, non-blackout/light-gap warning, clip quantity/side-clip rule
- Aluminium Venetian: real, separate Perfect Fit price list distinct from Arena's direct trade pricing, Standard/Special Frame tiers, colour/finish specification
- Roller: real fabric-band tables (Louvolite/Decora/Eclipse), Standard/Special Frame pricing grids, Konnect/accessory pricing
- Pleated: real Standard/Special Frame pricing grids, frame-tier colour mapping, fabric collections (Iverea, Lexington)

---

## 9. Version History

| Version | Date | Change |
|---|---|---|
| v0.1 | 2 August 2026 | Initial family document drafted from Claude Handover v0.1. No new evidence added. Structure, shared layer, and seven child-product sections built entirely from handover content. Status remains Working Draft — Partially Verified. |
| v0.2 | 2 August 2026 | Part D (Aluminium Venetian) fully rewritten with real Decora SPEC40 and Arena technical evidence, replacing the previous "no evidence" state. Three discrepancies flagged, not resolved. |
| v0.3 | 2 August 2026 | Part D reordered: Arena (purchased via Beverley Blinds) confirmed as Solara's primary channel; Decora SPEC40 demoted to secondary/comparison evidence. New open question flagged on Beverley vs Arena pricing. |
| v0.4 | 2 August 2026 | Open pricing question resolved: Beverley has its own separate, genuinely distinct price list for Arena-manufactured Perfect Fit blinds, now recorded as Solara's real cost basis. New open item: Standard/Special Frame tiers and colour-range comparison. |
| **v0.5** | **2 August 2026** | **Part C (Pleated/Cellular) fully rewritten** with real Decora Perfect Fit technical evidence (SPEC70, "Cruze" range — CZP11/CZP12, Perfect Fit Profile, bracket codes, handle rules, both fabric collections) and real Beverley Perfect Fit Pleated evidence (Standard/Special Frame pricing, frame-tier mapping, fabric collections) gathered earlier in this session but not yet incorporated into v0.4. New **Decora vs Beverley Pleated comparison table** added (§C.5), matching the format already used for Shutter Lite. Manufacturing-relationship pattern (Beverley manufactures Roller, Pleated, and Aluminium Venetian in-house using third-party fabrics/components) now recorded at family level (§8) and applied consistently across Parts A, C, D. Part A (Roller) updated with real Beverley in-house evidence and the Decora frame/corner-cap/bracket colour table. Part D's Standard/Special Frame question reframed as a strong inference from the now-twice-confirmed convention, not an isolated open question. §3.5's fixing-hole convention updated to reflect Pleated/Cellular's confirmation of the drop-trigger rule, further isolating SPEC40's width-trigger as a likely inconsistency. Deliverable 2's structure tree (below) corrected — the stale "no supplier technical spec extracted" line for Aluminium Venetian, uncorrected through v0.4, is now fixed. Status remains Working Draft — Partially Verified. |

---
---

# Deliverable 2 — Proposed Child-Product Structure

```
MCD-01B-10 Perfect Fit Blinds Family
│
├── Family Layer (shared)
│   ├── Measurement rule (glass size)
│   ├── Frame colour
│   ├── Handle clearance / packers (2mm, 6mm)
│   ├── Handle rebate / handle insert
│   ├── Shared accessory catalogue
│   ├── Bracket/clip selection (bead depth) — drop-trigger convention confirmed across 5 Decora products
│   ├── Blocking rules (shared)
│   └── Warning rules (shared)
│
├── A — Perfect Fit Roller Blind
│   └── Decora evidence (verified) | Beverley evidence (verified, in-house manufactured) | other suppliers (gap)
│
├── B — Perfect Fit Day & Night Blind
│   └── Decora evidence (verified) | other suppliers (gap)
│
├── C — Perfect Fit Pleated Blind          ─┐
├── C — Perfect Fit Cellular Blind          ├─ separate products, shared structure only
│   └── Both: Decora evidence (verified, SPEC70/Cruze). Pleated additionally has Beverley evidence
│       (verified, in-house manufactured, Standard/Special Frame). Cellular: Beverley-specific
│       evidence still a gap
│
├── D — Perfect Fit Aluminium Venetian Blind
│   └── Arena evidence (verified, primary channel via Beverley) | Decora evidence (verified,
│       secondary/comparison) | Beverley's own Perfect Fit price list (verified, real cost basis)
│
├── E — Perfect Fit Wooden Venetian Blind
│   └── Decora/Sunwood evidence (verified) | other suppliers (gap)
│
└── F — Perfect Fit Lite Shutters
    └── Decora evidence (verified, strongest) + Beverley evidence (verified, screenshots only)
```

Pleated and Cellular are structurally identical in the tree (siblings under the family layer, sharing operating-style and pricing-structure patterns) but are explicitly **not merged** — each retains independent fabric, technical-limit, and supplier-restriction data.

---

# Deliverable 3 — Change Log (this revision, v0.4 → v0.5)

| # | Change | Source |
|---|---|---|
| 1 | Part C fully rewritten with real Decora SPEC70 (Cruze) Perfect Fit Pleated/Cellular technical spec — previously the single biggest unresolved evidence gap in the family | User-supplied SPEC70 PDF |
| 2 | Part C's earlier-gathered real Beverley Pleated evidence (Standard/Special Frame pricing, frame-tier mapping, fabric collections) — present in memory from earlier this session but never incorporated into v0.4 — now written into the document | User-supplied Beverley pricing screenshots (earlier this session) |
| 3 | New Decora vs Beverley Pleated comparison table added (§C.5), following the same format as the existing Shutter Lite comparison | Derived from the two evidence sets above |
| 4 | Part A (Roller) updated with real Beverley in-house-manufactured evidence (fabric bands from Louvolite/Decora/Eclipse, Standard/Special Frame pricing, Konnect pricing) and the Decora frame/corner-cap/bracket colour table from SPEC07 — both gathered earlier this session, not yet in v0.4 | User-supplied SPEC07 PDF and Beverley pricing screenshots |
| 5 | Family-wide fixing-hole convention (§3.5) updated: Pleated/Cellular's confirmation of the 1100mm-**drop** trigger further isolates SPEC40's Aluminium Venetian 1100mm-**width** trigger as a likely source inconsistency, not a genuine product difference — not resolved, just re-flagged with stronger evidence behind it | Cross-reference across SPEC07/SPEC08/SPEC42/SPEC73/SPEC70 |
| 6 | Part D's Standard/Special Frame open question reframed as a strong inference (not confirmation) now that the same convention has been independently confirmed twice elsewhere (Roller, Pleated) | Cross-reference, no new Aluminium-Venetian-specific evidence |
| 7 | Deliverable 2's structure tree corrected — the stale v0.1 line for Aluminium Venetian ("no supplier technical spec extracted") persisted uncorrected through v0.2, v0.3, and v0.4; fixed in this revision | Internal consistency fix |
| 8 | Manufacturing-relationship pattern (Beverley manufactures Roller, Pleated, and Aluminium Venetian in-house using third-party fabric/components rather than reselling a finished product) recorded at family level (§8) for the first time, having previously only appeared in scattered per-product notes | User-confirmed, gathered earlier this session |

No contradictions in the underlying evidence required resolution during this revision.

---

# Deliverable 4 — Evidence Matrix

| Product | Decora evidence | Beverley evidence | Other suppliers | Pricing extracted? |
|---|---|---|---|---|
| Roller | ✅ Verified (SPEC07) | ✅ Verified (fabric bands, Standard/Special Frame, Konnect pricing) | ❌ None | ❌ No |
| Day & Night | ✅ Verified (SPEC73) | ❌ None | ❌ None | ❌ No |
| Pleated | ✅ Verified (SPEC70/Cruze) | ✅ Verified (Standard/Special Frame, fabric collections) | ❌ None | ❌ No (structure known both sides) |
| Cellular | ✅ Verified (SPEC70/Cruze) | ❌ None (Beverley-specific evidence not yet supplied) | ❌ None | ❌ No |
| Aluminium Venetian | ✅ Verified (SPEC40, secondary) | ✅ Verified (Arena via Beverley, primary channel + own price list) | ✅ Verified (Arena) | ❌ No (structure known, values not transcribed) |
| Wooden Venetian | ✅ Verified (SPEC08, Sunwood) | ❌ None | ❌ None | ❌ No |
| Lite Shutters | ✅ Verified (SPEC42) | ⚠️ Screenshots only (pp.40–45), workbook not extracted | ❌ None | ❌ No (structure only) |

**Pleated is now among the most-evidenced products in the family** — real technical + pricing structure from both intended suppliers. **Day & Night and Wooden Venetian are now the weakest** — single-supplier evidence only, no Beverley data yet gathered for either.

---

# Deliverable 5 — Unresolved Questions

1. Which non-Decora, non-Beverley suppliers (if any) offer Perfect Fit Roller and Perfect Fit Day & Night, and what are their size/control limits?
2. Does any supplier offer a spring/tab Perfect Fit Day & Night system, as the family structure allows for but Decora doesn't evidence?
3. Does Beverley manufacture Perfect Fit Day & Night and Perfect Fit Wooden Venetian in-house too, following the same pattern confirmed for Roller, Pleated, and Aluminium Venetian? Not yet asked/confirmed.
4. Does Decora's Perfect Fit Pleated/Cellular (SPEC70) have its own Standard/Special Frame pricing tier, or is that purely a Beverley-specific structure? Not evidenced either way in SPEC70.
5. Does SPEC40's Privacy system genuinely use Grey corner caps where Free Hanging uses Tan, or is one a source error?
6. Does SPEC40's Aluminium Venetian genuinely trigger the third fixing hole at 1100mm width (not drop, as every other Decora Perfect Fit product now including Pleated/Cellular does) — a real product difference, or a source inconsistency?
7. Is the "Pleated Bottom Bar" colour set appearing in SPEC40's Glide section actually a Glide-system option, or a misplaced cross-reference from a different product spec?
8. What wand-length options exist for either Venetian product?
9. What is Beverley's full Shutter Lite technical picture (louvre size, midrail rule, max opening) beyond what the five screenshot pages showed?
10. Does Beverley's Standard/Special Frame tier (confirmed for Roller and Pleated) apply identically to Aluminium Venetian? Strongly inferred, not directly confirmed.
11. Is there Beverley-specific technical/pricing evidence for Cellular, distinct from Pleated?

---

# Deliverable 6 — Contradictions Found

**None identified within the newly-added SPEC70 evidence itself, and no new contradiction introduced against existing family evidence.** SPEC70's Perfect Fit fixing-hole trigger (1100mm drop) is fully consistent with every other Decora Perfect Fit product except SPEC40 — this strengthens, rather than creates, the existing flagged SPEC40 discrepancy (see Deliverable 5, item 6).

**Carried forward, unresolved from earlier revisions:**
1. Privacy system corner caps (SPEC40) are listed as White/Beige/Grey/Brown/Anthracite/Black, while Free Hanging (same document) lists White/Beige/Tan/Brown/Anthracite/Black — Grey vs. Tan, otherwise identical.
2. The third side-frame fixing hole for SPEC40 Aluminium Venetian is triggered by 1100mm **width**, while every other Decora Perfect Fit product evidenced across the family (Roller, Softshade, Sunwood, Shutter Lite, and now Pleated/Cellular) triggers it by 1100mm **drop** — five products now confirm drop, only Aluminium Venetian states width.
3. A "Pleated Bottom Bar" colour set appears within the Glide system's section of SPEC40, which is unexpected for a Venetian product — may be a genuine Glide-system component or a page-layout artifact carried over from a different product's spec sheet.

These need direct confirmation against the source PDF or with Decora before Aluminium Venetian is treated as fully reconciled.
