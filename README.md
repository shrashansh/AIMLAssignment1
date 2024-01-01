# Wav2Lip with Colab Notebook

## Overview
This Colab notebook provides a step-by-step guide for running the Wav2Lip inference on Google Colab. Wav2Lip is a lip-syncing tool that generates realistic lip movements based on audio input.

### 3. Setup Google Drive
- In your Google Drive:
  1. Create a folder called `input` in `MyDrive`.
  2. Upload your input video (`video.mp4`) and input audio (`audio.wav`) to this folder.
  3. Download the pretrained model weights from [https://github.com/Rudrabha/Wav2Lip#getting-the-weights](https://github.com/Rudrabha/Wav2Lip#getting-the-weights).
  4. Create a folder called `pretrained` in `MyDrive` and upload the pretrained model there.


## How to Run

### 1. Setup Environment
- Select T4 GPU for running the code.
- 
### 2. Clone Wav2Lip Repository
- from [https://github.com/Rudrabha/Wav2Lip.git](https://github.com/Rudrabha/Wav2Lip.git).

### 3. Check Google Drive Contents
- List the contents of the specified Google Drive folder to ensure the required input files (`audio.wav` and `video.mp4`) are present.

### 4. Copy Pre-trained Model
- Copy the pre-trained Wav2Lip-GAN (or any other pretrained model) model (`wav2lip_gan.pth`) from Google Drive to the Wav2Lip checkpoints folder.

### 5. Install Dependencies
- Install the necessary dependencies listed in `requirements.txt`. Note: There might be an issue with OpenCV version compatibility, and an attempt to install a specific version of OpenCV might fail.

### 6. Fix OpenCV Version Issue
- install librosa==0.8.0
  
### 7. Download Face Detection Model
- Download the face detection model (`s3fd.pth`) from [https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) and save it in the appropriate directory.

### 8. Copy Input Files to Sample Data
- Copy input video and audio files from Google Drive to the Colab sample data folder.

### 9. Run Wav2Lip Inference
- Run the Wav2Lip inference script (`inference.py`) with the specified checkpoint path, input video, and audio files. The inference is initially attempted without resizing, and later, a resized version is attempted with a specified resize factor.

### 10. View Results
- The final step involves viewing the generated lip-synced video results.

