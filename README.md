# American Sign Language (ASL) Image Classification with CNN

This repository implements a Convolutional Neural Network (CNN) for classifying American Sign Language (ASL) letters from RGB images.

The model demonstrates supervised image classification using a compact convolutional architecture and evaluates performance on a held-out test set.


<img width="1151" height="307" alt="image" src="https://github.com/user-attachments/assets/15bd1220-7d17-4d18-bf92-1dc632d2e668" />

## Dataset

- Image size: 50 × 50 RGB
- Classes: A, B, C
- ~1,600 training samples
- ~400 test samples
- Balanced class distribution

---

## Model Architecture

- Conv2D (5 filters, 5×5 kernel, ReLU)
- MaxPooling
- Conv2D (15 filters, 5×5 kernel, ReLU)
- MaxPooling
- Flatten
- Dense (Softmax output)

**Total Parameters:** 2,453  
**Trainable Parameters:** 2,453  

---

## Training Details

- Optimizer: RMSProp
- Loss: Categorical Cross-Entropy
- Epochs: 2
- Batch Size: 32
- Validation Split: 20%

---

## Results

- Validation Accuracy: 96.25%
- Test Accuracy: **96.75%**

---

## Error Analysis

Misclassified samples were visualized to analyze ambiguity in hand pose, lighting variation, and intra-class similarity.

---

## Future Improvements

- Extend to full ASL alphabet
- Data augmentation for improved generalization
- Deeper CNN architecture
- Transfer learning (e.g., ResNet / MobileNet)
- Real-time webcam inference
