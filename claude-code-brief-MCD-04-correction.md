Update MCD-04.md only, on branch claude/mcd-04-structured-technical-value.
Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, or MCD-01B-03.

This corrects three gaps in the previous brief, where the underlying
data existed but was never actually transcribed into the brief text.

## 1. Supplier name and source document title

For every one of the 8 new Roman capability records added in the
previous pass (§7.2 through §7.9, or wherever they now sit), set the
Source Reference field to:

Supplier: Decora
Document: "SPEC46 - Roman and Curtain Specification - Issue V15.pdf"

Do not use "Not provided to Claude Code" any longer for these records
— replace that placeholder with the above in each Source Reference
field. Leave the pre-existing Vertical record (Louvolite) untouched.

The one exception: the "face fabric GSM — Not Provided" record should
keep its Evidence Status as "Not Provided" / "Supplier data required"
— that item is genuinely absent from the source document, not a
citation gap. Its Source Reference may still note that Decora/SPEC46
was checked and did not contain this figure, so the "not provided"
status itself is traceable to a real search rather than an unexplained
gap.

## 2. Rod/fold count tables — actual band boundaries, per construction

Replace the schema-pattern-only rod count entry (and add proper Roman
records for each construction) with these actual confirmed values,
Evidence Status: Supplier Confirmed, Source Reference as in Part 1.
Note the boundaries are NOT identical across all four constructions —
transcribe exactly as given, including the No-Drill variation:

Standard Headrail (also matches Cassette Headrail exactly):
Drop < 700mm: 2 rods/folds
Drop 701-1200mm: 3
Drop 1201-1600mm: 4
Drop 1601-2200mm: 5
Drop 2201-2800mm: 6
Drop 2801-3200mm: 7

Breakaway configuration: identical to Standard's table above.

No-Drill Headrail (boundaries differ slightly from Standard):
Drop < 700mm: 2
Drop 705-1200mm: 3
Drop 1205-1600mm: 4
Drop 1605-2200mm: 5
Drop 2205-2800mm: 6
Drop 2805-3200mm: 7

Create one Structured Technical Value entry per construction (Standard
and Cassette may share one entry if you note both Applies To values,
since their tables are identical; Breakaway likewise matches Standard;
No-Drill needs its own entry due to the differing boundaries).

## 3. Cord count tables — actual band boundaries, per construction

Same treatment. These do NOT all match the rod count tables above —
transcribe exactly:

Standard Headrail (also matches Cassette Headrail exactly):
Drop < 700mm: 2 cords
Drop 701-1200mm: 3
Drop 1201-1700mm: 4
Drop 1701-2200mm: 5
Drop 2201-2700mm: 6
Drop 2701-3000mm: 7

Breakaway configuration (differs from Standard's cord table — matches
the rod/fold boundaries instead, not the cord boundaries above):
Drop < 700mm: 2
Drop 701-1200mm: 3
Drop 1201-1600mm: 4
Drop 1601-2200mm: 5
Drop 2201-2800mm: 6
Drop 2801-3200mm: 7

No-Drill Headrail:
Drop < 700mm: 2
Drop 705-1200mm: 3
Drop 1205-1700mm: 4
Drop 1705-2200mm: 5
Drop 2205-2700mm: 6
Drop 2705-3000mm: 7

## 4. Chain-length formula — confirm as fact, not a grouping assumption

The previous brief asked you to "confirm from source whether identical"
for No-Drill and Cassette's chain formula, without supplying a source.
This is now confirmed directly: per Decora SPEC46, the chain-length
formula (installation height minus 1500mm, falling back to two-thirds
of blind drop when no installation height is given, 200mm minimum) is
identical across Standard, No-Drill, and Cassette Headrail. Only
Breakaway differs (installation height minus 600mm, same fallback and
minimum). Update the existing chain-length Structured Technical Value
entries so "Applies To" correctly lists Standard, No-Drill, and
Cassette together for the shared formula, with Breakaway as its own
separate entry — remove any "not independently verified" caveat on
this point, since it is now sourced.

## Verification

- Confirm all 8+ new Roman records now cite Decora / SPEC46 (except
  the genuinely-absent GSM item, which explains its own gap instead).
- Confirm rod count and cord count each have real band-boundary data,
  not schema-pattern-only placeholders, and confirm the No-Drill
  variation and the Breakaway cord-table difference are both preserved
  exactly as given above, not smoothed into one universal table.
- Confirm the chain-length entries no longer carry an "unverified"
  caveat for No-Drill/Cassette.
- Confirm no data was invented beyond what's given in this brief —
  where something here is still incomplete, retain "Not Provided"
  rather than fill the gap.
- git diff --stat origin/main shows only MCD-04.md changed.

Commit and push to the existing branch. Do not open a pull request or
merge.
