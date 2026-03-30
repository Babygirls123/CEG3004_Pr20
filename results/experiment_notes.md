# Experiment Notes

## Preprocessing Used
The final preprocessing pipeline includes:
- DC offset removal
- fixed-length padding or truncation to 5 seconds
- pre-emphasis
- RMS normalization
- mild clipping

## Features Used
The final feature set includes:
- MFCC mean and standard deviation statistics
- delta and delta-delta MFCC features
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

## Models Tested
The following models were tested:
- LinearSVC
- Logistic Regression
- RBF SVM
- Voting Classifier

## Feature Selection
The following feature selection settings were explored:
- all features
- top 384 features
- top 512 features

## Evaluation Metric
Model selection was based on validation Macro-F1 score.

## Final Approach
The final saved model is the best-performing pipeline found during the validation sweep.
