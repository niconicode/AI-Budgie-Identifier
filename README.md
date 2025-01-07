# Image Classifier with Finetuned Models

This project implements an image classifier using finetuned models from HuggingFace. Models used include ResNet-18, ResNet-152, and MobileNet-V2

## Project Overview

The project uses models pre-trained on ImageNet and fine-tunes them for a 5-class image classification task. The main steps involved are:

1. **Data Loading:** Loads preprocessed images from Google Drive using HDF5 files.
2. **Model Loading:** Loads the respective model, adjusts the final layer for 5 output classes, and initializes weights using Xavier uniform initialization.
3. **Training and Evaluation:** Trains and evaluates the model with different hyperparameters (epochs, learning rates, and batch sizes).

## Dataset

The dataset contains images of different colored budgies and is split into test, training, and validation sets.

## Results

ResNet-18:
The model achieves an accuracy of ~90-95% with the following hyperparameters:
- Epochs: 10-15
- Learning rate: 5e-5
- Batch size: 64
- Optimizer: Adam

ResNet-152:
The model achieves an accuracy of ~95% with the following hyperparameters:
- Epochs: 15
- Learning rate: 1e-3
- Batch size: 50
- Accumulation steps: 2
- Optimizer: Adam

MobileNet-V2:
The model achieves an accuracy of ~96-98% with the following hyperparameters:
- Epochs: 18
- Learning rate: 5e-5
- Weight Decay: .01
- Batch size: 64
- Optimizer: AdamW


## Usage

1. **Mount Google Drive:** Mount your Google Drive to access the data files.
2. **Install Libraries:** Install the necessary libraries using `pip`:
