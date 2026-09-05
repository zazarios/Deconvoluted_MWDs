# Molecular Representation Is Target- and State-Dependent: Minimum Sufficient Resolution and Grouping of Experimentally Resolved Polypropylene MWDs

This repository contains the MATLAB code, qualified numerical inputs, literature-derived component-resolved molecular-weight-distribution (MWD) datasets, verification files, and frozen numerical outputs supporting the manuscript:

**Molecular Representation Is Target- and State-Dependent: Minimum Sufficient Resolution and Grouping of Experimentally Resolved Polypropylene MWDs**

The repository contains six qualified computational evidence blocks and two post-freeze reproducibility blocks:

1. final process-domain representation requalification (Stage K);
2. experimental cross-state portability (Pass 7);
3. tie-aware topology identification (Pass 8);
4. grouping-baseline challenge (Pass 9);
5. broader external/process grouping generality (Pass 10);
6. accuracy-complexity comparison (Pass 11);
7. normalized-tolerance response readout from frozen Stage-K outputs; and
8. reproduction of the sealed Pass-5 moment-matched MWD benchmark.

The relationship between manuscript/SI claims and individual computational outputs is documented in [`REPRODUCIBILITY_MAP.md`](REPRODUCIBILITY_MAP.md). Dataset origins, transformations, scope restrictions, and source-integrity handling are documented in [`DATA_PROVENANCE.md`](DATA_PROVENANCE.md).

## Repository structure

```text
Deconvoluted_MWDs/
├── README.md
├── REPRODUCIBILITY_MAP.md
├── DATA_PROVENANCE.md
├── LICENSE
│
├── Spherizone_JIEC_V3_6_STAGE_K_FINAL_REPRESENTATION_REQUALIFICATION/
├── JIEC_V3_7_3_PASS7_DELIMITER_AND_PATH_SAFE_HOTFIX/
├── JIEC_V3_8_1_PASS8_VERIFIER_SHAPE_SAFE_HOTFIX/
├── JIEC_V3_9_PASS9_GROUPING_BASELINE_CHALLENGE/
├── JIEC_V3_10_2_PASS10_FINAL_GROUPING_GENERALITY_CHECK/
├── JIEC_V3_11_PASS11_ACCURACY_COMPLEXITY_COMPARISON/
├── JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT/
└── JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION/
```

The six Stage-K/Pass-7-to-Pass-11 directories retain their qualified release names. The two additional directories are explicitly post-freeze reproducibility blocks; they do not modify or replace the qualified model chain.

## MATLAB environment

The archived MATLAB packages were developed and checked with **MATLAB R2025b**.

No internet download is required during execution of the deposited calculations. Numerical inputs needed by the archived packages are included in their package directories.

## Package integrity

The six qualified computational packages were checked against their original SHA-256 manifests:

| Package | Manifest result |
|---|---:|
| Stage K v3.6 | **436/436 matched** |
| Pass 7.3 | **46/46 matched** |
| Pass 8.1 | **33/33 matched** |
| Pass 9 | **18/18 matched** |
| Pass 10.2 | **32/32 matched** |
| Pass 11 | **38/38 matched** |

The two added reproducibility packages also contain SHA-256 manifests:

| Supporting reproducibility block | Manifest result |
|---|---:|
| Post-freeze tolerance-response readout | **12/12 matched** |
| Pass-5 reproduction wrapper | **27/27 matched** |
| Nested sealed Pass-5 audit | **13/13 matched** |

No manifest-listed payload file is missing or hash-mismatched in the prepared repository.

For reproducibility testing, make a working copy before running a package so that the deposited SHA-256 snapshot remains unchanged.

## Quick start

### 1. Final process-domain representation requalification

Directory:

```text
Spherizone_JIEC_V3_6_STAGE_K_FINAL_REPRESENTATION_REQUALIFICATION
```

Run:

```matlab
Run_JIEC_V3_StageK_FinalRepresentationRequalification
```

Primary status:

```text
Outputs_StageK/STAGE_K_STATUS.txt
Outputs_StageK/StageK_verification.csv
```

Expected qualification: **23/23 gates PASS**.

### 2. Experimental cross-state portability

Directory:

```text
JIEC_V3_7_3_PASS7_DELIMITER_AND_PATH_SAFE_HOTFIX
```

Run:

```matlab
Run_JIEC_V3_7_3_Pass7_ExperimentalStatePortability
```

Expected qualification: **11/11 gates PASS**.

### 3. Tie-aware topology identification

Directory:

```text
JIEC_V3_8_1_PASS8_VERIFIER_SHAPE_SAFE_HOTFIX
```

Run:

```matlab
Run_JIEC_V3_8_1_Pass8_TieAwarePartitionIdentifiability
```

Expected qualification: **9/9 gates PASS**.

### 4. Primary grouping-baseline challenge

Directory:

```text
JIEC_V3_9_PASS9_GROUPING_BASELINE_CHALLENGE
```

Run:

```matlab
Run_JIEC_V3_9_Pass9_GroupingBaselineChallenge
```

Expected qualification: **12/12 gates PASS**.

### 5. Broader external/process grouping generality

Directory:

```text
JIEC_V3_10_2_PASS10_FINAL_GROUPING_GENERALITY_CHECK
```

Run:

```matlab
Run_JIEC_V3_10_Pass10_FinalGroupingGeneralityCheck
```

Expected qualification: **16/16 gates PASS**.

The directory carries the v3.10.2 verifier release; the scientific release recorded in the status file remains `3.10-pass10-final-grouping-generality-check`.

### 6. Accuracy-complexity comparison

Directory:

```text
JIEC_V3_11_PASS11_ACCURACY_COMPLEXITY_COMPARISON
```

Run:

```matlab
Run_JIEC_V3_11_Pass11_AccuracyComplexityComparison
```

Expected qualification: **14/14 gates PASS**.

### 7. Post-freeze tolerance-response readout

Directory:

```text
JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT
```

Run:

```matlab
Run_JIEC_PostFreeze_Tolerance_Response_Readout
```

This script reads only three frozen Stage-K partition-bound CSV files. It reproduces:

- SI Table S29;
- SI Table S30;
- SI Table S31; and
- the no-closure counts used in main-text Figure 5B.

It does not rerun the reactor model, refit parameters, alter the support domain, or tune tolerances.

### 8. Moment-matched MWD benchmark

Directory:

```text
JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION
```

Run:

```matlab
Run_JIEC_Pass5_MomentMatched_Benchmark_Reproduction
```

The unchanged sealed numerical audit is retained under `sealed_reference/`. The MATLAB companion reproducer reconstructs the primary 12-case lognormal, Schulz-Zimm/gamma, and phase-wise single-Flory comparisons from frozen Stage-E MWD curves and sealed comparator parameters.

The archived cross-check reproduces the sealed numerical audit to floating-point precision.

## What this repository supports

The deposited files support the reported computational results concerning:

- 29 measured polypropylene states in six experimental families;
- target-dependent minimum retained resolution `K*`;
- target-dependent and tie-aware grouping topology;
- cross-state portability of common grouping topology versus observed anchor-state molecular-weight information;
- unrestricted versus molecular-weight-contiguous grouping;
- optimized target-specific versus target-blind grouping;
- the 19-distribution external polypropylene cohort;
- process-domain representation selection under restricted state information;
- normalized-tolerance response and full-resolution closure floors;
- the 12-case moment-matched conventional-MWD benchmark;
- accuracy-complexity comparison across 95 non-`Mn` distribution-target cases; and
- numerical qualification and claim-to-output traceability.

The repository does **not** establish unique chemical active-site identities, plant-scale Spherizone validation, a unique second-stage phase split, absolute industrial throughput, detailed particle morphology, or detailed gas/solid residence-time distributions.

## Frozen outputs and package metadata

Qualified outputs are retained in the `Outputs_*` directories. Independent expected results are retained in `Independent_Audit/` where applicable. SHA-256 manifests are retained so that accidental changes to frozen package contents can be detected.

### Stage K metadata note

Stage K is qualified as release `3.6-stageK-final-representation-requalification`, as recorded in:

```text
Outputs_StageK/STAGE_K_STATUS.txt
Outputs_StageK/StageK_verification.csv
README_STAGE_K.md
STAGE_K_3_6_RELEASE_NOTES.md
```

Because Stage K is a cumulative frozen package, some historical root metadata remain from earlier development stages. The files listed above are the authoritative Stage-K release-identification records for the present study.

### Post-freeze readout status

`JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT` is a deterministic readout from frozen Stage-K numerical bounds. It is not part of the Stage-K qualification chain and does not change the qualified model.

`JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION` preserves the original sealed Pass-5 numerical audit unchanged and adds a transparent MATLAB reproduction layer. It does not rerun the reactor model.

## Reproducibility coverage

The repository now contains explicit script/input/output support for the numerical evidence blocks referenced in the current manuscript and Supporting Information, including the normalized-tolerance readout and the moment-matched conventional-MWD benchmark.

The manuscript's Data and Code Availability statement can therefore refer to the repository without excluding those two analyses, provided the public GitHub repository is updated with this complete prepared version before submission.

## Data and copyright

**License.** Original software code and repository documentation are released under the MIT License; see `LICENSE`. This license does not relicense third-party publications, publisher materials, or literature-derived source material. Numerical transcriptions derived from published sources are provided for reproducibility and retain their original source attribution.

The repository does not redistribute publisher PDFs or other copyrighted full-text source files. Original literature sources remain identified by the manuscript/SI references and the provenance records supplied with the numerical datasets.

## Citation

After publication, please cite the corresponding article. Before publication, cite the manuscript title above together with the repository commit or release used for reproduction.
