# Dataset Guide

This folder contains the deep learning datasets used in this project. Due to storage limits, the actual data files are hosted on Google Drive.

##  Dataset Access (Google Drive)
- [Link]('https://drive.google.com/drive/folders/195bFDcqPE6EA0yreicHfaE_PjMiBgSZO?usp=drive_link')

## Dataset Overview
The dataset is derived from the **Kaggle FaceForensics++ (FF++) dataset (c23 HQ)** and has been preprocessed through the following pipeline:
1. **Frame Extraction**: Extracted frames at every 20th frame using `ffmpeg`.
2. **Face Detection & Cropping**: Detected and cropped faces from the extracted frames using `MTCNN`.
3. **Data Generation**: Processed 100 video sequences per deepfake technique across four distinct variations.

## Directory Structure
Once you download and extract the dataset, please place the folders under the `Data/` directory as shown below:

```text
Data/
├── README.md (This file)
├── original/               # Source cropped faces before diffusion processing
├── 02_diffusion_s10/       # Diffusion-processed faces with noise intensity step 10
├── 02_diffusion_s50/       # Diffusion-processed faces with noise intensity step 50
└── 02_diffusion_s75/       # Diffusion-processed faces with noise intensity step 75
```

