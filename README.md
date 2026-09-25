# 3D-Glioblastoma-MRI

## Project Title
3D Deep Learning-Based Glioblastoma Classification and Segmentation from Multimodal MRI

## Overview
The project investigates 3D deep-learning methods for multimodal MRI analysis of glioblastoma, with classification and tumor segmentation as the core objectives.

The project uses multimodal brain MRI, with the expected modalities including:
- T1
- T1ce / T1Gd
- T2
- FLAIR

Tumor detection is currently an optional experimental extension that may be investigated if technically feasible.

## Project Objectives
- Study multimodal 3D MRI data.
- Develop an appropriate MRI preprocessing pipeline.
- Develop a 3D deep-learning classification component.
- Develop a 3D tumor segmentation component.
- Evaluate models using appropriate quantitative metrics.
- Visualize MRI volumes and model predictions.
- Investigate optional tumor detection.
- Investigate generalization using additional datasets where feasible.

## Current Progress

### Completed / Initiated
- Project title finalized.
- GitHub repository initialized.
- Project directory structure created.
- Dataset investigation completed/initiated.
- Multiple candidate datasets reviewed.
- BraTS 2021 dataset obtained from Kaggle.
- BraTS 2021 data extracted locally.
- Initial dataset organization started.
- Dataset modalities and annotations are being investigated.

### In Progress
- Dataset inspection.
- MRI visualization.
- Dataset preprocessing design.
- Classification-label definition.
- Segmentation pipeline design.
- Experimental setup.

### Planned
- MRI preprocessing.
- Dataset splitting.
- Classification model.
- 3D segmentation model.
- Training.
- Evaluation.
- Visualization.
- Optional detection.
- External dataset validation/generalization.

## Dataset
BraTS 2021 is currently the primary development dataset. Additional datasets have been investigated for secondary reference or external validation. See `data/README.md` for extended details.

| Dataset | Purpose/Role | MRI Data | Segmentation | Classification/Clinical Information | Status |
|---|---|---|---|---|---|
| [BraTS 2021](https://www.med.upenn.edu/cbica/brats2021/) | Primary development candidate | Multimodal | Yes | MGMT-related classification | Obtained |
| [BraTS 2020](https://www.med.upenn.edu/cbica/brats2020/data.html) | Secondary/reference | Multimodal | Yes | Clinical/survival information | Investigated |
| [UPenn-GBM](https://www.cancerimagingarchive.net/collection/upenn-gbm/) | External/future | Multimodal | Yes | Clinical/molecular | Investigated |
| [TCGA-GBM](https://www.cancerimagingarchive.net/collection/tcga-gbm/) | External/future | MRI | Dataset-dependent | Clinical/genomic | Investigated |
| [BraTS-TCGA-GBM](https://www.cancerimagingarchive.net/analysis-result/brats-tcga-gbm/) | External/future | Multimodal | Yes | Research/clinical information | Investigated |

## Methodology
The intended workflow for the deep learning pipeline is:

Multimodal MRI → preprocessing → normalization/alignment → multimodal 3D representation → 3D feature extraction → classification → segmentation → evaluation → visualization

*(Note: Detection is explicitly an optional component.)*

## Model Development
Model architecture selection and implementation are currently under development. Possible future models may include:
- 3D CNN-based classification
- 3D U-Net / related encoder-decoder architecture for segmentation

## Evaluation
Planned quantitative metrics for evaluation:

**Classification metrics:**
- Accuracy
- Precision
- Recall
- F1-score

**Segmentation metrics:**
- Dice coefficient
- IoU

## Repository Structure
```
3D-Glioblastoma-MRI/
├── data/
│   ├── raw/
│   ├── processed/
│   └── metadata/
├── notebooks/
├── preprocessing/
├── classification/
├── segmentation/
├── detection/
├── models/
├── training/
├── evaluation/
├── visualization/
├── experiments/
├── configs/
├── scripts/
├── docs/
└── tests/
```
- **data/**: Contains datasets, dataset documentation, and processed data.
- **notebooks/**: Jupyter notebooks for EDA, prototyping, and visualization.
- **preprocessing/**: Scripts for MRI normalisation, alignment, and dataset preparation.
- **classification/**: Code for the 3D MRI classification pipeline.
- **segmentation/**: Code for the 3D tumor segmentation pipeline.
- **detection/**: Optional scripts for tumor detection experiments.
- **models/**: Neural network architecture definitions.
- **training/**: Training loops, schedulers, and optimization scripts.
- **evaluation/**: Metrics and evaluation logic.
- **visualization/**: Plotting and MRI volume visualization scripts.
- **experiments/**: Tracking different runs and ablation studies.
- **configs/**: Hyperparameters and environment configuration files.
- **scripts/**: Utility bash/python scripts.
- **docs/**: Detailed project documentation.
- **tests/**: Unit and integration tests.

## Data Handling
Raw MRI datasets are not stored in this repository due to dataset size, licensing/access conditions, and responsible handling of medical imaging data. Users should obtain datasets from the official sources linked in `data/README.md` and place them locally.

## Reproducibility
The project will progressively document the following to ensure reproducibility:
- Dataset source
- Dataset organization
- Preprocessing
- Train/validation/test split
- Model configuration
- Training configuration
- Evaluation metrics
- Experimental results

## Project Status
Active Development — Initial Dataset and Repository Setup

## Future Work
- Complete preprocessing pipeline.
- Define and prepare classification labels.
- Develop baseline classification model.
- Develop baseline segmentation model.
- Train and evaluate models.
- Visualize predictions.
- Investigate optional detection.
- Evaluate cross-dataset/generalization performance where feasible.

## Disclaimer / Research Use
This project is an academic/research prototype developed for a B.Tech Major Project and is not intended for clinical diagnosis, medical decision-making, or commercial use.