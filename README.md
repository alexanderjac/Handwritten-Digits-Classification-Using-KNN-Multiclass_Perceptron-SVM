Problem Statement
The task at hand is to classify handwritten digits using supervised machine learning methods. The digits belong to classes of 0 to 9.

“Given a query instance (a digit) in the form of an image, our machine learning model must correctly classify its appropriate class.

Dataset

MNIST Handwritten Digits dataset is used for this task. It contains images of digits taken from a variety of scanned documents, normalized in size and centered. Each image is a 28 by 28 pixel square (784 pixels total). The dataset contains 60,000 images for model training and 10,000 images for the evaluation of the model.

Methodology

I have used supervised machine learning models to predict the digits. Since this is a comparative study hence we will first describe the K-Nearest Neighbors Classifier as the baseline method which will then be compared to Multiclass Perceptron Classifier and SVM Classifier.

1) Convolutional Neural Network
<img width="1027" alt="Screen Shot 2022-09-13 at 8 27 12 PM" src="https://user-images.githubusercontent.com/90269638/190032730-72cab176-687e-400e-9a22-3343e7a659f0.png">


2) SVM Classifier using Histogram of Oriented Gradients (HOG) Features:

Just for comparison purposes, we have also used a third supervised machine learning technique named Support Vector Machine Classifier. The model isn’t implemented. Its imported directly from scikit learn module of python and used.

In K-NN and Multiclass Perceptron Classifier we trained our models on raw images directly instead of computing some features from the input image and training the model on those computed measurements/features.

A feature descriptor is a representation of an image that simplifies the image by extracting useful information and throwing away extraneous information. Now we are going to compute the Histogram of Oriented Gradients as features from the digit images and we will train the SVM Classifier on that. The HOG descriptor technique counts occurrences of gradient orientation in localized portions of an image - detection window.
<img width="1017" alt="Screen Shot 2022-09-13 at 8 28 18 PM" src="https://user-images.githubusercontent.com/90269638/190032534-dae4a97e-16a7-40f5-9746-89cbd6f55626.png">

