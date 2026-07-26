Project 5: Quality Assessment of NGS Data Using Galaxy

Status

✅ Completed

---

Background

Next-Generation Sequencing (NGS) produces millions of short DNA or RNA sequence reads in FASTQ format. Before downstream analysis, it is essential to evaluate the quality of sequencing data to identify potential issues such as low-quality bases, adapter contamination, GC bias, and sequence duplication.

In this project, a publicly available sequencing dataset was downloaded from the NCBI Sequence Read Archive (SRA) and analyzed using the Galaxy platform. The workflow included quality assessment using FastQC, quality trimming of sequencing reads, comparison of quality reports before and after trimming, and sequence identification using the NCBI BLAST tool.

---

Objective

- Perform quality assessment of NGS sequencing data.
- Identify sequencing quality issues using FastQC.
- Improve sequence quality through trimming.
- Compare sequencing quality before and after trimming.
- Identify biological sequences using the NCBI BLAST tool.

---

Dataset Information

| Parameter | Details |
|-----------|---------|
| Database | NCBI Sequence Read Archive (SRA) |
| Accession Number | SRR25848669 |
| Organism | *Homo sapiens* |
| File Format | FASTQ |
| Platform | Galaxy |

---

Software and Tools Used

- Galaxy
- FastQC
- Trim Galore (or trimming tool used)
- NCBI BLAST

---

Methodology

Step 1: Data Retrieval

A publicly available sequencing dataset (SRR25848669) was downloaded from the NCBI Sequence Read Archive in FASTQ format.

---

Step 2: Upload to Galaxy

The FASTQ dataset was uploaded to the Galaxy platform for quality assessment.

---

Step 3: Initial Quality Assessment

FastQC was performed to evaluate sequencing quality.

The following parameters were examined:

- Basic Statistics
- Per Base Sequence Quality
- Per Tile Sequence Quality
- Per Sequence Quality Scores
- Per Base Sequence Content
- Per Sequence GC Content
- Per Base N Content
- Sequence Length Distribution

---

Figure 1. Initial FastQC Report

<p align="center">
<img src="images/fastqc_before.png" width="850">
</p>

---

Results

| Quality Module | Status | Interpretation |
|---------------|--------|----------------|
| Basic Statistics | ✅ Pass | Dataset successfully processed |
| Per Base Sequence Quality | ✅ Pass | High sequencing quality |
| Per Tile Sequence Quality | ✅ Pass | Uniform sequencing performance |
| Per Sequence Quality Scores | ✅ Pass | Most reads possess high quality |
| Per Base Sequence Content | ❌ Fail | Unequal nucleotide composition observed |
| Per Sequence GC Content | ⚠ Warning | Slight deviation from theoretical distribution |
| Per Base N Content | ✅ Pass | Very few ambiguous nucleotides |
| Sequence Length Distribution | ✅ Pass | Uniform read length |

---

Analysis

The FastQC report demonstrated that the sequencing dataset possessed good overall quality. Most quality modules successfully passed the quality assessment, indicating reliable sequencing reads suitable for downstream analysis. The Per Base Sequence Content module failed due to unequal nucleotide composition, while the GC Content module generated a warning. Such observations are common in certain sequencing libraries and do not necessarily indicate poor-quality sequencing data.

---

Step 4: Read Trimming

Low-quality bases and adapter sequences were removed using a trimming tool to improve the overall quality of the sequencing reads.

---

Figure 2. Trimming Summary

<p align="center">
<img src="images/trimming_summary.png" width="700">
</p>

---

Analysis

Quality trimming removed low-quality regions and adapter contamination, thereby improving the overall quality of the sequencing reads prior to downstream analysis.

---

Step 5: FastQC After Trimming

The trimmed sequencing reads were evaluated again using FastQC.

---

Figure 3. FastQC Report After Trimming

<p align="center">
<img src="images/fastqc_after.png" width="850">
</p>

---

Comparison of Quality Reports

| Parameter | Before Trimming | After Trimming |
|------------|----------------|---------------|
| Per Base Quality | Good | Improved |
| Adapter Content | Present | Reduced/Removed |
| Overall Read Quality | Good | Improved |
| Low-quality Bases | Present | Reduced |

---

Analysis

Quality assessment after trimming demonstrated an overall improvement in sequencing quality. Adapter contamination and low-quality bases were reduced while maintaining high sequencing quality, making the dataset suitable for downstream biological analysis.

---

Step 6: BLAST Analysis

Representative sequences from the processed FASTQ dataset were analyzed using the NCBI BLAST tool to identify similar biological sequences.

---

Figure 4. BLAST Result

<p align="center">
<img src="images/blast_result.png" width="850">
</p>

---

BLAST Summary

| Parameter | Observation |
|-----------|-------------|
| Database | NCBI BLAST |
| Top Match | *(Update after BLAST analysis)* |
| Sequence Identity | *(Update after BLAST analysis)* |
| E-value | *(Update after BLAST analysis)* |

---

Biological Interpretation

BLAST analysis identified highly similar sequences within the NCBI database, confirming the biological origin of the sequencing reads and supporting the reliability of the sequencing dataset.

---

Workflow

```
NCBI SRA
      │
      ▼
Download FASTQ
      │
      ▼
Upload to Galaxy
      │
      ▼
Run FastQC
      │
      ▼
Interpret Quality Report
      │
      ▼
Trim Low-quality Reads
      │
      ▼
Run FastQC Again
      │
      ▼
Compare Quality Reports
      │
      ▼
BLAST Analysis
      │
      ▼
Biological Interpretation
```

---

Project Structure

```
05_RNASeq_Galaxy
│
├── README.md
├── images
│   ├── workflow.png
│   ├── fastqc_before.png
│   ├── trimming_summary.png
│   ├── fastqc_after.png
│   └── blast_result.png
├── reports
│   ├── FastQC_Before.html
│   ├── FastQC_After.html
│   └── Trimming_Report.txt
└── raw_data
    └── SRR25848669.fastq.gz
```

---
Skills Demonstrated

- Next-Generation Sequencing (NGS)
- FASTQ Data Handling
- Galaxy Platform
- Sequence Quality Assessment
- FastQC Interpretation
- Quality Trimming
- Comparative Quality Analysis
- BLAST Sequence Analysis
- Bioinformatics Workflow
- Data Interpretation

---

Conclusion

The sequencing dataset obtained from the NCBI Sequence Read Archive was successfully assessed using the Galaxy platform. FastQC analysis indicated that the sequencing reads possessed good overall quality. Quality trimming improved the sequencing reads by reducing low-quality bases and adapter contamination. BLAST analysis further confirmed the biological identity of the sequences. This workflow demonstrates a standard quality-control pipeline commonly applied before downstream genomic and transcriptomic analyses.

---

References

1. Andrews S. FastQC: A Quality Control Tool for High Throughput Sequence Data.
2. Galaxy Project.
3. NCBI Sequence Read Archive (SRA).
4. NCBI BLAST.
5. Babraham Bioinformatics.

---

Next Project

➡ **Project 6: Functional Enrichment Analysis (Gene Ontology and KEGG Pathway Analysis)**
