Project Title
Deep Learning Image Classification using CNN for Cat and Dog Images

Overview
This project was completed as part of Task 2 of the Alfido Tech AI Internship. The goal was to build a small deep learning image classification model in Google Colab using TensorFlow. The model classifies images into two categories: cat and dog.

Package Requirements
The notebook uses the following Python packages:

tensorflow

matplotlib

numpy

seaborn

scikit-learn

If needed, install them using:

python
!pip install tensorflow matplotlib numpy seaborn scikit-learn
How to Run the Notebook
Open Google Colab.

Create a new notebook.

Copy and paste the Task 2 code into the notebook.

Run all cells from top to bottom.

Wait for the training process to complete.

Review the outputs including training curves, test accuracy, classification report, confusion matrix, and sample predictions.

Dataset Used
The project uses the CIFAR-10 dataset loaded from TensorFlow using:

python
tf.keras.datasets.cifar10.load_data()
Only the cat and dog classes are filtered and used for binary classification.

Model File Save Location
After training, the model is saved in Google Colab at the following path:

python
/content/task2_simple_cnn_cats_dogs.keras
This file contains the trained deep learning model and can be downloaded from the Colab file panel or by using:

python
from google.colab import files
files.download('/content/task2_simple_cnn_cats_dogs.keras')
How Inference Works
Inference means using the trained model to predict whether an image belongs to the cat or dog class.

In the notebook, inference is demonstrated in two ways:

1. Predictions on Test Data
The trained model predicts labels for the test dataset using:

python
y_pred_probs = model.predict(x_test, verbose=0)
y_pred = (y_pred_probs > 0.5).astype(int).flatten()
If the prediction value is greater than 0.5, the image is classified as dog. Otherwise, it is classified as cat.

2. Loading the Saved Model
The saved model can be loaded again for future predictions using:

python
loaded_model = tf.keras.models.load_model('/content/task2_simple_cnn_cats_dogs.keras')
After loading, the model can be used on image data to generate predictions in the same way.

Outputs Generated
The notebook generates the following outputs:

Training accuracy and validation accuracy curves

Training loss and validation loss curves

Test accuracy and test loss

Classification report

Confusion matrix

Sample image predictions

Saved .keras model file

Submission Files
Recommended files for submission:

Task 2 notebook file (.ipynb)

Saved model file (.keras)

Report document (.pdf, .docx, or .md)

README file

Screenshots of results and plots

Conclusion
This project demonstrates a complete deep learning workflow including dataset preparation, image preprocessing, CNN model training, evaluation, model saving, and inference in Google Colab.
