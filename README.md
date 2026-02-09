# Benchmarking Deep Generative Models and Classical Baselines for Single-Cell Analysis of Peripheral Blood and Thymic Tissues in Myasthenia Gravis

**Course:** Applied Data Science for Computational Biology @ Columbia University  
**Team:** María Dolores Navarro Maturana, Daria Lykova, Yitian Tan

## Project Overview
This project presents a systematic benchmarking of representation-learning methods for single-cell RNA sequencing (scRNA-seq) data in the context of Myasthenia Gravis (MG). We analyzed two distinct biological environments: **Peripheral Blood Mononuclear Cells (PBMCs)** and **Thymic Tissue**.

The goal was to evaluate whether deep generative models (like scVI) provide tangible advantages over classical linear baselines (PCA) and probabilistic factor models (MOFA+) when recovering immune cell identities and disease-associated structures.

## Key Objectives
1.  **Benchmarking:** Compare PCA, MOFA+, and scVI across diverse datasets.
2.  **Biological Context:** Analyze immune dysregulation in MG patients vs. healthy controls.
3.  **Evaluation:** Assess model performance using quantitative metrics (Silhouette Score, ARI, NMI) and qualitative visualization (UMAP).

## Methodology & Tech Stack
* **Language:** Python
* **Libraries:** Scanpy, scvi-tools, mofapy2, AnnData, Matplotlib/Seaborn.
* **Data Sources:**
    * *PBMC:* Okuzono et al., 2024 (MG & Healthy controls).
    * *Thymus:* Joint analysis of MG Thymus (Broad Institute) and Healthy Human Thymus Atlas (Yayon et al., 2024).

### Models Implemented
* **PCA (Principal Component Analysis):** Used as a linear baseline.
* **scVI (Single-cell Variational Inference):** A deep generative model using variational autoencoders (VAE) to model technical noise.
* **MOFA+ (Multi-Omics Factor Analysis):** A Bayesian factor model used for the complex Thymus dataset.

## Key Findings
* **PBMC Analysis:** The immune populations in PBMCs were well-defined and nearly linearly separable. Consequently, **PCA** outperformed scVI in clustering metrics (ARI, NMI), as scVI tended to smooth fine-grained subtype boundaries.
* **Thymus Analysis:** In the more heterogeneous thymic tissue, **PCA and MOFA+** maintained better global cell-type separation compared to scVI. While scVI is powerful for denoising and continuous trajectories, the classical baselines were more effective at preserving discrete cell-type annotations in this specific context.

## Contributors
* **María Dolores Navarro Maturana** (SPS, Columbia University)
* **Daria Lykova** (Columbia College, Columbia University)
* **Yitian Tan** (SEAS, Columbia University)

---
*Note: This project was conducted as the final capstone for the Applied Data Science for Computational Biology class.*
