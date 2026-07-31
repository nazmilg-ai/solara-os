# Decora Softshade & Roller Pricing Extraction Report

**Scope:** Decora only, per instruction ("complete Decora before moving to Arena or Beverley"). Covers the six named files. Report only — **MCD-04 has not been modified.** MCD-01B-09 has not been modified.

**Method:** Every file opened directly with `openpyxl` (both `data_only=True` for cached values and `data_only=False` for formulas), workbook structure inspected directly — sheet names, merged-cell ranges, row/column positions, explicit "WIDTH"/"DROP" header labels, full-grid blank-cell scans, document metadata, and a full-text search across every populated cell in every sheet for supplier/motor/component keywords. No flattened text extraction was used.

---

## 0. Supplier-attribution caveat (read before using this report)

**The word "Decora" does not appear anywhere inside any of the six files** — not in cell content, not in document metadata (`creator`, `title`, `company`, `lastModifiedBy` all read "Unknown Creator" or a generic product title). Attribution to Decora rests entirely on:

- this task's own framing ("Continue with Decora only");
- the Summary sheet's account code (`BLIN418`), which is Solara's own trading account reference with whichever supplier issued the file, not a supplier name;
- naming correspondence with product/system terms already recorded in MCD-01B-09 §7.1/§7.2 ("Decora Essentials," "Cruze fascia hardware system").

This is circumstantial, not documentary, evidence of supplier identity. It should be treated as Confirmed Operational Knowledge at most, not as a source-document-confirmed fact, until an actual Decora-branded document is available. Recorded here rather than silently assumed.

---

## 1. Files inspected

| File | Sheets | Main sheet dimensions | Merged-cell count |
|---|---|---|---|
| `prime-softshade-open-system_2026-07-07-151219.xlsx` | Summary; Price Calculator Prime Softshad | A1:BD111 | 84 |
| `prime-softshade-closed-system_2026-07-07-151219.xlsx` | Summary; Price Calculator Prime Softshad | A1:BD111 | 84 |
| `premier-softshade_2026-07-07-151219.xlsx` | Summary; Price Calculator Premier Softsh | A1:BF111 | 39 |
| `prime-cruze-fascia-softshade-40mm-fascia_2026-07-07-151219.xlsx` | Summary; Price Calculator Prime Cruze Fa | A1:BF111 | 90 |
| `prime-cruze-fascia-softshade-70mm-fascia_2026-07-07-151219.xlsx` | Summary; Price Calculator Prime Cruze Fa | A1:BF111 | 90 |
| `prime-roller_2026-07-07-151219.xlsx` | Summary; Price Calculator Prime Roller | A1:BD111 | 90 |

**Note on scope boundary:** a seventh file, `cruze-fascia-softshade-40mm-fascia_2026-07-07-151219.xlsx` (no "prime-" prefix), also exists in the repo root and was **not** in this task's file list. A brief check shows it is a distinct workbook (`Price Calculator Cruze Fascia S...`, dimensions A1:BF139, its own Summary sheet listing five price bands A–E rather than three) — not a duplicate of the Prime Cruze Fascia file. It was not extracted in depth here, since it falls outside the six named files; flagged for a deliberate future pass rather than folded in as an assumption.

---

## 2. Structural pattern common to all six files

Every file follows the same two-sheet template:

- **Summary sheet**: titled "DISCOUNTED PRICE TABLES 2026," states `Account Code: BLIN418`, and lists each price-band product name with a flat **Discount %** (35% for every Softshade file; 5% for the Roller file).
- **Main sheet ("Price Calculator ...")**: one or more repeating price-band blocks, each with:
  - a title row naming the price range (e.g. "PRICE RANGE A");
  - a fabric/collection-name row (present in the Essentials and Roller files; **blank** in both Cruze Fascia files — see §6);
  - an explicit **`WIDTH`** label row with millimetre values across columns;
  - an explicit **`DROP`** label column with millimetre values down rows;
  - a rectangular price grid at the intersections.
- Each block is duplicated twice, side by side: a **`DISCOUNTED COST`** block (left) and a **`SUGGESTED SELL PRICE`** block (right) — see §5 for why the right-hand block cannot be transcribed as-is.
- A small calculator area (`Account Code`, `Mark Up`, `VAT`, `Additional Charge`) feeds the `SUGGESTED SELL PRICE` block by formula.

**Width and drop orientation is unambiguous in every file and every block** — both axes carry explicit `WIDTH` and `DROP` text labels next to the actual header rows/columns, not inferred from position. No price was transcribed from any block where this was not the case; there were none.

**No blank cells / exclusion zones were found inside any priced grid** — every width×drop cell within each block's stated range is populated. This was checked cell-by-cell for all 14 price-band blocks across the six files (0 holes in each).

All prices are in GBP (confirmed by the `£` symbol on the `Additional Charge` field; no explicit currency number format is set — cells use `General`).

---

## 3. Per-file extraction

### 3.1 `prime-softshade-open-system_2026-07-07-151219.xlsx`

- **Sheet:** `Price Calculator Prime Softshad`
- **Product/system represented:** "Prime Softshade - Open System" (three price bands)
- **Price bands:** A ("Luna"), B ("Rift"), D ("Kanza, Nobis")
- **Width axis:** confirmed, columns, 300–2300mm, 100mm steps (21 points)
- **Drop axis:** confirmed, rows, 1000–2300mm, 100mm steps (14 points)
- **Min/max priced dimensions:** 300×1000mm to 2300×2300mm, all three bands
- **Increment structure:** uniform 100mm steps, both axes
- **Surcharges/additions:** none found in this file
- **Exclusions/blank-cell rules:** none — full rectangular grid
- **Wholesale or SSP:** `DISCOUNTED COST` block = wholesale (Solara's discounted cost, 35% off an undisclosed list price). `SUGGESTED SELL PRICE` block = see §5 — not a usable value as cached.
- **Motor/accessory or blind-only:** blind-only; no motor/component content anywhere
- **Conflict with MCD-01B-09:** MCD-01B-09 §7.1 states Open cassette max drop = **1,900mm**; this pricing grid prices Open System up to **2,300mm** drop — a genuine conflict, not resolved here (see §7). Pricing-grid minimum width (300mm) is below the tech spec's stated 350mm minimum; pricing-grid minimum drop (1000mm) is above the tech spec's stated 500mm minimum. Per this project's standing discipline, a pricing grid's own start/end points are not assumed to equal true technical manufacturing limits in either direction.

### 3.2 `prime-softshade-closed-system_2026-07-07-151219.xlsx`

- **Sheet:** `Price Calculator Prime Softshad`
- **Product/system represented:** "Prime Softshade - Closed System" (three price bands)
- **Price bands:** A ("Luna"), B ("Rift"), D ("Kanza, Nobis") — identical fabric names to the Open System file
- **Width axis:** confirmed, columns, 300–2300mm, 100mm steps (21 points)
- **Drop axis:** confirmed, rows, 1000–2300mm, 100mm steps (14 points)
- **Min/max priced dimensions:** 300×1000mm to 2300×2300mm, all three bands
- **Increment structure:** uniform 100mm steps, both axes
- **Surcharges/additions:** none found
- **Exclusions/blank-cell rules:** none — full rectangular grid
- **Wholesale or SSP:** `DISCOUNTED COST` = wholesale; `SUGGESTED SELL PRICE` — see §5
- **Motor/accessory or blind-only:** blind-only
- **Conflict with MCD-01B-09:** matches MCD-01B-09 §7.1's Closed cassette max drop (2,300mm) exactly. Same width/drop pricing-grid-vs-technical-minimum gap as §3.1 (300mm/1000mm pricing start vs 350mm/500mm technical minimum stated in the spec).

### 3.3 `premier-softshade_2026-07-07-151219.xlsx`

- **Sheet:** `Price Calculator Premier Softsh`
- **Product/system represented:** "Premier Softshade" — **only one price band**, unlike every other Softshade file
- **Price bands:** A ("Luna") only. (Summary sheet actually labels this product "Fascia Softshade - A," not "Premier Softshade - A" — an internal naming inconsistency between the Summary tab and the main sheet's own title, noted but not resolved.)
- **Width axis:** confirmed, columns, 300–2500mm, 100mm steps (23 points)
- **Drop axis:** confirmed, rows, 1000–3000mm, 100mm steps (21 points)
- **Min/max priced dimensions:** 300×1000mm to 2500×3000mm
- **Increment structure:** uniform 100mm steps, both axes
- **Surcharges/additions:** none found
- **Exclusions/blank-cell rules:** none — full rectangular grid
- **Wholesale or SSP:** `DISCOUNTED COST` = wholesale; `SUGGESTED SELL PRICE` — see §5
- **Motor/accessory or blind-only:** blind-only
- **Conflict with MCD-01B-09 / open question:** the Summary tab's own label ("Fascia Softshade") suggests this file may represent the same "Cruze fascia hardware system" described in MCD-01B-09 §7.2 (general range stated there: 200–2,500mm width, 500–3,000mm drop) — its 2,500mm width and 3,000mm drop maxima match that spec's stated maxima exactly. **However, this cannot be safely equated with the "Prime Cruze Fascia Softshade" files (§3.4–3.5 below)**, which represent a materially different, narrower pricing grid (2,500mm width but only 2,500mm drop, three price bands not one, and explicit "Cruze Fascia" naming this file lacks). Whether "Premier Softshade" is: (a) the same underlying system as "Prime Cruze Fascia Softshade" under an older/different commercial tier name, (b) a distinct commercial product not yet described anywhere in MCD-01B-09, or (c) superseded by the Prime-tier files, is **not resolved by anything in the files themselves** and must not be assumed either way before MCD-04 population.

### 3.4 `prime-cruze-fascia-softshade-40mm-fascia_2026-07-07-151219.xlsx`

- **Sheet:** `Price Calculator Prime Cruze Fa`
- **Product/system represented:** "Prime Cruze Fascia Softshade - 40mm Fascia" (three price bands)
- **Price bands:** A, B, D — **fabric/collection names are blank for all three bands** (the merged cell that carries the fabric name in every other file, e.g. `C12:Z12`, exists here but contains no value). This was checked directly against the merged-cell range, not inferred from a missing label.
- **Width axis:** confirmed, columns, 300–2500mm, 100mm steps (23 points)
- **Drop axis:** confirmed, rows, 1000–2500mm, 100mm steps (16 points)
- **Min/max priced dimensions:** 300×1000mm to 2500×2500mm, all three bands
- **Increment structure:** uniform 100mm steps, both axes
- **Surcharges/additions:** none found (no separate line for 32mm-vs-40mm-tube surcharge, bracket type, or colour — the "40mm Fascia" distinction is expressed only by this being a separate file from the 70mm variant)
- **Exclusions/blank-cell rules:** none in the price grid — full rectangle. (The fabric-name blank above is a genuine data gap, not a grid exclusion.)
- **Wholesale or SSP:** `DISCOUNTED COST` = wholesale; `SUGGESTED SELL PRICE` — see §5
- **Motor/accessory or blind-only:** blind-only
- **Conflict with MCD-01B-09:** MCD-01B-09 §7.2 states the fascia system's general verified max drop as 3,000mm; this specific 40mm-fascia pricing grid only prices to 2,500mm drop. Not necessarily a contradiction (§7.2's figure is stated as a general range, possibly reflecting a different fascia width or the "Premier"/"Fascia Softshade" file in §3.3), but the two documents do not agree on a single number and this is flagged rather than reconciled by assumption.

### 3.5 `prime-cruze-fascia-softshade-70mm-fascia_2026-07-07-151219.xlsx`

- **Sheet:** `Price Calculator Prime Cruze Fa`
- **Product/system represented:** "Prime Cruze Fascia Softshade - 70mm Fascia" (three price bands)
- **Price bands:** A, B, D — fabric/collection names blank, identical situation to §3.4
- **Width axis:** confirmed, columns, 300–2500mm, 100mm steps (23 points)
- **Drop axis:** confirmed, rows, 1000–2500mm, 100mm steps (16 points)
- **Min/max priced dimensions:** 300×1000mm to 2500×2500mm, all three bands
- **Increment structure:** uniform 100mm steps, both axes
- **Surcharges/additions:** none found
- **Exclusions/blank-cell rules:** none — full rectangular grid
- **Wholesale or SSP:** `DISCOUNTED COST` = wholesale; `SUGGESTED SELL PRICE` — see §5
- **Motor/accessory or blind-only:** blind-only
- **Conflict with MCD-01B-09:** same drop-maximum discrepancy as §3.4 (2,500mm priced vs 3,000mm general figure in §7.2). Prices in this file are consistently higher than the 40mm-fascia file at every matching width/drop/band combination, consistent with 70mm fascia being a heavier/larger hardware option — this is an internally consistent relationship, not a conflict.

### 3.6 `prime-roller_2026-07-07-151219.xlsx`

- **Sheet:** `Price Calculator Prime Roller`
- **Product/system represented:** "Prime Roller" (four price bands) — this is the plain Roller Blind product, not Day & Night/Softshade
- **Price bands:** AA ("Scope"), A ("Splash, Nico"), C ("Bella"), AB ("Como")
- **Width axis:** confirmed, columns, **610–2800mm, irregular (non-100mm) steps**: 610, 762, 914, 1067, 1219, 1376, 1524, 1676, 1829, 1981, 2134, 2438, 2800 (13 points)
- **Drop axis:** confirmed, rows, **610–2438mm, a different and shorter set than the width axis**: 610, 762, 914, 1067, 1219, 1524, 1829, 2134, 2438 (9 points — note 1376mm, 1676mm, and 1981mm appear as width breakpoints but are *not* offered as drop breakpoints, and 2800mm is not offered as a drop breakpoint at all)
- **Min/max priced dimensions:** 610×610mm to 2800×2438mm, all four bands
- **Increment structure:** non-uniform; most values are close to (but not exactly) 25.4mm-multiples of round inch sizes — this was checked and is not a clean fit (e.g. 1376mm does not equal 54″ exactly, and 2800mm does not equal 110″ exactly), so an imperial-origin theory is **not asserted** here, only the raw mm breakpoints are reported
- **Surcharges/additions:** none found
- **Exclusions/blank-cell rules:** none — full rectangular grid for all four bands
- **Wholesale or SSP:** `DISCOUNTED COST` = wholesale (5% discount, per the Summary sheet — notably a much smaller discount than every Softshade file's 35%, itself worth flagging as a real commercial difference, not an error); `SUGGESTED SELL PRICE` — see §5
- **Motor/accessory or blind-only: blind-only. This file contains NO motor or accessory pricing.** See §4 for the full explicit check.
- **Conflict with MCD-01B-09:** MCD-01B-09 does not yet contain Decora Roller Blind technical dimensional limits to compare against (its scope is the Day & Night Blind); no conflict to report on that basis. No conflict found regarding motorisation architecture — the absence of motor pricing here is consistent with, not contrary to, §4.2a's own statement that motor pricing may live in "a wholesale components section, a dedicated motorisation section, or a separate motor price list" other than the finished-blind file — it simply establishes that *this particular* Roller file is not that place, for Decora.

---

## 4. Motor pricing check — explicit result

**None of the six files contain any motor, tube, barrel, crown/adaptor, remote, charger, hub, or control pricing or reference of any kind.**

This was checked, not assumed: every cell in every sheet of all six files (Summary and main sheet) was searched for the case-insensitive substrings `stelor`, `somfy`, `motor`, `tube`, `barrel`, `crown`, `adaptor`, `adapter`, `remote`, `charger`, `hub`, `battery`, `wired`, `mains`, `wireless`, `control`, and `chain`. Zero matches across all six files, including `prime-roller_2026-07-07-151219.xlsx`.

This means the Beverley precedent (§9.2 of MCD-01B-09: motor pricing lives in Beverley's Roller-section file) **does not hold for Decora on the evidence of these six files.** The Prime Roller file was checked specifically for this purpose, per the task's instruction, and does not contain Stelor or Somfy component pricing. Per MCD-01B-09 §4.2a's own governing rule, this is recorded as a checked absence in these six documents, not proof that no such Decora Stelor/Somfy price list exists anywhere — it simply establishes that it is not in any of the six files reviewed here. A dedicated Decora motor/component price list (if one exists) has not yet been supplied and remains an open evidence item, consistent with MCD-01B-09 §27's existing "Decora current Softshade motor-order mapping" and "current Somfy model mapping for Decora" open items — neither is resolved by this pass.

---

## 5. The "SUGGESTED SELL PRICE" columns are not usable as-is, and are not an independent supplier RRP

This applies identically to all six files and is important enough to state once, centrally, rather than repeat six times.

**What the sheet's own header claims:** each `DISCOUNTED COST` block is mirrored by a `SUGGESTED SELL PRICE` block, headed as if it were an independent, supplier-published recommended retail price.

**What it actually is, on inspection of the formulas (not just the cached values):** every `SUGGESTED SELL PRICE` cell is a live formula of the shape

```
=ROUND(<discounted cost>*(1+<VAT>)*(1+<Mark Up>)+<Additional Charge>,2)
```

where `VAT`, `Mark Up`, and `Additional Charge` are **editable input cells** in the same sheet (currently defaulted, identically, to `VAT: 20%`, `Mark Up: 100.00%`, `Additional Charge: £0` in every one of the six files — confirmed by direct inspection, not sampling). These are exactly the kind of inputs that belong to **Solara's own mark-up and customer-selling-price logic**, not to a supplier-published suggested selling price. The `Account Code` field above them (`=Summary!$B$2`, i.e. `BLIN418`) is *not* actually referenced by the sell-price formula at all — it is informational only.

**The cached values are also wrong as they stand.** Every `SUGGESTED SELL PRICE` cell in every file currently displays the text `'0'`, not a computed number — this is a stale cached result left over from before the Mark Up/VAT/Additional Charge cells held their current values, not a recalculation. For example, `open-system` band A row 1: cost `28.41`, and the formula `=ROUND(28.41*(1+0.20)*(1+1.00)+0,2)` would evaluate to `68.18` if recalculated today, but the cell's stored cached value reads `'0'`.

**Conclusion for MCD-04 and the pricing engine:**
- The `DISCOUNTED COST` blocks are genuine, usable **supplier wholesale blind prices** (net of Decora's 35%/5% discount to Solara) and are the only numbers in these files safe to load into MCD-04 as such.
- The `SUGGESTED SELL PRICE` blocks must **not** be loaded into MCD-04 as a supplier-side price layer. They are, functionally, an embedded Solara mark-up calculator with placeholder default inputs, and their cached output is additionally stale/wrong. Nothing here has been transcribed as a "supplier suggested selling price."
- No genuine, independent supplier-published RRP/suggested-selling-price figure was found in any of the six files.

---

## 6. Summary of findings requiring a decision before MCD-04 population

1. **Supplier identity is not evidenced inside the files** — see §0.
2. **"Premier Softshade" vs "Prime Cruze Fascia Softshade" relationship is unresolved** — see §3.3. Do not assume they are the same product or that one supersedes the other.
3. **Fabric/collection names for the Cruze Fascia 40mm/70mm price bands (A/B/D) are blank** in the source files — see §3.4/§3.5. Cannot be populated into MCD-04 without another source.
4. **Open System pricing (to 2,300mm drop) exceeds MCD-01B-09's own stated Open cassette technical maximum (1,900mm)** — a genuine conflict between two already-recorded documents, not resolved here.
5. **Pricing-grid minimums (300mm width / 1000mm drop across the Essentials/Fascia files) do not match MCD-01B-09's stated technical minimums (350mm/500mm for Essentials; 200mm/500mm for the fascia system)** in either direction — treated as pricing-grid limits only, per this project's standing distinction between pricing evidence and verified technical manufacturing limits (the same distinction already applied to Beverley in §9.1 of MCD-01B-09).
6. **No motor/accessory pricing was found anywhere, including in the Roller file** — see §4. The Decora motor-pricing source remains unidentified and open.
7. **The "SUGGESTED SELL PRICE" columns must not be recorded as a supplier layer** — see §5.
8. **A seventh, non-"prime-" Cruze Fascia file exists in the repo root but was out of this task's scope** — see §1 note. Not extracted; flagged for a future, deliberate pass.

None of these were resolved by assumption. Recommend obtaining supplier confirmation (or the equivalent internal clarification) on items 2, 3, 4, and 6 before any of this data is written into MCD-04's Decora section.

---

## Verification

- All six named files were opened and inspected directly via `openpyxl`, not via flattened text extraction.
- Width and drop axes were confirmed via explicit in-sheet `WIDTH`/`DROP` labels for every price-band block in every file — no price was transcribed where orientation was ambiguous (none were found to be ambiguous).
- No "extracted, orientation to be confirmed" status was used anywhere in this report.
- Every price grid was checked cell-by-cell for blank/exclusion cells; none were found.
- Perfect Fit Softshade was not referenced or examined — out of scope for MCD-01B-09, per instruction.
- Motor/accessory pricing was checked explicitly and exhaustively (full-text search across every sheet, every cell, all six files) — none found in any file, including Prime Roller.
- Wholesale, supplier-suggested-sell, and Solara mark-up/customer-sell layers were kept analytically separate throughout — see §5 for why the sheet's own "SUGGESTED SELL PRICE" label does not correspond to that third layer.
- **MCD-04 was not modified.** **MCD-01B-09 was not modified — no commercial prices were added to it.**
- **Nothing was committed except this report file.** No pull request was opened.
