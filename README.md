# 🌿 Sugarcane Disease Detection using MobileNetV2

This project implements a deep learning–based image classification system to detect sugarcane leaf diseases using **MobileNetV2 with transfer learning**. The model classifies images into two categories: **Healthy** and **Unhealthy**, enabling early detection and better crop management.

---

## 🚀 Features

* Transfer Learning using MobileNetV2 (ImageNet pretrained)
* Two-phase training:

  * Feature extraction (frozen base)
  * Fine-tuning (last layers unfrozen)
* Data augmentation for better generalization
* Performance evaluation using multiple metrics
* Visualization of training performance and results

---

## 📂 Dataset Structure

```
Images/
 ├── Healthy/
 ├── Unhealthy/
 ├── test set/
      ├── healthy/
      ├── unhealthy/
```

---

## 🧠 Model Architecture

* Base Model: MobileNetV2 (pretrained on ImageNet)
* Custom Layers:

  * GlobalAveragePooling
  * Batch Normalization
  * Dense layers (256 → 128)
  * Dropout (regularization)
  * Output layer (Sigmoid for binary classification)

---

## 📊 Results

```
Accuracy   : 73.91%
AUC        : 0.9192
Precision  : 0.9286
Recall     : 0.4815
F1 Score   : 0.6341
```

### 🔍 Detailed Classification Report

| Class     | Precision | Recall | F1-score | Support |
| --------- | --------- | ------ | -------- | ------- |
| Healthy   | 0.68      | 0.97   | 0.80     | 61      |
| Unhealthy | 0.93      | 0.48   | 0.63     | 54      |

* **Overall Accuracy:** 73.91%
* **Macro Avg F1:** 0.72
* **Weighted Avg F1:** 0.72

---

## 📈 Visualizations

The project generates:

* Accuracy & Loss curves
* AUC curve
* Confusion Matrix
* ROC Curve
* Final metrics summary

Saved as:

```
mobilenet_results.png
```

---

## 💾 Model Output

* Trained model saved as:

```
best_mobilenet_sugarcane.keras
```

---

## ⚙️ Tech Stack

* Python
* TensorFlow / Keras
* NumPy, Matplotlib, Seaborn
* Scikit-learn

---

## ⚠️ Observations

* High **precision (0.93)** for detecting unhealthy leaves
* Lower **recall (0.48)** → some diseased cases are missed
* Model is slightly biased toward predicting “healthy”

---

## 🔮 Future Improvements

* Improve recall using class balancing or weighted loss
* Increase dataset size for better generalization
* Try advanced architectures (EfficientNet, ResNet)
* Apply Grad-CAM for model interpretability

---

## 📌 Conclusion

The model demonstrates strong capability in distinguishing sugarcane leaf conditions using deep learning. While overall performance is good, improving recall for unhealthy cases will further enhance real-world reliability.



* Add **badges (GitHub style)**
* Or tailor it for **resume/portfolio impact**
