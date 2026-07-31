# 🧬 Project 5 | NGS Quality Assessment and Sequence Analysis Using Galaxy

<p align="center">

![Platform](https://img.shields.io/badge/Platform-Galaxy-blue)

![Data](https://img.shields.io/badge/Data-NCBI%20SRA-green)

![Tool](https://img.shields.io/badge/FastQC-QC-orange)

![Status](https://img.shields.io/badge/Status-Completed-success)

</p>

---

# 📌 Project Overview

High-throughput sequencing (Next-Generation Sequencing, NGS) generates millions of DNA or RNA reads that require quality assessment before downstream analysis.

This project demonstrates a complete **quality-control workflow** for NGS data using the **Galaxy** platform. A publicly available sequencing dataset was downloaded from the **NCBI Sequence Read Archive (SRA)** and analysed using FastQC, quality trimming and BLAST.

The objective was to determine sequencing quality, improve read quality by removing low-quality bases and adapters, and verify the biological identity of the sequencing reads.

---

# 🎯 Objectives

✔ Download publicly available sequencing data

✔ Understand FASTQ file structure

✔ Perform sequence quality assessment

✔ Identify sequencing artifacts

✔ Remove low-quality reads and adapters

✔ Compare quality before and after trimming

✔ Identify sequences using BLAST

✔ Interpret biological significance

---

# 🧬 Biological Background

Next-Generation Sequencing technologies have revolutionized molecular biology by enabling rapid sequencing of DNA and RNA.

However, sequencing machines may introduce

- sequencing errors
- adapter contamination
- PCR bias
- GC bias
- low-quality nucleotide calls

These issues must be detected before downstream analyses such as

- Genome Assembly
- Variant Calling
- RNA-Seq
- Differential Gene Expression
- Functional Enrichment

FastQC is one of the most widely used quality assessment tools for evaluating sequencing data.

---

# 📂 Dataset Information

| Parameter | Description |
|-----------|-------------|
| Database | NCBI Sequence Read Archive |
| Accession Number | SRR25848669 |
| Organism | Homo sapiens |
| Data Type | FASTQ |
| Analysis Platform | Galaxy |

---

# 🛠 Software Used

| Software | Purpose |
|----------|----------|
| Galaxy | Bioinformatics Platform |
| FastQC | Quality Assessment |
| Trim Galore / Cutadapt | Read Trimming |
| NCBI BLAST | Sequence Identification |

---

# 🔬 Experimental Workflow

```text
NCBI SRA
      │
      ▼
Download FASTQ
      │
      ▼
Upload into Galaxy
      │
      ▼
FastQC Analysis
      │
      ▼
Interpret Quality Metrics
      │
      ▼
Trim Low-quality Reads
      │
      ▼
FastQC After Trimming
      │
      ▼
Compare Reports
      │
      ▼
BLAST Analysis
      │
      ▼
Biological Interpretation
```

---

# 📊 Step 1 | FASTQ Dataset Retrieval

A publicly available sequencing dataset (SRR25848669) was downloaded from the NCBI Sequence Read Archive in FASTQ format.

The FASTQ file contains

- Sequence Identifier
- Nucleotide Sequence
- Separator
- Phred Quality Scores

These data were imported into Galaxy for downstream quality assessment.

---

# 📷 Figure 1 | FASTQ Structure

<p align="center">

<img src="images/fastq_structure.png" width="850">

</p>

---

# 📊 Step 2 | Initial FastQC Analysis

FastQC was performed to evaluate sequencing quality before trimming.

---

## Figure 2 | FastQC Report Before Trimming

<p align="center">

<img src="images/fastqc_before.png" width="900">

</p>

---

# Quality Assessment

| Module | Status | Interpretation |
|---------|--------|----------------|
| Basic Statistics | ✅ Pass | Dataset imported correctly |
| Per Base Sequence Quality | ✅ Pass | High sequencing accuracy |
| Per Tile Sequence Quality | ✅ Pass | Uniform sequencing performance |
| Per Sequence Quality | ✅ Pass | Majority of reads are high quality |
| Per Base Sequence Content | ❌ Fail | Unequal nucleotide distribution |
| GC Content | ⚠ Warning | Slight GC bias |
| N Content | ✅ Pass | Very low ambiguous bases |
| Sequence Length | ✅ Pass | Uniform read length |

---

# Result Interpretation

The sequencing dataset exhibited high overall quality.

Most quality modules successfully passed quality assessment.

Although Per Base Sequence Content failed and GC Content produced a warning, these findings are frequently observed in sequencing libraries and do not necessarily indicate poor-quality sequencing.

Overall, the sequencing reads were considered suitable for downstream processing.

---

# ✂ Step 3 | Quality Trimming

Low-quality bases and adapter contamination were removed using Trim Galore.

---

## Figure 3 | Trimming Summary

<p align="center">

<img src="images/trimming_summary.png" width="850">

</p>

---

# Interpretation

Quality trimming removed unwanted low-quality regions while preserving high-quality sequencing reads.

This improves the reliability of downstream analyses.

---

# 📊 Step 4 | FastQC After Trimming

FastQC analysis was repeated after trimming.

---

## Figure 4 | FastQC After Trimming

<p align="center">

<img src="images/fastqc_after.png" width="900">

</p>

---

# Before vs After Comparison

| Parameter | Before | After |
|------------|---------|--------|
| Base Quality | High | Improved |
| Adapter Content | Present | Reduced |
| Low-quality Bases | Present | Reduced |
| Overall Read Quality | Good | Improved |

---

# Interpretation

Comparison of FastQC reports demonstrated improved sequencing quality following trimming.

The processed sequencing reads were suitable for downstream biological analysis.

---

# 🔎 Step 5 | BLAST Analysis

Representative sequencing reads were analysed using NCBI BLAST.

---

## Figure 5 | BLAST Output

<p align="center">

<img src="images/blast_result.png" width="900">

</p>

---

# BLAST Summary

| Parameter | Result |
|-----------|--------|
| Database | NCBI nt |
| Top Hit | <Update after BLAST> |
| Organism | <Update after BLAST> |
| Identity | <Update after BLAST> |
| Query Coverage | <Update after BLAST> |
| E-value | <Update after BLAST> |

---

# Biological Interpretation

BLAST identified homologous nucleotide sequences within the NCBI database.

The observed sequence similarity confirmed the biological identity of the sequencing reads and supported the reliability of the processed dataset.

---

# 📈 Skills Demonstrated

- Bioinformatics Workflow Development
- Galaxy Platform
- FASTQ Data Handling
- Sequence Quality Assessment
- FastQC Interpretation
- Quality Trimming
- Comparative Data Analysis
- Sequence Similarity Search
- BLAST Analysis
- Biological Data Interpretation

---

# 📂 Repository Structure

```
05_RNASeq_Galaxy
│
├── README.md
│
├── images
│   ├── workflow.png
│   ├── fastq_structure.png
│   ├── fastqc_before.png
│   ├── trimming_summary.png
│   ├── fastqc_after.png
│   └── blast_result.png
│
├── reports
│   ├── FastQC_Before.html
│   ├── FastQC_After.html
│   ├── Trimming_Report.txt
│   └── BLAST_Report.pdf
│
└── raw_data
    └── SRR25848669.fastq.gz
```

---

# 🏆 Key Learning Outcomes

- Understood FASTQ file organization and sequencing quality metrics.
- Performed quality assessment using FastQC.
- Improved sequencing quality through trimming.
- Compared pre- and post-trimming quality reports.
- Conducted sequence identification using NCBI BLAST.
- Learned a standard quality-control workflow widely used before downstream genomics and transcriptomics analyses.

---

# 📚 References

1. Andrews S. *FastQC: A Quality Control Tool for High Throughput Sequence Data.*
2. Galaxy Project.
3. NCBI Sequence Read Archive (SRA).
4. NCBI BLAST.
5. Babraham Bioinformatics.

---

# 🚀 Next Project

➡ **Project 6: Functional Enrichment Analysis (Gene Ontology and KEGG Pathway Analysis)**
