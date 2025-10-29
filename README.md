# 👗 Fashion MNIST Classifier using Convolutional Neural Networks (CNN)

A beginner-friendly **Machine Learning mini project** built using **TensorFlow** and **Keras** that classifies clothing items (like T-shirts, sneakers, bags, etc.) from the **Fashion MNIST dataset**.

---

## 🧠 Overview

This project demonstrates how to build and train a **Convolutional Neural Network (CNN)** to recognize clothing items from grayscale images.  
It covers all key ML steps — from loading data and preprocessing to training, evaluation, and visualization.

**Goal:** Predict the correct category of a clothing image among 10 classes:
> T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot.

---

## 🚀 Tech Stack

- 🐍 **Python**
- 🧩 **TensorFlow** & **Keras**
- 📊 **NumPy**
- 🎨 **Matplotlib**
- ☁️ **Google Colab**

---

## 📂 Dataset

- **Dataset:** [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist)
- **Images:** 70,000 grayscale (28×28 pixels)
- **Classes:** 10 clothing categories  
- **Split:** 60,000 training + 10,000 testing images

---

## ⚙️ Model Architecture

| Layer Type        | Output Shape   | Parameters |
|-------------------|----------------|-------------|
| Conv2D (3×3, 32)  | 26×26×32       | 320         |
| MaxPooling2D (2×2)| 13×13×32       | 0           |
| Conv2D (3×3, 64)  | 11×11×64       | 18,496      |
| MaxPooling2D (2×2)| 5×5×64         | 0           |
| Flatten           | 1600           | 0           |
| Dense (128, ReLU) | 128            | 204,928     |
| Dense (10, Softmax)| 10            | 1,290       |

🧮 **Total parameters:** ~225K  
💡 **Optimizer:** Adam  
🎯 **Loss Function:** Sparse Categorical Crossentropy

---

## 📊 Results

- ✅ **Training Accuracy:** ~91–92%
- 🧠 **Test Accuracy:** ~90%
- 🔍 Visualized predictions with correctly classified (green) and misclassified (red) labels

---

## 🖼️ Sample Output

*(You can add a screenshot here)*  
Example:  
![Sample Output](images/fashion_output.png)

---

## 💾 How to Run

1. Open the notebook in **Google Colab**  
   → [Open in Colab](https://colab.research.google.com/)
2. Run all cells sequentially.
3. After training, evaluate the model and visualize predictions.
4. Save the trained model:
   ```python
   model.save("fashion_mnist_cnn_model.h5")
