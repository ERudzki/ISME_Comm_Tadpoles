# Source and concentration of natural microbial inoculum influences growth, survival, and associated microbiota of larval amphibians

**Elizabeth N. Rudzki, Claire Chiang, Tate A. Yawitz, Kevin D. Kohl**

This repository contains the scripts, QIIME2 command logs, metadata, and output files used for the analyses in the publication above.

> [!NOTE]
> Raw sequencing reads are available from the NCBI Sequence Read Archive under BioProject [`PRJNA1298324`](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1298324).

## Contents

1. [Citation](#citation)
2. [Repository Layout](#repository-layout)
3. [Scripts](#scripts)
4. [GraphPad Prism Files](#graphpad-prism-files)
5. [Metadata Files](#metadata-files)
6. [QIIME2 Feature Tables](#qiime2-feature-tables)
7. [Input Files per Script](#input-files-per-script)

***

## Citation

If you use this code or data, please cite the publication. Citation details are in [`CITATION.cff`](CITATION.cff), and GitHub's **Cite this repository** button (in the sidebar) generates APA and BibTeX formats from it.

```
Rudzki, E. N., Chiang, C., Yawitz, T. A., & Kohl, K. D. 2026. Source and concentration
of natural microbial inoculum influence growth, survival, and associated microbiota of
larval amphibians. ISME Communications. https://doi.org/DOI
```

***

## Repository Layout

```
.
├── ANCOM-BC2/
│   ├── Output/
│       ├── ancombc2_foi.csv
│       ├── ancombc2_results_PLE.rds
│       ├── ancombc2_results_PM.rds
│       └── ...
│   ├── table-family.csv
│   ├── Tadpole_AncomBC2_Pub.Rmd
│   └── Tadpole_Metadata_AncomBC2.txt
├── PRISM/
│   ├── Tadpole_Gut_TaxaAbundances.prism
│   ├── Tadpole_WaterChemistry
│   └── Output_Tables/
│       └── *_Dunns_ForCorrection.csv
├── QIIME2/
│   ├── features-to-exclude.txt
│   ├── Metadata_Files/
│       └── *.txt
│   ├── Output/
│       ├── core_metrics_results/
│           └── core-metrics-results-*/
│               ├── exported_alpha/
│                   ├── bray_curtis/
│                   ├── bray_curtis_pcoa/
│                   ├── evenness/
│                   └── ...
│               └── *.qza/qzv
│       ├── exported-gut/
│       ├── exported-skin/
│       ├── exported-water/
│       ├── feature_tables/
│       └── family_export/
│   └── Tadpole-QIIME2-Log-Pub.txt
├── R_Analyses/
│   ├── Input_Files/
│       └── *.csv
│   ├── Output_Tables/
│       └── *.csv
│   ├── Scripts/
│       └── *.Rmd
├── Raw_Data.xlsx                             # Non-16S Raw Data
├── CITATION.cff
└── README.md
```

***

## Scripts

| Directory | File | Purpose |
|---|---|---|
| `ANCOM-BC2/` | `Tadpole_AncomBC2_Pub.Rmd` | Differential abundance analysis with ANCOM-BC2 |
| `QIIME2/` | `Tadpole-QIIME2-Log-Pub.txt` | Full log of QIIME2 commands |
| `R_Scripts/` | `Tadpole_Decontam_Pub.Rmd` | Identifies contaminant features with decontam |
| `R_Scripts/` | `Tadpole_VennDiagrams_Pub.Rmd` | Shared and unique ASV Venn diagrams |
| `R_Scripts/` | `Tadpole_Adonis_Pub.Rmd` | PERMANOVA (ADONIS) on Bray-Curtis and Jaccard distances |
| `R_Scripts/` | `Tadpole_Beta_Div_Plots_Pub.Rmd` | PCoA plots of beta diversity |
| `R_Scripts/` | `Tadpole_Jonckheere_TwoSided_Pub.Rmd` | Two-sided Jonckheere-Terpstra trend tests |
| `R_Scripts/` | `Tadpole_Taxa_Barplots_Pub.Rmd` | Taxonomic composition barplots |
| `R_Scripts/` | `Tadpole_Taxa_RelAbun_Stats_Pub.Rmd` | Statistics on taxon relative abundance |

***

## GraphPad Prism Files

*To be added.*

***

## Metadata Files

**`ANCOM-BC2/`**

- `Tadpole_Metadata_AncomBC2.txt`

**`QIIME2/Metadata_Files/`**

| File | Original parent folder |
|---|---|
| `Tadpole_Metadata_All_Q2.txt` | `All-seq` |
| `Tadpole_Metadata_All_Q2_NT.txt` | `All-seq` |
| `Tadpole_Metadata_SampleType_Q2.txt` | `All-seq` |
| `Tadpole_Metadata_All.txt` | `All-seq` |
| `Tadpole_Metadata.txt` | `All-seq` |
| `Tadpole_Metadata_Water_Qiime2R.txt` | `core-metrics-results-water` |
| `Tadpole_Metadata_Water_Barplots.txt` | `core-metrics-results-water` |
| `Tadpole_Metadata_Water_Qiime2R_Dep.txt` | `core-metrics-results-water-dep` |
| `Tadpole_Metadata_Water_Qiime2R_Con.txt` | `core-metrics-results-water-con` |
| `Tadpole_Metadata_Gut_Qiime2R.txt` | `core-metrics-results-gut` |
| `Tadpole_Metadata_Gut_Alpha_Con_Q2.txt` | `core-metrics-results-gut` |
| `Tadpole_Metadata_Gut_Alpha.txt` | `core-metrics-results-gut` |
| `Tadpole_Metadata_Gut_Qiime2R_Dep.txt` | `core-metrics-results-gut-dep` |
| `Tadpole_Metadata_Gut_Qiime2R_Con.txt` | `core-metrics-results-gut-con` |
| `Tadpole_Metadata_Skin_Qiime2R.txt` | `core-metrics-results-skin` |
| `Tadpole_Metadata_Skin_Alpha_Con_Q2.txt` | `core-metrics-results-skin` |
| `Tadpole_Metadata_Skin_Alpha.txt` | `core-metrics-results-skin` |
| `Tadpole_Metadata_Skin_Qiime2R_Dep.txt` | `core-metrics-results-skin-dep` |
| `Tadpole_Metadata_Skin_Qiime2R_Con.txt` | `core-metrics-results-skin-con` |

***

## QIIME2 Feature Tables

Location: `QIIME2/Output/feature_tables/`

### Core Processing Chain

| Table | How it was made | What it was used for |
|---|---|---|
| `table.qza` | DADA2 output | Summarized and filtered to make the next table. Input to the decontam R script and the starting point for the sequencing-depth tables. |
| `table-sans-a-m-c.qza` | Removed archaea, chloroplast, and mitochondria | Summarized; parent of the decontam table; used to flag the seven samples with 0 reads. Also the base for the sequencing-depth tables. |
| `decontam-table-sans-a-m-c.qza` | Removed contaminant features listed in `features-to-exclude.txt` | Parent of the tannin and control filters. Exported to `.tsv` to calculate num. reads. |
| `decontam-sans-a-m-c-t.qza` | Removed tannin samples | Intermediate step toward the `-k` table; also used for the `decontam-sans-a-m-c-t-pcr` table. |
| `decontam-sans-a-m-c-t-k.qza` | Removed control samples | Core-metrics at depth 500 (`core-metrics-results-decontam-d30-NT`). Parent of the `-w` table and of all gut, skin, and water splits. Read by the Venn diagram script (`phy`). |
| `decontam-sans-a-m-c-t-k-w.qza` | Removed control tank water and D0 water (`Remove = N`) | Used for the Venn diagrams. Core-metrics at depth 500 (`core-metrics-results-decontam-d500-sampletype`), which feeds the all-sample-type ADONIS and the beta diversity plots. |

### Per-Sample-Type Tables

Each sample type (gut, skin, water) has one base table and two subsets.

| Table | Used for |
|---|---|
| `{gut,skin,water}-decontam-sans-a-m-c-t-k.qza` | Core-metrics at depths 5700, 940, and 600, plus `alpha-group-significance`. These feed the beta diversity plot script and the Jonckheere tests. Parents of the subsets below and the source of the family-level collapsed tables. The gut table is also exported to `.tsv` for the barplots. |
| `dep-*` | Depletion comparisons: core-metrics for the ADONIS depletion tests (`core-metrics-results-*-dep`). |
| `con-*` | Concentration comparisons: core-metrics for the ADONIS concentration tests (`core-metrics-results-*-con`). |

### Sequencing-Depth and Unique-ASV Tables (summaries only)

These were made only to obtain read and ASV counts; nothing downstream uses them.

- `table-t`, `table-t-pcr`, `table-sans-a-m-c-t`, `table-sans-a-m-c-t-pcr`, `decontam-sans-a-m-c-t-pcr`
- The gut, skin, water, and kit-control splits of `table-t-pcr` and `table-sans-a-m-c-t-pcr` (`*_GUT`, `*_SKIN`, `*_WATER`, `*_KC`)
- `decontam-sans-a-m-c-t-pcr_onlykc`

### Family-Level Collapsed Tables

- `qiime taxa collapse` at level 5 on the water, gut, and skin tables produces `collapsed_table.qza` in each `QIIME2/Output/family_export/` folder.
- These are exported to `L5_abs_freq_{water,gut,skin}.tsv` for the family-level abundance percentages reported in the Results.
- No R script reads them directly. The relative abundance CSVs used by `Tadpole_Taxa_RelAbun_Stats_Pub.Rmd` were built from these exports.

***

## Input Files per Script

### QIIME2

| Input | Used by |
|---|---|
| `Tadpole_Manifest.csv` | `qiime tools import` |
| Raw FASTQ files | See NCBI SRA BioProject `PRJNA1298324` |
| `Tadpole_Metadata_All.txt` | `feature-table summarize` (`--m-sample-metadata-file`); `feature-table filter-samples` (`--m-metadata-file`) with `--p-where` filters on `Tannins` (Y/N), `Control`, `Remove`, `Type` (Gut, Skin, Water, PCR_Blank), `25_Keep`, `Dep_Keep`, and `Con_Keep`; `core-metrics-phylogenetic` in the early whole-dataset runs (`decontam-d30-NT` and `d500-sampletype`) |
| `Tadpole_Metadata.txt` | `core-metrics-phylogenetic`; `alpha-group-significance` (Faith PD, Shannon, and observed features) |
| `features-to-exclude.txt` | `filter-features --m-metadata-file` with `--p-exclude-ids`, to remove the feature IDs identified by `Tadpole_Decontam_Pub.Rmd` |

### Tadpole_Decontam_Pub.Rmd

| Input | Type |
|---|---|
| `Tadpole_Metadata_All_Q2.txt` | Metadata |
| `table.qza` | Feature table |
| `taxonomy.qza` | Taxonomy |

### Tadpole_VennDiagrams_Pub.Rmd

| Input | Type |
|---|---|
| `Tadpole_Metadata_All_Q2_NT.txt` | Metadata |
| `decontam-sans-a-m-c-t-k.qza` | Feature table |
| `decontam-sans-a-m-c-t-k-w.qza` | Feature table |
| `rooted-tree.qza` | Phylogenetic tree |
| `taxonomy.qza` | Taxonomy |

### Tadpole_Adonis_Pub.Rmd

**Metadata**

- `Tadpole_Metadata_SampleType_Q2.txt`
- `Tadpole_Metadata_{Water,Gut,Skin}_Qiime2R_Dep.txt`
- `Tadpole_Metadata_{Water,Gut,Skin}_Qiime2R_Con.txt`

**Exported distance matrices (`.tsv`)**

Each folder below supplies both a Bray-Curtis and a Jaccard `distance-matrix.tsv`, from its `exported_alpha/bray_curtis/` and `exported_alpha/jaccard/` subfolders:

- `core-metrics-results-decontam-d500-sampletype`
- `core-metrics-results-water-dep` and `core-metrics-results-water-con`
- `core-metrics-results-gut-dep` and `core-metrics-results-gut-con`
- `core-metrics-results-skin-dep` and `core-metrics-results-skin-con`

### Tadpole_Beta_Div_Plots_Pub.Rmd

**Metadata**

- `Tadpole_Metadata_SampleType_Q2.txt`
- `Tadpole_Metadata_{Water,Gut,Skin}_Qiime2R.txt`

**PCoA artifacts (`.qza`)**

Each folder below supplies both `bray_curtis_pcoa_results.qza` and `jaccard_pcoa_results.qza`:

- `core-metrics-results-decontam-d500-sampletype`
- `core-metrics-results-water`
- `core-metrics-results-gut`
- `core-metrics-results-skin`

### Tadpole_Jonckheere_TwoSided_Pub.Rmd

| Input | Type | Note |
|---|---|---|
| `Tadpole_Metadata_Gut_Alpha_Con_Q2.txt` | Metadata | |
| `Tadpole_Metadata_Skin_Alpha_Con_Q2.txt` | Metadata | |
| `exported-{water,gut,skin}/{water,gut,skin}-decontam-sans-a-m-c-t-k.tsv` | Exported feature tables | |
| `exported-{water,gut,skin}/taxonomy.tsv` | Exported taxonomy | |
| `exported-{water,gut,skin}/tree.nwk` | Exported trees | Built into the phyloseq object but not used |

### Tadpole_Taxa_Barplots_Pub.Rmd

| Input | Type | Note |
|---|---|---|
| `Tadpole_Metadata_Water_Barplots.txt` | Metadata and alpha diversity results | |
| `Tadpole_Metadata_Gut_Alpha.txt` | Metadata and alpha diversity results | |
| `Tadpole_Metadata_Skin_Alpha.txt` | Metadata and alpha diversity results | |
| `exported-{water,gut,skin}/{water,gut,skin}-decontam-sans-a-m-c-t-k.tsv` | Exported feature tables | |
| `exported-{water,gut,skin}/taxonomy.tsv` | Exported taxonomy | |
| `exported-{water,gut,skin}/tree.nwk` | Exported trees | Built into the phyloseq object but not used |

### Tadpole_Taxa_RelAbun_Stats_Pub.Rmd

All inputs are CSV tables in `PRISM_Output_Tables/`.

| Input | Note |
|---|---|
| `Gut_Con_RelAbun.csv` | Relative abundance |
| `Skin_Con_RelAbun.csv` | Relative abundance |
| `Gut_Dep_Dunns_ForCorrection.csv` | Dunn's test values calculated in Prism 10 |
| `Gut_Source_Dunns_ForCorrection.csv` | Dunn's test values calculated in Prism 10 |
| `Skin_Dep_Dunns_ForCorrection.csv` | Dunn's test values calculated in Prism 10 |
| `Skin_Source_Dunns_ForCorrection.csv` | Dunn's test values calculated in Prism 10 |
| `Water_D6Tank_Source_Dunns_ForCorrection.csv` | Dunn's test values calculated in Prism 10 |
| `Water_D6Tank_Source_Kruskal_ForCorrection.csv` | Kruskal-Wallis test values calculated in Prism 10 |
