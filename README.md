# 🧵 Fashion-MNIST Image Classification using a Custom CNN

This project is end-to-end implementation of an **image classification model** built using a **Convolutional Neural Network (CNN)** from scratch.  
I chose the **Fashion-MNIST dataset** and designed the entire architecture manually without using any pre-trained models, so I could fully demonstrate my understanding of deep-learning fundamentals.

The notebook covers the complete workflow:  
**data exploration → preprocessing → model building → training → tuning → evaluation → visualization → analysis.**

---

## 🌟 1. Project Overview

The goal of this project was to build a CNN that can classify 28×28 grayscale clothing images into 10 different categories (e.g., T-shirt, Dress, Sneaker, Bag).  
I avoided transfer learning and implemented the entire architecture myself using TensorFlow/Keras.

This helped me strengthen my understanding of how convolution layers extract features, how pooling reduces spatial dimensions, and how hyperparameters like learning rate impact training.

---

## 📂 2. Dataset: Fashion-MNIST

I used the **Fashion-MNIST dataset** created by Zalando Research. It is widely used as a more realistic and challenging alternative to the original MNIST digits dataset.

### 🔗 Official Dataset Links
- GitHub (Zalando Research):  
  https://github.com/zalandoresearch/fashion-mnist  
- Dataset documentation:  
  https://github.com/zalandoresearch/fashion-mnist#dataset  
- TensorFlow/Keras loader:  
  https://www.tensorflow.org/api_docs/python/tf/keras/datasets/fashion_mnist  

### 📊 Dataset Summary
- 60,000 training images  
- 10,000 test images  
- 10 balanced classes  
- Grayscale, 28×28 pixels  

### Class Labels
T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot.

In my notebook, I visualized sample images, plotted the class distribution, and explored pixel intensity patterns to understand the dataset before training.

---

## 🛠️ 3. Preprocessing Steps

Before feeding the images into the model, I applied:

- **Normalization**: Converted pixel values from 0–255 to 0–1  
- **Reshaping**: Added a channel dimension → (28, 28, 1)  
- **Validation Checks**: Verified shapes, dtypes, normalization range, and label integrity

All preprocessing validation tests passed successfully.

---

## 🧠 4. My CNN Architecture

I built a custom CNN architecture consisting of:

### 🔹 Convolutional Blocks
- Conv2D (32 filters) + BatchNormalization + MaxPooling  
- Conv2D (64 filters) + BatchNormalization + MaxPooling  
- Conv2D (64 filters) + BatchNormalization  

### 🔹 Dense Layers
- Flatten  
- Dense(64, ReLU)  
- Dropout(0.3)  
- Dense(10, Softmax)

Total parameters: ~94k  
The model is lightweight, efficient, and well-suited for Fashion-MNIST.

---

## ⚙️ 5. Training Strategy

- **Optimizer:** Adam  
- **Loss Function:** Sparse Categorical Crossentropy  
- **Epochs:** 10  
- **Batch Size:** 64  
- **Validation Split:** 10%

To better understand optimization behavior, I also conducted a **Learning Rate Experiment**, testing:

`0.1, 0.01, 0.001, 0.0001`

This experiment showed how dramatically the learning rate affects model stability and accuracy.

---

## 📊 6. Evaluation & Results

After training, I evaluated the model on the test set and achieved:

### 🎯 **Final Test Accuracy: 86.12%**  
### 📉 **Final Test Loss: 0.4379**

I also generated:

- Confusion matrix  
- Classification report (precision, recall, F1-score)  
- Per-class performance table  
- Correct prediction examples  
- Incorrect prediction examples  

Certain classes such as Trouser, Sandal, Sneaker, and Bag showed very high accuracy, while Shirt and Pullover were more challenging due to visual similarities — a common issue for this dataset.

---

## 🎨 7. Visualizations Included

The notebook contains the following visualizations:

- Training vs Validation **Accuracy Curve**  
- Training vs Validation **Loss Curve**  
- Confusion Matrix Heatmap  
- Sample images grid  
- Class distribution bar chart  
- Pixel intensity histogram  
- Correct & incorrect predictions comparison

These help explain the model’s behavior and areas for improvement.

---

## 🔍 8. Key Insights

- Batch Normalization stabilized training  
- Dropout reduced overfitting  
- Lower learning rates (0.001 / 0.0001) gave the best results  
- Similar-looking classes tend to get confused  
- 86% accuracy is strong for a custom CNN without augmentation

---

## 🚀 9. Future Improvements

If I extend this project, I plan to explore:

- Data augmentation  
- Learning rate scheduling  
- Early stopping & checkpointing  
- Additional convolution layers  
- Regularization techniques  

These steps can help push accuracy above 90%.

---

## 📁 10. What This Notebook Includes

- Full data exploration  
- Preprocessing & shape validation  
- Custom CNN built from scratch  
- Learning rate experiments  
- Training performance visualizations  
- Confusion matrix & classification report  
- Correct vs incorrect prediction visualizations  
- Final performance summary  

This notebook demonstrates my understanding of CNNs, deep learning workflows, and model evaluation techniques.

---

## 🏁 Final Summary

This project allowed me to strengthen my foundation in deep learning by building, training, and evaluating a CNN without relying on pre-trained models.  
It reflects my ability to implement clean, understandable, and reproducible machine learning pipelines — something I aim to apply and improve further in real-world AI projects.
<<<<<<< HEAD
=======

>>>>>>> f476148d4d7a9513fe730104daa42c952b7efa36
