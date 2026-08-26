# 🧠 Handwritten Digit Classification using CNN

A Deep Learning mini project that uses a **Convolutional Neural Network (CNN)** to classify handwritten digits from **0 to 9** using the **MNIST dataset**.

The project demonstrates the complete workflow of an image classification problem, including data loading, preprocessing, CNN architecture design, model training, evaluation, confusion matrix analysis, and prediction on handwritten digit images.

---

## 📌 Project Overview

Handwritten digit recognition is a fundamental Computer Vision problem with applications in areas such as:

* Postal automation
* Bank cheque processing
* Digitizing handwritten documents
* Optical Character Recognition (OCR)
* Document processing

In this project, a CNN is trained to automatically learn visual features from handwritten digit images and classify them into one of the ten digit classes from **0 to 9**.

### Project Workflow

```text
MNIST Dataset
      ↓
Data Preprocessing
      ↓
DataLoader
      ↓
CNN Model
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Confusion Matrix
      ↓
Prediction on New Images
```

---

## 🎯 Objectives

* Understand the fundamentals of Convolutional Neural Networks.
* Work with the MNIST handwritten digit dataset.
* Preprocess image data using PyTorch.
* Build a CNN from scratch.
* Train the CNN for multi-class classification.
* Evaluate the model using test accuracy.
* Analyze classification performance using a confusion matrix.
* Test the trained model on new handwritten digit images.

---

## 📊 Dataset

The project uses the **MNIST handwritten digit dataset**.

MNIST contains grayscale images of handwritten digits from **0 to 9**.

### Dataset Characteristics

| Property          | Description                  |
| ----------------- | ---------------------------- |
| Dataset           | MNIST                        |
| Image Type        | Grayscale                    |
| Image Size        | 28 × 28 pixels               |
| Number of Classes | 10                           |
| Classes           | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 |
| Training Images   | 60,000                       |
| Test Images       | 10,000                       |
| Channels          | 1                            |

Each image is represented as:

```text
1 × 28 × 28
```

where:

```text
1  → Grayscale channel
28 → Image height
28 → Image width
```

---

## 🖼️ Sample Dataset

The MNIST dataset contains handwritten examples such as:

```text
  0     1     2     3     4
  5     6     7     8     9
```

Each image is associated with a corresponding label representing the digit.

---

## 🧹 Data Preprocessing

The images are converted into PyTorch tensors before being passed to the CNN.

The main preprocessing step is:

```python
transforms.ToTensor()
```

This converts the image into a tensor and scales pixel values into the range:

```text
0 → 1
```

The processed input has the shape:

```text
[Batch Size, 1, 28, 28]
```

---

## 🧠 CNN Architecture

The CNN architecture used in this project consists of convolutional layers, activation functions, pooling layers, and fully connected layers.

### Architecture

```text
Input Image
1 × 28 × 28
      ↓
Conv2D
32 Filters
      ↓
ReLU
      ↓
MaxPooling
      ↓
Conv2D
64 Filters
      ↓
ReLU
      ↓
MaxPooling
      ↓
Flatten
      ↓
Fully Connected Layer
      ↓
ReLU
      ↓
Output Layer
10 Classes
```

### Model Components

#### 1. Convolutional Layer

The convolutional layers learn spatial features from the handwritten images, such as:

* Edges
* Lines
* Curves
* Shapes
* Digit-specific patterns

#### 2. ReLU Activation

The ReLU activation function introduces non-linearity into the network.

```text
ReLU(x) = max(0, x)
```

#### 3. Max Pooling

Max pooling reduces the spatial dimensions of feature maps while retaining important features.

#### 4. Flatten

The extracted feature maps are converted into a one-dimensional vector before being passed to the fully connected layers.

#### 5. Fully Connected Layer

The fully connected layers use the extracted features to classify the image into one of the ten digit classes.

---

## ⚙️ Model Training

The CNN is trained using:

* **Framework:** PyTorch
* **Loss Function:** Cross Entropy Loss
* **Optimizer:** Adam
* **Batch Size:** 64
* **Epochs:** 10
* **Task:** Multi-class classification

During training, the model learns by:

```text
Forward Pass
     ↓
Prediction
     ↓
Calculate Loss
     ↓
Backpropagation
     ↓
Update Weights
```

---

## 📈 Model Evaluation

The trained model is evaluated using the MNIST test dataset.

The primary evaluation metric is:

### Test Accuracy

```text
Accuracy =
Correct Predictions / Total Predictions × 100
```

The project also uses a **confusion matrix** to analyze how well the model classifies each digit.

---

## 📊 Confusion Matrix

A confusion matrix helps identify which digits are correctly classified and which digits are being confused with one another.

For example:

```text
Actual 7 → Predicted 7
```

is a correct prediction.

While:

```text
Actual 7 → Predicted 1
```

is an incorrect prediction.

The diagonal of the confusion matrix represents correctly classified samples.

---

## 🧪 Prediction on New Images

After training, the model can be used to predict handwritten digits from new images.

Example workflow:

```text
New Image
    ↓
Resize to 28 × 28
    ↓
Convert to Grayscale
    ↓
Convert to Tensor
    ↓
CNN Model
    ↓
Predicted Digit
```

Example:

```text
Input Image → 7

Model Prediction → 7
```

---

## 🛠️ Technologies Used

* **Python**
* **PyTorch**
* **Torchvision**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Jupyter Notebook**

