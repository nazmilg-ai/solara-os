Update MCD-01B-08B.md only, on branch
claude/mcd-01b-08b-side-guide-aluminium-venetian (base this off the
current tip of that branch, commit 93cb10f — do NOT branch from main).

Do not modify MCD-01A, MCD-01B-01 through MCD-01B-08A, or MCD-04.

---

## IMPORTANT — this task does NOT promote the document

Unlike every prior product ratification in this project, this task
must **not** change the Status line. MCD-01B-08B remains:

Status: Working Draft — Unverified

Do not set it to Approved Draft Baseline. Do not bump the version
beyond a research-stage increment. Do not prepare a Claude Code
implementation brief. The document stays open until the remaining
supplier evidence items and the ambiguous size boundary are resolved.

---

## 1. Ratify DR-01 — neutral document naming

Your neutral drafting is ratified. Update DR-01's status language from
"pending ratification" to "confirmed by Nazmil Ghany, 26 Jul 2026."
Preserve the existing reasoning; append this supporting confirmation
alongside it:

The governance document remains supplier-neutral: "Side-Guide
Window-Mounted Aluminium Venetian Blind." The research handover's
earlier instruction to place the supplier system name directly into
this neutral governance document as the advisor-facing product name is
**formally withdrawn** — it conflicted with the ratified
supplier-neutrality rule, with MCD-01B-08's ratified controlled-
reference precedent, and with MCD-01B-08A, which had already applied
that rule to this same supplier system. Two sibling variants of one
Construction Group cannot run opposite naming rules.

The following remain recordable in this document as verified product
requirements (this is what the withdrawn instruction was correctly
protecting, and it survives intact):

* the application must provide a distinct advisor-facing product name;
* the internal construction-system reference must not replace that
  familiar advisor-facing name in the sales or survey workflow;
* the actual supplier-facing and advisor-facing name strings belong in
  MCD-04, not in the neutral product specification.

Raised By: confirmed by Nazmil Ghany, 26 Jul 2026.

## 2. Ratify DR-03 — application context, not platform category

Your treatment is ratified. Update DR-03's status language the same
way, preserving existing reasoning and appending:

"Bi-Fold Door / [supplier system name]" is demoted from platform
category to application context, and does not define this product's
neutral platform classification. The document must distinguish:

* **Product:** aluminium Venetian blind
* **Construction Group:** side-guide window-mounted system
* **Application contexts:** bi-fold doors, tilt-and-turn windows, and
  other compatible glazed frames
* **Supplier or commercial family name:** managed separately in MCD-04

"Bi-Fold Door" describes an application, not the product's governing
category.

Raised By: confirmed by Nazmil Ghany, 26 Jul 2026.

Check §2/§3 and any classification table in the document for
consistency with this ratified distinction, and correct any wording
that still implies bi-fold-door application is a platform or family
classification rather than an application context.

## 3. Record open item 13's controlled treatment — it stays unresolved

Your finding is confirmed: the two supplier statements are not
logically equivalent, and the worked boundary example is correct.
Update the open item (and the corresponding Evidence Conflict Register
entry) to record this controlled treatment explicitly — it is a
**confirmed treatment of an unresolved question**, not a resolution of
the question itself:

Record the two supplier statements exactly as written, in endpoint
form only:

* a width of 1,500mm is only available up to a maximum drop of
  2,000mm;
* a drop of 2,300mm is only available up to a maximum width of
  1,300mm.

The broader interpreted rule (width above 1,300mm → maximum drop
2,000mm; drop above 2,000mm → maximum width 1,300mm) **must not be
implemented as verified logic**. It is a stricter reading than the
supplier's literal wording supports.

Retain the intermediate boundary region as unresolved pending supplier
clarification. That uncertain region is:

* width above 1,300mm and below 1,500mm, **and**
* drop above 2,000mm and below 2,300mm.

No automatic pass or fail rule may be inferred for that region without
further supplier evidence. Record this explicitly so a future
implementation pass cannot mistake the endpoint statements for a
complete rule set.

Raised By: treatment confirmed by Nazmil Ghany, 26 Jul 2026; the
underlying supplier ambiguity remains open.

## 4. Confirm DR-06 and DR-09 remain separate actions

Update both entries to record that they are confirmed as deliberate
cross-document review actions to be handled separately, not during
this work package — your decision not to apply them automatically was
correct:

* **DR-06** — the gasket-rule refinement's likely effect on
  MCD-01B-08A's own pending DR-07 must be handled as its own
  controlled review, not silently changed during 08B work.
* **DR-09** — the supplier-identity disclosure that would resolve a
  standing "Not Provided" field in MCD-04 §7.15 requires its own
  deliberate pass. The neutral product document must not expose
  supplier identities; MCD-04 may hold supplier-specific display names
  or mappings where operationally required, but that disclosure must
  remain governed and must not leak back into supplier-neutral
  documents.

Raised By: confirmed by Nazmil Ghany, 26 Jul 2026.

## 5. Version History

Add a version-history entry recording this ratification pass and,
explicitly, that the document was **not** promoted — naming the
reasons it remains open (the unresolved minimum-width conflict, the
unresolved coupled-restriction boundary region, the folding-handle and
handle-free availability questions, and the remaining Open Evidence
Register items). Use a research-stage version increment only (e.g.
0.1 → 0.2), not a promotion.

## Verification

* Confirm the Status line still reads "Working Draft — Unverified" and
  was not changed to Approved Draft Baseline.
* Confirm DR-01, DR-03, DR-06, and DR-09 read "confirmed by Nazmil
  Ghany, 26 Jul 2026" and no longer say "pending ratification."
* Confirm open item 13 records the endpoint-only treatment as
  confirmed, while the underlying supplier ambiguity is still recorded
  as open — these are two distinct statuses and must not be conflated.
* Confirm the uncertain boundary region is stated explicitly (width
  1,300-1,500mm and drop 2,000-2,300mm) with no inferred pass/fail
  rule.
* Confirm no supplier names, trademarks, product names, system names,
  or document codes were introduced anywhere in the document — full
  sweep, including the Decision Register and Version History.
* Confirm no implementation brief, validation logic, or code blocks
  were introduced.
* Confirm the folding-handle and handle-free options remain recorded
  as unavailable/unconfirmed.
* Confirm MCD-01A, MCD-01B-01 through MCD-01B-08A, and MCD-04 remain
  byte-for-byte unchanged.
* Commit and push to the existing branch. Do not open a pull request
  or merge.
