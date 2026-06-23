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

[]
