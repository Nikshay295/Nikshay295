#  Colon Cancer Detection Using Deep Learning (CNN vs ResNet-50)

This project applies deep learning to automate the classification of colon histopathological images into **benign** or **cancerous (adenocarcinoma)** categories. It compares a custom-built **Convolutional Neural Network (CNN)** with a transfer learning model, **ResNet-50**, to determine which architecture provides better performance for medical image classification.

---

##  Project Summary

- **Domain**: Medical Image Classification
- **Objective**: Detect colon cancer from histopathological images using deep learning
- **Dataset**: 500 original images (250 benign, 250 cancer), augmented to 5000 per class
- **Tools Used**: Python, TensorFlow, Keras, NumPy, Matplotlib
- **Models**: CNN (from scratch) vs ResNet-50 (transfer learning)

---

##  Methodology

###  Data Preprocessing
- Resized all images to a consistent input size
- Normalized pixel values for better model performance
- Augmented data using `ImageDataGenerator` to enhance generalization
- Split into **training (80%)** and **validation (20%)**

###  Model Development
#### CNN Model (Custom):
- Convolutional, pooling, and fully connected layers
- Trained from scratch
- Struggled with overfitting and poor generalization

#### ResNet-50 (Pretrained):
- Transfer learning using ImageNet weights
- Fine-tuned last few layers
- Achieved near-perfect training and validation performance
- 
## Model Evaluation

| Metric      | CNN         | ResNet-50    |
|-------------|-------------|--------------|
| Accuracy    | 50%         | 100%         |
| Precision   | Low         | 1.00         |
| Recall      | Low         | 1.00         |
| F1-Score    | Poor        | 1.00         |
| Confusion Matrix | 100% benign only | Perfect across both classes |

## Results

- **CNN** struggled to classify adenocarcinoma samples and failed to improve over epochs.
- **ResNet-50** achieved perfect classification with almost no errors on both training and validation sets.

## Project Structure

