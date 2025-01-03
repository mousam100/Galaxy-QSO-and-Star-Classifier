# Stellar Classification Project

## Overview
This project aims to classify astronomical objects into three categories: **Stars**, **Galaxies**, and **Quasars (QSOs)** using data from the **Sloan Digital Sky Survey (SDSS)**. The dataset contains 100,000 observations, each described by 17 features and a class label. Machine Learning (ML) and Deep Learning (DL) models are implemented to achieve accurate classification.

## Dataset
**Stellar Classification Dataset - SDSS17**
- **Source:** [Kaggle](https://www.kaggle.com/fedesoriano/stellar-classification-dataset-sdss17)
- **Features:** 17 features including magnitudes and colors, with a target class (Star, Galaxy, QSO).
- **Size:** 100,000 observations.

### Citation
fedesoriano. (January 2022). Stellar Classification Dataset - SDSS17. Retrieved [Date Retrieved] from [Kaggle](https://www.kaggle.com/fedesoriano/stellar-classification-dataset-sdss17).

### Acknowledgements
The data released by the SDSS is under public domain. It is taken from the current data release RD17.
More information about the license: [SDSS License Information](http://www.sdss.org/science/image-gallery/)

## Methodology

### Preprocessing
1. **Feature Engineering:** Added derived features like "G-I" (difference between `g` and `i` magnitudes) and "Z-G" (difference between `z` and `g` magnitudes).
2. **Feature Scaling:** Standardized all feature values using `StandardScaler`.
3. **Class Balancing:** Used class weights to address imbalanced data.

### Models
1. **Multi-Layer Perceptron (MLP):** Fully connected neural network with dropout layers for regularization.
2. **Convolutional Neural Network (CNN):** 1D CNN with convolution and max-pooling layers, designed for sequential data.
3. **Long Short-Term Memory (LSTM):** LSTM network to capture sequential dependencies in features.

### Training and Evaluation
- **Train-Test Split:** 80% training, 20% testing.
- **Validation Split:** 5% of the training data used for validation.
- **Metrics:** Accuracy, confusion matrix.
- **Optimization:** Categorical cross-entropy loss with the Adam optimizer.

## Results
Each model’s performance was evaluated, and the best-performing model was selected based on accuracy. Confusion matrices were used to analyze the classification results further.

## How to Use
1. Clone the repository.
2. Install required Python libraries: `scikit-learn`, `tensorflow`, `numpy`, `matplotlib`.
3. Load the dataset and follow the preprocessing steps in the code.
4. Train models and evaluate results.
5. Use the best-performing model for predictions on new data.

## License
This project uses publicly available SDSS data, which is under the public domain. For more details, refer to the [SDSS License Information](http://www.sdss.org/science/image-gallery/).


