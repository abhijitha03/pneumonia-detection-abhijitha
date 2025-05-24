# Pneumonia Detection Using CNN

This project uses a Convolutional Neural Network (CNN) to detect **Pneumonia** from chest X-ray images. It is trained on a labeled dataset containing X-ray images classified as either **Pneumonia** or **Normal**.

---

##  Dataset

The dataset used is from the [Kaggle Chest X-ray Images (Pneumonia) dataset](https://www.kaggle.com/code/kashyapgohil/pneumonia-detection-using-cnn/input), which contains images organized in the following structure:
chest_xray/
├── train/
├── val/
└── test/

Each folder contains subfolders: `NORMAL` and `PNEUMONIA`.

---

##  Model Architecture

The CNN model consists of:

- 3 Convolutional layers each followed by MaxPooling
- A Dense layer with 512 neurons and ReLU activation
- A Dropout layer with rate 0.5 to reduce overfitting
- A final Dense output layer with sigmoid activation for binary classification
Conv2D → MaxPooling → Conv2D → MaxPooling → Conv2D → MaxPooling → Flatten → Dense(512) → Dropout → Dense(1)

---

##  Optimizations Applied

- Data Augmentation (rotation, zoom, horizontal flip)
- Early Stopping to prevent overfitting
- ReduceLROnPlateau to reduce learning rate on plateau
- Dropout layer for regularization
- Proper image normalization and resizing to 150x150 RGB

---

##  Running the Notebook

You can run this project in **Google Colab**.

### Steps:

1. Open the notebook (`pneumonia_detection.ipynb`) in Google Colab.
2. Upload your Kaggle API key (`kaggle.json`) to access the dataset.
3. Download and unzip the dataset.
4. Train the CNN model using the provided code.
5. Upload a custom chest X-ray image to get a prediction: Normal or Pneumonia.

---

##  Predict on New Image

After training, upload any new chest X-ray image and the model will output:

- `Prediction: Pneumonia `  
- `Prediction: Normal `

---

##  Results

The model achieves over **90% accuracy** on the test dataset with minimal overfitting thanks to the optimizations applied.

---

##  Author

**Abhijitha**  

---
