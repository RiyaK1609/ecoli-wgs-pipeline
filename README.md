# E. coli Whole Genome Sequencing (WGS) Pipeline: From Raw FASTQ to Variant Calling

## Project Overview

This repository presents an end-to-end Whole Genome Sequencing (WGS) analysis pipeline for *Escherichia coli* using publicly available Illumina sequencing data. The workflow includes quality assessment, read trimming, reference genome alignment, BAM processing, and variant calling to generate a filtered Variant Call Format (VCF) file.

---

## Workflow

               Raw FASTQ
                    │
                    ▼
              Quality Check
               (FastQC)
                    │
                    ▼
            Read Trimming
            (Trimmomatic)
                    │
                    ▼
         Quality Assessment
         (FastQC After Trim)
                    │
                    ▼
       Reference Alignment
           (BWA-MEM)
                    │
                    ▼
        SAM → BAM Conversion
           (SAMtools)
                    │
                    ▼
      Sorting & Indexing BAM
           (SAMtools)
                    │
                    ▼
         Variant Calling
           (BCFtools)
                    │
                    ▼
            Filtered VCF 

---

## Tools Used

| Tool | Purpose |
|------|---------|
| FastQC | Quality assessment |
| Trimmomatic | Read trimming |
| BWA-MEM | Read alignment |
| SAMtools | BAM processing |
| BCFtools | Variant calling and filtering |

---

## Output Files

- FastQC Reports
- Trimmed FASTQ
- Sorted BAM
- BAM Index (.bai)
- Raw VCF
- Filtered VCF

---

## Project Scope

This repository demonstrates the NGS workflow up to **variant calling**.