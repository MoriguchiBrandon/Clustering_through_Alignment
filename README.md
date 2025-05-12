# Hierarchical Clustering of RNA-Seq Reads via Needleman-Wunsch Alignment and Smith-Waterman

This project performs pairwise sequence alignment on RNA-Seq reads using the Needleman-Wunsch algorithm and Smith-Waterman, clusters them based on alignment similarity, and performs BLAST on specific clusters to identify biological relevance.

---

## 📁 Project Structure

- `Global_similarity_matrix.csv` — Pairwise similarity scores between selected reads.
- `Global_reduced_reads.csv` — Subsampled reads used for alignment and clustering.
- Notebook/script steps include:
  - Reading and parsing `.fastq.gz` files
  - Subsampling reads
  - Needleman-Wunsch pairwise alignment
  - Similarity matrix saving/loading
  - Hierarchical clustering
  - (Optional) BLAST for biological relevance

---

## ⚙️ Installation Requirements

---
```bash
pip install biopython
```

## 🚀 Usage

## Required files for both options:
1. 'GLDS-255_rna_seq_GSM3932708_trimmed.fastq.gz'

## Required files for option 2:
1. `Global_similarity_matrix.csv`
2. `Global_reduced_reads.csv`
3. `Local_similarity_matrix.csv` 
4. `Local_reduced_reads.csv`

all files can be found at my google drive:
https://drive.google.com/drive/folders/1jQhBv4KrMrLi_3w51WT8Y-JJGIf3EdBL?usp=sharing

### 🔁 Option 1: Run Entire Pipeline

1. Mount Google Drive.
2. Parse `.fastq.gz` file.
3. Subsample reads (e.g., every 10,001st).
4. Compute pairwise similarity scores using Needleman-Wunsch or SmithWaterman. (takes about 3 hours each)
5. Save similarity matrix and reads.
6. Perform hierarchical clustering and visualize dendrogram.
7. Analyze or BLAST reads from selected clusters. (takes about 1 hour for 50 Blast reads)

✅ Run **all cells from top to bottom** to execute the full workflow.

---

### 🔄 Option 2: Skip Alignment (Reuse Results)

1. Mount Google Drive.
2. If you have already saved `Global_similarity_matrix.csv` and `Global_reduced_reads.csv` or `Local_similarity_matrix.csv` and `Local_reduced_reads.csv`:
**Load saved files instead:**
3.Perform hierarchical clustering and visualize dendrogram.
4. Analyze or BLAST reads from selected clusters. (takes about 1 hour for 50 Blast reads)

✅ Run **Setup and all cells below "Reading All Cells into Colab"** to execute the shortened workflow.