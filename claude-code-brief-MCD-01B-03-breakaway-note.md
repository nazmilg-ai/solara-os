Update MCD-01B-03.md only, on branch claude/mcd-01b-03-roman-blinds.
Do not modify MCD-01A, MCD-01B-01, MCD-01B-02, or MCD-04.

Decision Register entry #10 (Breakaway reclassification) is already
ratified. Add one clarifying sentence to its reasoning column — do not
alter the ratification status or any other text in the entry:

"Breakaway's dimensional limits (400x300mm to 2400x2500mm, a smaller
maximum than Standard's 350x250mm to 2600x4000mm) and its distinct
child-safety chain-length formula (installation height minus 600mm,
vs. Standard/No-Drill/Cassette's installation height minus 1500mm —
both falling back to two-thirds of blind drop when no installation
height is supplied, both with a 200mm minimum) do not reopen this
classification. These are configuration-dependent Supplier Capability
and Child Safety Engine parameters — the same kind of variation
Vertical's Control Mechanism selection already demonstrated at
Configured (MCD-01B-02 section 17) — not evidence of a different
underlying construction route."

Do not name the supplier or cite the source document by name in this
sentence — per this document's standing supplier-neutrality rule, use
"supplier technical documentation" if any attribution is needed.

Verify:
- The rest of entry #10 is unchanged.
- No supplier names introduced anywhere in the document.
- git diff --stat main shows only MCD-01B-03.md changed, and the diff
  is small (one added sentence).

Commit and push to the existing branch. Do not open a pull request or
merge.
