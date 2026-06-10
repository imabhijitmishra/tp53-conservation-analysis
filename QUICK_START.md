# 🚀 TP53 Conservation Analysis – Quick Start Guide

## Overview

This repository contains a comparative bioinformatics analysis of the **TP53 (p53) tumor suppressor protein** across six vertebrate species. The project explores sequence conservation, evolutionary relationships, and functional significance using multiple sequence alignment and phylogenetic analysis.

---

## 🧬 Project Workflow

```text
NCBI Protein Database
          ↓
   FASTA Retrieval
          ↓
 Multiple Sequence Alignment
      (Clustal Omega)
          ↓
 ┌────────┬─────────┬─────────┐
 ↓        ↓         ↓
PIM     Trees    Alignment
 ↓        ↓         ↓
Analysis  Visualization
          ↓
       WebLogo
```

---

## 📂 Repository Structure

```text
tp53-conservation-analysis/
│
├── data/
│   ├── TP53_Canis_lupus_familiaris.fasta
│   ├── TP53_Danio_rerio.fasta
│   ├── TP53_Gallus_gallus.fasta
│   ├── TP53_Homo_sapiens.fasta
│   ├── TP53_Mus_musculus.fasta
│   ├── TP53_Rattus_norvegicus.fasta
│   ├── TP53_all_species.fasta
│   └── species_metadata.txt
│
├── figures/
│   ├── TP53_sequence_logo.pdf
│   └── phylogenetic_tree.io.png
│
├── results/
│   ├── TP53_alignment.aln-clustal_num
│   ├── TP53_alignment_seqret.fasta
│   ├── TP53_percent_identity_matrix.pim
│   ├── TP53guidetree.tree
│   └── TP53.phylotree
│
├── README.md
├── report.md
├── ANALYSIS_REPORT.md
├── FINAL_SUMMARY.md
├── DATA_DICTIONARY.md
├── CONTRIBUTING.md
├── PROJECT_CHECKLIST.md
├── QUICK_START.md
└── LICENSE
```

---

## 📊 Key Results

### Sequence Identity

| Comparison         | Identity (%) |
| ------------------ | ------------ |
| Mouse vs Rat       | 88.86        |
| Human vs Dog       | 83.16        |
| Human vs Rat       | 77.38        |
| Human vs Mouse     | 77.26        |
| Human vs Chicken   | 54.95        |
| Human vs Zebrafish | 51.83        |

### Major Findings

* TP53 is highly conserved across vertebrates.
* Rodent TP53 proteins exhibit the highest similarity.
* Mammalian sequences cluster together.
* Chicken occupies an intermediate evolutionary position.
* Zebrafish is the most divergent species in this dataset.
* Conserved residues likely represent functionally important regions of the protein.

---

## 🔍 Viewing the Results

### Multiple Sequence Alignment

**File:**

```text
results/TP53_alignment.aln-clustal_num
```

**Symbols Used**

| Symbol | Meaning                         |
| ------ | ------------------------------- |
| *      | Fully conserved residue         |
| :      | Strongly conserved substitution |
| .      | Weakly conserved substitution   |
| -      | Alignment gap                   |

---

### Percent Identity Matrix

**File:**

```text
results/TP53_percent_identity_matrix.pim
```

**Purpose**

* Quantifies sequence similarity.
* Estimates evolutionary divergence.
* Supports phylogenetic interpretation.

---

### Phylogenetic Trees

**Files**

```text
results/TP53guidetree.tree
results/TP53.phylotree
```

**Format**

* Newick tree format

**Visualization Tools**

* Phylo.io
* FigTree
* MEGA

---

### Sequence Logo

**File**

```text
figures/TP53_sequence_logo.pdf
```

**Interpretation**

* Larger letters = higher conservation
* Smaller letters = higher variability
* Shows amino acid conservation at each alignment position

---

## 🔬 Reproducing the Analysis

### Step 1: Sequence Retrieval

Download TP53 protein sequences from the NCBI Protein Database.

### Step 2: Create Multi-FASTA Dataset

Combine all protein sequences into:

```text
TP53_all_species.fasta
```

### Step 3: Multiple Sequence Alignment

Upload the multi-FASTA file to Clustal Omega and run the alignment.

### Step 4: Download Outputs

Retrieve:

* Alignment file
* Guide tree
* Phylogenetic tree
* Percent identity matrix

### Step 5: Generate Sequence Logo

Upload the aligned FASTA file to WebLogo.

### Step 6: Visualize Phylogenetic Tree

Upload the Newick tree file to Phylo.io.

---

## 🛠️ Tools Used

| Tool                  | Purpose                         |
| --------------------- | ------------------------------- |
| NCBI Protein Database | Sequence retrieval              |
| Clustal Omega         | Multiple sequence alignment     |
| EMBOSS Seqret         | Alignment format conversion     |
| WebLogo               | Conservation visualization      |
| Phylo.io              | Phylogenetic tree visualization |

---

## 🎓 Learning Outcomes

By exploring this repository, users can learn:

* FASTA sequence handling
* Protein sequence retrieval
* Multiple sequence alignment
* Conservation analysis
* Percent identity interpretation
* Phylogenetic tree construction
* Comparative evolutionary bioinformatics

---

## 📚 Useful Resources

### Databases

* NCBI Protein Database: https://www.ncbi.nlm.nih.gov/protein/

### Analysis Tools

* Clustal Omega: https://www.ebi.ac.uk/jdispatcher/msa/clustalo
* WebLogo: https://weblogo.berkeley.edu/
* Phylo.io: https://phylo.io/

### Concepts

* FASTA Format: https://en.wikipedia.org/wiki/FASTA_format
* Sequence Alignment: https://en.wikipedia.org/wiki/Sequence_alignment
* Phylogenetic Inference: https://en.wikipedia.org/wiki/Phylogenetic_inference

---

## 📖 Citation

```text
Mishra, A. (2026).
TP53 Conservation Analysis Across Vertebrate Species.
GitHub Repository.
```

---

## 📄 License

This project is distributed under the CC-BY 4.0 License.

---

**Last Updated:** June 2026
