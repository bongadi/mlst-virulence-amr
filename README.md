# mlst-virulence-amr

# MLST (Multilocus Sequence Typing)

## Purpose:
MLST (Multilocus Sequence Typing) is used to classify bacterial strains by sequencing internal fragments of multiple housekeeping genes. This method helps in the identification of bacterial species, understanding evolutionary relationships, and epidemiological studies.

## Installation:
1. Create a new environment for MLST:
   ```
   conda create -n mlst_env
   ```

2. Activate the environment:
   ```
   conda activate mlst_env
   ```

3. Install the MLST tool:
   ```
   conda install -c bioconda mlst
   ```

## How to Run:
To run MLST on an assembled genome:
```
mlst <assembly_file.fasta>
```
Example:
```
mlst sample_assembly.fasta
```

---

# Abricate (Virulence and AMR Gene Detection)

## Purpose:
Abricate is a tool used to scan bacterial genome assemblies (in FASTA format) for the presence of known virulence, resistance, or plasmid genes using databases like **virulencefinder** for virulence genes and **resfinder** for antimicrobial resistance genes.

## Installation:
1. Create a new environment for Abricate:
   ```
   conda create -n abricate_env
   ```

2. Activate the environment:
   ```
   conda activate abricate_env
   ```

3. Install Abricate:
   ```
   conda install -c bioconda abricate
   ```

## How to Run:
To detect virulence genes:
```
abricate --db virulencefinder <assembly_file.fasta>
```
Example:
```
abricate --db virulencefinder sample_assembly.fasta
```

To detect AMR genes:
```
abricate --db resfinder <assembly_file.fasta>
```

---

# AMRFinderPlus (Antimicrobial Resistance Gene Detection)

## Purpose:
AMRFinderPlus is a powerful tool developed by NCBI to detect AMR (Antimicrobial Resistance) genes and also identify virulence factors and other resistance elements from bacterial genome assemblies or protein sequences.

## Installation:
1. Create a new environment for AMRFinderPlus:
   ```
   conda create -n amrfinder_env
   ```

2. Activate the environment:
   ```
   conda activate amrfinder_env
   ```

3. Install AMRFinderPlus:
   ```
   conda install -c bioconda ncbi-amrfinderplus
   ```

## How to Run:
To run AMRFinderPlus on a set of contigs:
```
amrfinder -n <assembly_file.fasta> -o amr_results.txt
```
Example:
```
amrfinder -n sample_assembly.fasta -o amr_output.txt
```

This will generate a text file (`amr_results.txt`) with detected AMR genes.
