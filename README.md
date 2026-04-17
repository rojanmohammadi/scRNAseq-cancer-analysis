# scRNAseq-cancer-analysis



## 🧬 Project Overview

This project explores the analysis of **single-cell RNA sequencing (scRNA-seq)** and **spatial omics data** in the context of cancer research.  

The work follows a complete computational pipeline from **raw data processing to biological interpretation**, integrating both single-sample and multi-sample workflows, and extending into **trajectory inference and spatial analysis**.



## 🎯 Aims

- To develop a strong understanding of **single-cell omics technologies**
- To apply **computational pipelines** for analysing scRNA-seq data
- To explore how **cellular heterogeneity** drives cancer biology
- To investigate **spatial organisation and cell-cell interactions** in tumour environments



## 📌 Objectives

- Understand the principles of **single-cell omics and spatial omics**
- Perform **end-to-end scRNA-seq analysis**
- Apply **multi-sample integration techniques**
- Identify **cell clusters and biological functions**
- Conduct **trajectory (pseudotime) analysis**
- Perform **cell-cell communication analysis**
- Analyse **spatial transcriptomics data**



## ⚙️ Methods & Workflow

### 🧪 Single-Cell RNA-seq Pipeline

The analysis follows a standard Scanpy-based workflow:

1. **Data Loading & QC**
   - Filtering low-quality cells
   - Removing genes expressed in few cells
   - Mitochondrial and ribosomal QC metrics

2. **Normalisation**
   - Library size normalisation (10,000 counts per cell)
   - Log transformation

3. **Feature Selection**
   - Highly Variable Genes (HVGs)

4. **Dimensionality Reduction**
   - PCA
   - Selection of optimal PCs

5. **Clustering**
   - Neighbour graph construction
   - Leiden clustering (multiple resolutions)

6. **Visualisation**
   - UMAP embedding
   - Feature plots
   - Sample/condition comparison



### 🔗 Multi-Sample Integration

- Integration of multiple datasets using:
  - Batch correction (e.g., Harmony)
- Recomputed:
  - PCA
  - Neighbour graph
  - UMAP



### 🧠 Downstream Analysis

#### 📍 Cell Annotation
- Assigning biological identities to clusters using marker genes

#### 📈 Trajectory Analysis (Pseudotime)
- Modelling dynamic transitions between cell states  
- Example: epithelial → mesenchymal transition (EMT)

👉 Key insight:
- Some genes are only expressed in **transient states**
- These would be **missed in bulk RNA-seq**



### 🔬 Cell–Cell Communication

Method used: **CellPhoneDB**

- Based on ligand–receptor interactions
- Uses permutation testing for significance
- Outputs:
  - Interaction networks
  - Heatmaps

⚠️ Limitation:
- Based on RNA, not protein
- No spatial context



### 🧭 Spatial Omics Analysis

#### Sequencing-based:
- **10x Visium**
  - Whole transcriptome
  - Lower resolution (multi-cell spots)

#### Imaging-based:
- **Xenium**
  - Single-cell resolution
  - Limited gene panel



### 📍 Spatial Analysis Methods

- Cell segmentation
- Clustering and phenotyping
- Spatial proximity analysis:
  - Distance-based metrics
  - Permutation testing



## 🧠 Key Insights

- Single-cell analysis reveals **cellular heterogeneity**
- Trajectory analysis captures **dynamic biological processes**
- Bulk RNA-seq fails to detect **transient gene expression**
- Spatial omics provides **contextual tissue organisation**
- Integration is critical for **multi-sample consistency**



## ⚠️ Challenges & Considerations

- Dropout effects in scRNA-seq
- Doublets and mixed signals
- Ambiguous cell annotations
- Lack of spatial information in some methods



## 🛠️ Skills Demonstrated

- Single-cell data analysis (Scanpy)
- Data preprocessing and QC
- Dimensionality reduction (PCA, UMAP)
- Clustering (Leiden)
- Batch correction (Harmony)
- Trajectory inference
- Cell–cell communication analysis
- Spatial transcriptomics analysis


