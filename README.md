# CEG3004 Environmental Sound Classification

## Project Overview
This project implements a robust audio classification pipeline for Environmental Sound Classification.

The goal is to classify environmental sounds into 50 classes while maintaining performance under:
- clean audio
- noisy audio
- band-limited audio

The system uses digital signal processing (DSP) feature extraction and machine learning classification.

## Aim
To design a robust audio classification pipeline for Environmental Sound Classification that performs well under clean and distorted conditions.

## Objectives
- Train on labeled environmental sound data
- Extract meaningful DSP features
- Use a machine learning classifier to classify into 50 sound classes
- Demonstrate robustness to noise and bandwidth distortions

## Dataset
The dataset is derived from ESC-50 and contains:
- 2,000 audio clips
- 50 sound classes
- 40 clips per class
- 5 seconds per clip
- mono waveform audio

The submission data contains three versions of each clip:
- clean
- noisy
- band-limited

These are used to evaluate robustness.

## Repository Structure
```text
CEG3004-Environmental-Sound-Classification/
│
├── README.md
├── requirements.txt
├── .gitignore
├── Pr_20_model.joblib
├── Pr_20_predictions.csv
├── ceg3004_project.py
├── results/
│   └── experiment_notes.md
└── submission/
    └── repository_link.txt
```

## Methodology

### 1. Audio Preprocessing
The preprocessing pipeline includes:
- DC offset removal
- fixed length adjustment to 5 seconds
- pre-emphasis filtering
- RMS normalization
- mild clipping

### 2. Feature Extraction
The extracted DSP features include:
- MFCC statistics
- delta MFCC
- delta-delta MFCC
- log-mel spectrogram statistics
- chroma features
- spectral flux
- spectral centroid
- spectral bandwidth
- spectral rolloff
- spectral flatness
- zero-crossing rate
- RMS energy
- spectral contrast

### 3. Model Training
The project evaluates several machine learning models:
- LinearSVC
- Logistic Regression
- RBF SVM
- Voting Classifier ensembles

Feature scaling and feature selection are applied using scikit-learn pipelines.

The final model is selected based on validation Macro-F1 score.

## Reproducible Instructions

### Step 1: Clone the repository
```bash
git clone https://github.com/<your-username>/CEG3004-Environmental-Sound-Classification.git
cd CEG3004-Environmental-Sound-Classification
```

### Step 2: Install dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Run the project
Run:
```bash
python ceg3004_project.py
```

Or open the script in Google Colab and run the cells sequentially.

### Step 4: Set the group ID
At the top of the file, set:
```python
GROUP_ID = "Pr_20"
```

### Step 5: Download and extract dataset
The code automatically downloads the dataset using `gdown` and extracts it.

### Step 6: Train the model
Run the script to:
- load training labels
- preprocess audio
- extract features
- split into train and validation sets
- train and evaluate the model

### Step 7: Generate submission files
The code automatically generates:
- `Pr_20_model.joblib`
- `Pr_20_predictions.csv`

## Final Submission Files
The final files for Dropbox submission are:
- `Pr_20_model.joblib`
- `Pr_20_predictions.csv`
- `repository_link.txt`

## Notes
- Submission clip IDs were not modified
- Only the marked TODO sections were improved from the baseline
- The output filenames follow the required group ID naming

## Author
Group ID: Pr_20  
Module: CEG3004
