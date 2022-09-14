Problem Statement
The task at hand is to classify handwritten digits using supervised machine learning methods. The digits belong to classes of 0 to 9.

“Given a query instance (a digit) in the form of an image, our machine learning model must correctly classify its appropriate class.

Dataset

MNIST Handwritten Digits dataset is used for this task. It contains images of digits taken from a variety of scanned documents, normalized in size and centered. Each image is a 28 by 28 pixel square (784 pixels total). The dataset contains 60,000 images for model training and 10,000 images for the evaluation of the model.

Methodology

I have used supervised machine learning models to predict the digits. Since this is a comparative study hence we will first describe the K-Nearest Neighbors Classifier as the baseline method which will then be compared to Multiclass Perceptron Classifier and SVM Classifier.

1) K-Nearest Neighbors Classifier – Our Baseline Method

k-Nearest Neighbors (k-NN) is an algorithm, which:

ﬁnds a group of k objects in the training set that are closest to the test object, and
bases the assignment of a label on the predominance of a class in this neighborhood.
When we used the K-NN method the following pros and cons were observed:

Pros

K-NN executes quickly for small training data sets.
No assumptions about data — useful, for example, for nonlinear data
Simple algorithm — to explain and understand/interpret
Versatile — useful for classification or regression
Training phase is extremely quick because it doesn’t learn any data
Cons

Computationally expensive — because the algorithm compares the test data with all examples in training data and then finalizes the label
The value of K is unknown and can be predicted using cross validation techniques
High memory requirement – because all the training data is stored
Prediction stage might be slow if training data is large

2) SVM Classifier using Histogram of Oriented Gradients (HOG) Features:

Just for comparison purposes, we have also used a third supervised machine learning technique named Support Vector Machine Classifier. The model isn’t implemented. Its imported directly from scikit learn module of python and used.

In K-NN and Multiclass Perceptron Classifier we trained our models on raw images directly instead of computing some features from the input image and training the model on those computed measurements/features.

A feature descriptor is a representation of an image that simplifies the image by extracting useful information and throwing away extraneous information. Now we are going to compute the Histogram of Oriented Gradients as features from the digit images and we will train the SVM Classifier on that. The HOG descriptor technique counts occurrences of gradient orientation in localized portions of an image - detection window.

