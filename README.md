# Breast Cancer Genomics Analysis — TCGA-BRCA

## Abstract

Breast cancer remains one of the most prevalent malignancies worldwide, with molecular heterogeneity posing a significant challenge for diagnosis and treatment. This project presents a comprehensive genomics analysis of breast invasive carcinoma (BRCA) using publicly available data from The Cancer Genome Atlas (TCGA), integrating transcriptomic profiling via RNA-Seq and structural genomic characterization via Copy Number Variation (CNV) analysis.

The transcriptomic pipeline applied eleven independent feature selection methods to 20,531 genes across approximately 1,200 tumor and 100 normal samples, identifying a consensus set of 20 biomarker genes with strong discriminative power between tumor and normal tissue. These biomarkers — including well-characterized cancer-associated genes such as CAV1, MME, and LMOD1 — were subsequently used to train and evaluate five machine learning classifiers, with Random Forest achieving the highest cross-validation AUC. Near-perfect classification performance on the held-out test set confirmed the generalizability of the identified biomarkers.

To explore hidden biological substructure without relying on labels, ten unsupervised clustering algorithms were applied to the top 100 ranked genes. Across partitional, hierarchical, density-based, model-based, graph-based, and neural approaches, the dominant axis of variation consistently separated tumor from normal samples in PCA space, independently corroborating the supervised findings.

The CNV analysis revealed chromosome-level amplification and deletion patterns consistent with established BRCA genomic signatures. Most notably, amplification of chromosome 8 — harboring the MYC oncogene — and deletion of chromosome 13 — harboring BRCA2 — were independently reproduced from raw segmentation data, validating the biological integrity of the analysis.

Together, these results demonstrate that expression-level and structural genomic data independently converge on the same biological conclusion: breast cancer tumor samples carry a distinct and reproducible molecular signature separable from normal tissue using computational methods alone.

---

**Dataset:** TCGA-BRCA (GDC Data Portal)  
**Language:** R  
**Key Libraries:** `caret`, `randomForest`, `cluster`, `dbscan`, `mclust`, `kohonen`, `pheatmap`
