# Text-Detection-System

## Overview
The Text-Detection-System is designed to detect synthetic text in DICOM images. This project aims to create a robust text detection model tailored for medical images, specifically DICOM format.

## Project Goal
Develop a synthetic text detection system using Python that can accurately identify and locate text within DICOM images.

## Dataset
The dataset used for this project is sourced from Kaggle's NIH Chest X-rays collection.

## Implementation Steps

1. **Dataset Acquisition**:
   - Download the DICOM Image Dataset from Kaggle's NIH Chest X-rays.

2. **Random Text Generation**:
   - Process the DICOM images and overlay them with synthetic text. The text will have the following random attributes:
     - **Language**: English, Portuguese, Chinese (Using 10k+ most common word list for each language).
     - **Font**: Over 50 font options, such as Arial.
     - **Font Size**
     - **Text Length**
     - **Fill Color**
     - **Stroke Color**
     - **Stroke Width**
     - **Rotation Degree**
     - **Position**: Random (X, Y) coordinates on the image.

3. **Bounding Box Generation**:
   - Reduce the dimension of the image of the generated text using Numpy.
   - Analyze the x-axis and y-axis to determine the first and last indices/pixels of the generated text.
   - Save these bounding boxes as the correct labels for training.

4. **Dataset Splitting**:
   - Divide the dataset into training, validation, and testing sets.

5. **Model Training**:
   - Train the YOLOv6-S model with the "Text Detection" Jupyter Notebook using the generated training set and validation set.

6. **Deployment**:
   - Deploy the customized model.
   - Test the model's performance using the testing set.

## Conclusion
This project aims to provide a specialized solution for detecting synthetic text in DICOM images. By using a combination of random text generation and the YOLOv6-S model, we hope to achieve high accuracy in text detection for medical images.
