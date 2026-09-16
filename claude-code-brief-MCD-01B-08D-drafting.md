# Claude Code Brief — MCD-01B-08D Drafting

**Document:** MCD-01B-08D — Full-Frame Bead-Mounted Pleated & Cellular Blind
**Repository:** `nazmilg-ai/solara-os`
**Brief prepared:** 16 September 2026
**Direction confirmed by:** Nazmil Ghany (16 September 2026)

---

## 0. Controlling Instructions (read before anything else)

1. This brief has **two phases**. Carry out **Phase A only** first. Phase A is read-only: make no file changes, no commits, no branches and no pull requests. Report the Phase A results and **stop**. Begin Phase B only when Nazmil Ghany replies with the words **"Proceed to Phase B"**.
2. In Phase B, exactly **one file** is created: `MCD-01B-08D.md`. No other file in the repository may be created, modified, moved, renamed or deleted. That includes MCD-04, MCD-01B-10 research files, and this brief.
3. **Do not open a pull request and do not merge anything.** Push the branch and report. Merging happens only in a later, separately instructed step.
4. **Do not promote the document.** Its status stays `Working Draft — Partially Verified`, version `0.1`.
5. **Do not write code**, validation logic or implementation instructions.
6. **Supplier source documents are the final authority.** Section 5 lists figures carried in project records. If a source document says something different, the source wins: use the source figure and log the difference as an Open Evidence Item. Never silently "correct" either one.
7. **Never invent** dimensions, colours, compatibility, rules or prices. Anything not evidenced is recorded as `Not Provided` or as an Open Evidence Item.
8. **Supplier neutrality applies to the whole document**, including the Decision Register, Version History, Open Evidence Items and every meta-section. No supplier names, supplier brand or system names, supplier document numbers, product codes, fabric names or prices may appear anywhere. The one exception is the controlled-reference rule in Section 4.8.
9. MCD-00A is referenced but absent from the repository. Record it as the standard accepted missing-dependency note, as every other MCD-01B document does. Do not treat it as blocking.

---

## PHASE A — Read-Only Pre-Flight (no changes of any kind)

Run `git fetch origin` first so every check is made against the latest `origin/main`.

### A1. PR #23 status

In **`nazmilg-ai/solara-os`** only (PR numbers are repository-specific), report the current state of PR #23: open, closed or merged, its title, and its source branch.

Expected: this is the MCD-01B-08C pull request, which was superseded by a manual commit to main and should be **closed without merging**. **Do not close, merge or comment on it yourself.** Report only.

If the GitHub CLI or API is not available to you, say so plainly and do not guess.

### A2. MCD-04 Day & Night synchronisation check

Open the current MCD-04 file on `origin/main` and read the Day & Night sections (§7.16–§7.20, or wherever the Day & Night records now sit; report the actual section numbers). Report on each of the two items below as **Applied**, **Not Applied** or **Partially Applied**, and quote the relevant line numbers.

- **(a) Open vs Closed Cassette drop attribution.** The corrected position, per the supplier Essentials specification, is:
  - Open Cassette: width 350–2300 mm, drop 500–1900 mm.
  - Closed Cassette: width 350–2300 mm, drop 500–2300 mm.

  The earlier pricing-grid extraction attributed the 2300 mm figure to Open Cassette in error.
- **(b) Combined two-system semi-cassette figures.** Business decision: where the two fascia systems differ, use the more generous figure. The figures are:
  - drop 200–3000 mm
  - minimum control length 150 mm
  - minimum width 200 mm

  Also report whether MCD-04 records the separate decision that the **same child-safety device applies regardless of fascia system**.

**Do not edit MCD-04.** Report only.

### A3. Source evidence locations

Search the whole repository (all folders, including the root) and report the **exact paths** of:

1. The Route 1 Pleated & Cellular specification PDF, which covers the full-frame bead-mounted configurations. In project records this is the supplier's "SPEC70", Issue V7, 17/06/2026. Search for `SPEC70` and similar in filenames.
2. Route 2 evidence for its full-frame pleated range: price-list pages 35–39 and the specification page. This may be a PDF, screenshots, or `BeverleyBlinds-Master-2026.xlsx`. Search for `Beverley` and similar in filenames.
3. `research/perfect-fit-family/MCD-01B-10-working-draft-v0.5.md` (expected on main).
4. `MCD-01B-07.md`, `MCD-01B-08.md`, `MCD-01B-08A.md`, `MCD-01B-08C.md` and `MCD-01A.md` (or their actual filenames). Report the directory in which the MCD-01B product specifications live.

For anything you cannot find, state **"Not found"**. Do not substitute a similar file, and do not move or rename anything.

### A4. Clean-state checks

Report each of the following:

- **MCD-01B-08C.md** exists on `origin/main` with status `Approved Draft Baseline – Product Specification`, version `1.0`, and DR-02 recorded as ratified.
- **No filename collision:** no file named `MCD-01B-08D*` exists anywhere in the repository.
- **Identifier "MCD-01B-08D":** list every file where it already appears, with line numbers. "None" is an acceptable answer.
- **No branch collision:** no local or remote branch named `claude/mcd-01b-08d-full-frame-pleated-cellular` exists.
- **Stray paths:** no stray file or folder exists at a path beginning with `claude/` in the repository tree. The branch-name-as-path mis-filing happened before and must not recur.
- **Protected files:** list every tracked `.md` file on `origin/main` with its blob hash (`git ls-tree -r origin/main --name-only` plus hashes). This is the baseline for the "untouched" check in Phase B.

### A5. Phase A report format

Give one heading per check (A1–A4), each with a clear result. Finish with a short **"Blockers for Phase B"** list; write "None" if there are none. Then **stop and wait.**

---

## PHASE B — Draft MCD-01B-08D (only after "Proceed to Phase B")

### B1. Branch

```
git fetch origin
git checkout -b claude/mcd-01b-08d-full-frame-pleated-cellular origin/main
```

The branch must be created fresh from the latest `origin/main`, **after** this brief is on main. Confirm the starting commit hash in your report.

### B2. File

Create exactly one new file named `MCD-01B-08D.md`, in the **same directory as `MCD-01B-08C.md`** (as reported in A3).

The name is the file name only. Never use a branch name as a path.

### B3. Read before writing

Read these in full before drafting:

- **MCD-01A:** layering, the three-test classification, the twelve Shared Platform Services and the six-status Shared Service Profile.
- **MCD-01B-07:** the blind-technology base engine for Pleated & Cellular.
- **MCD-01B-08:** the family architecture, the Full-Frame Bead-Mounted Construction Group, the Organisational Role Schema, the Supplier Capability Engine and the controlled-reference rule.
- **MCD-01B-08A:** the sibling pattern for a Pleated & Cellular variant inside a Construction Group.
- **MCD-01B-08C:** the reference implementation for Full-Frame Bead-Mounted construction-layer conventions. **Mirror its section structure and its route-anonymisation convention.**
- **Source evidence:** the evidence found in A3, read page by page as images where tables are involved, not by text extraction alone.
- **Working draft:** `research/perfect-fit-family/MCD-01B-10-working-draft-v0.5.md`, Part C (Pleated/Cellular). This is **working evidence only, not an authority**.

---

## 4. Confirmed Architectural Direction (write each into the document)

Record 4.1–4.7 in the Decision Register as *"Confirmed by Nazmil Ghany, 16 Sep 2026 (pre-drafting direction)"*, **except** DR-01, which stays proposed.

### 4.1 Identity and numbering (DR-01: proposed, pending ratification)

- **Identifier:** `MCD-01B-08D`
- **Title:** `Full-Frame Bead-Mounted Pleated & Cellular Blind`
- **Header status:** `Working Draft — Partially Verified`
- **Version:** `0.1`
- **DR-01:** must carry `(pending ratification)`, following the same pattern MCD-01B-08C used before its ratification.

### 4.2 One document, two technologies kept distinct (DR-02)

Pleated and Cellular are covered in one document, consistent with MCD-01B-07 and MCD-01B-08A. They must stay technically distinct inside it:

- 20 mm pleat vs 25 mm cell
- separate fabric collections (referred to neutrally; no fabric names)
- any differing capability rules, stated per technology where the evidence differs

### 4.3 Inheritance chain (DR-03)

Use this exact wording:

> MCD-01B-08D inherits blind-technology rules from MCD-01B-07, family/construction-group rules from MCD-01B-08, and uses MCD-01B-08C as the reference implementation for Full-Frame Bead-Mounted construction-layer conventions.

Add an explicit statement that **Roller-specific rules in MCD-01B-08C do not transfer automatically**. Every rule carried over from 08C must be one that applies to the construction layer (frame, beading, brackets, fixing holes, handle packers, handle inserts, frame colour), not to roller-blind technology. Anything uncertain is logged, not assumed.

### 4.4 Bottom Up and Top Down Bottom Up (DR-04)

Bottom Up and Top Down Bottom Up are **Construction-layer capability**, consistent with the MCD-01B-07 ruling. They are not separate Blind Technologies and not separate Product Families. Apply the three-test classification and record the reasoning in the Decision Register.

### 4.5 Supplier capability envelopes are not merged (DR-05)

- Route 1 and Route 2 size and capability envelopes are recorded **independently**. The Supplier Capability Engine determines valid combinations.
- **No "most generous wins" rule applies.** The Day & Night (MCD-01B-09) treatment was a product-specific ruling and is **not** a project-wide precedent. Say this explicitly in DR-05.
- Follow the MCD-01B-08C convention: routes are identified only as **Route 1** and **Route 2**, and each figure is scoped to its route. The mapping of routes to named suppliers lives in MCD-04 only.
- **MCD-04 is not edited in this task.** In Open Evidence Items, log a follow-up: "MCD-04 enrichment for MCD-01B-08D Route 1 and Route 2 capability envelopes and commercial tiers — separate controlled task."

### 4.6 Frame tiers are commercial only (DR-06)

- **Frame Colour** is a mandatory selection field, separate from every other colour field: fabric, headrail/profile, bottom bar, corner cap, bracket, handle and handle insert.
- Route 2's Standard Frame / Special Frame distinction is recorded as a **commercial/pricing distinction belonging to MCD-04**. The neutral document states only that a route may apply commercial frame tiers, and that these do not change construction.
- If the evidence shows any **technical** difference between the tiers, log it as an Open Evidence Item. Do not classify it.

### 4.7 Motorisation (DR-07)

Motor Engine: **Not Provided**, as an evidence gate, not a status change. **Do not inherit** motorisation from free-hanging Pleated/Cellular (MCD-01B-07), from MCD-01B-08A, from MCD-01B-08C, or from any adjacent construction.

### 4.8 Naming governance (DR-12)

- The frame system's trademark may appear **only** as a controlled referential label, and only where MCD-01B-08 permits it: naming the related family, or cross-referencing MCD-04. It must **never** appear as the title, as a classification, or as a source of rules.
- **Preferred approach:** do not use it at all. MCD-01B-08C achieved zero occurrences.

---

## 5. Evidence to Incorporate

Verify every figure against the source. Source documents win.

### 5.1 Shared construction-layer facts (family level)

- **Mounting and measurement:** frame-mounted to the glazing bead without drilling the window frame; measured by glass size.
- **Handle packers:** 2 mm and 6 mm. The earlier 3 mm reference is **withdrawn** — carry this forward as withdrawn, as MCD-01B-08C did.
- **Family-wide items that are NOT evidenced and must not be assumed:**
  - universal bead-shape rules
  - universal bracket formula
  - universal handle-packer compatibility
  - universal deduction
  - universal frame-colour list
  - universal handle-rebate positions

### 5.2 Route 1 (expected figures)

**Two constructions:**

| Construction | Top profile | Bottom profile |
|---|---|---|
| Bottom Up | Standard | Reinforced |
| Top Down Bottom Up | Reinforced | Reinforced |

- **Control options:** Handle or No Handle, for both constructions.
- **Glass size limits:**
  - minimum width 200 mm
  - minimum drop 150 mm
  - maximum width 1500 mm
  - maximum drop 2300 mm
  - maximum area 3 m²
- **Construction-specific profile:** 38 mm wide × 26.4 mm high. This is distinct from the standard (22 × 16.4 mm) and reinforced (22 × 22 mm) profiles used on other constructions. Neutral wording only.
- **Frame:** aluminium, 7 colours — White, Beige, Anthracite, Brown, Golden Oak, Mahogany, Black. Verify the default colour against the source.
- **Clearance:** 25 mm required between handles/vents and glass.
- **Side-frame fixing holes:** 2 as standard, 3 when the drop is over 1100 mm (drop trigger).
- **Fixing brackets:**
  - 9 sizes, 18–38 mm
  - colours White, Brown, Anthracite, Black
  - quantity 4 up to 1100 mm drop, 6 from 1101–2300 mm drop
  - **product codes go to MCD-04 only — do not include them**
- **Control handle:**
  - standard handle in White, Black, Anthracite or Clear
  - folding handle available at a surcharge, Clear only (existence only; no price)
  - quantity: 1 per moving profile up to 1.2 m width, 2 over 1.2 m
  - supplied as handle plus insert
  - can be ordered with no handle
- **Handle insert:** 6 colours — White, Tan, Brown, Grey, Anthracite, Black. Position in the frame must be specified at order.
- **Profile-to-frame colour mapping:** recorded as **recommended matches, not exact matches**, as the source states.
  - Record the mapping in neutral form: profile colour → frame colour → corner colour.
  - Record the note that a beige frame is paired with a white profile, because there is no exact beige profile match.
  - Profile colour names that are supplier fabric or range names should be generalised or moved to MCD-04. Where you are unsure, log it.
- **Cords/ladders:** the closest colour to the fabric; white if no match.
- **Cell and pleat size:** 25 mm cell (Cellular) and 20 mm pleat (Pleated).

### 5.3 Route 2 (expected figures)

- **Build styles:** Standard, Dual Pull, Dual Meet. Record them **as the route names them**. See DR-09 (Section 6).
- **Size figures (the two sources may conflict):**
  - specification page: minimum width 80 mm, maximum width 1400 mm, maximum drop 2400 mm
  - pricing grid: width 400–1400 mm, drop 400–2400 mm

  The 80 mm specification minimum and the 400 mm pricing-grid start are different figures. Record them as **Technical Limit vs Priced Band**, following the MCD-01B-08C DR-07 convention. No stated technical minimum drop was found: record `Not Provided`, and note the priced-band start.
- **Headrail colours:** White, Silver, Black, Brown, Anthracite Grey, Tan.
- **Fixing brackets:** 9 sizes, 18–38 mm. Colours: White, Unpainted, Brown, Anthracite Grey, Black.
- **Window packing pieces:** 2 mm and 6 mm. The colour list in the source repeats "Brown". Record the colours as listed and log the duplicate as an Open Evidence Item.
- **Surcharge options that exist:** folding handle and handle rebate. Record **existence only; no amounts.**
- **Dual Pull / Dual Meet insert cost:** record only that an additional width-dependent component applies. No amounts.
- **Commercial frame tiers:** see 4.6. The tier-to-colour mapping belongs in MCD-04.
- **Manufacturing relationship:** Route 2 manufactures the finished blind in-house using fabric sourced from another organisation. Test this against the Organisational Role Schema; see DR-10 (Section 6).

### 5.4 Items that must be recorded but NOT resolved

These are Open Evidence Items (OEI):

1. **Route 2 nomenclature (DR-08).** Route 2 lists this range as "pleated". However:
   - at least one fabric in that range is listed by Route 1 as a **cellular** fabric
   - Route 2's related free-hanging page is headed as cell fabric only

   Whether Route 2's range is pleated, cellular or both is **unconfirmed**. Describe this neutrally, with no fabric names. **Do not reclassify.**
2. **Route 2 build-style mapping (DR-09).** Whether Standard = Bottom Up, and how Dual Pull and Dual Meet map to Bottom Up / Top Down Bottom Up, is **not evidenced**. Record no mapping; logic may not assume one.
3. **Route 2 packing-piece colour duplicate** (see 5.3).
4. **Route 2 technical minimum drop:** Not Provided.
5. **Tier nature:** whether Route 2's commercial frame tiers carry any technical difference.
6. **Profile-colour naming:** any profile-colour naming that could not be neutralised with confidence.
7. **MCD-04 enrichment:** the follow-up task from 4.5.
8. **Route 2 technical figures:** its bracket quantity rule, fixing-hole rule, handle quantity rule and clearance rule, if not found in its evidence. Record **Not Provided** for each; **do not borrow Route 1's figures**.
9. **Motorisation evidence:** none for either route.
10. **MCD-00A:** the missing-dependency note (standard, non-blocking).

---

## 6. Required Document Content

Mirror MCD-01B-08C's structure. The document must include at least the following.

1. **Header:** identifier, title, status, version, date, owner (Nazmil Ghany), and dependencies (MCD-00A [missing], MCD-01A, MCD-01B-07, MCD-01B-08, MCD-01B-08C, MCD-04).
2. **Purpose, scope and exclusions.**
   - **In scope:** full-frame bead-mounted Pleated and Cellular only.
   - **Excluded (cross-referenced):**
     - free-hanging and tensioned constructions → MCD-01B-07
     - side-guide window-mounted constructions → MCD-01B-08A
     - skylight / roof constructions
     - other full-frame products → MCD-01B-08C, and future siblings
3. **Inheritance statement:** the exact wording from 4.3, plus the non-transfer statement.
4. **Classification:** the three-test analysis for the product, for Bottom Up / Top Down Bottom Up, for control options (handle / no handle / folding handle) and for Route 2's build styles. Build styles are recorded as supplier-named options pending OEI 2.
5. **Pleated vs Cellular distinction section.**
6. **Measurement section:** glass size.
7. **Capability envelopes:** Route 1 and Route 2 separately, with Technical Limit and Priced Band labelled clearly.
8. **Construction-layer components:** frame, brackets, fixing holes, handle packers, handle inserts, clearance and profile.
9. **Colour fields:** each one a separate field, with Frame Colour mandatory, and the recommended mapping table.
10. **Controls:** handle, folding handle and no handle, per route, as evidenced.
11. **Organisational Role Schema application:** Route 1 and Route 2 role assignments, including the Route 2 multi-role test (DR-10).
12. **Supplier Capability Engine application:** how envelopes are resolved per route, with no merging.
13. **Shared Service Profile:** all twelve Shared Platform Services from MCD-01A, each with one of the six statuses and a justification. Motor Engine is recorded per 4.7.
    - Apply the MCD-01A definitions precisely.
    - **Restricted** means a deliberate whole-engine exclusion; a data-availability gate is **Configured**.
    - A high volume of rules is parameterisation. It is never, by itself, **Extended**.
14. **Open Evidence Items:** Section 5.4, plus anything new you find.
15. **Decision Register:** DR-01 to DR-12 as below, plus any additional judgement calls you make, each with reasoning written into the entry.

| DR | Subject | Status |
|---|---|---|
| DR-01 | Numbering and title | **Proposed (pending ratification)** |
| DR-02 | One document, two technologies | Confirmed (pre-drafting direction) |
| DR-03 | Inheritance chain and non-transfer of Roller rules | Confirmed |
| DR-04 | Bottom Up / Top Down Bottom Up as Construction-layer | Confirmed |
| DR-05 | Envelopes not merged; Day & Night ruling not a precedent | Confirmed |
| DR-06 | Frame tiers commercial only; Frame Colour mandatory and separate | Confirmed |
| DR-07 | Motorisation Not Provided, not inherited | Confirmed |
| DR-08 | Route 2 nomenclature (pleated vs cellular) | Open — recorded, not resolved |
| DR-09 | Route 2 build-style mapping | Open — recorded, not resolved |
| DR-10 | Route 2 multi-role Organisational Role Schema test | Claude Code judgement — **pending ratification** |
| DR-11 | Whether a cassette/enclosure construction applies (compare 08C DR-05: the frame is the enclosure) | Claude Code judgement — **pending ratification** |
| DR-12 | Naming governance and neutrality sweep result | Record the result |

16. **Version History:** v0.1 entry dated 16 Sep 2026.

**Cross-references:** every § reference must point to a section that actually exists in the cited document. MCD-01B-08C originally shipped with four broken references; do not repeat this.

---

## 7. Phase B Verification (run all checks before committing, and report each result)

### 7.1 Neutrality sweep

Run a case-insensitive, word-boundary search across the **entire** file, including the Decision Register, Version History and Open Evidence Items, for the following. Report the command used and the result. **The expected result is zero matches.** For each match, either remove it or justify it under 4.8.

- **Supplier and organisation names:**
  `Decora`, `Beverley`, `Arena`, `Louvolite`, `Eclipse`, `Home Creations`
- **Supplier brand, range and system names:**
  `Cruze`, `Softcell`, `Softshade`, `Perfect Fit`, `PerfectFit`, `FITtoFRAME`, `Alumitex`, `Konnect`
- **Document numbers and product codes:**
  `SPEC\d+`, `MEAS\d+`, `CZP\d+`, `PF\d{3}`
- **Price indicators:**
  `£`, `GBP`, `VFM`
- **Fabric names:**
  `Iverea`, `Lexington`, `Astoria`, `Artezen`, `Blenheim`, `Bowery`, `Hudson`, `Soho`, `Tribeca`

  Also search for any other fabric name present in the source fabric tables. **No fabric name of any kind may appear.**

### 7.2 Scope check

Run `git diff --stat origin/main...HEAD`. It must show **exactly one file added** (`MCD-01B-08D.md`) and nothing else.

### 7.3 Protected files

Every `.md` file listed in A4 must have an unchanged blob hash.

### 7.4 Path check

The new file sits in the same directory as `MCD-01B-08C.md`. No `claude/` path exists in the tree.

### 7.5 Cross-reference check

List every § reference in the document and confirm that each one resolves.

### 7.6 Decision Register completeness

Read **every row in full**; do not pattern-match one column. List which entries are Confirmed, which are Proposed/pending, and which are Open.

### 7.7 Status check

The header reads `Working Draft — Partially Verified`, version `0.1`, with no promotion language anywhere.

### 7.8 Evidence discipline

List every place where a source figure differed from Section 5, and how each was logged.

---

## 8. Commit and Push

```
git add MCD-01B-08D.md
git commit -m "MCD-01B-08D v0.1: draft Full-Frame Bead-Mounted Pleated & Cellular Blind (Working Draft, DR-01 pending ratification)"
git push -u origin claude/mcd-01b-08d-full-frame-pleated-cellular
```

**Do not open a pull request. Do not merge.**

---

## 9. Phase B Report Format

1. **Branch and commits:** branch name, starting commit hash, new commit hash.
2. **File location:** file path and line count.
3. **Checks:** results of checks 7.1–7.8, one heading each.
4. **Judgement calls:** a summary of every judgement call made (DR-10, DR-11 and any new entries), for ratification.
5. **Open Evidence Items:** the full list.
6. **Anything outside this brief:** anything you noticed but deliberately did not act on.

Then stop and wait for review.

---

*End of brief.*
