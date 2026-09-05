# Data Provenance

## Manuscript

**Molecular Representation Is Target- and State-Dependent: Minimum Sufficient Resolution and Grouping of Experimentally Resolved Polypropylene MWDs**

This document records the origin, role, numerical treatment, and scope restrictions of the literature-derived and process-domain datasets contained in the repository.

The repository contains numerical data needed for computational reproduction. It does **not** redistribute publisher PDFs or other copyrighted full-text source files.

Reference numbers below correspond to the manuscript and Supporting Information bibliography.

## 1. Primary experimental cross-state polypropylene cohort

The primary cross-state cohort is implemented in Pass 7 and contains **29 measured polypropylene states**, organized as **six experimental families from four study clusters**.

Principal Pass-7 provenance files include:

```text
JIEC_V3_7_3_PASS7_DELIMITER_AND_PATH_SAFE_HOTFIX/data/
├── pass7_source_provenance.csv
├── pass7_state_family_registry.csv
├── pass7_state_component_data.csv
├── pass7_eligibility_protocol.csv
├── pass7_claim_scope.csv
└── pass7_prospective_hypotheses.csv
```

### Kissin et al. (2002) — manuscript reference [15]

- Study cluster: `Kissin_2002`
- Source location recorded in the package: Table 2
- Role: primary PP state family
- Experimental variation: hydrogen level
- States: 4
- Source components: 5
- Numerical treatment: reported component `Mw` values are converted to `Mn = Mw/2` under the reported Flory most-probable interpretation.

### Kissin et al. (2004) — manuscript reference [16]

- Study cluster: `Kissin_2004`
- Source location recorded in the package: Table 2
- Role: primary PP state family
- Experimental variation: temperature
- States: 6
- Source components: 4
- Material represented: crystalline PP fraction
- Numerical treatment: reported component `Mw` values are converted to `Mn = Mw/2`.

### Li et al. (2015) — manuscript reference [17]

Three primary families are constructed from explicit component tables:

- `LI2015_COCAT_DDS`
- `LI2015_COCAT_DCPDMS`
- `LI2015_DONOR_BLEND`

Each family contains 5 measured states and 5 source components. Reported component `Mw` values are converted to `Mn = Mw/2`.

Abbreviations used in the source treatment:

- TEA: triethylaluminum
- TIBA: triisobutylaluminum
- DDS: diphenyldimethoxysilane
- DCPDMS: dicyclopentyldimethoxysilane

### Poorsank et al. (2019) — manuscript reference [18]

- Study cluster: `Poorsank_2019`
- Source location recorded in the package: Supporting Information Table S5
- Role: primary PP family with molecular-weight-scale sensitivity
- States: 4
- Source components: 5
- Primary treatment: internally reconciled molecular-weight scale.
- Sensitivity: fixed factor-two transformation.
- Qualified result: the factor-two transformation does not change the reported optimal partitions.

### Daftaribesheli (2009) — SI-only reference [40]

- Dataset: `DAFTAR2009_PE_H2_SLURRY`
- Polymer: polyethylene
- Role: secondary cross-polyolefin sensitivity only
- States: 4
- Source components: 5
- Not counted in the 29-state primary PP cohort.

### Eligibility record retained for transparency

The Pass-7 provenance registry also records a Tu (2011) source that was excluded from the primary numerical cohort because the complete state-specific component table could not be reconstructed without graph digitization. The record is retained to document the eligibility decision; it is not used as a primary numerical dataset.

## 2. Broader 19-distribution external polypropylene cohort

The primary external cohort contains **19 component-resolved PP distributions from six study clusters**.

Principal registry:

```text
JIEC_V3_10_2_PASS10_FINAL_GROUPING_GENERALITY_CHECK/data/External19/External19_registry.csv
```

The registry is also frozen in the Pass-11 package:

```text
JIEC_V3_11_PASS11_ACCURACY_COMPLEXITY_COMPARISON/data/External19/External19_registry.csv
```

| Study cluster | Manuscript reference | Dataset count | Role |
|---|---:|---:|---|
| Kissin_2003 | [19] | 2 | Primary external PP |
| Jiang_2011 | [20] | 7 | Primary external PP |
| Zhou_2016 | [21] | 6 | Primary external PP |
| Poorsank_2019 | [18] | 2 | Primary external PP |
| Khare_2004 | [22] | 1 | Primary external PP |
| Luo_2009 | [23] | 1 | Primary external PP |

The 19 distributions are treated as **distribution-level cases nested within six study clusters**, not as 19 statistically independent studies.

### Dataset identifiers

```text
KISSIN_DELTA_PP80
KISSIN_SUPPORTED_1P_H0
JIANG_MSC
JIANG_LMSC9
JIANG_LMSC18
JIANG_LMSC31
JIANG_LMSC40
JIANG_LMSC46
JIANG_LMSC62
ZHOU_Cat1_SID1
ZHOU_Cat2_SID2
ZHOU_Cat3_SID3
ZHOU_Cat4_SID4
ZHOU_Cat5_SID5
ZHOU_CatD_DIBP
POORSANK_B
POORSANK_A3_ED0
KHARE2004_COMMERCIAL_PP
LUO2009_HYPOL_PP
```

The source resolution is dataset-specific and ranges from `N_ref = 4` to `N_ref = 6`.

### Source-integrity handling

The archived source-integrity records preserve the following safeguards:

- **Kissin_2003:** component `Mw` values are converted to `Mn` using the Flory dispersity-2 interpretation.
- **Jiang_2011:** published fractions are normalized when necessary to remove rounding-only deviation from unity; the published deconvoluted mixture is treated as the full reference.
- **Zhou_2016:** the published five-component representation is treated as the full reference even when separately reported whole-polymer GPC moments are not reproduced exactly; no claim is made that the component table reconstructs the raw GPC moments.
- **Poorsank_2019:** the molecular-weight-scale ambiguity is retained explicitly; representation-order conclusions are checked for invariance to uniform factor-two scaling.
- **Khare_2004 and Luo_2009:** retained as sealed external PP extensions in the 19-distribution primary cohort.

The external analysis does not fit Spherizone parameters and does not transfer a process-model uncertainty model into these literature-derived distributions.

## 3. Secondary external/sensitivity distributions

The Supporting Information contains a secondary cohort used to test the robustness of target-ordering interpretations. These cases are not counted in the 19-distribution primary PP cohort.

Sources include:

- additional Kissin and Poorsank conditions [18,19];
- Alghyamah and Soares [5];
- Soares [3];
- Matsko et al. [13]; and
- Shiri et al. [41] as a method-reanalysis sensitivity.

The retained `ALGHYAMAH_S4` reversal is used specifically to prevent the primary PP observation from being presented as a universal cross-polyolefin ordering rule.

## 4. Process-domain source representation

The conditional Spherizone application uses the fourth-generation Ziegler-Natta polypropylene source characterization reported by Alshaiban and Soares [24-27].

Primary data/code location:

```text
Spherizone_JIEC_V3_6_STAGE_K_FINAL_REPRESENTATION_REQUALIFICATION/
├── data/
├── inputs/
└── Outputs_StageK/
```

Relevant source tables are encoded in MATLAB data files including:

```text
data/data_flory_populations.m
data/data_source_whole_moments.m
```

The source characterization supports up to five Flory MWD components. Accordingly, `N_ref = 5` is used as the maximum source-supported molecular resolution for this process application. It is not interpreted as evidence for exactly five chemically distinct catalyst active sites.

## 5. Source-consistency treatment

The cumulative Stage-K package retains the source-consistency and qualification chain.

Important safeguards include:

- comparison of component-implied and separately reported whole-polymer molecular-weight moments;
- exclusion of the inconsistent `60_D` condition from the primary matched-temperature transfer construction;
- retention of source discrepancies for transparency rather than silent correction; and
- bounded use of matched source-condition transfers rather than a claim of a globally validated catalyst-response surface.

The process-state domain is a conditional engineering domain, not plant-scale validation.

## 6. Final process-state support

The final qualified process support contains 17 hydrogen/temperature states and is recorded in:

```text
Spherizone_JIEC_V3_6_STAGE_K_FINAL_REPRESENTATION_REQUALIFICATION/
Outputs_StageK/StageK_state_support.csv
```

The support combines:

- no-added-H2 boundary states;
- controlled 2 mol% H2 process-state stress cases; and
- retained 5 mol% H2 legacy comparators.

The source database terminates at 70 °C. The 80 °C second-stage support therefore uses a 70 °C boundary hold and admissible 10 °C transfers derived from matched source conditions. These are deterministic support constructions, not probabilistic confidence intervals.

Second-stage polymer fractions of 10, 20, and 30 wt% are specified design conditions and are not predicted phase yields.

## 7. Structural-survival evidence

The Stage-K cumulative package retains the qualified evidence used to test whether component-resolved MWD structure survives process-domain propagation.

Relevant files include:

```text
inputs/StageEQualifiedOutputs/StageE_worst_structural_witnesses.csv
inputs/StageGQualifiedOutputs/StageG_joint_W1_bounds_by_T.csv
inputs/StageGQualifiedOutputs/StageG_joint_W1_bounds_summary.csv
inputs/StageJQualifiedOutputs/StageJ_structural_survival.csv
```

The deterministic `W1` bounds are support bounds, not confidence intervals.

## 8. Data transformations used across representation-selection analyses

### Component ordering

Components are aligned or indexed by ascending molecular-weight rank. This is a numerical convention and does not imply one-to-one chemical active-site identity across states or studies.

### Flory conversion

Where a source explicitly provides Flory most-probable component `Mw`, the numerical representation uses:

```text
Mn = Mw / 2
```

as documented for that source.

### Mass fractions

Published component fractions are retained or normalized only when required to remove rounding-only deviation from unity. No source component is discarded during grouping.

### Group construction

A retained group combines source-component mass fractions and uses reciprocal-`Mn` aggregation. This preserves whole-distribution `Mn` by construction.

### Molecular targets

The model evaluates:

```text
Mn
Mw
dispersity
W1 on log10(M)
Tail@M90
Tail@M99
```

using the tolerances documented in the manuscript and Supporting Information.

## 9. Post-freeze normalized-tolerance readout provenance

The repository package

```text
JIEC_POSTFREEZE_TOLERANCE_RESPONSE_READOUT/
```

contains a deterministic readout of normalized-tolerance results from three frozen
Stage-K outputs:

```text
StageK_H_all_partition_minimax_bounds.csv
StageK_H1_all_partition_closure_bounds.csv
StageK_H2_all_partition_closure_bounds.csv
```

Byte-level source provenance and SHA-256 values are recorded in
`INPUT_PROVENANCE.csv`.

The readout uses the reference tolerances reported in the manuscript/SI and
applies `epsilon = q * epsilon_ref`. It selects state-informed `K*` using the
minimum certified upper error bound at each retained resolution, counts fixed-
information no-closure cases using the same upper-bound criterion, and obtains
K=5 closure floors by normalizing the frozen K=5 lower/upper bounds.

This operation does not rerun the reactor model, fit parameters, alter an
uncertainty/support domain, or optimize the reference tolerances.

## 10. Moment-matched conventional-MWD benchmark provenance

The repository package

```text
JIEC_PASS5_MOMENT_MATCHED_MWD_BENCHMARK_REPRODUCTION/
```

contains two layers.

First, the original sealed numerical audit is preserved unchanged under:

```text
sealed_reference/Hardening_Pass5_Conventional_Representation_Benchmark_SEALED/
```

Its internal `MANIFEST_SHA256.csv` verifies 13/13 payload files.

Second, the companion MATLAB reproducer reads frozen Stage-E reference and
adverse-witness MWD curves plus the comparator parameters retained by the sealed
Pass-5 audit.

The two Stage-E input files are:

```text
StageE_reference_MWD_curves.csv
StageE_worst_witness_MWD_curves.csv
```

They are byte-identical copies of the corresponding qualified Stage-K cumulative
inputs. The comparator-parameter file is copied from the sealed Pass-5 audit.

The reproducer reconstructs:

- the moment-matched lognormal weight distribution;
- the moment-matched Schulz-Zimm/gamma weight distribution;
- the contextual phase-wise single-Flory comparator from the frozen Stage-E export;
- Wasserstein-1 distance on `log10(M)`;
- Jensen-Shannon divergence;
- M90/M99 ratios and tail excess;
- direct lognormal-versus-Schulz-Zimm separation; and
- W1 tolerance counts.

The archived independent reconstruction used to prepare this repository matches
the sealed Pass-5 numerical audit to floating-point precision.

The benchmark is post-freeze and does not alter any Stage-A-to-Stage-K reactor
calculation or qualified support domain.

## 11. Copyright and source access

The repository should contain only the numerical transcriptions, derived tables, MATLAB source code, and audit files needed for computational reproduction.

Do **not** upload publisher PDFs, downloaded journal Supporting Information, or other copyrighted full-text material unless redistribution rights explicitly permit it.

Researchers wishing to inspect the original evidence should obtain the cited publications from publishers, institutional repositories, or other lawful sources.


## 12. Provenance and qualification files to preserve

Do not remove files of the following types from the qualified or reproducibility packages:

```text
*_source_provenance.csv
*_source_integrity_registry.csv
*_eligibility_protocol.csv
*_claim_scope.csv
*_verification.csv
*_STATUS.txt
INPUT_PROVENANCE.csv
PACKAGE_MANIFEST_SHA256.txt
PROSPECTIVE_FREEZE_SHA256.txt
MANIFEST_SHA256.csv
Independent_Audit/
sealed_reference/
```

These files document the distinction among literature-derived source data,
transformed numerical inputs, frozen model outputs, post-freeze readouts,
independent expected results, and qualification/reproduction checks.

## 13. Repository provenance coverage

The prepared repository contains explicit provenance and computational support for
the numerical evidence blocks used in the current manuscript and Supporting
Information, including the normalized-tolerance readout and the moment-matched
conventional-MWD benchmark. No publisher full-text files are required for
execution of these deposited calculations.
