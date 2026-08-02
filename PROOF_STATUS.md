# Proof status

This ledger was produced from the recovered Lean source at Epistemos main commit `987f0a976`.

## Declaration-level summary

| Status | Count | Meaning |
| --- | ---: | --- |
| Proof term present | 210 | The theorem/lemma declaration block contains no `sorry`; `lake build` is the type-checking gate. |
| Candidate | 37 | The declaration block contains `sorry` and is not claimed as proved. |

The source also contains `sorry` outside theorem/lemma blocks (for example umbrella or schema definitions), so a raw token count is larger than the candidate-declaration count. There are no explicit `axiom` declarations in this source tree.

## Candidate declarations

| Family | Declaration |
| --- | --- |
| E1 | `density_with_full_generators` |
| E2 | `sheaf_gluing_equals_kernel_of_coboundary` |
| E4 | `tsErrorTermSeparation` |
| E5 | `driftInflatesBound` |
| E5 | `mamba3IsSidecarNotTheorem` |
| E6 | `fiveFormalismsEmbedIntoEpiEpsilon` |
| E7 | `holds_within_ulp_bound` |
| H1 | `wbo7HoldsOperational` |
| H2 | `halfSoftmaxPostBoundedUlpDrift` |
| H2 | `babaiClosurePreserved` |
| H3 | `h3MonotonicityHolds` |
| H4 | `babaiRoundTripBounded` |
| H4 | `layerWiseErrorBoundTight` |
| H5 | `morphDslDeterministic` |
| H6 | `testTimeRegressionUnifiesFiveFamilies` |
| H7 | `evictionMonotonicityHolds` |
| H8 | `ospcSubstrateComplete` |
| H9 | `corticalPacketRuntimeExpressesE1ThroughE7` |
| H10 | `bilaminarMutexEnforced` |
| H11 | `spectralGapPositiveIffGlobalSectionAtMostOneDim` |
| H12 | `berryPhaseGaugeInvariant` |
| H13 | `klDivergenceEqualsHalfFisherQuadraticForm` |
| H14 | `localGlobalConjectureIsFalse` |
| H15 | `correctionImprovesConvergence` |
| H16 | `crtRouteUniquenessHolds` |
| H17 | `modernHopfieldExponentialCapacity` |
| H17 | `singleUpdateConverges` |
| PCF-1 | `reconstructionErrorVanishesAtGroundTruth` |
| PCF-2 | `qkDecompositionMatchesAtFrobenius1e5` |
| PCF-3 | `allEdgeWeightsInUnitInterval` |
| PCF-4 | `componentRouteSchemaIsFrozenUntilPcf1` |
| PCF-5 | `activeRankOneRecoversOutputNorm` |
| PCF-6 | `editSafetyBoundHolds` |
| PCF-7 | `dualMoreFaithfulThanEither` |
| PCF-8 | `spectralGapCorrelatesWithModularity` |
| PCF-9 | `distilledModelWithinDriftBudget` |
| PCF-10 | `faithfulSpdTransfersBoundedDrift` |

## Proof-bearing declarations by file

| File | Declarations with proof terms |
| --- | ---: |
| `E3.lean` | 1 |
| `E4.lean` | 2 |
| `E5.lean` | 2 |
| `EML.lean` | 24 |
| `EMLGeneratedSample.lean` | 9 |
| `Geometry.lean` | 14 |
| `GeometryGeneratedSample.lean` | 10 |
| `Info.lean` | 30 |
| `InfoGeneratedSample.lean` | 15 |
| `Operator.lean` | 14 |
| `OperatorGeneratedSample.lean` | 12 |
| `Scan.lean` | 15 |
| `ScanGeneratedSample.lean` | 10 |
| `Tropical.lean` | 32 |
| `TropicalGeneratedSample.lean` | 20 |

## Promotion rule

A candidate moves to proof-bearing only when its own declaration has no `sorry`, the whole Lake project builds, and the change includes a review of whether the formal statement still matches the natural-language claim.

