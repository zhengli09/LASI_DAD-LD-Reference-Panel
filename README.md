# LASI-DAD LD Reference Panel
<img src="https://github.com/zhengli09/LASI_DAD-LD-Reference-Panel/blob/main/LASI_DAD_logo.png" alt="Alt text" style="width:100px;">
This repository contains linkage disequilibrium (LD) resources estimated using high-coverage (30×) whole-genome sequencing (WGS) data from 2,680 Indian samples in the Longitudinal Aging Study in India-Diagnostic Assessment of Dementia (LASI-DAD) study. These resources come with the upcomping paper:

> Li, Z. A reference panel for linkage disequilibrium and genotype imputation
> using whole-genome sequencing data from 2,680 LASI-DAD participants across India

The specific resources include:
1. Broad-scale LD blocks estimated by LDetect and fine-scale LD blocks estimated by BigLD
2. Variation in LD (varLD) scores that evaluated the regional differences in LD between the LASI-DAD population and four super-populations from the 1000 Genomes Project (1000G), including the African, European, South Asian, and East Asian populations. varLD scores were also evaluated across three Indian sub-populations from LASI-DAD.
3. An LD lookup panel that calculated various LD statistics, including the squared Pearson correlation coefficient (r2) between the phased haplotypes and D-prime statistic (D’), for all pairs of genetic variants within 1 Mb of each other, with pairs of variants having r2 ≥ 0.2 reported in the lookup panel.
4. An LD reference panel for the polygenic risk score (PRS) analysis. The panel is in the HDF5 format that can be directly used by [PRS-CS](https://github.com/getian107/PRScs).

## LD blocks
[[Download LDetect Blocks]](https://www.dropbox.com/scl/fo/psu2w8yghmm2swcg032l2/AOxm7DgMPmFBIUSqkG-q5Mw?rlkey=f60seqkban8ofxb7wb2uexfh8&st=mh0e84jf&dl=1)
[[Download BigLD Blocks]](https://www.dropbox.com/scl/fo/bb3ahvza2zkf3dq6u2v4j/AJJ1k7yBxqIlTStYW9d59g4?rlkey=vn9q19trgcu08xsxa2fkj7avi&st=gp4bhno0&dl=1)

For LDetect blocks, columns of each file indicate the chromosome number, starting position of the block, and ending position of the block. For BigLD blocks, each file is in the RDS format that can be read by R with the function `readRDS`. The columns indicate the chrmosome number, indeces of the two boundary SNPs in the genotype data, SNP IDs of the two boundary SNPs, starting position of the block, ending position of the block, number of SNPs with a MAF ≥ 1% in the block, and the length of the LD block. BigLD blocks were also estimated in the four super-populations from the 1000 Genomes Project, in addition to the LASI-DAD population.
