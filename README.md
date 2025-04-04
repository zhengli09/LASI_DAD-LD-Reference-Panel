# LASI-DAD LD Reference Panel
<img src="https://github.com/zhengli09/LASI_DAD-LD-Reference-Panel/blob/main/LASI_DAD_logo.png" alt="Alt text" style="width:100px;">

This repository contains linkage disequilibrium (LD) resources estimated using high-coverage (30×) whole-genome sequencing (WGS) data from 2,680 Indian samples in the Longitudinal Aging Study in India-Diagnostic Assessment of Dementia (LASI-DAD) study. To use LASI-DAD as an imputation reference panel, please refer to the [Michigan imputation server](https://imputationserver.sph.umich.edu/#!). These resources come with the upcomping paper:

> Zheng Li, Wei Zhao, Xiang Zhou, Priya Moorjani, Yuk Yee Leung, Gerard D. Schellenberg,
> Li-San Wang, Sharmistha Dey, Aparajit B Dey, Jinkook Lee, Jennifer A. Smith,
> Sharon L.R. Kardia. A reference panel for linkage disequilibrium and genotype imputation
> using whole-genome sequencing data from 2,680 LASI-DAD participants across India. (2025+)

The specific LD resources include:
1. Broad-scale LD blocks estimated by LDetect and fine-scale LD blocks estimated by BigLD
2. Variation in LD (varLD) scores that evaluated the regional differences in LD between the LASI-DAD population and four super-populations from the 1000 Genomes Project (1000G), including the African (AFR), European (EUR), South Asian (SAS), and East Asian (EAS) populations. varLD scores were also evaluated across three Indian sub-populations from LASI-DAD.
3. An LD lookup panel that calculated various LD statistics, including the squared Pearson correlation coefficient (r2) between the phased haplotypes and D-prime statistic (D’), for all pairs of genetic variants within 1 Mb of each other, with pairs of variants having r2 ≥ 0.2 reported in the lookup panel.
4. LD matrices for the polygenic risk score (PRS) analysis. The data is in the HDF5 format that can be directly used by [PRS-CS](https://github.com/getian107/PRScs).

## LD blocks
[[Download LDetect Blocks]](https://www.dropbox.com/scl/fo/psu2w8yghmm2swcg032l2/AOxm7DgMPmFBIUSqkG-q5Mw?rlkey=yxticyc94yswpr172zup7zbbh&st=haoo74dx&dl=1)
[[Download BigLD Blocks]](https://www.dropbox.com/scl/fo/bb3ahvza2zkf3dq6u2v4j/AJJ1k7yBxqIlTStYW9d59g4?rlkey=cg1ablo8h4wchhtyzvotqn555&st=ewlqgvre&dl=1)

For LDetect blocks, columns of each file indicate the chromosome number, starting position of the block, and ending position of the block. For BigLD blocks, each file is in the RDS format that can be read by R with the function `readRDS`. The columns indicate the chrmosome number, indeces of the two boundary SNPs in the genotype data, SNP IDs of the two boundary SNPs, starting position of the block, ending position of the block, number of SNPs with a MAF ≥ 1% in the block, and the length of the LD block. BigLD blocks were also estimated in the four super-populations from the 1000 Genomes Project, in addition to the LASI-DAD population.

## varLD scores
- [[Download]](https://www.dropbox.com/scl/fo/xzhobzwr9fn023vg26q4e/ADGiSW3joiceXjQBrOhSTW0?rlkey=3caqdw1alxssh66fxfd57cm48&st=mimv66jm&dl=1) varLD scores evaluated between LASI-DAD and each of the four super-populations from 1000G. Columns in the file indicate the starting position and ending postion of the evaluated genomic window, varLD scores with respect to the AFR, EAS, EUR, or SAS population from 1000G, Pearson correlation coefficients of MAFs between LASI-DAD and the AFR, EAS, EUR, or SAS population from 1000G.
- [[Download]](https://www.dropbox.com/scl/fo/woh72e6yg6k3mklgddtxa/AEH5ZnjptX6JMtK_vtusmu8?rlkey=llst6ib19zp9xbogghgq6yr0p&st=8mlhbs8r&dl=1) varLD scores evaluated across three LASI-DAD sub-populations defined according to cline and proportion of Ancestral North Indian (%ANI) values. Columns in the file indicate the starting position and ending postion of the evaluated genomic window, varLD scores between the high %ANI group and low %ANI group, high %ANI group and the out-of-cline group, low %ANI group and the out-of-cline group.

## LD lookup panel
In the LD lookup panel, each file contains LD statistics for a single chromosome, with each row corresponding to a pair of variants. Columns of the file indicate the chromosome number (CHROM), genomic positions of the two variants (POS1, POS2), r2 statistic (R2), D' statistic (Dprime), variant IDs (variant1, variant2), allele frequencies of the alternative alleles (AF1, AF2), reference alleles (REF1, REF2), sign of the Pearson correlation coefficient between the phased haplotypes (Sign), and alternative alleles (ALT1, ALT2). <br>
[[Download Chrmosome 1]](https://www.dropbox.com/scl/fi/p7o1vgk62xsgimoroi9eq/chr1_ld.csv.gz?rlkey=c54pg99llygjr6fi2pyy4x5d0&st=pqifkum2&dl=1)(~1.2GB)<br>
[[Download Chrmosome 2]](https://www.dropbox.com/scl/fi/y236rldkwnmcdsa6y6z4o/chr2_ld.csv.gz?rlkey=qbceb8y1xgu0o88gvp66i2e2g&st=7hjepfuj&dl=1)(~1.4GB)<br>
[[Download Chrmosome 3]](https://www.dropbox.com/scl/fi/njefljx2n33ck9aqdt37e/chr3_ld.csv.gz?rlkey=uanf9ttwco8x5mj6ov62yrn2t&st=nguqwkmh&dl=1)(~1.3GB)<br>
[[Download Chrmosome 4]](https://www.dropbox.com/scl/fi/32ol3kq4rld0785kyb0p7/chr4_ld.csv.gz?rlkey=fun7wt3gt0uw8msoe4xugou00&st=98bgoth5&dl=1)(~1.4GB)<br>
[[Download Chrmosome 5]](https://www.dropbox.com/scl/fi/n68umm3lngk46yky8rj5s/chr5_ld.csv.gz?rlkey=1qdiwlmnc5j33jygoxqnc4nrb&st=3mhepxr5&dl=1)(~1.2GB)<br>
[[Download Chrmosome 6]](https://www.dropbox.com/scl/fi/fmztyed7zv43vk73z6ln7/chr6_ld.csv.gz?rlkey=8ggrxtoqmki3md6x4ssaihdc9&st=235o46xs&dl=1)(~1.5GB)<br>
[[Download Chrmosome 7]](https://www.dropbox.com/scl/fi/tlcdq01xtreemtnmpqji5/chr7_ld.csv.gz?rlkey=1vd03uyfyj7l181lb9svli0z5&st=t7wjm5nx&dl=1)(~1021MB)<br>
[[Download Chrmosome 8]](https://www.dropbox.com/scl/fi/8wbyvxpazyy05cugk65a2/chr8_ld.csv.gz?rlkey=xawnp8we3pn8vp9l4tkhqtgbb&st=75313oy5&dl=1)(~1.1GB)<br>
[[Download Chrmosome 9]](https://www.dropbox.com/scl/fi/byxeglc3h3yq59ss5ufed/chr9_ld.csv.gz?rlkey=82nr100mz59bw3p2vnixk0jnm&st=l75xd6pc&dl=1)(~720MB)<br>
[[Download Chrmosome 10]](https://www.dropbox.com/scl/fi/xkvgcz7osganezpoz3lwt/chr10_ld.csv.gz?rlkey=6ng6nxgnplz5q22d32m11e68f&st=224hpnk9&dl=1)(~918MB)<br>
[[Download Chrmosome 11]](https://www.dropbox.com/scl/fi/382kt19gkr4aqc9e5pbtj/chr11_ld.csv.gz?rlkey=whi6ytz9ta6qpagsir1p84gvt&st=50sjjf6x&dl=1)(~1.1GB)<br>
[[Download Chrmosome 12]](https://www.dropbox.com/scl/fi/0zashqe7y1bbj2bku8oa5/chr12_ld.csv.gz?rlkey=bat5sz25s3mr31yjh6mbf9urt&st=tjcix9hj&dl=1)(~776MB)<br>
[[Download Chrmosome 13]](https://www.dropbox.com/scl/fi/8zs28r4ou41smvjx5v4z5/chr13_ld.csv.gz?rlkey=qxczjhnvzivu933hmo7ts6xkh&st=zfrd3fj7&dl=1)(~612MB)<br>
[[Download Chrmosome 14]](https://www.dropbox.com/scl/fi/6bju3zfsyx2qyt7l00ly8/chr14_ld.csv.gz?rlkey=sh5rn0jfrt2my8w98ao99isv7&st=kg75jsqe&dl=1)(~562MB)<br>
[[Download Chrmosome 15]](https://www.dropbox.com/scl/fi/ovw69qti0a9pmjuz7aac0/chr15_ld.csv.gz?rlkey=5fudihdpzjptmvw3yfv87409c&st=3o59f52m&dl=1)(~463MB)<br>
[[Download Chrmosome 16]](https://www.dropbox.com/scl/fi/b1ali932nvdw5hir05xqi/chr16_ld.csv.gz?rlkey=8x5v8aae0jlnjq221fkwozgmp&st=n4hhdg73&dl=1)(~497MB)<br>
[[Download Chrmosome 17]](https://www.dropbox.com/scl/fi/kcg2cu7ccluwoo750rzql/chr17_ld.csv.gz?rlkey=j1x3c80a0q7dr2f6g3nmq1wql&st=8xgqpn3e&dl=1)(~467MB)<br>
[[Download Chrmosome 18]](https://www.dropbox.com/scl/fi/1mzdjybpy7d96bkxghfhc/chr18_ld.csv.gz?rlkey=lw18ts7wcwh52172qypiqr9q9&st=93d5mo3n&dl=1)(~422MB)<br>
[[Download Chrmosome 19]](https://www.dropbox.com/scl/fi/m4o2eleda1kix8ebbqmj7/chr19_ld.csv.gz?rlkey=g5zbomk33j6wst60eyo7ba4r7&st=d0nf3j9p&dl=1)(~357MB)<br>
[[Download Chrmosome 20]](https://www.dropbox.com/scl/fi/n8ni36grfkd55hs2re3ez/chr20_ld.csv.gz?rlkey=my4375ago4lzghxpnrhfn0f6f&st=etnstqwl&dl=1)(~338MB)<br>
[[Download Chrmosome 21]](https://www.dropbox.com/scl/fi/lzjt670dt0ngqu7loix1i/chr21_ld.csv.gz?rlkey=ispvrcadteqsu6asjdsyk29z6&st=byxm13y6&dl=1)(~189MB)<br>
[[Download Chrmosome 22]](https://www.dropbox.com/scl/fi/qmc0ovc9evd71os9nsc8a/chr22_ld.csv.gz?rlkey=clb5hy36jgc88n0vnt92b1gvh&st=1q9pkqvb&dl=1)(~177MB)<br>

## LD matrices
[[Download]](https://www.dropbox.com/scl/fo/h5qcxre4nqkx9se9mexbv/AH0e6kOW9LWjFTJFRjjIL1w?rlkey=pvxb5uslsgvrbi5rekltgkzvo&st=yxnl5fwg&dl=1)(~7.1GB)<br>
This panel can be directly used in the PRS analysis for GWAS of Indian or generally the South Asian ancestry. The files are in HDF5 format and a SNP information file is also included.
