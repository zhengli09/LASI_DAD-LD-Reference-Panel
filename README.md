# LASI-DAD LD Reference Panel
<img src="https://github.com/zhengli09/LASI_DAD-LD-Reference-Panel/blob/main/LASI_DAD_logo.png" alt="Alt text" style="width:100px;">

This repository contains linkage disequilibrium (LD) resources estimated using high-coverage (30×) whole-genome sequencing (WGS) data from 2,680 Indian samples in the Longitudinal Aging Study in India-Diagnostic Assessment of Dementia (LASI-DAD) study. To use LASI-DAD as an imputation reference panel, please refer to the [Michigan imputation server](https://imputationserver.sph.umich.edu/#!). These resources come with the upcomping paper:

> Li, Z. et al. A reference panel for linkage disequilibrium and genotype imputation
> using whole-genome sequencing data from 2,680 LASI-DAD participants across India

The specific LD resources include:
1. Broad-scale LD blocks estimated by LDetect and fine-scale LD blocks estimated by BigLD
2. Variation in LD (varLD) scores that evaluated the regional differences in LD between the LASI-DAD population and four super-populations from the 1000 Genomes Project (1000G), including the African (AFR), European (EUR), South Asian (SAS), and East Asian (EAS) populations. varLD scores were also evaluated across three Indian sub-populations from LASI-DAD.
3. An LD lookup panel that calculated various LD statistics, including the squared Pearson correlation coefficient (r2) between the phased haplotypes and D-prime statistic (D’), for all pairs of genetic variants within 1 Mb of each other, with pairs of variants having r2 ≥ 0.2 reported in the lookup panel.
4. An LD reference panel for the polygenic risk score (PRS) analysis. The panel is in the HDF5 format that can be directly used by [PRS-CS](https://github.com/getian107/PRScs).

## LD blocks
[[Download LDetect Blocks]](https://www.dropbox.com/scl/fo/psu2w8yghmm2swcg032l2/AOxm7DgMPmFBIUSqkG-q5Mw?rlkey=f60seqkban8ofxb7wb2uexfh8&st=mh0e84jf&dl=1)
[[Download BigLD Blocks]](https://www.dropbox.com/scl/fo/bb3ahvza2zkf3dq6u2v4j/AJJ1k7yBxqIlTStYW9d59g4?rlkey=vn9q19trgcu08xsxa2fkj7avi&st=gp4bhno0&dl=1)

For LDetect blocks, columns of each file indicate the chromosome number, starting position of the block, and ending position of the block. For BigLD blocks, each file is in the RDS format that can be read by R with the function `readRDS`. The columns indicate the chrmosome number, indeces of the two boundary SNPs in the genotype data, SNP IDs of the two boundary SNPs, starting position of the block, ending position of the block, number of SNPs with a MAF ≥ 1% in the block, and the length of the LD block. BigLD blocks were also estimated in the four super-populations from the 1000 Genomes Project, in addition to the LASI-DAD population.

## varLD scores
- [[Download]](https://www.dropbox.com/scl/fo/xzhobzwr9fn023vg26q4e/ADGiSW3joiceXjQBrOhSTW0?rlkey=oz9yet5avqndezh14c45dhj58&st=u7i0x55e&dl=1) varLD scores evaluated between LASI-DAD and each of the four super-populations from 1000G. Columns in the file indicate the starting position and ending postion of the evaluated genomic window, varLD scores with respect to the AFR, EAS, EUR, or SAS population from 1000G, Pearson correlation coefficients of MAFs between LASI-DAD and the AFR, EAS, EUR, or SAS population from 1000G.
- [[Download]](https://www.dropbox.com/scl/fo/woh72e6yg6k3mklgddtxa/AEH5ZnjptX6JMtK_vtusmu8?rlkey=y3eea9yl9t8iuqcb4t4wwptyx&st=m4tu4hpq&dl=1) varLD scores evaluated across three LASI-DAD sub-populations defined according to cline and proportion of Ancestral North Indian (%ANI) values. Columns in the file indicate the starting position and ending postion of the evaluated genomic window, varLD scores between the high %ANI group and low %ANI group, high %ANI group and the out-of-cline group, low %ANI group and the out-of-cline group.

## LD lookup panel
[[Download Chrmosome 1]](https://www.dropbox.com/scl/fi/p7o1vgk62xsgimoroi9eq/chr1_ld.csv.gz?rlkey=c54pg99llygjr6fi2pyy4x5d0&st=5ultde2b&dl=1)(~1.2GB)<br>
[[Download Chrmosome 2]](https://www.dropbox.com/scl/fi/y236rldkwnmcdsa6y6z4o/chr2_ld.csv.gz?rlkey=qbceb8y1xgu0o88gvp66i2e2g&st=rd7r64na&dl=1)(~1.4GB)<br>
[[Download Chrmosome 3]](https://www.dropbox.com/scl/fi/njefljx2n33ck9aqdt37e/chr3_ld.csv.gz?rlkey=uanf9ttwco8x5mj6ov62yrn2t&st=4nxt5hmh&dl=1)(~1.3GB)<br>
[[Download Chrmosome 4]](https://www.dropbox.com/scl/fi/32ol3kq4rld0785kyb0p7/chr4_ld.csv.gz?rlkey=fun7wt3gt0uw8msoe4xugou00&st=pfkv6b3b&dl=1)(~1.4GB)<br>
[[Download Chrmosome 5]](https://www.dropbox.com/scl/fi/n68umm3lngk46yky8rj5s/chr5_ld.csv.gz?rlkey=1qdiwlmnc5j33jygoxqnc4nrb&st=izma8qr3&dl=1)(~1.2GB)<br>
[[Download Chrmosome 6]]()(~1.5GB)<br>
[[Download Chrmosome 7]]()(~1021MB)<br>
[[Download Chrmosome 8]]()(~1.1GB)<br>
[[Download Chrmosome 9]]()(~720MB)<br>
[[Download Chrmosome 10]]()(~918MB)<br>
[[Download Chrmosome 11]]()(~1.1GB)<br>
[[Download Chrmosome 12]]()(~776MB)<br>
[[Download Chrmosome 13]]()(~612MB)<br>
[[Download Chrmosome 14]]()(~562MB)<br>
[[Download Chrmosome 15]]()(~463MB)<br>
[[Download Chrmosome 16]]()(~497MB)<br>
[[Download Chrmosome 17]]()(~467MB)<br>
[[Download Chrmosome 18]]()(~422MB)<br>
[[Download Chrmosome 19]]()(~357MB)<br>
[[Download Chrmosome 20]]()(~338MB)<br>
[[Download Chrmosome 21]]()(~189MB)<br>
[[Download Chrmosome 22]]()(~177MB)<br>

## LD reference panel
[[Download]]()(~7.1GB)<br>
This panel can be directly used in the PRS analysis for GWAS of Indian or generally the South Asian ancestry. The files are in HDF5 format and a SNP information file is also included.
