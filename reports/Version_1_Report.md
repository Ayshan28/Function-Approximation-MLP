# Version 1 Report

## Function Approximation Using a Multilayer Perceptron (MLP)

**Author:** Ayshan Gambarli

**Date:** July 2026

**Version:** 1

---

# 1. Objective

The objective of this project is to approximate a nonlinear mathematical function using a Multilayer Perceptron (MLP) implemented in Python with TensorFlow/Keras.

The target function is

\[
f(x_1,x_2)=5x_1^2+7x_1x_2-x_2^2-x_1+x_2+5
\]

---

# 2. Dataset Generation

A synthetic dataset containing **500 samples** was generated.

For every sample:

- random values of **x1** and **x2** were generated from the interval **[-1,1]**
- the exact function value **f(x)** was calculated
- a random variable **delta** was generated
- noisy target values were computed using

\[
y=f(x)(1+\alpha\delta)
\]

where

- α = 0
- α = 0.01
- α = 0.03
- α = 0.05

Three CSV files were created:

- dataset.csv
- train.csv
- test.csv

---

# 3. Train/Test Split

The dataset was divided into

| Dataset | Samples |
|---------|---------:|
| Train | 400 |
| Test | 100 |

---

# 4. Neural Network Architecture

The neural network was implemented using TensorFlow/Keras.

Architecture:

- Input neurons: **2**
- Hidden neurons: **5**
- Output neurons: **1**

Activation function:

- Sigmoid

Optimizer:

- Adam

Loss Function:

- Mean Squared Error (MSE)

Metric:

- Mean Absolute Error (MAE)

Training epochs:

- 2000

---

# 5. Results

## Training Performance

| Metric | Value |
|---------|---------:|
| MSE | 0.1741 |
| MAE | 0.2917 |

## Testing Performance

| Metric | Value |
|---------|---------:|
| MSE | 0.4037 |
| MAE | 0.4052 |

The model successfully learned the relationship between the input variables and the target function. The prediction values are close to the real values.

---

# 6. Visual Results

The following plots were generated during training:

- Training Loss
- Training MAE
- Prediction vs Real values

The loss and MAE decrease steadily during training, indicating successful convergence of the model.

The prediction plot shows that the predicted values closely follow the real function values.

---

# 7. Current Progress

Completed:

- Dataset generation
- Noise generation using different alpha values
- Train/Test split
- MLP architecture
- Weight initialization
- Bias initialization
- TensorFlow/Keras implementation
- Model training
- Model evaluation
- Visualization of results

---

# 8. Future Work

The following improvements are planned for the next versions:

- Mean Absolute Percentage Error (MAPE)
- Numerical analysis of backpropagation
- Different hidden layer sizes
- Different activation functions
- Hyperparameter tuning
- Comparison of different MLP architectures

---

# Repository Structure

```
Function-Approximation-MLP
│
├── Function_Approximation_MLP.ipynb
├── dataset.csv
├── train.csv
├── test.csv
├── reports/
│   └── Version_1_Report.md
└── figures/
```

---

# Notes

This is the first version of the project.

Future reports (Version 2, Version 3, ...) will document new experiments and improvements made during the internship.
