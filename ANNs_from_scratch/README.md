# Impelementing Artificial Neural Networks from Scartch

in this project I implement Fully Connected Neural Networks from Scratch for 3 diffrent tasks:
- Regression (for age estimation)
- multi-label classification (for race prediction)
- Logistic Regrresion (for prediction gentder)

In addition to implementing the backpropagation featureو the implemented network has the ability of adding layers and multiple activation functions like ReLU, Softmax and different loss functions like MSE, negative log likelihood.
The implementations have been done with the help of the ["Neural Networks from Scratch"](https://nnfs.io/) book

## Dataset
I used [UTKFace dataset](https://susanqq.github.io/UTKFace) for training and evaluation of Network for the tasks mentioned above. Normalization and Dimensionality Reduction have been applied to the data to prepare the data for training.


## Results

### Regression
The task of Regression is done to predict age of each face photo in dataset. The Implemented Network achoeve a MSE of 11,19 after training.

### multi-label classification
This task is implemented to prdeict the race of each photo of dataset. after training the network, the model got an accuracy of 50,6% for test data.


### Logistic Regrresion
For the task of predicting gender of images of this dataset we have to do a logistic regression task. For this purpose we needed to implement sigmoid activation function and logistic loss function.
after implementations and training network, the network reach to 68,08% accuracy for test data.


