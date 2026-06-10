# Data Dictionary

## Overview
This document describes the format and content of all data files in the TP53 Conservation Analysis project.

---

## Input Data Files

### Individual FASTA Sequence Files

**Location:** `data/TP53_*.fasta`

**Format:** Standard FASTA format

**Files:**
- `TP53_Homo_sapiens.fasta` - Human p53 protein sequence
- `TP53_Mus_musculus.fasta` - Mouse p53 protein sequence
- `TP53_Rattus_norvegicus.fasta` - Rat p53 protein sequence
- `TP53_Canis_lupus_familiaris.fasta` - Dog p53 protein sequence
- `TP53_Gallus_gallus.fasta` - Chicken p53 protein sequence
- `TP53_Danio_rerio.fasta` - Zebrafish p53 protein sequence

**File Structure:**
```
>ACCESSION DESCRIPTION [Species name]
SEQUENCE_DATA
```

**Example:**
```
>NP_000537.3 cellular tumor antigen p53 isoform a [Homo sapiens]
MEEPQSDPSVEPPLSQETFSDLWKLLPENNVLSPLPSQAMDDLMLSPDDIEQWFTEDPGPDEAPRMPEAA...
```

**Data Type:** Amino acid sequences
**Sequence Length:** 367-393 amino acids (species-dependent)

---

### Combined Multi-FASTA File

**File:** `data/TP53_all_species.fasta`

**Description:** Consolidated FASTA file containing all 6 species' TP53 sequences

**Purpose:** Input for multiple sequence alignment tools (Clustal Omega)

**Format:** Identical to individual files, concatenated

---

### Metadata File

**File:** `data/species_metadata.txt`

**Format:** Tab-separated, human-readable text

**Content:**
- Species scientific names
- Common names
- NCBI Protein accession numbers
- Sequence lengths (in amino acids)
- Analysis tools used and their purposes

**Usage:** Reference documentation for data provenance and reproducibility

---

## Output Files (Results)

### Clustal Alignment Format

**File:** `results/TP53_alignment.aln-clustal_num`

**Format:** Clustal ALN format with position numbering

**Description:** Multiple sequence alignment output from Clustal Omega

**Content:**
- Aligned sequences for all 6 species
- Gaps introduced where needed for alignment
- Position numbers on right margin
- Conservation symbols below alignments:
  - `*` = Fully conserved residue
  - `:` = Strongly conserved substitution
  - `.` = Weakly conserved substitution
  - ` ` (space) = Not conserved

**Example Line:**
```\`\`\`
Homo_sapiens_NP_000537.3       ---MEEPQSDPSVEPPLSQETFSDLWKLLPENNVLS   34
Mus_musculus_BAA82343.1        MTAMEESQSDISLELPLSQETFSGLWKLLPPEDILPS   37
Rattus_norvegicus_NP_001416923 ---MEDSQSDMSIELPLSQETFSCLWKLLPPDDILPT   34
                                   :*.** .* :*****.*****:***           
```

**Interpretation Guide:**
- Long stretches of `*` symbols indicate strong conservation
- Mix of `*`, `:`, `.` indicates moderate conservation
- Many spaces indicate variable regions
- Gaps (`-`) indicate sequence length differences

---

### FASTA Alignment Format

**File:** `results/TP53_alignment_seqret.fasta`

**Format:** Aligned sequences in FASTA format with gaps

**Description:** Clustal Omega alignment output reformatted as FASTA

**Usage:** Input for WebLogo or other sequence analysis tools

**Content:**
```
>Homo_sapiens_NP_000537.3
MEEPQSDPSVEPPLSQETFSDLWKLLPENNVLSPLPSQ-AMDDLMLSPDDIEQ...
```

---

### Percent Identity Matrix

**File:** `results/TP53_percent_identity_matrix.pim`

**Format:** Clustal PIM (Percent Identity Matrix) format

**Structure:**
```
     1: Species_name_1                   100.00   XX.XX   XX.XX   ...
     2: Species_name_2                   XX.XX  100.00   XX.XX   ...
     3: Species_name_3                   XX.XX   XX.XX  100.00   ...
```

**Values:** Percent identity (0-100%)

**Interpretation:**
- Diagonal values are always 100% (species compared to itself)
- Higher values = greater sequence similarity
- Lower values = greater evolutionary divergence
- Matrix is symmetric (value for A vs B = value for B vs A)

**Example Interpretation:**
- Mouse vs Rat: 88.86% (very close evolutionary relationship)
- Human vs Zebrafish: 51.83% (distant evolutionary relationship)

---

### Phylogenetic Trees

**Files:**
- `results/TP53guidetree.tree` - Guide tree from alignment (Newick format)
- `results/TP53.phylotree` - Phylogenetic tree (Newick format)

**Format:** Newick tree format

**Structure:**
```
(species1:branch_length,species2:branch_length)root;
```

**Interpretation:**
- Branch lengths represent evolutionary distance
- Nested parentheses indicate evolutionary relationships
- Longer branches = greater evolutionary divergence
- Tree topology shows which species are most closely related

**Example:**
```
((Mouse:0.1,Rat:0.1):0.2,(Human:0.15,Dog:0.15):0.2);
```
This indicates: Mice and rats are sister species; humans and dogs are sister species; mammals form one clade.

---

## Output Figures

### Sequence Logo

**File:** `figures/TP53_sequence_logo.pdf`

**Format:** PDF visualization

**Description:** WebLogo output showing amino acid conservation at each position

**Interpretation:**
- **X-axis:** Position in aligned protein sequence
- **Y-axis:** Information content (bits)
- **Letter size:** Proportional to amino acid frequency
  - Tall letters = highly conserved position
  - Short letters = variable position
- **Letter color:** Typically represents amino acid properties
  - Red = acidic residues
  - Blue = basic residues
  - Green = polar residues
  - Black = hydrophobic residues

**Usage:** Visualizes conservation patterns across species at a glance

---

### Phylogenetic Tree Visualization

**File:** `figures/phylogenetic_tree_io.png`

**Format:** PNG image

**Description:** Phylo.io visualization of phylogenetic relationships

**Content:**
- Tree diagram showing evolutionary relationships
- Branch lengths represent evolutionary distance
- Leaf nodes labeled with species names
- Clustering pattern reflects taxonomy

**Key Observations:**
- Rodents (mouse, rat) cluster together
- Mammals form a distinct clade
- Zebrafish is most distant from other species

---

## Data Quality and Validation

### Sequence Lengths

| Species | Length (aa) | Accession |
|---------|------------|-----------|
| Human | 393 | NP_000537.3 |
| Mouse | 390 | BAA82343.1 |
| Rat | 391 | NP_001416923.1 |
| Dog | 381 | NP_001376147.1 |
| Chicken | 367 | NP_990595.1 |
| Zebrafish | 374 | XP_073805887.1 |

### Key Conservation Statistics

- **Most conserved pair:** Mouse vs Rat (88.86% identity)
- **Least conserved pair:** Human vs Zebrafish (51.83% identity)
- **Mammalian average identity:** ~77-88%
- **Cross-class average identity:** ~52-55%

---

## Reproducibility Notes

- All sequences retrieved from NCBI Protein Database (https://www.ncbi.nlm.nih.gov/protein/)
- Alignment performed using Clustal Omega v1.2+ (https://www.ebi.ac.uk/jdispatcher/msa/clustalo)
- Logo generated using WebLogo (https://weblogo.berkeley.edu/)
- Tree visualization using Phylo.io (https://phylo.io/)

---

## File Naming Convention

All files follow the pattern:
- `TP53_[analysis_type].[extension]`
- Spaces replaced with underscores for command-line compatibility
- Extensions indicate file format:
  - `.fasta` = FASTA sequence format
  - `.aln-clustal_num` = Clustal alignment format
  - `.pim` = Percent identity matrix
  - `.tree` = Newick tree format
  - `.pdf` = PDF document
  - `.png` = PNG image
  - `.txt` = Plain text
