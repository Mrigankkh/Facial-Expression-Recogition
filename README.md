# Facial Expression Recognition

In this project, I have classified images of facial expressions into their 7 different categories i.e. {'Angry', 'Disgust', 'Fear', 'Happy', 'Sad', 'Surprise', 'Neutral'} .I built the network using pytorch, trained on Google Colab using thousands of images in the training set and attained an accuracy of 60% against the test set. The state of the art accuracy is 77%


# Contents
1. Python Libraries
2. Understanding the dataset
3. Key- points
4. Model Architecture 
5. Training the model
6. Prediction

#  Python Libraries
Pandas

Torch

Torchvision

Matplotlib

Numpy

# Understanding the Dataset
The FER2013 challenge train.csv dataset was used.I split the train.csv into train data and test data as the challenge set didnot provide already split data.

# Key-points
Images were made black and white so as to reduce the number of parameters as color is not required to classify traffic signs. 
Histogram Equalizer was used to standardize lighting in all images.
ImageGenerator was used for data augmentation i.e. to produce the images at different angles and views thus strengthening our test data.

# Model Architecture
16 layers were used.

1.Convolution with 16 different filters in size of (3x3)
2. A batch Normalization Layer
3. Max Pooling by 2
4. Convolution with 64 different filters in size of (3x3)
5. Max Pooling by 2
6. Convolution with 128 different filters in size of (3x3)
7. A batch Normalization Layer
8.  Max Pooling by 2
9. Convolution with 256 different filters in size of (3x3)
10. Max Pooling by 2
11. Flattening the 3-D output of the last convolutional operations.
12. Fully Connected Layer with 128 units
13. A dropout layer
14. Fully Connected Layer with 84 units
15. A dropout layer
16. Fully Connected Layer with 7 units



# Training the model
I trained this model in an online cloud instance on Google Colab over 50 epochs.

# Prediction

The model achieved 60% accuracy.


![Model_loss](https://user-images.githubusercontent.com/55614154/122716854-6c57a300-d288-11eb-978e-d1d4fb67ae1b.png)


![Model_accuracy](https://user-images.githubusercontent.com/55614154/122716862-6eb9fd00-d288-11eb-9519-f1f56c004631.png)


