# LASI-DAD LD Reference Panel
<img src="https://github.com/zhengli09/LASI_DAD-LD-Reference-Panel/blob/main/LASI_DAD_logo.png" alt="Alt text" style="width:100px;">
This repository contains linkage disequilibrium (LD) resources estimated using high-coverage (30×) whole-genome sequencing (WGS) data from 2,680 Indian samples in the Longitudinal Aging Study in India-Diagnostic Assessment of Dementia (LASI-DAD) study. These resources come with the upcomping paper:

> Li, Z. A reference panel for linkage disequilibrium and genotype imputation
> using whole-genome sequencing data from 2,680 LASI-DAD participants across India

The specific resources include:
1. Broad-scale LD blocks estimated by LDetect and fine-scale LD blocks estimated by BigLD
3. Variation in LD (varLD) scores that evaluated the regional differences in LD between the LASI-DAD population and four super-populations from the 1000 Genomes Project (1000G), including the African, European, South Asian, and East Asian populations. varLD scores were also evaluated across three Indian sub-populations from LASI-DAD.
4. An LD lookup panel that calculated various LD statistics, including the squared Pearson correlation coefficient (r2) between the phased haplotypes and D-prime statistic (D’), for all pairs of genetic variants within 1 Mb of each other, with pairs of variants having r2 ≥ 0.2 reported in the lookup panel.
5. An LD reference panel for the polygenic risk score (PRS) analysis. The panel is in the HDF5 format that can be directly used by [PRS-CS](https://github.com/getian107/PRScs).
