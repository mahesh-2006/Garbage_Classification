# 🚀 Garbage Classification - Week 3 (Final) Report

## 🎯 Focus of Week 3
The final week aimed to improve model performance and usability by fine-tuning the model, enhancing interpretability, and deploying the classifier via a web interface.

---

## ✅ Key Activities

### 🔧 1. Model Fine-Tuning
- Unfroze the top layers of EfficientNetV2B2
- Used a lower learning rate (1e-5) for safe adaptation
- Improved learning of dataset-specific features

### 🎨 2. Enhanced Data Augmentation
- Added more aggressive augmentations like:
  - Random rotation, contrast, zoom, and translation
- Improved robustness against overfitting

### 📊 3. Final Evaluation
- Evaluated the model on a reserved test set
- Generated a confusion matrix and classification report
- Visualized prediction results and identified strong/weak classes

### 🌐 4. Gradio Deployment
- Created a live web interface using Gradio
- Users can upload any image and receive predicted garbage class
- Deployment used `.keras` format model and image preprocessing

---

## 🧰 Tools & Libraries Used
- TensorFlow / Keras
- Matplotlib & Seaborn
- Scikit-learn
- Gradio

---

## 🏁 Outcome
The final model achieved strong performance across most classes. Gradio made it accessible through a simple UI, enabling easy testing and demonstration of the classifier.

