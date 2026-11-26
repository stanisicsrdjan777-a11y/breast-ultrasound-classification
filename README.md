# Breast Ultrasound Classification

AI model that classifies breast ultrasound images into **benign**, **malignant**, or **normal** using transfer learning.

## Approach

- **Base model:** EfficientNetB0 (ImageNet weights)
- **Loss:** Focal Loss (focuses training on harder examples)
- **Training:** Two-phase — frozen base + fine-tuning of the last 80 layers
- **Handling imbalance:** Class weights
- **Demo:** Gradio interface for single-image prediction

## Dataset

[Breast Ultrasound Images Dataset (BUSI)](https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset)  
Classes: benign, malignant, normal. Mask images were removed; only original ultrasound images were used.


## How to run

1. Open the notebook in Google Colab.
2. Add your Kaggle credentials to Colab Secrets:
   - `KAGGLE_USERNAME`
   - `KAGGLE_API_TOKEN`
3. Run all cells. The notebook downloads the dataset, trains the model, evaluates it, and launches a Gradio demo.

## Tech stack

- Python
- TensorFlow / Keras
- EfficientNetB0
- scikit-learn
- Gradio
- Google Colab

## Notes

This is a personal learning and portfolio project. It is not a medical device and should not be used for diagnosis.
