Update MCD-01B-08.md only, on branch claude/mcd-01b-08-family-architecture
(base this off the current tip of that branch, commit 5000d1a).

Do not modify MCD-01A or MCD-01B-01 through MCD-01B-07.

---

## Context — a new governance rule has been ratified

A standing governance rule has now been ratified for supplier-neutral
MCD-01B documents project-wide: "Perfect Fit" may appear as a
controlled referential label — naming an excluded product family,
cross-referencing a separately governed family, or recording a
historical scope/classification decision — but must never be used as
a neutral Construction Group, fixing method, capability classification,
source of technical rules, or substitute for a document's own neutral
title. This matches how MCD-01B-04, 05, 06, and 07 already use
"Perfect Fit Wooden Venetian," "Perfect Fit Metal Venetian," etc. —
that existing usage is confirmed correct and those four documents do
not need to be reopened or amended.

## 1. Replace "Perfect Fit-equivalent"

Your prior draft used "Perfect Fit-equivalent" in place of the bare
term, reasoning that the bare term might be too close to the
trademark. Under the now-ratified rule, this substitution is
unnecessary and actually less precise — it could incorrectly suggest
multiple mechanically equivalent systems have already been
established. Replace every instance of "Perfect Fit-equivalent" with
one of:

* Plain "Perfect Fit" — where a controlled reference to the named
  excluded/related family is actually necessary (e.g. in §4's
  exclusions list, referring to "specialist angled roof/side-window
  systems" that are Perfect Fit International-branded).
* The applicable neutral construction terminology — where no
  reference to the named family is actually necessary at all (e.g.
  "Full-Frame Bead-Mounted System," "Side-Guide Window-Mounted
  System," "Frame-Mounted Blind Systems").

Judge each occurrence on its own: if the sentence is naming/excluding
a recognised family, use "Perfect Fit." If it's describing this
document's own neutral architecture, use the neutral term instead —
do not default to "Perfect Fit" everywhere just because it's now
permitted somewhere.

## 2. Add the new Decision Register entry

Add this entry, verbatim, as its own Decision Register item (not
merged into any existing entry):

Decision: The term "Perfect Fit" may appear in supplier-neutral
MCD-01B documents solely as a controlled referential label for an
excluded, related, or separately governed product family. It must not
be used as a neutral Construction Group, fixing method, capability
classification, or source of technical rules.

Reason: preserves clarity when cross-referencing recognised product
families; aligns with established wording across four approved
specifications (MCD-01B-04, 05, 06, 07); avoids awkward or potentially
inaccurate substitutes such as "Perfect Fit-equivalent"; maintains the
substantive supplier-neutrality boundary by keeping ownership, exact
product identity, and capability in MCD-04.

Effect on existing documents: no amendments required — MCD-01B-04, 05,
06, and 07's existing "Perfect Fit [Product]" references already
satisfy this rule as excluded-family naming, confirmed rather than
treated as a prior inconsistency.

Raised By: confirmed by Nazmil Ghany, 19 Jul 2026.

## Verification

* Confirm no instance of "Perfect Fit-equivalent" remains anywhere in
  the document.
* Confirm every remaining use of "Perfect Fit" is a controlled
  referential use (naming an excluded/related family), never a
  Construction Group name, fixing method, or capability classification
  — spot-check each occurrence individually.
* Confirm the new Decision Register entry is present, distinct from
  other entries, and already marked confirmed (not pending
  ratification) — this is a ratified rule being recorded, not a new
  open question.
* Confirm no other content changed.
* Confirm MCD-01A and MCD-01B-01 through MCD-01B-07 remain unmodified.
* Commit and push to the existing branch. Do not open a pull request
  or merge — that remains a manual step.
