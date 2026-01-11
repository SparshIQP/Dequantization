# Dequantization: HQNN & Fourier Dequantization for WiFi Localization

This repository implements a **Hybrid Quantum Neural Network (HQNN)** for indoor WiFi localization and a **Fourier Surrogate Dequantization** technique to approximate the quantum model for efficient classical inference.

The goal is to predict indoor **(x, y)** coordinates using WiFi RSSI measurements from three access points, while demonstrating how a trained quantum model can be replaced by a fast classical surrogate without significant loss in accuracy.

---

## 🚀 Project Overview

- **Input:** WiFi RSSI signals from three access points  
- **Output:** 2D indoor position \((x, y)\)
- **Key Idea:**  
  1. Train a hybrid quantum–classical neural network  
  2. Replace the quantum layer with a Fourier-based classical surrogate  
  3. Perform inference without requiring a quantum simulator  

This approach significantly reduces inference time while maintaining near-identical localization performance.

---

## ✨ Key Features

- **Hybrid Architecture**
  - 3-qubit Quantum Neural Network (QNN) built with Qiskit
  - `ZZFeatureMap` for data encoding
  - `RealAmplitudes` variational ansatz
  - Classical regression layers implemented in PyTorch

- **Fourier Dequantization**
  - Approximates the quantum model using a Fourier surrogate
  - Enables fully classical, high-speed inference

- **Pruning Analysis**
  - Studies how reducing Fourier coefficients impacts localization accuracy
  - Visualizes the trade-off between model complexity and RMSE

- **End-to-End Pipeline**
  - Data normalization
  - Hybrid quantum–classical training
  - Fourier surrogate fitting
  - Performance comparison and visualization

---

## 🛠 Tech Stack

### Quantum
- Qiskit
- Qiskit Machine Learning

### Classical
- PyTorch
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## 📂 File Structure

```text
.
├── Dequantization.ipynb
├──RSSI-Dataset-for-Indoor-Localization-Finerprinting.zip
└── README.md
