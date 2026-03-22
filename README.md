* Overview:
This repository presents a novel deep learning framework for multi-omics data integration aimed at improving cancer prognosis prediction.
The proposed architecture combines:
- Autoencoders (CIAE)
- Causal Discovery (DirectLiNGAM)
- Causal Neural Networks (CausalNN)
- Evolutionary Game Theory (EGT)

The main objective is to identify optimal omics combinations (strategies) and improve predictive performance while preserving causal and non-linear relationships.

** Architecture:

The pipeline consists of the following steps:
1- Dimensionality Reduction:
    - Autoencoder (AE / VAE / Contrastive AE)
    - Latent space selection using the elbow method
2- Causal Discovery
    - Learn causal graph from latent representations
    - Methods: DirectLiNGAM / DAG-GNN
3- Causal Representation Learning:
    - CausalNN trained using adjacency matrix
    - Captures causal dependencies between features
4- Evolutionary Game Theory (EGT):
    - Each omics modality = strategy
    - Mixed strategies = omics combinations
    - Fitness = prediction performance
*** Data:
  - Source: TCGA (via Firebrowse):
      - Modalities:
        - mRNA expression
        - DNA methylation
        - RPPA
        - Mutation data
        - Clinical data
  - Preprocessing steps:
      - Z-score normalization
      - Feature filtering
