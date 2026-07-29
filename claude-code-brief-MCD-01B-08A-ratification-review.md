# Claude Code Brief — MCD-01B-08A Ratification Review (Report Only)

Proceed with a controlled ratification review of:

**MCD-01B-08A — Side-Guide Window-Mounted Pleated & Cellular Blind**

Do not start a new product specification. Do not decide the numbering
of the Full-Frame Bead-Mounted variants — that is a separate later
task.

---

## IMPORTANT — this pass produces a report, not document changes

This task makes **no modifications to any document**. Produce a
decision-ready ratification report only. Do not edit MCD-01B-08A.md,
do not change its Status line, do not promote it, and do not modify
MCD-01B-08B.md, MCD-04.md, MCD-01A, or MCD-01B-01 through MCD-01B-08.

The report will be reviewed and the decisions explicitly approved
before any document is edited. A separate follow-up task will apply
the approved outcomes.

You may create the report as a new file on a branch (e.g.
`mcd-01b-08a-ratification-report.md` on a branch such as
`claude/mcd-01b-08a-ratification-review`), or deliver it as your
response — state which you have done. If you create a file, that file
is the only permitted addition; no existing document may change.

---

## Purpose

Review and, where the evidence supports it, recommend resolutions for
the four outstanding judgment decisions in MCD-01B-08A's Decision
Register:

* DR-06 — Visible Glass measurement
* DR-07 — Square-profile policy
* DR-12 — Motor Engine
* DR-13 — Full Shared Service Profile

Plus one open evidence item (profile colours) that may now be
resolvable.

---

## 1. DR-06 — Visible Glass measurement

Review the existing measurement terminology against the verified
Side-Guide construction evidence. Keep the governance document
supplier-neutral.

Separate clearly:

* the neutral measurement concept used by the product specification;
* supplier-specific ordering labels or field names;
* gasket or seal conditions that determine which measurement route is
  used.

Do not place supplier ordering terminology into the neutral product
layer unless it is explicitly classified as an external supplier
mapping.

## 2. DR-07 — Square-profile policy

MCD-01B-08B's own research produced a relevant finding: that less than
2mm of gasket protrusion onto the glass does not automatically fail
the survey, and may instead select an alternative measurement method.

**Do not automatically copy that finding into this specification.**
The two documents cover different blind technologies with different
supplier evidence bases. First determine whether MCD-01B-08A's own
supplier evidence independently supports the same treatment.

Classify the outcome as exactly one of:

* verified for both Side-Guide variants;
* verified only for the Aluminium Venetian variant (i.e. 08B);
* unresolved for Pleated & Cellular pending supplier confirmation.

If 08A's own evidence does not support the less-than-2mm alternative
measurement route, retain the matter as unresolved rather than
generalising from 08B. State plainly which evidence you relied on to
reach your classification.

## 3. Profile colours (open evidence item)

Check whether MCD-01B-08A's outstanding profile-colour open evidence
item is now fully resolved by the verified MCD-04 §7.15 enrichment.

Do not propose duplicating supplier names or commercial colour
mappings inside the neutral product specification. Where the item is
resolved only through an external supplier mapping, recommend
recording the governance requirement in the product specification and
citing the controlled mapping location (MCD-04) rather than
transcribing the values.

State whether the item is: fully resolved; partially resolved (and
what remains); or not resolved.

## 4. DR-12 — Motor Engine

Two distinct questions must be answered separately here. Do not
conflate them — this project has twice ratified that they are
different (MCD-01B-06's Evidence Status / Quoting Status two-field
model, and MCD-01B-07's standing governance rule that a
data-availability gate is Configured, not Restricted).

**(a) Motorisation availability — a product-capability evidence
question.** Determine, from the evidence, whether motorisation for
this construction is: available and advisor-selectable; available but
factory-selected; supplier-dependent; restricted to certain
configurations; or unsupported by the current evidence. Do not infer
availability from other Pleated, Cellular, or Full-Frame products.
Where evidence is insufficient, the correct outcome is that
motorisation availability remains Not Provided and quoting stays
disabled.

**(b) Motor Engine Shared Service status — an architectural
classification question.** This must use only the approved MCD-01A
vocabulary: Full, Configured, Extended, Restricted, Not Applicable,
Future. "Unresolved" is not a valid Shared Service status and must not
be assigned.

MCD-01B-08A's existing DR-12 already concluded **Configured**, having
tested that conclusion individually against each status definition
rather than by analogy, with the absence of motorisation evidence
recorded as an evidence gate rather than an SSP status change. Review
whether that reasoning still holds. If it does, recommend ratifying it
as-is. If you find a genuine defect in the reasoning, say so and
explain — but do not change the status merely because the underlying
*evidence* about motorisation availability is thin, since that is
question (a), not question (b).

If the DR-12 entry genuinely cannot be ratified on its current
reasoning, recommend leaving the **Decision Register entry** pending
ratification. That is different from, and must not be expressed as,
assigning an out-of-vocabulary Shared Service status.

## 5. DR-13 — Shared Service Profile

Review every Shared Platform Service individually. Do not assign a
complete service profile by analogy alone.

For each of the twelve services, provide:

* proposed status (using only: Full, Configured, Extended, Restricted,
  Not Applicable, Future);
* the evidence or governing precedent supporting it;
* whether the status is product-specific, construction-group-level, or
  inherited from the platform;
* any unresolved dependency.

## 6. Cross-variant consistency

Compare MCD-01B-08A and MCD-01B-08B **only at the shared Side-Guide
Construction Group level**. Do not assume a rule verified for one
variant automatically applies to the other.

Clearly separate, throughout your report:

* Construction Group principles (shared, inherited from MCD-01B-08);
* Pleated & Cellular variant rules (08A);
* Aluminium Venetian variant rules (08B);
* supplier-specific capabilities (MCD-04).

## 7. Report format

For each of the four decisions (and the profile-colour item), state:

* **Current wording** — quoted from the document as it stands;
* **Evidence reviewed** — which documents/sections, named specifically;
* **Recommended decision**;
* **Proposed replacement wording** — the exact text you would apply,
  if approved;
* **Confidence level** — and what would raise it;
* **Remaining open evidence**, if any.

Also report:

* any place where the evidence does not support a recommendation, and
  what specifically is missing;
* any inconsistency you find between 08A, 08B, MCD-01B-08, or MCD-04
  while reviewing — flagged, not fixed;
* confirmation that no document was modified during this pass.

## Verification

* Confirm no existing document was modified — MCD-01B-08A.md,
  MCD-01B-08B.md, MCD-04.md, MCD-01A, and MCD-01B-01 through
  MCD-01B-08 must all be byte-for-byte unchanged.
* Confirm no status was promoted or changed.
* Confirm the report does not introduce supplier names, trademarks,
  system names, or document codes into any proposed replacement
  wording intended for the neutral product specification.
* Confirm any proposed Shared Service status uses only the six
  approved MCD-01A values.
* If you created a report file, confirm it is the only file added.
* Do not open a pull request or merge.
