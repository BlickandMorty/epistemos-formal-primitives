# epistemos-formal-primitives

This is the Lean work I did inside Epistemos, separated from the macOS app so the math can be read and checked on its own.

I am keeping both sides of it public:

- the declarations that already carry Lean proof terms
- the larger E1–E7, H1–H17, and PCF theorem candidates that still contain `sorry`

I do not want the unfinished claims to disappear, but I also do not want a candidate to look proved because it sits in a `.lean` file. [PROOF_STATUS.md](PROOF_STATUS.md) is the line I draw between them.

## Current source reality

- 247 theorem/lemma declarations
- 210 declarations with proof terms present
- 37 declarations whose body still contains `sorry`
- 0 explicit `axiom` declarations in the theorem source
- 48 Lean source files plus the Lake project

The proof-bearing work is concentrated in the EML, geometry, information, operator, scan, and tropical primitive modules and their generated certificate samples. E3 is also proof-bearing; E4 and E5 contain a mix of proofs and candidates.

## Build

The project pins Lean 4.16.0 and mathlib 4.16.0.

```text
lake update
lake build
```

`lake build` validates that the terms type-check. Lean permits `sorry` with a warning, which is why the separate status ledger matters.

## Provenance

Recovered from `BlickandMorty/Epistemos` at main commit `987f0a976`. The primitive IR Lean custody port landed in commit `ccd17bd5244c48bdc7b7f268e8d1a34770bd03d2` on 2026-05-30. The older theorem-canon specifications came through the May research/checkpoint branches.

## What “proof-term present” means here

It means Lean has a term for that declaration and the file does not discharge that declaration with `sorry`. It does not mean every surrounding research interpretation is automatically true, useful, novel, or empirically validated. Definitions and assumptions still matter, and I want reviews of those too.

