# Dual-Dataset Deblurring Project

## Overview
This project leverages deep learning to deblur images under both normal and low-light conditions using a dual-dataset approach. Our goal is to enhance mobile photography by improving image clarity impacted by various blurs, focusing on Gaussian blur due to computational constraints.

## Datasets

### HDR+ Dataset
- **Description**: High-quality images aimed at enhancing mobile photography under diverse lighting conditions, stored in raw DNG format with metadata.
- **License**: Creative Commons (CC-BY-SA)
- **Samples Used**: 200

### ExDark Dataset
- **Description**: Images captured in very low-light conditions, designed to enhance low-light image processing for object detection and recognition.
- **License**: Available for academic research.
- **Samples Used**: 300

## Methodology

### Models Employed
- **On HDR+ Dataset (200 Samples)**:
  - Convolutional Neural Networks (CNN)
  - AutoEncoders
  - U-Net
- **On ExDark Dataset (300 Samples)**:
  - Generative Adversarial Networks (GANs)
  - CNN
  - AutoEncoders
  - U-Net
- **On Combined Dataset (500 samples)**:
  - Advanced CNNs for optimal deblurring.

### Workflow
1. **Data Loading**: Import and prepare HDR+ and ExDark datasets.
2. **Exploratory Data Analysis (EDA)**: Analyze the datasets to understand the effects of Gaussian blur.
3. **Model Training**:
   - Independently on HDR+ and ExDark datasets.
   - On the merged dataset for enhanced results.
4. **Deblurring**: Evaluate the deblurring performance using SSIM, PSNR values, Validation/Loss Graph and Image Clarity.

## Results
The implementation of complex CNNs on the merged dataset significantly enhanced image clarity, demonstrating superior deblurring performance. Below is an example of the deblurring results:

![Deblurred Image Example](https://i.imgur.com/CVMoQig.png)

- Training History

![Training History](https://i.imgur.com/nBBNxNu.png)

Average SSIM: 0.4122613634069845
Average PSNR: 13.250429498226481

## Technologies Used
- Python
- TensorFlow/Keras
- OpenCV
- Jupyter Notebook

## Repository Structure
