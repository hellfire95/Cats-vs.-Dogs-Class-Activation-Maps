# Cats vs. Dogs Class Activation Maps

## Overview
Class Activation Maps (CAMs) for classifying images into two categories: Cats and Dogs. 

## Dataset
We will use the [Cats vs. Dogs dataset](https://www.tensorflow.org/datasets/catalog/cats_vs_dogs), which can be easily loaded using TensorFlow Datasets. The dataset consists of images labeled with 0 for cats and 1 for dogs.

## Building the Classifier
The model you will build is designed for binary classification, distinguishing between cats and dogs. 

For loss, you will use `binary_crossentropy` as the appropriate choice for a binary classification problem.

## Class Activation Maps (CAMs)
Armed with all this information, you can calculate the class activation map for an image. A class activation map is a matrix that shows what parts of the image the model was paying attention to when deciding what class to assign the image. It's a map of which pixels of the image sent activations that you use to determine the class of the object.

To get the class activation map, you will start by getting the features. The feature map output from the convolutional layer for the test set will be a tensor. You can then use this information to generate the class activation map, which will highlight the areas of the image that the model focused on during the classification process.
![CAT](https://github.com/hellfire95/Cats-vs.-Dogs-Class-Activation-Maps/blob/main/CAM-cat1.png?raw=true)
This concept is known as class activation maps and is a valuable tool for understanding where the model is directing its attention when making predictions.
![DOG](https://github.com/hellfire95/Cats-vs.-Dogs-Class-Activation-Maps/blob/main/CAM-dog1.png?raw=true)
## Model Performance
On training the model reaches 80% accuracy, you might observe that the presence of specific features, such as eyes and nose for dogs, and whiskers and a collar for cats, plays a significant role in determining the classification. However, there may still be misclassifications based on the presence or absence of these features. This suggests that the model is not yet performing optimally, and further refinement may be required, such as adding more data, training for a longer duration, using a different model architecture, or other adjustments.
