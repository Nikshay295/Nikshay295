#  Colon Cancer Detection Using Deep Learning (CNN vs ResNet-50)

This project applies deep learning techniques to detect colon cancer from histopathological images. We developed and compared two models: a custom-built **Convolutional Neural Network (CNN)** and a **ResNet-50** model using transfer learning. The aim is to assist in faster, more accurate cancer diagnosis by automating image-based classification.

---

##  Objective

Develop a classification model that can automatically distinguish between **benign colon tissue** and **colon adenocarcinoma** using histopathological images. The goal is to improve the efficiency and accuracy of cancer diagnosis processes.

---

## Dataset Summary

- **Total Images**: 500 original images  
  - 250 benign colon tissue  
  - 250 adenocarcinoma (colon cancer)  
- Images were augmented to 5,000 per class
- All images resized and normalized to standard dimensions for neural network input

---

## ⚙ Workflow

### 1. Data Preprocessing
- Image resizing and normalization
- Data augmentation using `ImageDataGenerator`
- Train-validation split (80/20)

### 2. Model Development
####  CNN Model
- Custom layers with convolution, ReLU activation, pooling, and fully connected layers
- Moderate performance, limited generalization (accuracy: ~50%)

#### ResNet-50 Model
- Pretrained on ImageNet
- Fine-tuned top layers
- Excellent performance (accuracy: 100%, precision and recall: 1.00)

---

## Results Summary

| Model   | Accuracy | Precision | Recall | F1 Score |
|---------|----------|-----------|--------|----------|
| CNN     | 50%      | Low       | Low    | Low      |
| ResNet  | 100%     | 1.00      | 1.00   | 1.00     |

- CNN failed to identify adenocarcinoma correctly (100% false negatives)
- ResNet-50 generalized well with almost perfect performance

---

## Visual Output

- Confusion matrices for both models
- Training and validation accuracy/loss plots
- Classification reports with precision, recall, F1 score

---

##  Key Takeaways

- **CNN** is not sufficient for complex histopathological patterns.
- **ResNet-50** provides significantly better results using transfer learning.
- Automation in histopathological image analysis can greatly improve diagnostic workflows in healthcare.

---

## 
---

## 👤 Author

**Nikshay Policepatel**  
📧 [nikshaypatels@gmail.com](mailto:nikshaypatels@gmail.com)  
🔗 [LinkedIn](https://linkedin.com/in/NikshayPolicepatel)

---

> ⚠️ *Disclaimer: This is an academic project using open image datasets and is not intended for real-world clinical decision-making.*


