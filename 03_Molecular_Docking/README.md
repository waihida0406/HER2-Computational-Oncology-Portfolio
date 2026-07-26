 Project 3: Molecular Docking of *Ventilago madraspatana* Phytochemicals Against HER2 (PDB ID: 5TDN)
 Status

Completed

---

Background

Molecular docking is a computational technique used to predict the preferred binding orientation of a ligand within the active site of a target protein. It estimates the binding affinity and identifies molecular interactions responsible for protein–ligand complex formation.

In this project, phytochemicals obtained from *Ventilago madraspatana* were screened against the Human Epidermal Growth Factor Receptor 2 (HER2), a clinically important therapeutic target in HER2-positive breast cancer. The objective was to identify phytochemicals with strong binding affinity that could serve as potential lead compounds for further computational investigation.

---

Objective

To evaluate the binding affinity and molecular interactions of selected phytochemicals from *Ventilago madraspatana* against the HER2 protein using molecular docking and identify promising lead compounds for molecular dynamics simulation.

---

Target Protein

| Parameter | Details |
|-----------|---------|
| Protein | Human Epidermal Growth Factor Receptor 2 (HER2) |
| Gene | ERBB2 |
| PDB ID | 5TDN |
| Organism | Homo sapiens |
| Disease | HER2-positive Breast Cancer |

---

Ligand Source

Selected phytochemicals from *Ventilago madraspatana*

Databases Used

- IMPPAT
- PubChem

---

Software Used

- PyRx
- AutoDock Vina
- BIOVIA Discovery Studio Visualizer
- PyMOL
- Protein Data Bank (PDB)

---

Methodology

Step 1: Protein Preparation

The HER2 crystal structure (PDB ID: 5TDN) was downloaded from the Protein Data Bank and prepared by removing water molecules, co-crystallized ligands, and unnecessary heteroatoms. Hydrogen atoms were added before docking.

Step 2: Ligand Preparation

Phytochemicals from *Ventilago madraspatana* were retrieved from the IMPPAT database. Their SMILES and structural information were obtained from PubChem and converted into docking-compatible formats.

Step 3: Energy Minimization

All ligands were energy minimized using PyRx to obtain stable conformations prior to docking.

Step 4: Molecular Docking

Docking was performed using AutoDock Vina integrated within PyRx. The HER2 active site was defined as the docking region, and binding affinity values were calculated for each ligand.

Step 5: Interaction Analysis

The best docking poses were analyzed in BIOVIA Discovery Studio Visualizer to identify:

- Hydrogen bonds
- Hydrophobic interactions
- Pi interactions
- Amino acid residues involved in ligand binding

---

Docking Results

A total of **14 phytochemicals** were docked against HER2. Binding affinity values ranged from **−5.9 to −7.7 kcal/mol**, where more negative values indicate stronger predicted binding.

| Ligand ID | Binding Affinity (kcal/mol) |
|-----------|----------------------------:|
| 931 | -5.9 |
| 3220 | -7.2 |
| 6780 | -6.5 |
| 10151 | -7.2 |
| 10208 | -7.1 |
| 10639 | -6.8 |
| 442767 | -7.2 |
| 11013000 | -7.3 |
| 11415004 | -7.1 |
| 12444971 | -7.1 |
| 15108779 | -7.0 |
| 76323252 | **-7.7** |
| 76326825 | -7.0 |
| 136247467 | -6.6 |

---

Top Performing Compounds

| Rank | Ligand ID | Binding Affinity (kcal/mol) |
|------|-----------|----------------------------:|
| 1 | 76323252 | **-7.7** |
| 2 | 11013000 | -7.3 |
| 3 | 3220 | -7.2 |
| 4 | 10151 | -7.2 |
| 5 | 442767 | -7.2 |

---

Result Interpretation

The molecular docking analysis demonstrated that the screened phytochemicals exhibited moderate to strong binding affinities towards the HER2 protein.

Among all compounds, **Ligand ID 76323252** showed the strongest predicted interaction with HER2, with a binding affinity of **−7.7 kcal/mol**, indicating the highest binding potential among the screened compounds.

Ligands **11013000**, **3220**, **10151**, and **442767** also displayed favorable binding affinities ranging from **−7.2 to −7.3 kcal/mol**, suggesting their potential as promising lead molecules for further computational analysis.

Based on these results, the top-performing compounds were selected for protein–ligand interaction analysis and subsequent **100 ns Molecular Dynamics simulation** to evaluate the stability of the docked complexes.

---

Project Deliverables

- HER2 Protein Structure (PDB ID: 5TDN)
- Prepared Ligand Structures
- Docking Results Table
- Binding Affinity Analysis
- 2D Protein–Ligand Interaction Diagrams
- 3D Binding Pose Visualizations
- PyRx Docking Output
- Discovery Studio Interaction Images

---

Skills Demonstrated

- Molecular Docking
- Virtual Screening
- Structure-Based Drug Discovery
- AutoDock Vina
- PyRx
- BIOVIA Discovery Studio
- Protein–Ligand Interaction Analysis
- Computational Drug Discovery

---

References

1. Protein Data Bank (https://www.rcsb.org/)
2. PubChem Database
3. IMPPAT Database
4. AutoDock Vina
5. PyRx Virtual Screening Tool
6. BIOVIA Discovery Studio Visualizer

---

Next Project

➡ **Project 4: 100 ns Molecular Dynamics Simulation of the HER2–Ligand Complex**
