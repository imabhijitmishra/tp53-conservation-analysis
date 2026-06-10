# 🧬 TP53 Conservation Analysis Across Vertebrate Species

![Bioinformatics](https://img.shields.io/badge/Bioinformatics-Project-blue)
![Protein Analysis](https://img.shields.io/badge/Protein-TP53-green)
![Evolutionary Biology](https://img.shields.io/badge/Evolutionary-Biology-orange)
![License](https://img.shields.io/badge/License-CC--BY--4.0-green)

---

## 📖 Overview

This project investigates the evolutionary conservation of the **TP53 tumor suppressor protein (p53)** across six vertebrate species using bioinformatics and comparative sequence analysis.

TP53 is often called the **"Guardian of the Genome"** because it plays a crucial role in:

- 🛡️ DNA Damage Response
- 🔬 Cell Cycle Regulation
- 💀 Apoptosis
- 🧪 Stress Response
- 🧬 Genome Stability

The objective was to determine how strongly TP53 has been conserved during vertebrate evolution and to explore evolutionary relationships using protein sequence analysis.

---

## 🎯 Research Question

**How conserved is the TP53 protein across vertebrate species, and what evolutionary relationships can be inferred from sequence similarity?**

---

## 🌍 Species Included

| Species | Common Name | Accession | Length |
|---|---|---|---|
| Homo sapiens | Human | NP_000537.3 | 393 aa |
| Mus musculus | Mouse | BAA82343.1 | 390 aa |
| Rattus norvegicus | Rat | NP_001416923.1 | 391 aa |
| Canis lupus familiaris | Dog | NP_001376147.1 | 381 aa |
| Gallus gallus | Chicken | NP_990595.1 | 367 aa |
| Danio rerio | Zebrafish | XP_073805887.1 | 374 aa |

---

## 🔬 Bioinformatics Workflow

```
NCBI Protein Database
        ↓
FASTA Sequence Collection
        ↓
Multi-FASTA Dataset Creation
        ↓
Clustal Omega Alignment
        ↓
Conservation Analysis
        ↓
Identity Matrix Generation
        ↓
Phylogenetic Tree Construction
        ↓
Sequence Logo Visualization
        ↓
Biological Interpretation
```

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| NCBI Protein Database | Sequence Retrieval |
| Clustal Omega (EMBL-EBI) | Multiple Sequence Alignment |
| WebLogo | Sequence Logo Generation |
| Phylo.io | Tree Visualization |
| GitHub | Project Documentation |

---

## 📊 Key Findings

✅ TP53 is highly conserved across vertebrates.

✅ Mouse and Rat exhibited the highest similarity (**88.86% identity**).

✅ Human and Dog shared **83.16% identity**.

✅ Human and Zebrafish shared **51.83% identity**.

✅ Conserved residues were concentrated in biologically important regions.

✅ Phylogenetic analysis grouped mammals together and identified Zebrafish as the most divergent lineage.

---

## 📁 Repository Structure

```
tp53-conservation-analysis/
│
├── data/                          # Input sequence data
│   ├── TP53_Homo_sapiens.fasta
│   ├── TP53_Mus_musculus.fasta
│   ├── TP53_Rattus_norvegicus.fasta
│   ├── TP53_Canis_lupus_familiaris.fasta
│   ├── TP53_Gallus_gallus.fasta
│   ├── TP53_Danio_rerio.fasta
│   ├── TP53_all_species.fasta
│   └── species_metadata.txt
│
├── results/                       # Analysis outputs
│   ├── TP53_alignment.aln-clustal_num
│   ├── TP53_alignment_seqret.fasta
│   ├── TP53_percent_identity_matrix.pim
│   ├── TP53guidetree.tree
│   └── TP53.phylotree
│
├── figures/                       # Visualizations
│   ├── TP53_sequence_logo.pdf
│   └── phylogenetic_tree_io.png
│
├── README.md                      # This file
├── report.md                      # Detailed analysis report
├── DATA_DICTIONARY.md             # File format documentation
├── ANALYSIS_REPORT.md             # Quality assessment
├── LICENSE                        # CC-BY 4.0 License
└── .gitignore                     # Git ignore rules
```

---

## 🧬 Major Outputs

📄 **Multiple Sequence Alignment** - Aligned protein sequences showing conservation

📈 **Percent Identity Matrix** - Pairwise sequence similarity comparisons

🌳 **Phylogenetic Tree** - Evolutionary relationships visualization

🧬 **Sequence Logo** - Amino acid conservation at each position

📑 **Detailed Analysis Report** - Complete results and interpretation

---

## 🚀 Quick Start

1. **Review the data:** Check `data/species_metadata.txt` for sequence information
2. **Examine results:** Open `results/TP53_percent_identity_matrix.pim` for identity scores
3. **View figures:** See `figures/phylogenetic_tree_io.png` for evolutionary tree
4. **Read analysis:** See `report.md` for complete methodology and results
5. **Understand formats:** Consult `DATA_DICTIONARY.md` for file descriptions

---

## 📚 Documentation

- **[report.md](report.md)** - Comprehensive methodology, results, and interpretation
- **[DATA_DICTIONARY.md](DATA_DICTIONARY.md)** - Detailed explanation of all file formats
- **[ANALYSIS_REPORT.md](ANALYSIS_REPORT.md)** - Quality assessment and improvement recommendations
- **[data/species_metadata.txt](data/species_metadata.txt)** - Dataset provenance and tool information

---

## 🎓 Findings Summary

### Sequence Conservation

The analysis revealed **extensive conservation** of TP53 across all vertebrate species analyzed. The central region of the protein showed the highest conservation, while terminal regions were more variable. This pattern is consistent with the functional importance of the central DNA-binding domain.

### Evolutionary Relationships

Phylogenetic analysis successfully reconstructed expected vertebrate evolutionary relationships:
- **Mammals** (human, dog, mouse, rat) clustered together
- **Non-mammalian vertebrates** (chicken, zebrafish) were more distant
- Zebrafish showed the greatest evolutionary divergence

### Biological Implications

The high conservation of TP53 (>50% identity even with distant zebrafish) indicates that TP53 function is under strong evolutionary constraint due to its critical role in:
- Cell cycle control
- DNA repair coordination
- Apoptosis regulation
- Genome stability maintenance

---

## 🔄 Future Improvements

* Include additional vertebrate species (amphibians, reptiles)
* Analyze TP53 nucleotide sequences
* Compare TP53 protein structures using AlphaFold
* Investigate conserved functional domains
* Map disease-associated mutations to conserved residues
* Perform evolutionary rate analysis (dN/dS ratios)
* Conduct bootstrap-supported phylogenetic analysis

---

## 📖 How to Use This Repository

### For Research/Education
1. Use individual FASTA files in `data/` for sequence analysis
2. Consult `report.md` for methodology replication
3. Review `results/` for pairwise identity comparisons

### For Code Development
1. Clone this repository
2. Check `.gitignore` to understand tracked files
3. Follow naming conventions (underscores instead of spaces)

### For Reuse
1. Cite using the CC-BY 4.0 license
2. See `LICENSE` file for attribution requirements
3. Reference accession numbers in `data/species_metadata.txt`

---

## 📋 References

1. National Center for Biotechnology Information (NCBI). Protein Database. https://www.ncbi.nlm.nih.gov/protein/

2. Sievers F, Higgins DG. (2018). Clustal Omega for making accurate alignments of many protein sequences. Current Protocols in Bioinformatics, 48(1), 3.13.1-3.13.23.

3. Crooks GE, Hon G, Chandonia JM, Brenner SE. (2004). WebLogo: A sequence logo generator. Genome Research, 14(6), 1188-1190.

4. Lane DP. (1992). Cancer. p53, guardian of the genome. Nature, 358(6381), 15-16.

5. Levine AJ. (1997). p53, the cellular gatekeeper for growth and division. Journal of Biological Chemistry, 272(32), 20555-20558.

6. Phylo.io: Interactive phylogenetic tree visualization platform. https://phylo.io/

---

## 👨‍🔬 Author

**Abhijit Mishra**

Aspiring Biologist • Bioinformatics Learner

- GitHub: https://github.com/imabhijitmishra
- Email: abhijitmishra02@outlook.com

---

## 📄 License

This project is licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)** license.

You are free to share and adapt this work with appropriate attribution.

See `LICENSE` file for details.

---

⭐ **If you found this project interesting, feel free to explore the repository and results!**
