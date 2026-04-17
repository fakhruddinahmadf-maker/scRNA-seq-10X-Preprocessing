# scRNA-seq 10X Single-Cell RNA Preprocessing Pipeline

## Overview
This project performs pre-processing of 10X Genomics Single-Cell RNA-seq data using Galaxy platform tools including RNA STARsolo and DropletUtils.

## Dataset
- **Source:** 1k PBMCs from a Healthy Donor (v3 chemistry) - 10X Genomics
- **Input:** Sub-sampled FASTQ files (~300 cells) from Zenodo
- **Genome:** Human hg19 (GRCh37)
- **Chemistry:** 10X Chromium v3

## Workflow Steps
1. Data Upload (FASTQ + GTF + Barcode Whitelist)
2. Demultiplexing & Mapping with RNA STARsolo
3. Quality Control with MultiQC
4. Cell Filtering with DropletUtils (DefaultDrops)
5. Barcode Ranking (Knee/Inflection Plot)
6. Custom Cell Filtering with DropletUtils (EmptyDrops)

## Key Results
| Metric | Value |
|--------|-------|
| Uniquely Mapped Reads | 18.3% |
| Cells Detected (STARsolo) | 5200 |
| Cells After DefaultDrops | 254 |
| Cells After EmptyDrops | 250 |

## Tools Used
| Tool | Version | Purpose |
|------|---------|---------|
| RNA STARsolo | 2.7.11a | Mapping & Quantification |
| MultiQC | 1.27 | Quality Control |
| DropletUtils | 1.10.0 | Cell Filtering |

## Repository Structure
