# 🧠 CIFAR-10 Image Classification Project

## 📌 Problem Statement
Image classification is a key problem in computer vision. The goal of this project is to correctly classify images from the **CIFAR-10 dataset** into one of 10 categories.

CIFAR-10 is challenging because:
- Images are very small (32x32 pixels)
- Classes have high similarity (e.g., cat vs dog)
- Limited feature visibility

---

## 🎯 Objective
To build and optimize deep learning models that can accurately classify CIFAR-10 images using:
- Transfer Learning
- Custom CNN Architecture

---

## 📊 Dataset Details
- **Dataset:** CIFAR-10
- **Total Images:** 60,000
- **Training:** 50,000
- **Testing:** 10,000
- **Classes (10):**
  - Airplane, Automobile, Bird, Cat, Deer
  - Dog, Frog, Horse, Ship, Truck

---

## ⚙️ Tech Stack
- **Programming Language:** Python  
- **Libraries:**
  - TensorFlow / Keras
  - NumPy, Pandas
  - Matplotlib, Seaborn
  - Scikit-learn  

---

## 🧪 Approach

### 1️⃣ Transfer Learning (MobileNetV2)

#### Step 1: Initial Setup
- Used pre-trained **MobileNetV2**
- Kept base model layers **frozen**
- Result: Low accuracy

#### Step 2: Fine-Tuning
- Unfroze some layers of base model
- Added:
  - GlobalAveragePooling layer
  - Dropout (to reduce overfitting)
- Used:
  - Adam optimizer (low learning rate)
  - Batch size = 8
  - EarlyStopping

#### ✅ Result:
- **Accuracy:** 77%
- **F1 Score:** 0.79

---

### 2️⃣ Custom CNN Model

#### Architecture:
- Conv2D layers
- Batch Normalization
- MaxPooling layers
- Dropout layers
- ReLU activation
- Adam optimizer
- EarlyStopping

#### ✅ Result:
- **Accuracy:** 80%

---

### 🔧 Final Optimization (Custom CNN)

Further improvements:
- Increased model depth (more layers)
- Applied learning rate scheduling
- Tuned hyperparameters
- Continued batch-wise training

#### 🏆 Final Result:
- **Accuracy:** 82%
- **F1 Score:** 0.79

---

## 📈 Evaluation Metrics
- Accuracy
- F1 Score
- Classification Report
- Confusion Matrix (Heatmaps)

---

## 📊 Outputs & Visualizations
- Confusion matrix heatmaps
- Training vs validation accuracy/loss graphs
- Classification reports for both models

---

## 🧪 Testing
- Model tested on **10 unseen images**
- Achieved good real-world prediction performance

---

## 💡 Key Learnings
- Transfer learning needs proper fine-tuning for small datasets
- Lightweight models may underperform without adjustments
- Custom CNNs can outperform pre-trained models when designed well
- Dropout and BatchNorm help reduce overfitting
- Learning rate tuning is critical for performance

---

## 🚀 Future Improvements
- Add **data augmentation** (flip, rotation, zoom)
- Try advanced models (ResNet, EfficientNet)
- Use **Optuna** for hyperparameter tuning
- Apply **Grad-CAM** for model explainability
- Deploy using:
  - Flask / FastAPI
  - Streamlit dashboard
- Convert model to **TensorFlow Lite** for mobile/edge use
- Experiment with **ensemble models**

---

## 🏁 Conclusion
This project demonstrates:
- End-to-end deep learning pipeline
- Model comparison (Transfer Learning vs Custom CNN)
- Performance improvement through tuning

Final model achieved **82% accuracy**, showing strong classification capability on CIFAR-10.

---

## ⭐ Support
If you found this project useful, consider giving it a ⭐ on GitHub!
