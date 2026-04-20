# 🧬 Identifying Overlapping Gene Expression and Biological Processes Between GDM and PPH

## 📌 Overview
This project investigates potential shared biological mechanisms between **Gestational Diabetes Mellitus (GDM)** and **Postpartum Hemorrhage (PPH)** using RNA-seq data analysis and network-based methods. 
While direct gene overlap between the two conditions was limited, this study explores whether shared pathways and biological processes emerge through systems-level analysis.

---

## 🔬 Objectives
- Identify differentially expressed genes (DEGs) in GDM samples  
- Compare GDM-associated genes with curated PPH gene sets  
- Explore shared biological patterns using network-based modeling  
- Investigate overlapping biological processes, phenotypes, and diseases  

---

## 🧪 Methods

### 1. RNA-seq Processing & Data Preparation
- Retrieved raw RNA-seq data from GEO (GSE203346)  
- Constructed gene-level count matrices from transcript-level data  
- Mapped transcript IDs to gene IDs using Ensembl annotations  
- Built and aligned metadata (condition, tissue type)

### 2. Quality Control & Normalization
- Assessed technical variation (GC content, gene length bias)  
- Applied within-lane and between-lane normalization (EDASeq)  
- Evaluated data quality using boxplots, mean-variance plots, and PCA  

### 3. Differential Expression Analysis
- Performed differential expression analysis using DESeq2  
- Identified significant genes (adjusted p-value < 0.05)  
- Conducted tissue-specific analysis (placenta vs. umbilical cord)

### 4. Data Integration (GDM vs PPH)
- Curated PPH-associated genes from protein and gene lists  
- Standardized identifiers (SYMBOL, ENSEMBL, ENTREZ)  
- Compared gene sets across conditions  

### 5. ML & Network-Based Analysis
- Applied GenePlexus (PPI-based supervised ML tool)  
- Predicted functionally related genes for each condition  
- Compared predicted gene sets, similar diseases, and biological processes  

### 6. Visualization
- Volcano plots, MA plots, PCA  
- Venn diagrams for overlap analysis  
- Word clouds for shared biological processes  

---

## 🔍 Key Findings
- No direct gene overlap between GDM and PPH was observed  
- Network-based predictions revealed shared biological processes and disease associations  
- Systems-level analysis provided insight beyond gene-level comparisons  

---

## 🧠 Key Takeaway
This project highlights the importance of **network-based and systems-level approaches** when studying complex diseases, especially when direct gene overlap is limited. 
It demonstrates how integrating multi-source biological data and applying computational methods can uncover hidden relationships between conditions.

---

## 🛠 Tools & Libraries
- R, Bioconductor  
- DESeq2, EDASeq  
- GEOquery, biomaRt  
- GenePlexus (web-based tool)  
- clusterProfiler, ggplot2  

---

## 📁 Data Sources
- GEO: GSE203346 (GDM RNA-seq dataset)  
- Curated PPH gene and protein lists  
