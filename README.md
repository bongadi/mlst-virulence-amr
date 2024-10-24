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
   <img width="608" alt="image" src="https://github.com/user-attachments/assets/8003f9ee-fc5b-4553-bef8-d1a52aee7e33">


3. Install the MLST tool:
   ```
   conda install -c bioconda mlst
   ```
<img width="544" alt="image" src="https://github.com/user-attachments/assets/cf4ab5c6-a8fd-4df5-89ef-c0f39a9ed8d3">

## How to Run:
To run MLST on an assembled genome:
```
mlst <assembly_file.fasta>
```
Example:
```
mlst sample_assembly.fasta
```
 <img width="615" alt="image" src="https://github.com/user-attachments/assets/43b99ec6-1f94-42d1-9f09-29e0d322c475">

 <img width="587" alt="image" src="https://github.com/user-attachments/assets/eb47f511-63c4-4f6e-ba4f-fc82d5f37ee7">

 <img width="607" alt="image" src="https://github.com/user-attachments/assets/7491b685-864f-448a-a979-3d15857139a3">


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
    <img width="620" alt="image" src="https://github.com/user-attachments/assets/587f8d59-06f3-41e2-89da-2a3406fd847f">


3. Install Abricate:
   ```
    <img width="474" alt="image" src="https://github.com/user-attachments/assets/7c58a4a6-887f-46bd-9900-5316c60d8c04">

   conda install -c bioconda abricate
   ```
    <img width="422" alt="image" src="https://github.com/user-attachments/assets/e45292cc-cec3-4a7a-809a-4655f543e7b2">


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
<img width="813" alt="image" src="https://github.com/user-attachments/assets/066fae91-7d2a-4f9a-8a89-7d2ba1bbcd91">

<img width="755" alt="image" src="https://github.com/user-attachments/assets/e9be9233-d03f-4ade-a1a7-40e708a9bdc3">

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
