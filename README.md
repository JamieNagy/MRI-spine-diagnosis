
# MRI Spine Condition Diagnosis

## Overview
This project focuses on the automated diagnosis of spine conditions using MRI data. We utilize advanced 3D convolutional neural networks (CNNs) to analyze MRI images, specifically targeting various spine conditions such as spinal canal stenosis, neural foraminal narrowing, and subarticular stenosis.

## Key Features
- **Data Processing**: The system retrieves and processes MRI scans in DICOM format, transforming them into point cloud data and voxel grids for analysis.
- **Deep Learning Models**: A 3D CNN-based multi-head model, leveraging efficient neural network architectures (e.g., EfficientNet, MaxViT), is employed to classify spine conditions across multiple anatomical levels.
- **Custom Loss Functions**: The project implements logistic cumulative link models (Spacecutter) for classification, ensuring accurate diagnosis across a spectrum of conditions.
- **Visualization**: The processed MRI data is visualized as voxel grids and point clouds for better interpretability and debugging.
- **Automation**: The system performs automated classification of conditions like spinal canal stenosis, neural foraminal narrowing, and subarticular stenosis at multiple spinal levels (L1 to S1).

## Conditions Detected
The model is designed to detect the following conditions across spinal levels (L1-L2, L2-L3, L3-L4, L4-L5, L5-S1):
- Spinal Canal Stenosis
- Left and Right Neural Foraminal Narrowing
- Left and Right Subarticular Stenosis

## Technologies and Libraries Used
- **Pandas**: For data handling and processing.
- **Open3D**: For processing MRI data into point clouds and visualizing them.
- **PyTorch**: For building the 3D CNN model and handling the training and inference.
- **TorchIO**: For medical image preprocessing and augmentation.
- **Spacecutter**: Used for implementing cumulative link models to handle ordinal classification.
- **PyDicom**: For handling DICOM images, which are the standard format for medical imaging data.
- **Timm_3D**: For efficient 3D neural network architectures (e.g., EfficientNet, MaxViT).

## Workflow
1. **Data Retrieval**: MRI scans are retrieved from the given path, organized by study and series ID.
2. **Image Processing**: The system converts MRI images into 3D point clouds and voxel grids for model input.
3. **Modeling**: The CNN model is trained to classify various spine conditions across different spinal levels.
4. **Prediction**: The model generates condition-specific predictions for each spinal level, with results presented in a structured format.
5. **Visualization**: The processed voxel grid data is visualized to provide insights into the MRI scans and model predictions.

## Model
The model architecture is based on multi-head CNNs, utilizing MaxViT and EfficientNet backbones for feature extraction. Each head of the model outputs predictions for different spine conditions, with logistic cumulative link functions applied for better accuracy.

The system is capable of classifying multiple conditions in parallel across various anatomical spinal levels, offering a comprehensive diagnosis.

## Performance and Efficiency
The use of modern deep learning techniques and GPU acceleration ensures efficient and scalable predictions, suitable for large-scale medical datasets.
