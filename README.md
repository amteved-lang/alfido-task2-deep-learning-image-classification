# Task 2: Deep Learning Image Classification
## Alfido Tech AI Internship

### Project
Cats vs Dogs Image Classification using TensorFlow and Transfer Learning

### Notebook Name
Task2_DeepLearning_Image_Classification_CatsVsDogs

### Requirements
- Python 3.x
- TensorFlow
- TensorFlow Datasets
- Matplotlib
- NumPy

### Run in Google Colab
1. Open Google Colab
2. Create a new notebook
3. Copy the code from `task2_google_colab_code.py`
4. Run all cells in sequence

### What the code does
- Loads cats_vs_dogs dataset from TensorFlow Datasets
- Applies image resizing and normalization
- Uses data augmentation
- Builds an image classifier with MobileNetV2 transfer learning
- Trains and validates the model
- Plots training curves
- Evaluates on test data
- Saves the trained model
- Runs inference on sample images

### Saved Model
The trained model is saved as:
`/content/task2_cats_dogs_mobilenetv2.keras`

### Inference
The notebook includes a section that loads the saved model and predicts labels for sample test images.

### Suggested Files for Submission
- task2 notebook (.ipynb)
- task2 report (.pdf/.docx)
- saved model file (.keras)
- screenshots of training curves and predictions
- README.md
