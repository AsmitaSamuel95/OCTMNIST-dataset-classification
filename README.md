# OCTMNIST Medical Image Processing & Classification 

## Processed and managed a biomedical image dataset (OCTMNIST), integrating retinal images with numeric labels and applying advanced data preprocessing, analysis, visualization, and model evaluation techniques in Python.

# OCTMNIST Image Classification

## Project Overview
This project develops and trains convolutional neural networks (CNNs) to classify optical coherence tomography (OCT) images using the OCTMNIST dataset from MedMNIST. It includes data augmentation, preprocessing, exploratory analysis, model training with weighted loss, early stopping, and performance evaluation.

## Dataset
- **Source:** [MedMNIST OCTMNIST dataset](https://medmnist.com/)  
- **Description:** Grayscale OCT images, 28x28 pixels each, labeled into 4 disease-related classes.  
- **Splits:** Training, Validation, and Test sets provided.  
- **Class Distribution:** Imbalanced across classes, analyzed and addressed during training.

## Data Preprocessing
- Data augmentation used on training data (random rotations, horizontal flips).  
- Conversion to tensor format for PyTorch compatibility.  
- Checked and visualized pixel intensity distributions and missing data (none significant).  
- Class imbalance handled via weighted cross entropy loss.  
- Split into train, validation, and test using MedMNIST splits.

## Exploratory Data Analysis
- Sample images displayed with class labels.  
- Histogram of class distribution to show imbalance.  
- Heatmap visualization of average pixel intensity and missing pixel counts.

## Model Architectures
- **Baseline CNN:** Four convolutional layers with BatchNorm, ReLU activations, MaxPooling, and global average pooling followed by a fully connected output layer.  
- **Improved CNN:** Adds dropout layers for regularization and an additional convolutional layer.  

## Training Details
- Loss function: CrossEntropyLoss (standard and weighted).  
- Optimizer: Adam with learning rate 0.001.  
- Scheduler: CosineAnnealingLR for learning rate adjustment.  
- Training incorporates gradient clipping (max norm 5.0) and early stopping (patience 5-10 epochs).  
- Batch size: 32, Number of epochs: up to 50.

## Evaluation and Results
- Metrics: Accuracy, precision, recall, F1-score (weighted), confusion matrix, ROC AUC per class.  
- Both baseline and improved models demonstrate good performance, with the improved model achieving better generalization and higher accuracy due to dropout and weighted loss.  
- Training, validation, and test accuracy and loss curves are provided for detailed model behavior insight.  
- Confusion matrix and ROC curves visualize classification quality across classes.

## How to Run
You can run the Jupyter Notebook file directly using Google Colab without installing anything locally:

1. Open Google Colab in your web browser.

2. Click File > Upload notebook.

3. Choose the .ipynb file from your computer and upload it.

4. Run the code cells by clicking the Run button, next to each cell or press Shift + Enter.

5. To run all cells sequentially, go to Runtime > Run all.

6. The notebook will be automatically saved in your Google Drive under the Colab Notebooks folder.


