# MRI-Image-Contrast-Generation-using-CycleGAN
This project uses a CycleGAN model with a modified U-Net architecture to generate artificial MRI images of different contrast levels from existing MRI scans. The objective is to improve diagnostic accuracy by providing radiologists with additional image variations without the need for costly and time-consuming imaging procedures.

## Introduction
Misdiagnosis in the medical field is a significant concern, particularly when it comes to interpreting MRI scans. Radiologists often need different contrast variations of MRI images to make accurate diagnoses. However, obtaining these variations can be both difficult and expensive.

In this project, we address this challenge by using deep learning techniques, specifically CycleGAN, to generate MRI images with different contrast levels (e.g., T1 to T2 and vice versa). This approach helps enhance the accuracy of diagnoses by providing additional, cost-effective image variations.

## Problem Statement

The task is to build a Generative Adversarial Model (CycleGAN with a modified U-Net) that can generate artificial MRI images with different contrast levels from existing MRI scans. The generated images aim to support radiologists in making more accurate and comprehensive diagnoses.

## Project Pipeline
 - Data Understanding: Load and visualize the MRI dataset.
 - Data Preprocessing: Resize, reshape, and prepare the images for training.
 - Model Building and Training: Develop and train Generators and Discriminators using a modified U-Net architecture.
 - Results Visualization: Generate and visualize the output, including the creation of a GIF to illustrate model performance over time.


## Dependencies
The project requires the following Python libraries:

 -- numpy==1.19.2
 -- tensorflow==2.4.1
 -- matplotlib==3.3.2
 -- skimage==0.17.2
 
## Data
The dataset comprises MRI images in T1 and T2 contrast levels:

 - T1 Images: 43 images
 - T2 Images: 46 images
 - Image Size: 217x181 pixels
 - The images should be resized and reshaped to 128x128 pixels for model input. 
 
## Data Preprocessing
 - Resizing: Resize images to 128x128 pixels.
 - Reshaping: Reshape images to (128, 128, 1) and normalize pixel values.
 - Batching and Shuffling: Batch size is set to 1024 for efficient training. 
 
 