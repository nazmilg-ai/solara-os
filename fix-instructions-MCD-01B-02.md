MCD-01B-02.md contains a stale cross-reference left over from a section
renumbering. Several places in the body reference "§19" as if it were the
Decision Register, but the Decision Register is §23 — §19 is Recommendation
Rules. §24 Version History already correctly says "§23," confirming this is
a leftover from before Recommendation Rules, Supplier Capability
Requirements, and Product Configuration Summary were inserted and pushed
the Decision Register down.

Fix: in the six locations below, change the Decision Register reference
from §19 to §23. Do not change any other content, reasoning, or
classification in these passages — this is a reference-number correction
only.

1. §4 Louvre Width — "Shared Service Profile treatment" paragraph:
   "...logged in §19 Decision Register (Question A)."
   → "...logged in §23 Decision Register (Question A)."

2. §5 Shared Service Profile — Validation Engine row, final sentence of the
   Note:
   "...see §4 and §19 (Decision Register, Question A/B)."
   → "...see §4 and §23 (Decision Register, Question A/B)."

3. §5 Shared Service Profile — Supplier Capability Engine row, final
   sentence of the Note:
   "...deliberately not exposed in Sales MVP advisor workflow — see §4 and
   §19."
   → "...deliberately not exposed in Sales MVP advisor workflow — see §4 and
   §23."

4. §5 Shared Service Profile — Recommendation Engine row:
   "Vertical-specific recommendation rules (§19a/§19), all advisor-overridable"
   → "Vertical-specific recommendation rules (§19), all advisor-overridable"
   (This row's reference to Recommendation Rules itself is correct at §19 —
   only the stray "§19a/" fragment from the same renumbering should be
   removed.)

5. §6 Survey Requirements, Dynamic Configuration Workflow — Motorised
   bullet:
   "See §19 (Decision Register) for the open question on how draw is
   operated in this configuration."
   → "See §23 (Decision Register) for the open question on how draw is
   operated in this configuration."

6. §8 Validation Rules — "Deliberate business restriction" paragraph:
   "...not validated as an active option. See §4 and §19."
   → "...not validated as an active option. See §4 and §23."

7. §17 Child Safety — Chain/cord safety device mapping bullet:
   "...needs supplier/business data before technical design (see §19)."
   → "...needs supplier/business data before technical design (see §23)."

After making these seven corrections (six §19→§23 fixes plus the one
§19a/§19 cleanup), re-run a full-text search for "§19" across MCD-01B-02.md
to confirm the only remaining occurrence is the correct one in §5's
Recommendation Engine row and the Recommendation Rules heading itself
(## 19. Recommendation Rules). Commit to the same branch
(claude/mcd-01a-architecture-review-4fz4qd) with a commit message noting
this is a cross-reference correction only, no content or classification
change.
