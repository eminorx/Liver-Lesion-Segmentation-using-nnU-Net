# Liver Lesion Segmentation using nnU-Net

This project focuses on liver and liver lesion segmentation from CT images using deep learning-based medical image segmentation methods. The notebook was developed on Kaggle and uses the nnU-Net framework for dataset preparation, preprocessing, model training, prediction, and evaluation.

## Project Overview

Liver lesion segmentation is an important task in medical image analysis, especially for supporting diagnosis, treatment planning, and quantitative evaluation from CT scans. In this project, I worked on automatic segmentation of the liver and liver lesions using abdominal CT volumes.

The main goal of this project is to build a segmentation pipeline that can:

- Prepare CT image and mask files for nnU-Net format
- Train a deep learning segmentation model
- Generate predictions on validation cases
- Evaluate liver and lesion segmentation performance using Dice score
- Visualize prediction results with CT slices, ground truth masks, and predicted masks

## Dataset

This project uses the LiTS dataset for liver and liver tumor segmentation.

The dataset is not included in this repository due to size and licensing restrictions. It was used through the Kaggle environment.

## Tools and Libraries

- Python
- nnU-Net v2
- NumPy
- nibabel
- Matplotlib
- tqdm
- Kaggle Notebook

## Workflow

The notebook includes the following main steps:

1. Installation of nnU-Net
2. Importing required libraries and setting environment variables
3. Finding CT volume and segmentation mask files
4. Creating case ID mappings and train/validation split
5. Converting the dataset into nnU-Net format
6. Creating the `dataset.json` file
7. Running preprocessing
8. Training a 2D nnU-Net model
9. Running prediction on validation cases
10. Calculating case-level Dice scores
11. Visualizing training curves and segmentation outputs

## Model

The project uses a 2D nnU-Net configuration for liver and liver lesion segmentation.

The model was trained using:

- nnU-Net dataset format
- CT images as input
- Liver and tumor masks as segmentation labels
- Dice-based evaluation

## Results

The project achieved the following Dice scores on the validation setup:

| Target | Dice Score |
|---|---:|
| Liver | 0.929 |
| Liver Lesion | 0.697 |

These results show that the model performs strongly on liver segmentation and provides a solid baseline for liver lesion segmentation, which is generally a more challenging task because lesions are smaller, more variable, and harder to distinguish from surrounding tissue.

<img width="415" height="343" alt="image" src="https://github.com/user-attachments/assets/3ee7b561-bef5-4bdd-9e72-5ffacaba87a3" />
<img width="432" height="174" alt="image" src="https://github.com/user-attachments/assets/5b2af0c7-bf38-48ff-892f-3d1c76fe29b1" />
<img width="427" height="174" alt="image" src="https://github.com/user-attachments/assets/48f5e10a-581c-4d95-9589-d78bc920055e" />


## Visualizations

The notebook includes visualizations for:

- Training loss and pseudo Dice curves
- Case-level Dice comparison
- CT image, ground truth mask, and prediction overlay
- TP / FP / FN breakdown for lesion segmentation

## Notes

This repository contains the Kaggle notebook version of the project. The dataset and trained model checkpoints are not included in the repository due to file size and dataset restrictions.


## Author

Emin Imanov  
Electrical and Electronics Engineering Student  
Interested in Data Science, Machine Learning, Deep Learning, and Computer Vision
