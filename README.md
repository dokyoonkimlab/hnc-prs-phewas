# hnc-prs-phewas
Polygenic risk score models for head and neck squamous cell carcinoma

### Head and neck squamous cell carcinoma - 972,182 variants
> [GAME-ON_HNC-all_PRSCS_auto.zip](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/GAME-ON_HNC-all_PRSCS_auto.zip)

### Oral cavity cancer - 972,182 variants
> [GAME-ON_HNC-OC_PRSCS_auto.zip](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/GAME-ON_HNC-OC_PRSCS_auto.zip)

### Oropharynx cancer - 972,182 variants
> [GAME-ON_HNC-OPC_PRSCS_auto.zip](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/GAME-ON_HNC-OPC_PRSCS_auto.zip)

---

## Descriptions. 

To generate polygenic risk score (PRS), we utilized the GWAS summary statistics from the Genetic Associations and Mechanisms in Oncology (GAME-ON) Network (https://epi.grants.cancer.gov/gameon/). The HNSCC, OPC, and OC cases were identified based on following ICD-10 codes: oral cavity (C02.0–C02.9, C03.0–C03.9, C04.0–C04.9 and C05.0–C06.9) and oropharynx (C01.9, C02.4 and C09.0–C10.9). The GWASs (HNSCC [5,974 cases and 4,012 controls], OPC [2,617 cases and 4,012 controls], and OC [2,958 cases and 4,012 controls]). The GWASs were performed using PLINK 1.90 with sex, age, 10 PCs, and genotyping batch as covariates. The genotype data for the oral and pharyngeal OncoArray study can be downloaded from the database of Genotypes and Phenotypes (dbGaP) under accession phs001202.v1.p1. Of note, the GWASs did not include the additional external controls (2,476 shared controls [1,453 from the EPIC study and 1,023 from the Toronto study]) beyond the GAME-ON data used by Lesseur, Corina, et al. in their GWAS analysis.

We constructed PRSs for HNSCC, OPC, and OC by using a Bayesian polygenic prediction method, PRS-CS, which infers the posterior mean effect size of each variant using the linkage disequilibrium (LD) reference panel and GWAS summary. The 1000G Project phase 3 EUR data was used to be the external LD reference panel. The posterior SNP effect sizes in PRS-CS were inferred from GAME-ON summary statistics, with default settings, and automatic estimation of the global shrinkage parameter (PRS-CS-auto). The individual PRSs were computed from beta coefficients as the weighted sum of the risk alleles by applying PLINK version 1.90 with the –score command.

Reference
*Lee, Y. C., *Jung, S. H., Shivakumar, M., Cha, S., Park. Y. W., … & Kim, D. (2024) Polygenic risk score-based phenome-wide association study of head and neck cancer across two large biobanks. 
