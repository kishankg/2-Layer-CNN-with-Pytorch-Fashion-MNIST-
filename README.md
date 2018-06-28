# 2-Layer-CNN-with-Pytorch-Fashion-MNIST-
I have used 2 layered CNN network, Autograd, Xavier weight and Avg-Pooling.
Highest accuracy till now on test-data is 91.45%.
For this project I have used Fashion MNIST dataset. It is a grayscale image of size 28*28. I have downloaded the train and test data from https://github.com/zalandoresearch/fashion-mnist. Data was in ubyte form so I used a function to convert data from Ubyte to CSV. The function takes image , label and datasize as input and convert them into csv file have matrix of 10x786. Rows having labels and columns having each pixels value(28x28). Then implemented a class that inherits the Dataset type and defines reading functions and data access. I loaded the csv file in dataset class and convert into numpy array and return image and label. into a Dataset having image and label to feed into Dataloader. Dataloader will actually read the data, batches it and shuffle it to prevent the overfitting on training data.

I have used Convolutional Neural Network to train the image because the pixel value in one region of an image can be related to other pixel values in same region, so assuming this fact CNN can work better. CNNs are used to learn Filter that when convoled with image it will extract the features. I have done ba

I have used batch normalization to speed up the learning. Batch Normalization allows each layer of a network to learn by itself a little bit more independetly of other layers and it reduces overfitting because it has slight regularization effect.

Now I iterate over batch of images. And calulated the loss on every step. Using the backpropagation we updated our parameter so decreased the loss to get better accuracy. Then I evaluated them on my test data.

