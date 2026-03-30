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
├── ceg3004_project.py
├── CEG3004_Project_Colab.ipynb
├── results/
│   └── experiment_notes.md
└── submission/
    └── repository_link.txt
