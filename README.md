# **Deep Learning Image Classification using CNN**

This repository contains **Task 2** of the **Alfido Tech AI Internship**. The project implements a deep learning image classification model in **Google Colab** using **TensorFlow/Keras** to classify **cat** and **dog** images from the **CIFAR-10** dataset.

## **Project Objective**
The main objective of this project is to build, train, and evaluate a small deep learning model for **binary image classification**. The workflow includes dataset filtering, preprocessing, data augmentation, CNN model training, performance evaluation, and saving the trained model for inference.

## **Dataset**
The project uses the **CIFAR-10** dataset loaded directly from TensorFlow using `tf.keras.datasets.cifar10.load_data()`. From the 10 available classes, only the **cat** and **dog** classes are selected to create a binary image classification problem.

## **Technologies Used**
- **Python**
- **TensorFlow / Keras**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Google Colab**

## **Project Workflow**
1. **Load** the CIFAR-10 dataset.
2. **Filter** only cat and dog images.
3. **Normalize** the image pixel values.
4. **Create** training, validation, and testing splits.
5. **Apply** data augmentation techniques such as random flip, rotation, and zoom.
6. **Build** a Convolutional Neural Network (CNN).
7. **Train** the model and validate performance.
8. **Evaluate** using test accuracy, classification report, and confusion matrix.
9. **Save** the trained model as a `.keras` file for future inference.

## **Model Architecture**
The CNN model consists of:
- **Input layer**
- **Data augmentation layer**
- **Convolutional layers** with ReLU activation
- **MaxPooling layers**
- **Flatten layer**
- **Dense hidden layer**
- **Dropout layer**
- **Output layer** with sigmoid activation for binary classification

## **Results**
The notebook generates the following results:
- **Training accuracy** and **validation accuracy** curves
- **Training loss** and **validation loss** curves
- **Test accuracy** and **test loss**
- **Classification report**
- **Confusion matrix**
- **Sample predictions** on test images

## **Package Requirements**
Install the required packages using:

```python
!pip install tensorflow matplotlib numpy seaborn scikit-learn
```

## **How to Run**
1. Open **Google Colab**.
2. Create a **new notebook**.
3. Copy the provided **Task 2 code** into the notebook.
4. Run **all cells** from top to bottom.
5. Wait for the **training process** to finish.
6. Review the generated **plots, metrics, and predictions**.

## **Saved Model**
The trained model is saved at:

```python
/content/task2_simple_cnn_cats_dogs.keras
```

To load the saved model again:

```python
loaded_model = tf.keras.models.load_model('/content/task2_simple_cnn_cats_dogs.keras')
```

## **Inference**
Inference is performed by predicting on the test dataset using the trained model. The output probability is converted into a binary class label:

```python
y_pred_probs = model.predict(x_test, verbose=0)
y_pred = (y_pred_probs > 0.5).astype(int).flatten()
```

If the predicted value is greater than **0.5**, the image is classified as **dog**; otherwise, it is classified as **cat**.

## **Repository Contents**
- **Task2_DeepLearning_Image_Classification_CNN_CatsVsDogs.ipynb**
- **README.md**
- **task2_report.md**
- **Saved model file** (`.keras`)
- **Output screenshots**

## **Internship Context**
This project was completed as part of the **Alfido Tech AI Internship**.

## **Conclusion**
This project demonstrates a complete deep learning image classification workflow in **Google Colab**, including preprocessing, augmentation, model training, evaluation, model saving, and inference. It helped strengthen practical understanding of **CNN-based image classification** using **TensorFlow**.
