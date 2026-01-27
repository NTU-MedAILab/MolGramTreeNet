# MolGramTreeNet

## A Multimodal Molecular Property Prediction Model via Grammar Tree-Constrained Molecular Representation

MolGramTreeNet is a novel deep learning framework that integrates 1D grammar tree structures (via Context-Free Grammar) and 2D molecular graphs to explicitly encode chemical rules and hierarchical semantics for accurate molecular property prediction.

---

### Environment Setup

This project requires **Python 3.8**. We recommend creating a virtual environment to manage dependencies.

**Installation steps:**

```bash
# 1. (Optional) Create a virtual environment using conda
conda create -n MolGramTreeNet python=3.8
conda activate MolGramTreeNet

# 2. Install required packages
pip install -r requirements.txt
```

### Datasets

The datasets analyzed in this study are **standardized public benchmarks**. All processed data files ready for training are located in the `data/` directory of this repository.

We utilize the following datasets:

**1. MoleculeNet**
- **Description:** Standard benchmarks including BACE, BBBP, ClinTox, Tox21, ToxCast, SIDER, HIV, ESOL, FreeSolv, and Lipophilicity.
- **Source:** [MoleculeNet Official](https://moleculenet.org/)
- **Location in Repo:** `data/BACE, BBBP, ClinTox, Tox21, ToxCast, SIDER, HIV, ESOL, FreeSolv, Lipophilicit`

**2. QM9**
- **Description:** Quantum chemistry benchmark for molecular properties.
- **Source:** [QM9 Database](https://quantum-machine.org/datasets/)
- **Location in Repo:** `data/qm9/`

**3. HBV (CC50)**
- **Description:** A curated hepatotoxicity dataset derived from ChEMBL (bioactive compounds with CC50 values).
- **Source:** [ChEMBL Database](https://www.ebi.ac.uk/chembl/)
- **Location in Repo:** `data/cc50/`

> **Note:** You can directly use the standardized `.csv` or `.pt` files provided in the `data/` folder to reproduce our results without re-downloading from the original sources.

### Usage

To train the model or reproduce the regression/classification results, please execute the corresponding fine-tuning script for your target dataset.

**Command Syntax:**
```bash
python finetune_regression_{dataset_name}.py
```
**Examples:**

To run the regression task on the ESOL dataset:

```bash
python finetune_regression_ESOL.py
```
> **Note:**(Please replace {dataset_name} with the specific dataset file name you wish to test, corresponding to the scripts available in the root directory.)
