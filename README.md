# SceneFake Audio Detection using LFCC, CNN, DNN and Federated Learning

This repository contains the implementation accompanying our paper on SceneFake audio detection using LFCC-based features with CNN, DNN and Federated Learning.

## Repository Structure

notebooks/
lfcc-cnn.ipynb
lfcc-dnn.ipynb
lfcc-cnn-federated-learning.ipynb
lfcc-dnn-federated-learning.ipynb

## Dataset

SceneFake Dataset
https://github.com/RedamancyAY/SceneFake

## Requirements

Python 3.11

Install dependencies:

pip install -r requirements.txt

## Feature Extraction

Librosa does not currently provide a native LFCC implementation. Therefore, the feature extraction pipeline follows the standard cepstral pipeline (STFT → Filter Bank → Log → DCT), using Librosa as the implementation framework. The primary conceptual difference between MFCC and LFCC is the use of linearly spaced filter banks instead of Mel-scaled filter banks.

## Notes

SMOTE is applied only to the training data to address class imbalance.
Evaluation is performed on the original unseen evaluation set.
