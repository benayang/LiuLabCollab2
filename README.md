# LiuLabCollab2

## 1. QC

**1a. Count distributions before and after filtering**

The log-transformed cpm values are ![here.](https://github.com/benayang/LiuLabCollab2/blob/main/lcpm_filt.csv)

<p align="center">
<img src="https://github.com/benayang/LiuLabCollab2/blob/main/Plots/count_distributions.png" width=50% height=50%>
</p>

**1b. Library Size**

<p align="center">
<img src="https://github.com/benayang/LiuLabCollab2/blob/main/Plots/RNAseqlibsize.png" width=50% height=50%>
</p>

**1c. Sample correlations**

| Pearson | Spearman |
| -------- | ---------- |
| ![](https://github.com/benayang/LiuLabCollab2/blob/main/Plots/pearson_hmp.png) | ![](https://github.com/benayang/LiuLabCollab2/blob/main/Plots/spearman_hmp.png) |

## 2. PCA

**2a. Plot**

PC1 separates 0 psi samples from the 4 psi samples. The 2 psi samples with BMP2 treatment clusters with the 0 psi samples.

<p align="center">
<img src="https://github.com/benayang/LiuLabCollab2/blob/main/Plots/pca.png" width=50% height=50%>
</p>

**2b. PCA Loadings**
Genes that separate samples along each PC. Genes with positive values push samples along the positive direction of each PC and vice versa. 

| | | | |
| --- | --- | --- | --- | 
| **Gene symbols** | ![](https://github.com/benayang/LiuLabCollab2/blob/main/Plots/pca_loadings_sym.png) | 
| **Ensembl IDs** | ![](https://github.com/benayang/LiuLabCollab2/blob/main/Plots/pca_loadings_ens.png) |

## 3. Reactome GSVA
Instead of differential gene expression analysis, we can score each sample by their expression of gene sets. Here, I've scored each sample how much they up/downregulate terms from the Reactome database. Positive scores indicate upregulation of the pathway (left plot). Next, I clustered the terms by the correlation of their scores (right plot). This might help you interpret the scoring results by seeing which pathways are going up or down in each sample. The clustering results are ![here.](https://github.com/benayang/LiuLabCollab2/blob/main/gsva_reactome_clusters_df.tsv)

| Reactome scores | Reactome clusters |
| -------- | ---------- |
| ![](https://github.com/benayang/LiuLabCollab2/blob/main/Plots/gsva_degPattern_hmp.png) | ![](https://github.com/benayang/LiuLabCollab2/blob/main/Plots/gsva_degPattern.png) |