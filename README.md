# AI-Generated vs. Real Image Classification Using CNN

A deep learning project that classifies images as **AI-generated** or **real** using a custom Convolutional Neural Network (CNN) built with TensorFlow and Keras.

## Features

- Custom CNN trained from scratch.
- Image preprocessing and normalization.
- Stratified train-validation-test split.
- Class weighting to handle dataset imbalance.
- Batch normalization, LeakyReLU, and dropout.
- Early stopping to help prevent overfitting.
- Model evaluation using accuracy, loss, and macro F1-score.
- Saved model for future integration with a Flask API.

## Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow, Keras
- **Data Processing:** NumPy, Pandas
- **Evaluation:** scikit-learn

## Dataset

The project uses the [AI-vs-Real dataset](https://huggingface.co/datasets/Parveshiiii/AI-vs-Real), containing **13,999 images**.

| Class | Label | Images |
|---|---|---:|
| AI-generated | 0 | 3,333 |
| Real | 1 | 10,666 |
| **Total** | | **13,999** |

### Dataset Split

- Training: 9,799 images (70%)
- Validation: 2,100 images (15%)
- Testing: 2,100 images (15%)

Class weights were used during training to address dataset imbalance.


### Model Configuration

- **Input size:** 128 × 128 × 3
- **Total parameters:** 110,561
- **Optimizer:** Adam
- **Loss function:** Binary cross-entropy
- **Maximum epochs:** 20
- **Early stopping:** Patience of 5 epochs

## Results

Evaluation on the held-out test set:

| Metric | Score |
|---|---:|
| Test Accuracy | **94.00%** |
| Macro F1-score | **0.9163** |
| Test Loss | **0.1619** |
