# hnc-prs-phewas
#### Polygenic risk score models for head and neck squamous cell carcinoma and its subtypes
Lee, Y. C., Jung, S. H., Shivakumar, M., Cha, S., Park. Y. W., … & Kim, D. (2024) Polygenic risk score-based phenome-wide association study of head and neck cancer across two large biobanks.

### Head and neck squamous cell carcinoma - 972,182 variants
> [GAME-ON_HNC-all_PRSCS_auto.zip](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/GAME-ON_HNC-all_PRSCS_auto.zip)

### Oral cavity cancer - 972,182 variants
> [GAME-ON_HNC-OC_PRSCS_auto.zip](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/GAME-ON_HNC-OC_PRSCS_auto.zip)

### Oropharynx cancer - 972,182 variants
> [GAME-ON_HNC-OPC_PRSCS_auto.zip](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/GAME-ON_HNC-OPC_PRSCS_auto.zip)

---

## Description

To generate polygenic risk score (PRS), we utilized the genome-wide association study (GWAS) summary statistics from the [Genetic Associations and Mechanisms in Oncology (GAME-ON)](https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001202.v1.p1) Network. The HNSCC, OPC, and OC cases were identified based on following ICD-10 codes: oral cavity (C02.0–C02.9, C03.0–C03.9, C04.0–C04.9, and C05.0–C06.9) and oropharynx (C01.9, C02.4, and C09.0–C10.9). The GWASs (HNSCC [5,974 cases and 4,012 controls], OPC [2,617 cases and 4,012 controls], and OC [2,958 cases and 4,012 controls]). The GWASs were performed using PLINK 1.90 with sex, age, 10 PCs, and genotyping batch as covariates. The genotype data for the oral and pharyngeal OncoArray study can be downloaded from the database of Genotypes and Phenotypes (dbGaP) under accession phs001202.v1.p1. Of note, the GWASs did not include the additional external controls (2,476 shared controls [1,453 from the EPIC study and 1,023 from the Toronto study]) beyond the GAME-ON data used by Lesseur, Corina, et al. [1] in their GWAS analysis.

We constructed PRSs for HNSCC, OPC, and OC by using a Bayesian polygenic prediction method, PRS-CS [2], which infers the posterior mean effect size of each variant using the linkage disequilibrium (LD) reference panel and GWAS summary. The 1000G Project phase 3 EUR data was used to be the external LD reference panel. The posterior SNP effect sizes in PRS-CS were inferred from GAME-ON summary statistics, with default settings, and automatic estimation of the global shrinkage parameter (PRS-CS-auto). The individual PRSs were computed from beta coefficients as the weighted sum of the risk alleles by applying PLINK version 1.90 with the –score command [3].

### Reference
1. Lesseur C, Diergaarde B, Olshan AF, Wünsch-Filho V, Ness AR, Liu G, et al. Genome-wide association analyses identify new susceptibility loci for oral cavity and pharyngeal cancer. Nat Genet. 2016;48:1544–50.
2. Ge T, Chen CY, Ni Y, Feng YCA, Smoller JW. Polygenic prediction via Bayesian regression and continuous shrinkage priors. Nat Commun. 2019;10:1776.
3. Chang CC, Chow CC, Tellier LC, Vattikuti S, Purcell SM, Lee JJ. Second-generation PLINK: rising to the challenge of larger and richer datasets. GigaScience. 2015;4:7.
