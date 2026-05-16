# Greedy MASS for RNA Secondary Structure Analysis

This project implements and benchmarks a simplified greedy heuristic inspired by the Maximum Agreement Secondary Structures (MASS) problem. 

The goal of MASS is to preserve as many RNA structural features as possible while keeping the number of induced clusters below a chosen limit tau. This project uses a lightweight greedy feature-selection approach:

1. Start with no selected features
2. Sort features by multiplicity (number of 1s in each column)
3. Add a feature only if the number of induced clusters stays ≤ tau
4. Prefer features that create more clusters

The project compares:
- Greedy MASS heuristic
- Hierarchical clustering (Ward linkage)
- Consensus feature selection baseline
- Small beam-search extension

Experiments are run on both simulated binary matrices and a real dataset from the tRNA family (RF00005) from Rfam.

---

## Files

- `greedy_mass_projectCS466.ipynb` — main notebook
- `rfam.txt` — Rfam seed alignment dataset
- `README.md`

---

## Running in Google Colab

1. Open `greedy_mass_projectCS466.ipynb` in Google Colab
2. Upload `rfam.txt`
3. Install ViennaRNA: !pip install ViennaRNA
