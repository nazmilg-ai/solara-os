# Claude Code Brief — MCD-01B-04 / MCD-01B-05 Review and Redraft

## Branch

Create a new branch from current main: claude/mcd-01b-04-05-venetian-review

## Read before writing

* MCD-01A_v1.5_for_Claude_Code.md
* MCD-01B-01.md, MCD-01B-02.md, MCD-01B-03.md (structural and governance precedent — especially MCD-01B-03's §4a/§7a/§2 pattern of required documented reasoning before finalising a classification)
* MCD-04.md

Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, MCD-01B-03, or MCD-04 in this task except where instructed in Part 2 below.

---

## Context

Two working drafts exist as plain text (not yet committed to the repo): a Wooden Venetian Blinds specification and a Faux Wood Venetian Blinds specification. Both were written outside the established review process and self-declared "Approved Draft Baseline." Neither status is valid. Both are hereby downgraded to:

Status: Working Draft — Unverified

Attached as reference material for this task:
* mcd-01b-04-working-draft.md
* mcd-01b-05-working-draft.md

Treat these as source material to be corrected and verified, not as approved content to preserve unchanged.

---

## Part 1 — Create MCD-01B-04.md

Import the Wooden Venetian working draft as the starting point. It does not name suppliers or ranges directly and is structurally cleaner than the Faux Wood draft, but it is not yet approved. Apply the following before this can be considered for promotion:

### 1a. Add a Decision Register

Create a numbered Decision Register (Date | Decision | Reasoning | Raised By), matching the format used in MCD-01B-01/02/03. At minimum, log:
* the decision that Wooden Venetian is the Venetian-family reference implementation, and why;
* the decision that Perfect Fit Wooden Venetian is excluded from this specification;
* the reasoning for each Shared Service Profile classification (see 1c below) — this is the most important entry, do not summarise it away.

### 1b. Add Version History

Create a Version History section. v1.0 entry should honestly describe this as a working draft assembled from Decora Sunwood/Starwood/Timberlux research, pending independent review, cross-supplier verification (Arena, Beverley), and Decision Register ratification — not as a finished, evidenced baseline.

### 1c. Re-derive the Shared Service Profile — do not accept the existing table as given

The working draft marks all twelve Shared Platform Services "Configured" with no reasoning shown. Apply MCD-01A's actual test to each one and write out your reasoning in the Decision Register before finalising the table. Pay particular attention to:

* **Validation Service** — the draft's own §17 describes width/drop combination matrices, colour-level size restrictions, and conditional logic ("if width ≤ X then max drop Y"). Does representing this require the Validation Engine itself to gain new capability, or is this an ordinary parameterised use of dimension/compatibility rules the engine already provides (compare to how MCD-01B-02 handled Vertical's stack-width rules, and MCD-01B-03's own Configured conclusion for Roman's area/join validation)? Reach your own conclusion — do not assume Configured or Extended in advance.
* **Supplier Capability Engine** — the draft describes colour-specific dimensional restrictions, material-subtype-level resolution (Supplier → Range → Material Subtype → Construction Capability), and original-owner-versus-reseller separation (relevant once Arena's Infusion range, resold through Beverley, is added — see MCD-04). Does the existing schema already represent this, or does it need new capability?
* **Motor Engine** — does existing motor logic already support tilt-only versus tilt-and-lift selection and supplier eligibility checking (as demonstrated in MCD-01B-02's Vogue Motorised Tilt work), or does Wooden Venetian's width/drop/area/weight combination requirement (§15.3) require something new?
* **Recommendation Engine** — does the guidance in §28 (moisture, shallow recess, bedrooms, street-facing, large/heavy blinds) use only the existing advisor-overridable suggestion pattern already established in Roller/Vertical/Roman, or does it require new capability?

Reassess the remaining eight services on the same basis, even though they are less likely to change. Write the reasoning for all twelve, not just the four flagged above.

### 1d. Verify no supplier-specific facts have leaked into shared rules

Search the working draft for anything that states a specific number, name, or range as if it were universal Wooden Venetian behaviour rather than a Supplier Capability value. Known risk areas from the underlying research: tape widths (§12.2 lists 10mm/19mm/25mm/38mm as "known tape widths" — confirm this is presented as an illustrative, non-exhaustive list rather than an implied universal set, since Sunwood/Starwood/Timberlux each support different subsets); control-arrangement examples; any numeric example that reads like a specific supplier's real figure rather than a generic illustration.

### 1e. Confirm exclusions

Confirm the document correctly excludes Faux Wood, Metal Venetian, Perfect Fit Wooden Venetian, and Perfect Fit Metal Venetian, and that Perfect Fit is stated as a separate construction-system family per the existing project decision (recorded in prior chat context, not yet its own MCD document).

---

## Part 2 — Create MCD-01B-05.md

Import the Faux Wood Venetian working draft, but do NOT import it as-is. Section 41 of the working draft ("Beverley/Home Creations colour governance") is a supplier-neutrality violation and must be removed and replaced.

### 2a. Remove Section 41 entirely

Delete the section naming Beverley, Home Creations, Embassy, Forestwood, and all specific colour names (Honey, Pecan, Raven, Victoria Walnut, Antique Oak, Haze Grey, Anthracite, 35mm Mist, Pebble, Shadow Grey, Vanilla Essence, Fluid Pewter).

### 2b. Replace it with a supplier-neutral governance rule

In its place, state only the general principle (this may already be adequately covered by the draft's existing §13/§40 discontinued-colour language — check for duplication before adding a new section):

"Discontinued, limited-stock, and legacy colours must be excluded from standard quoting and customer-facing selection, even where they remain visible in a supplier portal for residual stock or remakes."

### 2c. Repeat 1a through 1e above for MCD-01B-05

Decision Register, Version History, re-derived Shared Service Profile with documented reasoning (apply the same four-service scrutiny as 1c, adjusted for Faux Wood specifics — e.g. colour-dependent size restrictions in §23 are a strong candidate for testing Validation Service and Supplier Capability Engine against the Extended threshold), verification that no supplier facts leaked into shared rules, confirmed exclusions (including the standing decision that Perfect Fit Faux Wood does not exist as a product).

### 2d. Confirm correct inheritance from MCD-01B-04

Confirm §4's "Relationship to the Venetian reference implementation" section accurately lists only concepts actually shared, and that genuine Faux Wood differences (PVC construction, moisture suitability, heat-deformation risk, colour-dependent size limits, narrower motorisation availability) are documented as differences rather than duplicated wholesale from MCD-01B-04.

---

## Part 3 — Update MCD-04.md with the Embassy colour provenance

Add a Supplier Capability Record (or extend an existing Beverley/Home Creations section if one exists) with the following, using the Structured Technical Value / evidence conventions already established in MCD-04:

Supplier: Beverley / Home Creations
Range: Embassy
Colour status: Discontinued
Colours: Pebble, Shadow Grey, Vanilla Essence, Fluid Pewter
Source: Home Creations portal bulletin
Evidence type: User-provided portal screenshot
Evidence date: 15 July 2026
Standard quoting: Disabled

Also add the active/discontinued Forestwood and Embassy data referenced in the working drafts (active Embassy: Honey, Pecan, Raven; discontinued Forestwood: Victoria Walnut, Antique Oak, Haze Grey, Anthracite, 35mm Mist) with the same evidence attribution — these came from the same source material and should carry the same provenance record, not be treated as more casually sourced than the discontinued Embassy colours.

Mark the following as "Evidence gathered — Extraction completed — Independent verification pending" rather than confirmed, since they have not been through the same independent-verification process as the Decora records: Arena Sherwood motorisation, Arena Expressions motorisation, Home Creations motor compatibility, colour-specific size restrictions, and any control/tape/motor rule derived from complex PDF tables referenced in the working drafts but not independently re-checked in this task.

---

## Verification

* Confirm MCD-01B-04.md and MCD-01B-05.md both carry Status: Working Draft — Unverified (not Approved Draft Baseline) after this task — this task does not promote either document, only prepares them for eventual review.
* Confirm zero supplier names, trademarks, or specific colour names appear anywhere in MCD-01B-05.md (full sweep, including any section not explicitly mentioned above) — grep for Beverley, Home Creations, Embassy, Forestwood, Decora, Arena, Somfy, and the twelve named colours.
* Confirm the same sweep on MCD-01B-04.md.
* Confirm both documents have a Decision Register and Version History section.
* Confirm the Shared Service Profile reasoning is written into each document's Decision Register, not only asserted as a table.
* Confirm MCD-04.md's new/updated records carry explicit evidence type and date, and that the "pending independent verification" items are marked as such rather than presented as confirmed.
* Confirm MCD-01A, MCD-01B-01, MCD-01B-02, and MCD-01B-03 remain unmodified.
* Report a diff summary for independent review.
* Commit and push to the new branch. Do not open a pull request or merge — both documents remain Working Draft pending explicit ratification of the Decision Register entries.
