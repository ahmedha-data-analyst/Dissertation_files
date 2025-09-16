# Appendix A.1 — README

## Overview
This repository contains the code for the Elliptic Bitcoin transaction graph dissertation.  
It covers:
- **EDA:** exploration of the graph and tabular attributes.
- **Modeling:** K-Fold training of GNNs, extraction of node embeddings, and enhancement of baseline ML models.
- **Results/Plots:** consolidated figures and tables.

**Notebooks**
1. `elliptic_eda.ipynb`  
2. `elliptic_clean_train_test.ipynb`  
3. `results_plots.ipynb`

**Dataset**  
Elliptic Data Set (Kaggle): [https://www.kaggle.com/datasets/ellipticco/elliptic-data-set](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set)

---

## Repository Structure
    Dissertation_files/
    ├─ elliptic_eda.ipynb
    ├─ elliptic_clean_train_test.ipynb
    ├─ results_plots.ipynb
    └─ (place dataset CSVs here)

---

## Data Requirements
Place the three CSVs **in the same directory as the notebooks**:
- `elliptic_txs_features.csv`  (loaded with `header=None`)
- `elliptic_txs_classes.csv`
- `elliptic_txs_edgelist.csv`

No prior preprocessing is required.

---

## Dependencies
The following Python libraries are used across the notebooks:
- **Core:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Graphs:** `networkx`
- **Statistics:** `scipy`
- **Machine Learning:** `scikit-learn`
- **Gradient Boosting:** `xgboost`
- **Deep Learning:** `torch`
- **Graph Neural Networks:** `torch_geometric`

Additional: `pathlib`, `warnings` (stdlib)

---

## Quick Start

1. **Clone the repo**
   ```bash
   git clone https://github.com/ahmedha-data-analyst/Dissertation_files.git
   cd Dissertation_files

2. **Set up environment**
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt

3. **Download data**
Get the dataset from Kaggle and place:
	•	elliptic_txs_features.csv
	•	elliptic_txs_classes.csv
	•	elliptic_txs_edgelist.csv
into the repo root (same folder as the notebooks).

4. **Run notebooks**
jupyter lab   # or: jupyter notebook

Execute notebooks in this order:
	1.	elliptic_eda.ipynb
	2.	elliptic_clean_train_test.ipynb
	3.	results_plots.ipynb

## Notebook Details
    	•	elliptic_eda.ipynb
    Exploratory analysis and visualization of the dataset.
    	•	elliptic_clean_train_test.ipynb
    K-Fold GNN training and baseline ML enhancement.
    Output: baseline_enhancement_results_optimized.csv
    	•	results_plots.ipynb
    Consolidates results and generates figures.
    Outputs: f1_heatmap.png, f1_grouped_bars.png

## Troubleshooting
	•	File not found: Ensure the three CSVs are present in the repo root and named exactly as above.
	•	Torch Geometric install issues: Ensure you install the correct build of torch (CPU or CUDA) before torch_geometric.
	•	Memory issues: The dataset is large. Run notebooks one at a time and close other apps if needed.

## Citation
	•	Elliptic Dataset (Kaggle): https://www.kaggle.com/datasets/ellipticco/elliptic-data-set



