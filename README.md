# Convolutional Neural Networks - Image Classification
The objective of this project is to carry out supervised image classification on a collection of colored images. It employs a convolutional neural network design and applies data augmentation and transformations to recognize the category of images from a predefined set of 10 classes.

## Data Set ([CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html))
The dataset used is [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html), which is a widely used benchmark dataset in the field of computer vision and machine learning. It serves as a standard dataset for training and evaluating machine learning algorithms, particularly for image classification tasks. 

The dataset has the following features:
- Consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class.
- Comprises 50,000 training images and 10,000 test images.
- Classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck.

## Image Classification Details
The project is implemented in several steps simulating the essential data processing and analysis phases. <br/>

**STEP 1 - Initialization:** importing necessary libraries and modules.

**STEP 2 - Loading Dataset:** loading the dataset from [keras library](https://www.tensorflow.org/api_docs/python/tf/keras/datasets/cifar10) and checking its details.

**STEP 3 - Image Preprocessing:** data transformation and augmentation using [ImageDataGenerator](https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/image/ImageDataGenerator), as follows:
1. Scaling the pixel values of the images to be in the range [0, 1].
2. Randomly applying shear transformations to the images.
3. Randomly applying zoom transformations to the images.
4. Randomly flipping images horizontally.

**STEP 4 - Building CNN Model:** CNN model consists of the following [Sequential](https://www.tensorflow.org/api_docs/python/tf/keras/Sequential) layers:
1. Input layer.
2. Two convolutional layers with [ReLU](https://www.tensorflow.org/api_docs/python/tf/keras/activations/relu) activation function and an increasing number of filters.
3. Two max pooling layers following the convolutional layers.
4. Flattening layer.
5. Two dense/fully connected layers with [ReLU](https://www.tensorflow.org/api_docs/python/tf/keras/activations/relu) activation function.
6. Output layer with [Softmax](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Softmax) activation function.

**STEP 5 - Model Training:** model is compiled and trained using the following configurations:

- Optimizer: [Adam](https://www.tensorflow.org/api_docs/python/tf/keras/optimizers/Adam).
- Loss function: [Categorical Crossentropy](https://www.tensorflow.org/api_docs/python/tf/keras/losses/categorical_crossentropy).
- Batch size: 32
- Epochs: 10

**STEP 6 - Performance Analysis:** model accuracy is plotted and analyzed across the epochs. 
- Training and validation accuracy across epochs (Tensorflow)
