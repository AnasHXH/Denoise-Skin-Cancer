# 🩺 Denoise Skin Cancer using Diffusion Model

This repository presents a diffusion-based denoising framework designed to remove noise from dermoscopic skin images. The model is adapted from the DM-AHR framework and extended for noise reduction tasks to enhance image quality prior to lesion analysis. The project is tested on two benchmark skin lesion datasets: **PH2** and **HAM10000**.

---

## 🔬 Introduction

Dermoscopic images often suffer from noise caused by acquisition conditions, sensor artifacts, or preprocessing errors, which negatively impact diagnostic performance. Traditional filtering methods reduce noise but also degrade lesion structures and clinical features. To address this challenge, we propose a **diffusion-based image denoising approach** that:

- Removes noise while **preserving lesion edges and textures**
- Produces high-quality clean images
- Enhances diagnostic reliability for melanoma detection
- Supports multiple medical datasets

This project demonstrates how diffusion models can effectively denoise medical images while retaining critical diagnostic information.

---

# How to Test
## Prerequisites:
Ensure Python is installed on your system.
Have the required libraries and dependencies installed as per the project requirements.

## Step 1: Access the Dataset

we used [HAM10000](https://www.kaggle.com/datasets/eliocordeiropereira/skin-cancer-the-ham10000-dataset). and PH2 dataset [HAM10000](https://www.kaggle.com/datasets/athina123/ph2dataset).

## Step 2: Extract the Dataset
Extract the contents of akiec_16_128.zip. Ensure all files are successfully extracted and available for further processing.

## Step 3: Configure Paths
Navigate to the config directory and open akiec.json. Here, update all paths to correspond to the locations where you extracted the dataset files. Confirm that all paths are accurate and accessible.

Step 4: Execute the Script
Once the dataset is extracted and paths are configured, you are ready to execute the testing script. Use the following command to initiate the process:
```bash
python Denoise_skin_cancer/data/prepare_data.py \
  --path Input_path_images \
    --out Output_path_images --size 16,128
```
```bash
python Denoise_skin_cancer\sr.py\
-p train -c Denoise_skin_cancer\config\val.json
```
# Downloading Model Weights
To ensure the accuracy and efficiency of your tests, it is crucial to use the appropriate model [weights](https://drive.google.com/drive/folders/1OINKjCZQNzU1OxFQ64i3GlYkgbe_zrIh?usp=sharing).
---


## 🔗 Results

The denoising results for both PH2 and HAM10000 datasets, including visual comparisons and evaluation metrics (PSNR, SSIM, MS-SSIM), can be found at the link below:

📁 **Google Drive Results Folder:** [ADD YOUR DRIVE LINK HERE]

---

## 🖼️ Sample Result

Below is an example showing the effect of diffusion-based denoising on a dermoscopic image:

| Original Image | Noisy Image | Denoised Output |
|----------------|-------------|------------------|
| <img src="ADD_LINK_TO_ORIGINAL_IMAGE" width="250"> | <img src="ADD_LINK_TO_NOISY_IMAGE" width="250"> | <img src="ADD_LINK_TO_DENOISED_IMAGE" width="250"> |

---


## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License. You are free to use, share, and adapt this material for non-commercial purposes, as long as you provide attribution to the original author(s) and the source.
## Acknowledgement

The codes are based on [SR3](https://github.com/Janspiry/Image-Super-Resolution-via-Iterative-Refinement).

## Contribute
For any questions or suggestions, please open an issue on the [GitHub issue tracker](https://github.com/AnasHXH/DM-AHR/issues).

