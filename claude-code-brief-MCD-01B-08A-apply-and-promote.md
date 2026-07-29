# Claude Code Brief — MCD-01B-08A: Apply Ratified Decisions and Promote

Work on the existing branch `claude/mcd-01b-08a-ratification-review`
(base off its current tip, commit `2da7dc8` — the branch already
carries the ratification report). Do not branch from main.

Modify **MCD-01B-08A.md only**. Do not modify MCD-01A, MCD-01B-01
through MCD-01B-08, MCD-01B-08B, or MCD-04.

---

## Context

All six recommendations in your ratification report are ratified by
Nazmil Ghany (29 Jul 2026). Apply them, run the verification checks,
and — only if those checks are clean — promote the document.

Use your report's own "Proposed replacement wording" for each decision
as the basis for the edits, adjusted where the ratification below adds
or refines wording.

---

## 1. DR-06 — Measurement service: ratified Configured

Keep the existing classification. Add the clarification, recording
that:

* the governance document records the neutral measurement concept;
* supplier ordering labels remain external mappings;
* supplier terminology must not replace the neutral platform
  terminology.

Update DR-06's status language to "confirmed by Nazmil Ghany, 29 Jul
2026."

## 2. DR-07 — Square-profile policy: ratified as unresolved for Pleated & Cellular

Do not transfer the sibling variant's interpretation into this
document. Retain the existing wording treating the 2mm requirement as
a conservative operational restriction, unchanged.

Append the cross-variant finding. Use this ratified wording as the
substance (integrate it with your report's proposed wording rather
than duplicating — the two say the same thing, so produce one clean
combined statement, not both):

> The Aluminium Venetian research does not independently resolve the
> Pleated & Cellular rule. The alternative measurement-route
> interpretation remains unconfirmed for both variants.

This wording matters: it must not upgrade the sibling variant's
provisional interpretation to verified status. Your report correctly
identified that the original three-way classification would have done
so — the ratified framing avoids it.

Update DR-07's status language to record that the **treatment** is
confirmed by Nazmil Ghany, 29 Jul 2026, while the **underlying
supplier question remains open**. These are two distinct statuses and
must not be conflated — the same discipline applied to MCD-01B-08B's
open item 13.

## 3. Profile colours: ratified as fully resolved

Close the open evidence item by citing the governed MCD-04 §7.15
mapping. Do not reproduce supplier names, colour values, or
supplier-specific mappings inside this neutral specification.

## 4. DR-12(a) — Motorisation availability: ratified Not Provided

Confirm motorisation availability remains **Not Provided**, with
quoting disabled. Record explicitly that this is a **checked absence
in the available evidence, not merely an unsearched gap** — both
source documents were specifically checked for motorisation content
during the 26 Jul 2026 enrichment pass and neither mentions it.

State that no advisor or quoting workflow should expose motorisation
for this product unless new supplier evidence is added.

## 5. DR-12(b) — Motor Engine service status: ratified Configured

Ratify as-is. Make the distinction explicit and durable in the
document, so a future reader cannot collapse the two:

* **product capability:** Not Provided;
* **shared service behaviour:** Configured — the shared Motor Engine
  is configured to suppress or disable motor options for this product.

State plainly that the Configured classification describes how the
shared Motor Engine behaves for this product when no supported motor
capability exists, and **does not imply that motorisation is
available**.

Update DR-12's status language to "confirmed by Nazmil Ghany, 29 Jul
2026."

## 6. DR-13 — Shared Service Profile: ratified, all twelve Configured

Apply the full twelve-service profile from your report. Each row must
be supported by MCD-01A architecture and must clearly distinguish:

* platform-service configuration;
* product capability;
* supplier evidence;
* unavailable or disabled options.

Validation Engine and Child Safety Engine remain Configured, provided
this does not imply the existence of unsupported product-specific
rules. Their configured behaviour may include applying known rules,
suppressing unsupported options, and preserving evidence gaps — state
this explicitly in those two rows, extending the same evidence-gap-
versus-status-change separation your report already applied.

Update DR-13's status language to "confirmed by Nazmil Ghany, 29 Jul
2026."

## 7. Cross-variant minimum-width observation — record, do not act on

The minimum-width difference is recorded but is **not** a conflict
within this document:

* this document (Pleated & Cellular): 200mm minimum width, confirmed
  by its own evidence;
* the sibling Aluminium Venetian variant: 200mm versus 250mm remains
  unresolved.

Different minimums may legitimately apply to different blind
technologies using the same broader Construction Group.

Accordingly:

* **Do not create a shared Side-Guide minimum width.**
* **Do not reopen or change this document's own 200mm figure** — it is
  confirmed by its own evidence and is not in question.
* **Do not modify the sibling variant's document** in this pass. The
  discrepancy is captured for that document's next supplier enquiry,
  which is a separate task.

## 8. Verification — must pass before promotion

Run these checks and report each result:

* MCD-01A, MCD-01B-01 through MCD-01B-08, MCD-01B-08B, and MCD-04 are
  byte-for-byte unchanged.
* Full supplier-neutrality sweep of MCD-01B-08A.md — zero supplier
  names, trademarks, system names, product names, colour values, or
  source-document codes anywhere, including the Decision Register,
  Open Evidence Items, and Version History.
* Every Shared Service status uses only the six approved MCD-01A
  values (Full, Configured, Extended, Restricted, Not Applicable,
  Future).
* DR-07 carries its two statuses distinctly (treatment confirmed;
  underlying supplier question open) and has not been collapsed into
  one.
* DR-12's (a) and (b) remain visibly separate, and nothing in the
  document implies motorisation is available.
* The profile-colour item is closed by citation, with no supplier
  values transcribed.

## 9. Promotion — only if §8 passes

Review the full Decision Register. Confirm every entry is either
resolved/ratified or is a genuine supplier-data gap or
confirmed-treatment-of-an-open-supplier-question — **not** an
unresolved architectural or business decision.

Note specifically: **DR-07's ratified state does not block promotion.**
Its treatment is confirmed; only the underlying supplier question is
open. That is structurally the same as the supplier-data gaps that
MCD-01B-01 (B5), MCD-01B-03, and others carried into their own
Approved Draft Baselines, and the same shape as MCD-01B-08B's open
item 13. It is a data gap, not an open architectural decision.

If that review confirms no unresolved architectural or business
decision remains: update Status from "Working Draft — Unverified" to
**"Approved Draft Baseline – Product Specification"**, set Version to
**1.0** (matching MCD-01B-08's own 0.1 → 1.0 promotion precedent), and
add a version-history entry naming the remaining open items **by
content**, not just by cross-reference — including that DR-07's
underlying supplier question and the motorisation-availability
evidence gap both remain open, alongside the other Open Evidence
Items.

If the review finds a genuine unresolved architectural or business
decision: do **not** promote. Report exactly what is blocking it
instead.

Commit and push to the existing branch. Do not open a pull request or
merge — that remains a manual step.
