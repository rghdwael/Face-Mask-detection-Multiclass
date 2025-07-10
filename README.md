# Face-Mask-detection-Multiclass
This project presents a Face Mask Detection model built using Convolutional Neural Networks (CNNs) with TensorFlow and Keras. The primary goal is to accurately classify images into three categories: "with mask," "without mask," and "mask weared incorrect."

## 🔍 Dataset
- Source: [Kaggle - vijaykumar1799/face-mask-detection](https://www.kaggle.com/datasets/vijaykumar1799/face-mask-detection)
- Preprocessing:
  - Duplicates removed across train/val/test
  - Resized to 128x128
  - Augmented with flip, brightness, contrast, zoom

## 🧠 Model
- Custom CNN with BatchNorm, Dropout, and ReduceLROnPlateau
- Trained with categorical crossentropy
- Accuracy: **97%** on internal test set

## 🚀 How to Run
1. You can view and run the full notebook on Google Colab:https://colab.research.google.com/drive/1LQV5d-63BKa50-eTkwvwHBZfGphxpaVq#scrollTo=cnuRgquJqIza
2. OR Download The Jupyter Notebook

## ⚠️ Known Limitations

The model in the last cell includes a preprocessing step using OpenCV's Haar Cascade face detector to automatically detect and crop faces from external photos before classification.

However, some real-world images are still misclassified due to:

- Domain shift: lighting, angles, occlusion, backgrounds
- Limited variation in the original training dataset (clean, well-lit, cropped images

### 🔧 Recommendations for Improvement:
- Fine-tune the model with additional real-world face mask images
- Use stronger augmentations or synthetic image generation
- Try adding pre-trained model (MobileNet,etc..)


