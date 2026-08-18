# assignment_02_genome_exploration
# Genome Exploration II

## Species
Pelophylax lessonae

## NCBI Assembly Accession
GCF_965119305.1

## Assembly Level
Scaffold

## FASTA File Used
GCF_965119305.1_aPelLes1.hap1.1_genomic.fna.gz

## Genome Source
NCBI Assembly Database

## Objective
To explore the structure of a genome assembly using Galaxy by generating assembly statistics, examining sequence lengths, performing a length-filtering experiment, and identifying potential open reading frames (ORFs).

## Tools Used and Important Parameters

### 1. Fasta Statistics
Purpose:
Generate assembly statistics for the complete genome assembly.

Parameters:
- Input dataset: GCF_965119305.1_aPelLes1.hap1.1_genomic.fna.gz
- Estimated genome size: Not provided
- Generate gap statistics: False

### 2. Compute Sequence Length
Purpose:
Calculate the length of each scaffold in the assembly.

Parameters:
- Input dataset: GCF_965119305.1_aPelLes1.hap1.1_genomic.fna.gz
- Output sorted from largest to smallest sequence length

### 3. Filter Sequences by Length
Purpose:
Create a filtered version of the assembly for comparison.

Parameters:
- Input dataset: GCF_965119305.1_aPelLes1.hap1.1_genomic.fna.gz
- Minimum length: 10,000 bp
- Maximum length: 0 (no maximum limit)

### 4. Fasta Statistics on Filtered Assembly
Purpose:
Compare assembly statistics before and after filtering.

Parameters:
- Input dataset: Filter sequences by length on dataset 2 (≥10 kb)

### 5. EMBOSS getorf
Purpose:
Identify potential open reading frames (ORFs) in a selected scaffold.

Input:
- HAP1_SCAFFOLD_108 (NW_028120139.1)

Parameters:
- Genetic code: Standard
- Maximum nucleotide size: 5000
- Output: Translation of regions between STOP codons
- All START codons code for Methionine: Yes
- Reverse complement search: Yes
- Output format: FASTA

## Short Interpretation

The Pelophylax lessonae genome assembly appears relatively complete because a large portion of the genome is contained within a few very large scaffolds. The scaffold N50 value is high and the L50 value is low, indicating that much of the genome is represented by long sequences. Filtering sequences shorter than 10 kb removed 106 scaffolds but caused only a small decrease in total genome size, showing that short scaffolds contribute little to the assembly length. The GC content was 43.74%, which is within the expected range for vertebrate genomes. The ORF analysis identified many potential protein-coding regions, including several long ORFs. However, ORFs are only possible coding sequences and cannot be considered confirmed genes without additional evidence such as annotation, transcript data, or similarity to known proteins.
