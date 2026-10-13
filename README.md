# Multimodal Survival Prediction for Non-Small Cell Lung Cancer

This repository contains the source code developed for the study:

**"Survival Prediction in NSCLC: A Comparison of Unimodal and Multimodal Models"**

The study investigates unimodal and multimodal approaches for survival prediction in patients with Non-Small Cell Lung Cancer (NSCLC), combining clinical data and computed tomography (CT) images from the NSCLC-Radiomics (Lung1) dataset.

## Dataset

The experiments were conducted using the **NSCLC-Radiomics (Lung1)** dataset, publicly available through The Cancer Imaging Archive (TCIA).

Due the size of the imaging data, the dataset is not included in this repository.

## Repository Structure

### clinical_preprocessing.ipynb

Notebook containing the preprocessing pipeline for clinical variables, including data cleaning, transformation, and preparation for survival analysis.

### image_preprocessing.ipynb

Notebook containing the preprocessing pipeline for CT images, including image conversion, resampling, clipping, windowing, and tensor generation.

### models.ipynb

Notebook containing the implementation and evaluation of the survival prediction models:

- CoxNet
- Random Survival Forest (RSF)
- ResNet-18 3D
- Multimodal DeepSurv
- Multimodal RSF

### supplementary/

Supplementary materials containing descriptive statistics and cohort information used in the study.

### img/

Figures and images used in the repository documentation.

## Software Requirements

The experiments were developed in Python.

Main libraries:

- NumPy
- Pandas
- Scikit-learn
- Scikit-survival
- Lifelines
- PyTorch
- MONAI
- Nibabel
- SimpleITK

## Reproducibility

This repository provides the source code used for:

- Clinical data preprocessing;
- Image preprocessing;
- Model training;
- Model evaluation.

Researchers interested in reproducing the experiments should first obtain access to the Lung1 dataset through TCIA and then execute the notebooks following the workflow described above.

## Citation

If you use this repository, please cite:

```bibtex
@InProceedings{10.1007/978-3-032-39892-5_6,
author="da Costa Bezerra, Lara Vit{\'o}ria
and de Oliveira, Amanda Gondim
and de Lima Oliveira Filho, Isaac
and de Medeiros Santos, Araken",
editor="Recamonde-Mendoza, Mariana
and Barros, Rodrigo C.",
title="Survival Prediction in NSCLC: A Comparison of Unimodal and Multimodal Models",
booktitle="Intelligent Systems",
year="2027",
publisher="Springer Nature Switzerland",
address="Cham",
pages="81--95",
abstract="Non-small cell lung cancer (NSCLC) is the leading cause of cancer-related death, and predicting survival is critical for treatment planning. Unimodal models, however, may limit the capture of clinical and tumor heterogeneity. This study investigates the impact of different multimodal integration strategies on survival modeling. Five models were evaluated using the NSCLC-Radiomics (Lung1) dataset from The Cancer Imaging Archive: DeepSurv and Random Survival Forest (RSF) with clinical data, and two distinct multimodal strategies: (I) a DeepSurv model employing a late-fusion strategy, and (II) a feature-level fusion strategy that combines ResNet-18 image features with clinical variables for survival prediction using a Random Survival Forest (RSF). The evaluation was performed using stratified cross-validation in 5 folds, employing the C-index and the Integrated Brier Score (IBS). The clinical models performed similarly, while the image-only model performed worse. Multimodal approaches improved the C-index, particularly the multimodal DeepSurv model (0.5935 {\textpm} 0.0159; p = 0.013984), although they were associated with a slight degradation in IBS, indicating a trade-off between discrimination and calibration. The multimodal RSF model also showed an improvement (0.5611 {\textpm} 0.0334; p = 0.001180). The results indicate that different multimodal integration strategies can improve discriminative performance in survival models for NSCLC, with the late fusion approach showing the best overall performance. However, performance remains moderate, suggesting that further improvements are needed for clinical application.",
isbn="978-3-032-39892-5"
}
```
