# White Flight: Replication Fork

Replication materials for *White Flight in Public Higher Education? Racial Avoidance of Hispanic-Serving Institutions*, by Laura Hamilton, Charlie Eaton, and Simon Cheng.

This repository is Megan Allen's fork of the [original authors' repository](https://github.com/HigherEdData/White-Flight). It preserves their materials and adds Stata replication scripts developed during research with Christopher Brooks at the University of Michigan. The original study, data assembly, and original analysis code are credited to Hamilton, Eaton, and Cheng.

## Repository roles

- [Original study repository](https://github.com/HigherEdData/White-Flight): upstream data and analysis code.
- [This replication fork](https://github.com/meeallen/White-Flight): replication work and Stata adaptations.
- [Multiverse analysis repository](https://github.com/meeallen/white_flight_multiverse): the separate extension examining robustness across alternative analytic specifications.

Replication of a published specification and evaluation of alternative multiverse specifications are distinct tasks. Results or implementation checks in this fork should not be interpreted as completed results for the multiverse.

## Study and data

The original study examines enrollment changes around transitions to Hispanic-Serving Institution status using U.S. public four-year institutional data from 1990–2019.

The upstream repository documents IPEDS enrollment, admissions/test-score, and institutional-characteristics sources, alongside California and Texas applications/admissions data. Its [data directory](https://github.com/HigherEdData/White-Flight/tree/main/data) includes:

- `d_hsi_white_enrollment_final3.dta`: enrollment analysis data.
- `d_hsi_ca_tx_applications.dta`: applications analysis data.
- `c_enrollment_data_compute_measures.ipynb` and `c_applications_data_finalize.ipynb`: data-preparation notebooks.

Use the input required by the particular analysis. Preserve the source file and record its version and checksum before modifying or transforming it.

## Finding the code

The inherited analysis files follow the authors' table/figure naming convention: `t1_`, `t2_`, and `t3_` for tables; `f1_`, `f3_`, and related prefixes for figures; and `fa1_` for an appendix figure.

Added Stata replication files include:

- `replicate_fig1_in_Stata` through `replicate_fig6_in_Stata`, with Figure 2 absent from the current listed set.
- `replicate_tab1_in_Stata`
- `replicate_tab2_in_Stata (published version)`
- `replicate_tab2_in_Stata (simple agg branch)`
- `replicate_tab3_in_Stata`

The two Table 2 files represent different labeled versions. Use the published-version file when examining replication of that specification; do not silently substitute the simple-aggregation branch.

File presence is not a certification that every table and figure has been independently checked against the publication.

## Running a replication

1. Download or clone this repository and retain the commit identifier used.
2. Obtain the required complete data file from the upstream data directory.
3. Open the relevant replication script in Stata's Do-file Editor. Several replication scripts currently have no `.do` extension.
4. Review its data paths, output paths, and required user-written Stata commands before execution. Adapt machine-specific paths to your environment.
5. Run the script while saving a Stata log, then compare the resulting sample, specification, estimates, and figure or table with the corresponding published analysis.

For example, `replicate_fig4_in_Stata` currently sets `local project "K:/White Flight Data for Stata"`. Replace that directory with the location of your input file. Its setup copies `d_hsi_white_enrollment_final3.dta` into a temporary workspace under the filename expected by the authors' Figure 4 code.

The exact tested Stata version, package versions, and per-script requirements still need to be recorded. These instructions describe the current workflow; this repository is not yet packaged as a one-command reproducibility release.

## Relationship to the multiverse preregistration

The original-study replication preceded the multiverse registration. A separate real-data implementation pilot of the full never-HSI/CSDID outcome-regression branch was run on August 7, 2026. That pilot followed the original comparison-pool definition and estimation approach, but used developing multiverse outcome and aggregation specifications.

The pilot produced preliminary effect estimates and a standard error. Its self-comparison quality classification tested the software; it did not establish equivalence against an independently fitted benchmark. The final multiverse registration will distinguish replication, pilot work, preliminary pretreatment validation, and subsequent analyses.

See the multiverse repository for the developing analysis plan and implementation. This fork's README does not itself constitute an OSF registration.

## Attribution and citation

When using the original data or methods, cite Hamilton, Eaton, and Cheng's study and the [upstream repository](https://github.com/HigherEdData/White-Flight). When using these replication adaptations, additionally identify [this fork](https://github.com/meeallen/White-Flight) and the exact commit used.

Original study and materials: Laura Hamilton, Charlie Eaton, and Simon Cheng.
Replication work: Megan Allen, working with Christopher Brooks, University of Michigan.

Full publication metadata and a versioned software citation will be consolidated with the project's existing reference list.

## Reuse

Retain attribution and any applicable notices for inherited materials. This README does not assign a new license to third-party code or data. Reuse terms for inherited materials and a license for original contributions should be documented separately.
