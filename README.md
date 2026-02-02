# 🐱🐶 Cats vs Dogs Image Classifier

This project is part of the [freeCodeCamp Machine Learning with Python curriculum](https://www.freecodecamp.org/learn/machine-learning-with-python/).  
It uses **TensorFlow 2.0** and **Keras** to build a Convolutional Neural Network (CNN) that classifies images of cats and dogs.

The goal of the challenge is to achieve at least **63% accuracy** on the test set (extra credit for 70%+).  
My implementation passes the challenge ✅.

---

## 📂 Dataset Structure

The dataset is automatically downloaded and extracted into the following structure:

cats_and_dogs/
│__ train/
│   ├── cats/
│   └── dogs/
│__ validation/
│   ├── cats/
│   └── dogs/
│__ test/
├── 1.jpg
├── 2.jpg
└── ...


- **Train**: 2000 images (cats & dogs)  
- **Validation**: 1000 images (cats & dogs)  
- **Test**: 50 unlabeled images  

---

## ⚙️ Project Workflow

1. **Data Preparation**  
   - Images are rescaled to values between 0 and 1.  
   - `ImageDataGenerator` is used to load train, validation, and test sets.  
   - For training, data augmentation (rotation, zoom, flips, shifts) is applied to reduce overfitting.

2. **Model Architecture**  
   - Sequential CNN with Conv2D + MaxPooling layers.  
   - Dense fully connected layer with ReLU activation.  
   - Dropout for regularization.  
   - Final sigmoid layer for binary classification (cat vs dog).

3. **Training**  
   - Optimizer: `Adam`  
   - Loss: `binary_crossentropy`  
   - Metric: `accuracy`  
   - Trained for 15 epochs with batch size 128.

4. **Evaluation**  
   - Accuracy and loss curves are plotted.  
   - Predictions are made on the 50 test images.  
   - Final accuracy compared against ground truth answers.
