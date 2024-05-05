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

## Datasets
- HDR+ Burst Photography Dataset: Hasinoff, S. W., Sharlet, D., Geiss, R., Adams, A., Barron, J. T., Kainz, F.,
Chen, J., & Levoy, M. (2016). Burst photography for high dynamic range and low-light imaging on mobile
cameras. ACM Transactions on Graphics (Proc. SIGGRAPH Asia 2016), 35(6).
http://hdrplusdata.org/dataset.html
- ExDark Dataset Loh, Y. P., Chan, C. S., Por, L. Y., & Ling, C. Y. (2018). Getting to Know Low-light Images with
The Exclusively Dark Dataset. arXiv preprint arXiv:1805.11227.
https://paperswithcode.com/dataset/exdark

## Usage
To use this project effectively, follow these detailed steps:

1. **Obtain the Datasets**:
   - Download the HDR+ and ExDark datasets from their respective sources.
   - Due to licensing, the full datasets cannot be directly included in this repository.

2. **Setup Google Drive**:
   - Upload the downloaded datasets to your Google Drive in a specific folder, e.g., `datasets/your-project-name`.

3. **Google Colab Setup**:
   - Download the provided Jupyter notebook from the `notebooks/` directory of this repository.
   - Upload the notebook to your Google Drive, preferably in the same project folder where the datasets are stored.

4. **Open with Google Colab**:
   - Navigate to Google Drive and open the uploaded notebook with Google Colab.
   - Ensure that the notebook is configured to use the correct path to the datasets in your Google Drive.

5. **Consider Upgrading to Google Colab Pro+**:
   - Since this project requires significant computational power to process and deblur the images effectively, consider subscribing to Google Colab Pro+. This will provide you with enhanced access to faster GPUs and longer runtime, which are crucial for training deep learning models efficiently.

6. **Run the Notebook**:
   - Follow the instructions within the notebook to train the models and perform image deblurring. Make sure all paths in the code are correctly set to where your data is stored in Google Drive.

## Contributing
Interested in contributing? Great! Please open an issue to discuss proposed changes or submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Citation
If you use this project or the datasets in your research, please cite it as follows:

```bibtex
@misc{Enhancing Motion Blurred Images in normal and low light conditions,
  author = {Abhinav Mishra},
  title = {Deblurring Motion Blurred Images in Normal and Low Light: Deep Learning-based Deblurring Using Dual Datasets},
  year = {2024},
  publisher = {GitHub},
  journal = {https://github.com/amishra15/enhancing-motion-blurred-images-in-normal-and-low-light-condition-for-mobile-photography},
  howpublished = {\\https://github.com/amishra15/enhancing-motion-blurred-images-in-normal-and-low-light-condition-for-mobile-photography}}
}
