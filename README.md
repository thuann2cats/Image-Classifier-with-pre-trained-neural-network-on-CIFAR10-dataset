# Experiment: Image Classifier - using DenseNet pre-trained network on CIFAR10 dataset

In this [experiment](..%2FExperiment_Image_Classifier_CIFAR10_dataset.ipynb), in order to reinforce what I am learning about deep neural network, I use `DenseNet`, a neural network that is pre-trained and available through the `torchvision` module in order to train a neural network to classify the CIFAR10 image dataset into 10 labels.

`DenseNet` was trained on *ImageNet*, a massive dataset with 1 million labeled images. It has a stack of convolutional layers and a classifier. Here, I will experiment by replacing the `classifier` part with a simple network with a hidden layer that will output 10 probabilities corresponding to 10 labels in this CIFAR10 dataset. The rest of the network is frozen so we can make use of the pre-trained parameters.

Because `DenseNet` has been pre-trained, the expectation is that it can detect features very well, so that a simple classifier can be plugged in to make the whole network train easily on a new image dataset, and the test accuracy is expected to be high.

This experiment follows the instructions from Udacity's Intro to Neural Network with Pytorch. 

## Result

On Udacity's GPU-enabled workspace, running one epoch (about 800 batches of 64 images) takes about 1 hour, and the testing accuracy was at 80%.
