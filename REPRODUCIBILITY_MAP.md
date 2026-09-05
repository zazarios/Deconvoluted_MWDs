# Reproducibility Map

## Manuscript

**Molecular Representation Is Target- and State-Dependent: Minimum Sufficient Resolution and Grouping of Experimentally Resolved Polypropylene MWDs**

This file maps the principal manuscript and Supporting Information results to the MATLAB packages and numerical outputs deposited in the repository.

## Core qualification overview

| Evidence block | Package | Qualified status |
|---|---|---:|
| Final process-domain representation requalification | `Spherizone_JIEC_V3_6_STAGE_K_FINAL_REPRESENTATION_REQUALIFICATION` | 23/23 gates PASS |
| Experimental cross-state portability | `JIEC_V3_7_3_PASS7_DELIMITER_AND_PATH_SAFE_HOTFIX` | 11/11 gates PASS |
| Tie-aware topology identification | `JIEC_V3_8_1_PASS8_VERIFIER_SHAPE_SAFE_HOTFIX` | 9/9 gates PASS |
| Primary grouping-baseline challenge | `JIEC_V3_9_PASS9_GROUPING_BASELINE_CHALLENGE` | 12/12 gates PASS |
| External/process grouping generality | `JIEC_V3_10_2_PASS10_FINAL_GROUPING_GENERALITY_CHECK` | 16/16 gates PASS |
| Accuracy-complexity comparison | `JIEC_V3_11_PASS11_ACCURACY_COMPLEXITY_COMPARISON` | 14/14 gates PASS |

## Post-freeze reproducibility blocks

| Evidence block | Package | Status |
|---|---|---|
| Normalized-tolerance response | `JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT` | Reconstructed and verified from frozen Stage-K outputs |
| Moment-matched conventional-MWD benchmark | `JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION` | Reproduced and verified against sealed Pass-5 audit |

The post-freeze blocks do not alter the qualified Stage-K/Pass-7-to-Pass-11 computational chain.

## Manuscript/SI claim-to-output map

| Result | Package | Primary output(s) |
|---|---|---|
| 29 measured PP states and state-specific `K*` | Pass 7.3 | `Outputs_Pass7/Pass7_state_specific_order_map.csv` |
| Common-topology versus observed-anchor fixed-property portability | Pass 7.3 | `Outputs_Pass7/Pass7_moderate_portability_penalties.csv` |
| Poorsank factor-two molecular-weight-scale sensitivity | Pass 7.3 | `Outputs_Pass7/Pass7_Poorsank_scale_sensitivity.csv` |
| 145/145 unique numerical non-`Mn`, `K=2` optima | Pass 8.1 | `Outputs_Pass8/Pass8_K2_target_dependence_tieaware.csv` |
| State-dependent topology examples | Pass 8.1 | `Outputs_Pass8/Pass8_K2_state_variation_tieaware.csv` |
| Primary unrestricted/contiguous equivalence: 834/834 | Pass 9 | `Outputs_Pass9/Pass9_contiguity_error_equivalence.csv` |
| Primary preservation of `K*` under contiguity restriction: 0/174 penalties | Pass 9 | `Outputs_Pass9/Pass9_contiguity_Kstar_comparison.csv` |
| Primary target-blind comparison: 56/145 lower-error cases, 4 added failures, 13/29 common-`K` penalties | Pass 9 | `Outputs_Pass9/Pass9_targetblind_minimax.csv`; `Pass9_targetblind_commonK.csv`; `Pass9_primary_summary.csv` |
| 19-distribution external PP registry | Pass 10.2 / Pass 11 | `data/External19/External19_registry.csv` |
| External unrestricted/contiguous equivalence: 570/570 | Pass 10.2 | `Outputs_Pass10/Pass10_external_contiguity_error_equivalence.csv` |
| External preservation of `K*`: 114/114 | Pass 10.2 | `Outputs_Pass10/Pass10_external_contiguity_Kstar_comparison.csv` |
| External target-specific lower `K=2` error: 45/95 | Pass 10.2 | `Outputs_Pass10/Pass10_external_targetblind_minimax.csv` |
| External target-specific prevention of `K=2` failure: 10 cases | Pass 10.2 | `Outputs_Pass10/Pass10_external_targetblind_minimax.csv`; `Pass10_external_summary.csv` |
| External target-blind common-`K` penalty: 3/19 | Pass 10.2 | `Outputs_Pass10/Pass10_external_targetblind_commonK.csv` |
| Process-domain contiguous and target-blind grouping baselines | Pass 10.2 | `Outputs_Pass10/Pass10_spherizone_*` |
| State-informed process `K*` | Stage K | `Outputs_StageK/StageK_H_target_order_map.csv` |
| Scenario-informed fixed representation | Stage K | `Outputs_StageK/StageK_H1_target_order_map.csv` |
| State-independent fixed representation | Stage K | `Outputs_StageK/StageK_H2_target_order_map.csv` |
| Final 17-state H2/temperature support | Stage K | `Outputs_StageK/StageK_state_support.csv` |
| Process-domain minimax/closure bounds | Stage K | `Outputs_StageK/StageK_H_all_partition_minimax_bounds.csv`; `StageK_H1_all_partition_closure_bounds.csv`; `StageK_H2_all_partition_closure_bounds.csv` |
| State-informed tolerance response, SI Table S29 | Tolerance readout | `Outputs_ToleranceReadout/Tolerance_state_informed_Kstar_counts.csv`; `Tolerance_casewise_Kstar.csv` |
| Fixed-information no-closure counts, SI Table S30 / Figure 5B | Tolerance readout | `Outputs_ToleranceReadout/Tolerance_fixed_no_closure_counts.csv` |
| Full-resolution normalized closure floors, SI Table S31 | Tolerance readout | `Outputs_ToleranceReadout/Tolerance_K5_closure_floors.csv` |
| Structural-survival witness cases | Stage K cumulative package | `inputs/StageEQualifiedOutputs/StageE_worst_structural_witnesses.csv` |
| Deterministic joint `W1` bounds | Stage K cumulative package | `inputs/StageGQualifiedOutputs/StageG_joint_W1_bounds_by_T.csv`; `StageG_joint_W1_bounds_summary.csv` |
| Structural-survival hydrogen challenge | Stage K cumulative package | `inputs/StageJQualifiedOutputs/StageJ_structural_survival.csv` |
| Same-moment lognormal/Schulz-Zimm non-uniqueness | Pass-5 reproduction | `Outputs_Pass5_Reproduced/Pass5_Reproduced_same_moment_nonuniqueness.csv`; `Pass5_Reproduced_same_moment_summary.csv` |
| Conventional comparator W1/JS/tail metrics, SI Tables S37-S38 / Figure 6 | Pass-5 reproduction | `Outputs_Pass5_Reproduced/Pass5_Reproduced_casewise_comparator_metrics.csv`; `Pass5_Reproduced_comparator_summary.csv` |
| W1 tolerance counts, SI Table S39 | Pass-5 reproduction | `Outputs_Pass5_Reproduced/Pass5_Reproduced_W1_tolerance_counts.csv` |
| Original sealed Pass-5 numerical audit | Pass-5 reproduction | `sealed_reference/Hardening_Pass5_Conventional_Representation_Benchmark_SEALED/` |
| 86/95 cases reduced below full source resolution | Pass 11 | `Outputs_Pass11/Pass11_Kstar_comparison.csv`; `Pass11_cohort_summary.csv` |
| Mean retained-resolution reduction = 38.25% | Pass 11 | `Outputs_Pass11/Pass11_cohort_summary.csv` |
| Target-level reduction counts and mean/median reductions | Pass 11 | `Outputs_Pass11/Pass11_target_summary.csv` |
| 51/67: every same-`K*` alternative fails | Pass 11 | `Outputs_Pass11/Pass11_cohort_summary.csv` |
| 51/65: every target-mismatched alternative fails | Pass 11 | `Outputs_Pass11/Pass11_cohort_summary.csv` |
| Median normalized errors 0.380, 7.14, and 3.77 | Pass 11 | `Outputs_Pass11/Pass11_cohort_summary.csv` |
| Four main-text Figure-7 cases | Pass 11 | `Outputs_Pass11/Pass11_representative_cases.csv`; `Pass11_representative_curve_data.csv` |

## Main-text figure and table map

| Main-text item | Computational source |
|---|---|
| Table 1 | Pass-7 experimental registry and state-component data |
| Figure 1 | Conceptual summary of Pass-7 information conditions |
| Figure 2 | Pass-8 tie-aware target/topology outputs |
| Table 2 | Pass-7 portability outputs |
| Figure 3 | Pass-7 portability outputs |
| Table 3 | Pass-9 grouping-baseline outputs |
| Figure 4 | Pass-10 external PP grouping outputs |
| Table 4 | Stage-K state-informed process order map |
| Figure 5A | Stage-K state-informed process order map |
| Figure 5B | `JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT` |
| Figure 6 | `JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION` |
| Table 5 | Pass-11 target summary |
| Figure 7 | Pass-11 representative-case and representative-curve outputs |

## Supporting Information map

| SI section | Primary computational source |
|---|---|
| S1 Representation definitions | Shared formulation implemented across Stage K and Passes 7-11 |
| S2 Experimental PP cross-state datasets | Pass 7.3 |
| S3 Experimental cross-state portability | Pass 7.3 |
| S4 Tie-aware topology identification | Pass 8.1 |
| S5 Primary experimental grouping baselines | Pass 9 |
| S6 Broader external PP evaluation | Pass 10.2 / external source registry |
| S7 Broader external grouping baselines | Pass 10.2 |
| S8 Accuracy-complexity comparison | Pass 11 |
| S9 Spherizone source MWD and process-state qualification | Stage K cumulative package |
| S10 Reduced-order Spherizone molecular-state propagation | Stage K cumulative package |
| S11 Qualified H2/temperature process-state support | Stage K |
| S12 Process-model representation results | Stage K |
| S13 Tolerance-response analysis | `JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT` |
| S14 Structural survival | Stage-K cumulative Stage-E/Stage-G/Stage-J evidence |
| S15 Process grouping-baseline result | Pass 10.2 |
| S16 Conventional moment-matched MWD benchmark | `JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION` |
| S17 Numerical qualification | Status and verification files in the six qualified packages |
| S18 Claim-to-output traceability | This map plus the individual package outputs |
| S19 Scope safeguards | Claim-scope files and manuscript/SI interpretation |

## Reproduction entry points

Core qualified packages use the launchers documented in their individual READMEs.

### Tolerance response

```matlab
cd JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT
Run_JIEC_PostFreeze_Tolerance_Response_Readout
```

Check:

```text
Outputs_ToleranceReadout/TOLERANCE_READOUT_STATUS.txt
Outputs_ToleranceReadout/Tolerance_readout_verification.csv
```

### Moment-matched benchmark

```matlab
cd JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION
Run_JIEC_Pass5_MomentMatched_Benchmark_Reproduction
```

Check:

```text
Outputs_Pass5_Reproduced/PASS5_REPRODUCTION_STATUS.txt
Outputs_Pass5_Reproduced/Pass5_Reproduction_verification.csv
```

The unchanged sealed reference audit is retained under `sealed_reference/`.

## Package-integrity status

```text
Stage K                         436/436 matched
Pass 7.3                         46/46 matched
Pass 8.1                         33/33 matched
Pass 9                           18/18 matched
Pass 10.2                        32/32 matched
Pass 11                          38/38 matched
Tolerance-response readout       12/12 matched
Pass-5 reproduction wrapper      27/27 matched
Nested sealed Pass-5 audit       13/13 matched
```

## Reproducibility coverage status

The repository now contains explicit code/input/output support for the normalized-tolerance response and the moment-matched conventional-MWD benchmark in addition to the six qualified core evidence blocks. No computational evidence block identified in the current manuscript/SI claim-to-output chain remains intentionally omitted from the prepared repository.
