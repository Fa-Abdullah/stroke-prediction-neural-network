# Stroke Prediction using Neural Networks

A deep learning project that predicts the likelihood of stroke using a **Binary Classification Neural Network** built with **TensorFlow/Keras**. The model is trained on patient health records and achieves approximately **93% test accuracy**.

---

## Features

* Binary classification using a Deep Neural Network
* TensorFlow/Keras implementation
* Data preprocessing and normalization
* Dropout regularization to reduce overfitting
* Performance evaluation on unseen test data
* Easy to run in Jupyter Notebook or Google Colab

---

## Dataset

The model is trained on a stroke prediction dataset containing anonymized patient health information.

### Input Features

| Feature               | Description    |
| --------------------- | -------------- |
| Gender                | Encoded gender |
| Age                   | Normalized age |
| Hypertension          | 0 / 1          |
| Heart Disease         | 0 / 1          |
| Ever Married          | Encoded        |
| Work Type             | Encoded        |
| Residence Type        | Urban / Rural  |
| Average Glucose Level | Normalized     |
| BMI                   | Normalized     |
| Smoking Status        | Encoded        |

**Target Variable**

* **Stroke**

  * `0` → No Stroke
  * `1` → Stroke

---

## Model Architecture

```text
Input (10 Features)
        │
Dense (128, ReLU)
        │
Dense (64, ReLU)
        │
Dropout (0.5)
        │
Dense (32, ReLU)
        │
Dense (16, ReLU)
        │
Dense (8, ReLU)
        │
Dense (1, Sigmoid)
```

---

## Training Configuration

| Parameter        | Value               |
| ---------------- | ------------------- |
| Optimizer        | Adam                |
| Loss Function    | Binary Crossentropy |
| Epochs           | 150                 |
| Batch Size       | 16                  |
| Validation Split | 20%                 |
| Train/Test Split | 80/20               |

---

## Performance

| Metric        | Value      |
| ------------- | ---------- |
| Test Accuracy | **≈93%**   |
| Test Loss     | **0.2379** |

The model demonstrates stable convergence during training while maintaining good generalization on unseen data.

---

## Technologies Used

* Python
* TensorFlow / Keras
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

