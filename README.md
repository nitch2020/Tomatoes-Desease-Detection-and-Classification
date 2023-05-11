# DESCRIPTION OF THE SOLUTION
# Dataset description
Our dataset comes from plantvillage which is a research and development unit of Penn State University. This dataset consists of 14530 images of tomato leaves divided into ten classes including nine classes of leaves with different diseases and one class of healthy leaves.
# Methodology
In order to have an optimal result at the end of the project, we decided to use two approaches, one based on transfer learning and the other based on a sequential model developed by ourselves. For the transfer learning-based approach, we decided to use the pre-trained InceptionV3 model.
InceptionV3 is an extended network from the popular GoogLeNet that has achieved good classification performance in several biomedical applications using transfer learning.
For the sequential model, we split our dataset into 80% for the data training, 10% for test data and 10% for validation. For the model based on learning transfer, we split 80% for training and 20% for testing.

# Dataset preprocessing
# Preprocessing for the transfer learning based model with InceptionV3
The most important feature here is the size of the images at the input of the model. We set a size of 299 x 299 pixels for the set training pictures. We have labeled the different classes thanks to the predefined methods available in keras. We have also used some techniques to augment our dataset
such as rotation, zoom, horizontal translation and change of scale.
# Preprocessing for the sequential model
The treatment is almost the same than the previous model with the only difference that we have
normalized the size of the images here to 200 x 200 pixels.
# Results 
# The sequential model
The evaluation of this model on the test data gave us an accuracy of 96.82%. with Loss of 0.10.
# Model with InceptionV3
In the first approach we performed the training only on a fully connected layer that we added to the model output, for this reason, the number of parameters updated during training was very little. For this reason, this approach performed poorly with an accuracy of 49.77% and a loss of 1.50.

In the second approach, we performed the training on all the layers of the InceptionV3 model as well as on the output layer completely connected that we have added. We have obtained better results with an accuracy of 97.22% and a Loss of 0.08.
