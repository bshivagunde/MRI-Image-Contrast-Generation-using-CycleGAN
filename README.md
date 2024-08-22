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

 - numpy==1.19.2
 - tensorflow==2.4.1
 - matplotlib==3.3.2
 - skimage==0.17.2
 
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
 
## Model Architecture
### Generator
The Generator is based on a modified U-Net architecture, which performs the following steps:

 - Downsampling: Extracts features from the input image.
 - Upsampling: Reconstructs the image with the desired contrast level.
 
### Discriminator
The Discriminator is a traditional Convolutional Neural Network (CNN) used to classify real and generated images. It uses downsampling layers for feature extraction.

### Loss Functions
 - Binary Cross-Entropy: Used for classification in the Discriminator.
 - Cycle Loss: L1 loss between the original and cycled image.
 - Identity Loss: L1 loss between the input and output when no translation is needed.
 
### Optimizer
 - Adam Optimizer: Used to update model weights efficiently.
 
## Model Training
The model is trained for 300 epochs. The training flow includes:

 1. Generating fake images and cycled images.
 2. Calculating Discriminator and Generator losses.
 3. Updating weights using the Adam Optimizer.
 4. Saving model checkpoints for future use.
 
## Results
During training, the Generators improve their ability to produce realistic MRI images with each epoch. The project includes a GIF to visualize the progression of generated images over time.
Below is a GIF illustrating the progression of generated images over time:

![Result](https://github.com/bshivagunde/MRI-Image-Contrast-Generation-using-CycleGAN/blob/main/MRI_cyclegan.gif)

## Conclusion
This project successfully demonstrates how deep learning can be used to enhance medical imaging by generating additional MRI image variations. This approach has the potential to reduce costs and improve diagnostic accuracy in clinical settings.

## Contact
Created by [@bshivagunde](https://github.com/bshivagunde) - Feel free to contact me!
