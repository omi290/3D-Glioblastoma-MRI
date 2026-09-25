# Dataset Information

## Purpose
This directory is designated for organizing datasets used in the "3D Deep Learning-Based Glioblastoma Classification and Segmentation from Multimodal MRI" project. It provides information regarding the datasets investigated, the primary dataset used for ongoing technical development, data access links, and details about local data organization.

## Primary Dataset
The primary dataset currently obtained for technical development is **BraTS 2021**.

- **Official Source:** [https://www.med.upenn.edu/cbica/brats2021/](https://www.med.upenn.edu/cbica/brats2021/)
- **Kaggle Source Used:** [https://www.kaggle.com/datasets/dschettler8845/brats-2021-task1](https://www.kaggle.com/datasets/dschettler8845/brats-2021-task1)

BraTS 2021 provides multimodal MRI data and tumor segmentation annotations. The available MRI modalities are:
- T1 (native T1-weighted)
- T1ce / T1Gd (post-contrast T1-weighted)
- T2 (T2-weighted)
- FLAIR (T2 Fluid Attenuated Inversion Recovery)

Additionally, the BraTS 2021 dataset includes a classification component associated with MGMT promoter methylation status. This is a specific classification target and differs from a simple "glioblastoma vs. non-glioblastoma" classification task. 

**Note:** The exact classification target for this project will be finalized as part of the formal project methodology based on mentor and project requirements.

## Additional Candidate Datasets Investigated
The following datasets have been researched and investigated as potential candidates for future experiments, secondary reference, or external validation. **They have not yet been downloaded or used for model training.**

### 1. BraTS 2020
- **Official Source:** [https://www.med.upenn.edu/cbica/brats2020/data.html](https://www.med.upenn.edu/cbica/brats2020/data.html)
- **Registration/Access:** [https://www.med.upenn.edu/cbica/brats2020/registration.html](https://www.med.upenn.edu/cbica/brats2020/registration.html)
- **Description:** A multimodal brain MRI dataset with tumor segmentation annotations and associated clinical information. It is being considered as a secondary/reference dataset.

### 2. UPenn-GBM
- **Official Source:** [https://www.cancerimagingarchive.net/collection/upenn-gbm/](https://www.cancerimagingarchive.net/collection/upenn-gbm/)
- **Description:** A large-scale glioblastoma imaging dataset providing MRI, segmentation, clinical, and molecular/genomic information. Its significant scale makes it highly suitable for future external validation or selected-subset experiments, rather than immediate local processing.

### 3. TCGA-GBM
- **Official Source:** [https://www.cancerimagingarchive.net/collection/tcga-gbm/](https://www.cancerimagingarchive.net/collection/tcga-gbm/)
- **Description:** A comprehensive glioblastoma imaging collection associated with clinical and genomic information. It is being investigated as a possible future research or external-validation resource.

### 4. BraTS-TCGA-GBM
- **Official Source:** [https://www.cancerimagingarchive.net/analysis-result/brats-tcga-gbm/](https://www.cancerimagingarchive.net/analysis-result/brats-tcga-gbm/)
- **Description:** A processed research dataset derived from TCGA-GBM that contains multimodal MRI and segmentation-related data. It is considered another strong candidate for future experiments or external validation.

## Large-Scale Datasets
Large-scale datasets were also investigated as potential future resources. Due to their substantial storage and computational requirements, they are currently being considered for future cloud-based or selected-subset experiments rather than immediate full-scale local processing.

## Local Data Organization
The project directory structure is designed to keep raw datasets, processed outputs, and metadata organized locally. 

```
data/
├── raw/
│   └── BraTS2021/
├── processed/
└── metadata/
```

- **`data/raw/`**: Original downloaded datasets. Not committed to GitHub.
- **`data/processed/`**: Future preprocessed MRI volumes.
- **`data/metadata/`**: Dataset metadata, labels, split information, and related non-raw data.

## Data Privacy and GitHub Data Policy
**Raw MRI datasets are not stored in this repository.**

Due to the massive scale of medical imaging data, licensing/access conditions, and standard data privacy practices, no raw medical imaging files (e.g., `.nii`, `.nii.gz`, `.tar`, `.zip`, patient cases) are uploaded to GitHub. 

The `.gitignore` strictly prevents these file types from being committed. Other researchers looking to reproduce this work should obtain the datasets directly from the official sources linked above and place them in the `data/raw/` directory.

## Future Plans
Future work involving this data directory will include:
- Completing dataset extraction and structural setup.
- Designing an MRI preprocessing pipeline (e.g., normalization, alignment).
- Finalizing the classification labels and data splits (train/val/test).
