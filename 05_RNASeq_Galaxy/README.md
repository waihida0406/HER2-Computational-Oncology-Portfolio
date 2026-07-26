 Project 5: RNA-Seq Analysis of HER2-Positive Breast Cancer Using Galaxy

 Status

Completed

---

 Background

RNA sequencing (RNA-Seq) is a high-throughput sequencing technique used to study the complete transcriptome of a biological sample. It enables researchers to quantify gene expression, identify differentially expressed genes (DEGs), and investigate molecular mechanisms associated with diseases.

In this project, publicly available RNA-Seq data from HER2-positive breast cancer samples were analyzed using the Galaxy platform. The workflow included quality assessment, read alignment, read counting, differential gene expression analysis, and visualization of the results.

The identified differentially expressed genes provide insights into molecular alterations associated with HER2-positive breast cancer and serve as the foundation for downstream functional enrichment analysis.

---
 Objective

To analyze RNA-Seq data from HER2-positive breast cancer samples using the Galaxy platform and identify differentially expressed genes for downstream biological interpretation.

---
Dataset Information

| Parameter | Details |
|-----------|---------|
| Database | NCBI Sequence Read Archive (SRA) |
| Dataset | SRR25848669 *(replace with your actual SRR IDs if multiple)* |
| Organism | Homo sapiens |
| Disease | HER2-positive Breast Cancer |
| Platform | Illumina RNA Sequencing |

---

Software and Tools Used

- Galaxy Europe
- FastQC
- Trim Galore *(if performed)*
- HISAT2
- featureCounts
- DESeq2
- MultiQC *(if performed)*

---

Methodology

Step 1: Dataset Retrieval

RNA-Seq datasets corresponding to HER2-positive breast cancer samples were obtained from the NCBI Sequence Read Archive (SRA).

---

Step 2: Quality Control

Raw sequencing reads were assessed using FastQC.

Quality parameters evaluated included:

- Per base sequence quality
- GC content
- Sequence length distribution
- Adapter contamination
- Overrepresented sequences

---

Step 3: Read Trimming *(if performed)*

Low-quality bases and adapter sequences were removed to improve overall read quality before alignment.

---

Step 4: Read Alignment

High-quality sequencing reads were aligned to the human reference genome using HISAT2.

The alignment process generated BAM files representing mapped sequencing reads.

---

Step 5: Read Quantification

Mapped reads were assigned to genomic features using featureCounts.

Gene-level read counts were generated for downstream statistical analysis.

---

Step 6: Differential Gene Expression Analysis

Gene count data were analyzed using DESeq2.

The analysis compared HER2-positive breast cancer samples with control samples to identify significantly differentially expressed genes.

Genes were evaluated using:

- Log2 Fold Change
- Adjusted p-value (False Discovery Rate)

---

Step 7: Visualization

Differential gene expression results were visualized using:

- MA Plot
- Volcano Plot
- Heatmap *(if generated)*
- Principal Component Analysis (PCA) *(if generated)*

---

Workflow

NCBI SRA Dataset

↓

FastQC

↓

Read Trimming *(optional)*

↓

HISAT2 Alignment

↓

featureCounts

↓

DESeq2

↓

Differential Gene Expression

↓

Visualization

↓

Functional Enrichment (Project 6)

---

 Results

The RNA-Seq analysis identified a set of genes exhibiting significant differential expression between HER2-positive breast cancer samples and control samples.

The combination of statistical significance (adjusted p-value) and fold change enabled the identification of both upregulated and downregulated genes associated with HER2-positive breast cancer.

These differentially expressed genes were used as the input for downstream Gene Ontology and pathway enrichment analyses.

*(Replace this paragraph with your actual observations once your DEG analysis is complete.)*

---

Key Outputs

- Quality Control Report (FastQC)
- Read Alignment Statistics
- Gene Count Matrix
- Differential Expression Results
- MA Plot
- Volcano Plot
- Heatmap *(if available)*
- PCA Plot *(if available)*

---

Project Deliverables

```
05_RNASeq_Galaxy
│
├── README.md
├── images
│   ├── workflow.png
│   ├── fastqc_report.png
│   ├── alignment_statistics.png
│   ├── ma_plot.png
│   ├── volcano_plot.png
│   ├── heatmap.png
│   └── pca_plot.png
├── results
│   ├── gene_counts.csv
│   ├── deg_results.csv
│   └── significant_genes.csv
└── workflow
    └── galaxy_history.pdf
```

---

Skills Demonstrated

- RNA-Seq Analysis
- Galaxy Platform
- Next Generation Sequencing (NGS)
- Quality Control
- Read Alignment
- Gene Quantification
- Differential Gene Expression Analysis
- Transcriptomics
- Bioinformatics Data Analysis

---
References

1. Galaxy Project
2. NCBI Sequence Read Archive (SRA)
3. HISAT2 Documentation
4. featureCounts Documentation
5. DESeq2 Bioconductor Package
6. FastQC Documentation

---

Next Project

➡ **Project 6: Functional Enrichment Analysis (Gene Ontology and KEGG Pathway Analysis)**
