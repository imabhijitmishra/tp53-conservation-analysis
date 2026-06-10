# TP53 Protein Conservation Analysis Across Vertebrate Species

## Author

Abhijit Mishra

## Project Overview

This project investigates the evolutionary conservation of the TP53 protein across representative vertebrate species using comparative bioinformatics approaches.

TP53 encodes the tumor protein p53, often referred to as the "guardian of the genome" due to its critical role in maintaining genomic stability. The protein regulates cell cycle progression, DNA repair, apoptosis, senescence, and stress-response pathways. Because of these essential cellular functions, TP53 is expected to be highly conserved throughout vertebrate evolution.

To test this hypothesis, TP53 protein sequences from six vertebrate species were retrieved from the NCBI Protein database and analyzed using multiple sequence alignment, sequence conservation analysis, pairwise identity comparison, sequence logo visualization, and phylogenetic reconstruction.

---

# Objectives

The objectives of this study were:

* Retrieve TP53 protein sequences from diverse vertebrate species.
* Compare amino acid conservation across species.
* Identify conserved and variable regions within the TP53 protein.
* Quantify sequence similarity using pairwise identity analysis.
* Infer evolutionary relationships based on TP53 protein sequences.
* Visualize conservation patterns using a sequence logo.
* Interpret the biological significance of TP53 conservation.

---

# Species Included

| Species                | Common Name | Accession Number |
| ---------------------- | ----------- | ---------------- |
| Homo sapiens           | Human       | NP_000537.3      |
| Mus musculus           | Mouse       | BAA82343.1       |
| Rattus norvegicus      | Rat         | NP_001416923.1   |
| Canis lupus familiaris | Dog         | NP_001376147.1   |
| Gallus gallus          | Chicken     | NP_990595.1      |
| Danio rerio            | Zebrafish   | XP_073805887.1   |

These species were selected to represent major vertebrate lineages while including widely used model organisms in biological research.

---

# Biological Background

The TP53 gene encodes a transcription factor that functions as a master regulator of cellular stress responses.

When DNA damage or cellular stress occurs, p53 becomes activated and can:

* Pause cell cycle progression
* Promote DNA repair mechanisms
* Trigger programmed cell death (apoptosis)
* Induce cellular senescence
* Prevent propagation of genetically damaged cells

Mutations in TP53 are among the most common alterations observed in human cancers.

Because TP53 performs essential functions, strong evolutionary pressure is expected to maintain its structure and activity across species.

---

# Data Collection

## Sequence Retrieval

TP53 protein sequences were downloaded in FASTA format from the NCBI Protein Database.

Tool Used:

https://www.ncbi.nlm.nih.gov/protein/

Downloaded sequences were stored individually and subsequently combined into a multi-FASTA file.

Files Generated:

* TP53 Homo sapiens.fasta
* TP53 Mus musculus.fasta
* TP53 Rattus norvegicus.fasta
* TP53 Canis lupus familiaris.fasta
* TP53 Gallus gallus.fasta
* TP53 Danio rerio.fasta
* TP53_all_species.fasta

---

# Methodology

## Step 1: Multiple Sequence Alignment

The combined TP53 protein dataset was analyzed using Clustal Omega.

Tool:

https://www.ebi.ac.uk/jdispatcher/msa/clustalo

Clustal Omega aligns homologous amino acid positions across multiple sequences by introducing gaps where necessary to maximize biological similarity.

Outputs:

* TP53_alignment.aln-clustal_num
* TP53_alignment_seqret.fasta
* TP53guidetree.tree
* TP53.phylotree
* TP53 percent identity matrix.pim

---

## Step 2: Sequence Conservation Analysis

The Clustal alignment was examined to identify conserved amino acid residues.

Alignment Symbols:

| Symbol | Meaning                         |
| ------ | ------------------------------- |
| *      | Fully conserved residue         |
| :      | Strongly conserved substitution |
| .      | Weakly conserved substitution   |
| -      | Gap introduced during alignment |

A high frequency of "*" symbols indicates strong evolutionary conservation.

---

## Step 3: Pairwise Identity Analysis

Clustal Omega generated a percent identity matrix measuring sequence similarity between all species pairs.

This analysis quantifies the proportion of identical amino acids shared between sequences.

Higher identity values indicate stronger evolutionary conservation and closer relationships.

---

## Step 4: Sequence Logo Generation

The aligned TP53 sequences were visualized using WebLogo.

Tool:

https://weblogo.berkeley.edu/

Output:

* TP53_sequence_logo.pdf

The sequence logo provides a graphical representation of amino acid conservation.

Interpretation:

* Tall letters indicate high conservation.
* Short letters indicate variability.
* Conserved positions often correspond to functionally important residues.

---

## Step 5: Phylogenetic Analysis

Phylogenetic relationships were inferred from the aligned TP53 protein sequences.

Tree visualization was performed using:

https://phylo.io/

Output:

* phylogenetic tree.io.png

The resulting tree illustrates evolutionary relationships inferred from TP53 sequence similarity.

---

# Results

## Multiple Sequence Alignment

The alignment revealed extensive conservation throughout the TP53 protein.

Key observations:

* Numerous fully conserved amino acid positions were detected.
* Conservation was strongest in the central region of the protein.
* The N-terminal region displayed greater variability.
* The C-terminal region exhibited moderate sequence divergence.
* Mammalian TP53 proteins shared particularly high similarity.

The abundance of conserved residues indicates strong evolutionary pressure to maintain TP53 function.

---

## Pairwise Sequence Identity Matrix

Selected results:

| Species Pair       | Percent Identity |
| ------------------ | ---------------- |
| Mouse vs Rat       | 88.86%           |
| Human vs Dog       | 83.16%           |
| Human vs Rat       | 77.38%           |
| Human vs Mouse     | 77.26%           |
| Human vs Chicken   | 54.95%           |
| Human vs Zebrafish | 51.83%           |

### Interpretation

Mouse and rat displayed the highest sequence similarity, reflecting their close evolutionary relationship.

Human and dog also showed strong conservation, consistent with their shared mammalian ancestry.

Human and zebrafish exhibited the lowest similarity, yet more than half of all amino acid positions remained identical despite hundreds of millions of years of evolutionary divergence.

This highlights the exceptional conservation of TP53 across vertebrates.

---

## Guide Tree Analysis

The guide tree generated during alignment showed the following clustering pattern:

* Mouse clustered with rat.
* Human clustered with dog.
* Chicken occupied an intermediate position.
* Zebrafish appeared as the most distant lineage.

Although guide trees are primarily used to assist alignment construction, the observed clustering closely matched accepted vertebrate evolutionary relationships.

---

## Phylogenetic Tree Analysis

The phylogenetic tree reconstructed from TP53 protein sequences revealed:

* A close relationship between mouse and rat.
* Strong similarity between human and dog TP53 proteins.
* Intermediate divergence of chicken.
* Greater divergence of zebrafish.

These relationships are consistent with established vertebrate phylogeny and support the reliability of the alignment.

---

## Sequence Logo Analysis

The sequence logo demonstrated extensive amino acid conservation across species.

Several positions displayed dominant amino acids with minimal variation.

Highly conserved residues likely correspond to regions essential for:

* DNA binding
* Structural stability
* Protein-protein interactions
* Regulatory functions

The sequence logo provides visual confirmation of the strong evolutionary constraints acting on TP53.

---

# Biological Significance

The results indicate that TP53 has been maintained under strong purifying selection throughout vertebrate evolution.

Key implications include:

* Essential cellular function.
* Strong evolutionary constraint.
* Preservation of critical protein domains.
* Maintenance of genome stability mechanisms.

The high degree of conservation observed across distantly related species suggests that many TP53 residues are functionally indispensable.

Mutations affecting these conserved positions are likely to disrupt protein function and may therefore be eliminated by natural selection.

---

# Limitations

This study has several limitations:

* Only six vertebrate species were included.
* Protein sequences were analyzed without nucleotide-level comparisons.
* Functional domains were not analyzed separately.
* Structural conservation was not investigated.
* Bootstrap-supported phylogenetic reconstruction was not performed.

---

# Future Directions

Potential extensions of this work include:

* Inclusion of additional vertebrate and invertebrate species.
* TP53 nucleotide sequence analysis.
* Structural comparisons using AlphaFold models.
* Domain-specific conservation studies.
* Evolutionary rate analysis.
* Mapping disease-associated TP53 mutations onto conserved residues.

---

# Conclusion

This study successfully analyzed TP53 protein conservation across six vertebrate species using bioinformatics approaches.

Multiple sequence alignment, pairwise identity analysis, sequence logo visualization, and phylogenetic reconstruction consistently demonstrated that TP53 is highly conserved throughout vertebrate evolution.

The highest similarity was observed between mouse and rat (88.86%), while human and zebrafish showed the lowest similarity (51.83%). Despite this divergence, substantial conservation remained across all species, emphasizing the fundamental biological importance of TP53.

Overall, the results support the hypothesis that TP53 has been maintained under strong evolutionary pressure due to its indispensable role in cellular regulation and genome stability.

---

# References

1. National Center for Biotechnology Information (NCBI) Protein Database.

2. Sievers F, Higgins DG. Clustal Omega for making accurate alignments of many protein sequences.

3. Crooks GE, Hon G, Chandonia JM, Brenner SE. WebLogo: A sequence logo generator.

4. Lane DP. Cancer. p53, guardian of the genome.

5. Levine AJ. p53, the cellular gatekeeper for growth and division.

6. Phylo.io: Interactive phylogenetic tree visualization platform.
