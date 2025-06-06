👁️ Face Detection with SVM and HOG Features

Final Project for the course "Machine Learning: Advanced Techniques"
Master’s Program in Data Science

📌 Project Overview

This project focuses on developing a machine learning model for face detection.
The goal is to detect the presence of human faces in an image and draw bounding boxes around them.

The detection strategy is divided into two main phases:

Train a binary classifier to distinguish between face and non-face images.
Apply a sliding window technique across full images to detect faces at various positions.
🧠 Model & Methodology

Classifier: Support Vector Machine (SVM)
Image Features: Histogram of Oriented Gradients (HOG)
Detection Technique: Sliding Window
🔍 Sliding Window
This method involves scanning the image with a fixed-size rectangular window and classifying each windowed region to check for the presence of a face.

🗂️ Datasets

Two datasets were used to train and test the model:

1. Olivetti Face Dataset (Positive Class)
📥 Source: GitHub – Olivetti PNG
📸 Description: Contains 400 PNG images of 40 individuals under different angles
🧩 Size: 64x64 pixels
2. Non-Face and Face Dataset (Negative Class)
📥 Source: Kaggle – Nonface and Face Dataset
📸 Description: Contains 2900+ images, with 1331 face images
⚠️ Only non-face images were used as negative examples for better accuracy
Note: Initially, the Kaggle dataset was used for both classes. However, the face images contained too much background, which led the model to associate background patterns with faces. This was corrected by using the Olivetti dataset for cleaner positive samples.
⚙️ How It Works

Extract HOG features from training images
Train the SVM using face and non-face image samples
Apply sliding window over input images
Classify each window, and draw bounding boxes around detected faces

📈 Limitations & Future Work

❗ Current detection is limited to fixed-size windows (no scale invariance)
🔄 Future improvements may include:
Multi-scale detection
CNN-based approaches (e.g., using pre-trained models like Haar Cascades or SSD)
Real-time webcam integration
