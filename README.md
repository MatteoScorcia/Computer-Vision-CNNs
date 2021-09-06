# Computer-Vision-CNNs

Computer Vision And Pattern Recognition course.

## Problem Statement

This project requires the implementation of an image classifier based on CNNs. The provided dataset (from [Lazebnik et al., 2006]), contains 15 categories (office, kitchen, living room, bedroom, store, industrial, tall building, inside city, street, highway, coast, open country, mountain, forest, suburb), and is already divided in training set and test set.

There are 3 main topics covered in the project:

1. Train a shallow network from scratch according to the specifications:

   - Split the provided training set in 85% for actual training set and 15% to be used as validation set.

   - Since the input image is 64×64 you will need to resize the images in order to feed them to the network; follow the simple approach of rescaling the whole image independently along x and y to get the proper size.

   - Employ the stochastic gradient descent with momentum optimization algorithm.

   - Use minibatches of size 32 and initial weights drawn from a Gaussian distribution with a mean of 0 and a standard deviation of 0.01; set the initial bias values to 0.

   - Use the network layout shown in the project assignment.

2. Improve the previous result, according to the following suggestions:

   - Data augmentation: given the small training set, data augmentation is likely to improve the performance.Left-to-right reflections, random cropping, small rotations, rescaling are reasonable augmentation techniques.

   - Add batch normalization layers before the reLU layers [Ioffe and Szegedy, 2015].

   - Change the size and/or the number of the convolutional filters.

   - Switch to the adam optimizer.

   - Add some dropout layer to improve regularization.

   - Employ an ensemble of networks (five to ten), trained independently. Use the arithmetic average of the outputs to assign the class, as in [Szegedy et al., 2015].

3. Use transfer learning based on a pre-trained network, for instance VGG19, in the following two manners:

   - Freeze the weights of all the layers but the last fully connected layer and fine-tune the weights of the last layer based on the same train and validation sets employed before.

   - Employ the pre-trained network as a feature extractor, accessing the activation of an intermediate layer (for instance the last convolutional layer) and train a multiclass linear SVM.

## Description of the approach, implementation choices and results

For each one of the previous points, there is a notebook.

1. -> Basic.ipynb

2. -> ImprovedCNN.ipynb

3. -> TransferLearningCNN.ipynb
