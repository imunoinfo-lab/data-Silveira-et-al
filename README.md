# Generation of pMHC Models and Image Dataset

## Overview

This repository contains structural models (PDB files) and corresponding electrostatic surface images of peptide–MHC (pMHC) complexes.

The dataset is divided into two main categories:
- **Human (self-peptides)**
- **Viral (immunogenic peptides)**

Each category is further organized into:
- `PDBs/` – structural models of pMHC complexes  
- `images/` – electrostatic surface representations  

---

## Peptide Selection

A total of **353 peptides** were included in this dataset.

### Human Peptides (Self-peptides) — 106 total

- **65 peptides** were obtained from the HLA Ligand Atlas  
  Selection criteria:
  - Restricted to **HLA-A*02:01**
  - Length of **9 amino acids**
  - Present in **at least 3 tissues**
  - **No reported immunogenicity** in IEDB

- **41 peptides** were derived from the following proteins:
  - **Cytosolic proteins:**
    - Gelsolin (UniProt: P06396)
    - Actin (UniProt: P63261)
  - **Secreted protein:**
    - Insulin (UniProt: P01308)

---

### Viral Peptides — 247 total

- Retrieved from the **Immune Epitope Database (IEDB)**
- Selected based on **reported immunogenicity**

---

## pMHC Model Generation

All peptides were docked into **HLA-A*02:01** to generate pMHC structural models.

- Tool: DockTope  
- Docking engine: AutoDock Vina  

Each peptide was individually docked into the MHC binding groove.

---

## Electrostatic Potential Calculation

Electrostatic potentials were calculated focusing on the peptide-binding cleft region.

- Software: DelPhi  

These calculations were used to characterize surface charge distribution and potential interaction patterns.

---

## Image Generation

Molecular surface visualizations were generated using:

- GRASP2  

Outputs include electrostatic surface representations of the peptide-binding region.

---

## Computational Details

- Time per model: **2–3 hours**
- Hardware:
  - 8 CPU cores  
  - 12 GB RAM  

For **353 complexes**, total compute time was approximately:

**~700–1,050 hours**

---

## Quality Control

Each model was manually inspected to ensure:

- Correct peptide positioning  
- Proper epitope representation  

This step ensured dataset reliability.

---

## Repository Structure

- PDBs/
  - human/ (self-peptides)
  - viral/ (immunogenic peptides)
- images/
  - human/
  - viral/
