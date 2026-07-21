Update MCD-01B-07.md on branch claude/mcd-01b-07-pleated-cellular
(base this off the current tip of that branch, commit 86e4458 — do
NOT branch from main).

Do not modify MCD-01A, MCD-01B-01 through MCD-01B-06, or MCD-04.

---

## 1. Ratify the three classification entries

Locate the three Required Classification Question entries in the
Decision Register and update their status language from "pending
ratification by Nazmil Ghany" to "confirmed by Nazmil Ghany, 18 Jul
2026." Preserve the existing reasoning in each entry — append the
following supporting confirmation alongside it, the same way prior
ratifications in this project have preserved rather than replaced
existing analysis.

**Question 1 (Free-Hanging vs. Tensioned):** Ratified. They differ in
fundamental mechanical behaviour — Free-Hanging relies on gravity and
the lifting mechanism; Tensioned relies on continuous restraint
through cords, wires, springs, or equivalent components. That
difference affects suitability, fixing, controls, dimensions,
operation, and supplier eligibility, and therefore belongs at the
Construction layer.

**Question 2 (Bottom Up / TDBU / Dual-Fabric):** Ratified. These are
not merely advisor-selected settings applied to the same finished
mechanism — they materially alter rail arrangement, fabric layout,
number of moving components, control logic, manufacturing method,
supplier eligibility, and measurement/size restrictions. The rejected
comparison with Manual versus Motorised is correct: Manual and
Motorised describe how a compatible construction is operated; Bottom
Up, TDBU, and Dual-Fabric describe what is physically being
manufactured.

**Question 3 (Fixed Bottom Bar):** Ratified as reclassified. A fixed
bottom bar does not create a seventh independent construction family
— it modifies the lower fixing and movement arrangement of an
eligible Tensioned construction. Represent it as:

```
Bottom Bar Configuration
├── Moving Bottom Bar
└── Fixed Bottom Bar
```

Subject to supplier capability and construction eligibility. It must
not be offered where mechanically incompatible, including Tensioned
Dual-Fabric where the supplier configuration does not support it
(matching what §3's tree already shows as "not applicable" for that
combination).

## 2. Ratify the Shared Service Profile as originally concluded — do not alter it

Your original Shared Service Profile conclusion (all twelve services
Configured, including Validation Engine and Motor Engine) is correct
and is hereby ratified as originally written — do not change the
classification. Update the Decision Register entry's status language
from "pending ratification by Nazmil Ghany" to "confirmed by Nazmil
Ghany, 18 Jul 2026," and append the following supporting confirmation
alongside the existing reasoning:

**Validation Engine — Configured.** Pleated & Cellular has many
conditional rules, but those rules still operate through the existing
shared validation model: dimensions, area, construction eligibility,
fabric eligibility, control compatibility, and supplier capability.
Greater rule volume or more parameter combinations does not by itself
justify Extended.

**Motor Engine — Configured.** Motorisation varies by construction,
supplier, and configuration, but that is a normal capability-based
eligibility gate. Unsupported or unconfirmed combinations should be
blocked through supplier capability data. That does not make the
Motor Engine Restricted. Restricted should remain reserved for an
intentional Solara policy or business limitation imposed on an
otherwise technically available capability — not for supplier
variation, incomplete evidence, or combination-specific eligibility.

## 3. Log a standing governance clarification for future product reviews

Add a new Decision Register entry (not tied to any of the four above)
recording this as a general principle for all future product
specifications, not just this one:

Decision: The distinction between Configured and Restricted must be
applied consistently across product reviews. A high volume of
conditional rules, many dependencies, or eligibility that varies by
supplier/construction/configuration does not by itself justify
Extended or Restricted — this is parameterisation depth, which MCD-01A
§2 explicitly excludes from the Extended test. Restricted is reserved
specifically for an intentional Solara business policy or limitation
imposed on a capability the platform or supplier could otherwise
provide — not for ordinary supplier variation, incomplete evidence, or
combination-specific eligibility gating. Raised By: Nazmil Ghany,
following a reconsideration during MCD-01B-07's ratification review,
where an initial Validation Engine (Extended) / Motor Engine
(Restricted) proposal was reconsidered against Claude Code's own
tested conclusion and this project's established precedent, and
corrected to Configured/Configured for both.

## 4. Final open-item check

Review the full Decision Register. Confirm every entry is now either
resolved (including the four ratified above) or is a genuine
supplier-data gap — not an unresolved architectural or business
decision. Expected remaining open items are supplier-data gaps only:
whether "Fixed Bottom Bar" remains the final neutral term; unconfirmed
neutral-construction mappings for the named alias terms and product
codes; unconfirmed motorisation eligibility for specific combinations;
supplier control-side and Dual-Fabric fabric-order rules; current
lead times, warranties, and pricing; and the standing MCD-00A
dependency note. If anything else reads as an open architectural or
business question, flag it and do not promote — report exactly what's
blocking promotion instead.

## 5. Promotion

If the check in Part 4 confirms no other open architectural/business
item remains: update Status from "Working Draft — Unverified" to
"Approved Draft Baseline – Product Specification", set Version to
1.1, and add a version-history entry naming the remaining open items
by content, matching the standard set by every prior product in this
project.

## Verification

* Confirm all four ratified entries (three classification questions
  plus the Shared Service Profile) read "confirmed by Nazmil Ghany, 18
  Jul 2026" and no longer say "pending ratification."
* Confirm the Shared Service Profile table and all twelve rows'
  classifications are unchanged from the original draft (all
  Configured) — this task ratifies the existing conclusion, it does
  not alter it.
* Confirm the new standing governance entry (Part 3) is present as its
  own Decision Register entry, distinct from the four ratifications.
* Confirm the promotion decision matches what Part 4's check actually
  found.
* Confirm no supplier names, trademarks, product names, or part
  numbers were introduced anywhere in the document.
* Confirm MCD-01A, MCD-01B-01 through MCD-01B-06, and MCD-04 remain
  unmodified.
* Commit and push to the existing branch. Do not open a pull request
  or merge — that remains a manual step.
