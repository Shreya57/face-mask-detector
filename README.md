# Face Mask Detection and Alert System
## About

We all know how the year 2020 brought an alarming pandemic and we, as citizens should follow steps to prevent the increase of COVID-19 cases. The least we could do is to wear a mask at all public places. 

This project proposes one of the methods to ensure that each person coming under any CCTV surveillance wears a mask. This system uses LLE algorithm for face detection and convolutional neural network (CNNs) to reconfigure the image to fit into the network. The neural network is trained with the help of an image dataset. The method attains training accuracy and validation accuracy up to 99.87% and 93.41% respectively on two different datasets. If a person without a mask is detected, an alarm goes off and it continues until the person wears a mask.

## Motivation

The spread of this deadly virus can be stopped if proper precautions are taken, wearing a mask being one of them. But sadly, many people are not wearing masks in public places which increases the need for monitoring.

## Objective

The system will be deployed using a CCTV camera. The camera will capture real live footage of public areas from which facial images are extracted and these images are used to identify the mask on the face. The Convolutional Neural Network (CNN) learning algorithm is used for feature extraction from the images then these features are learned by multiple hidden layers. Whenever a person without mask is detected, the alarm goes off.

## Proposed System

The parts of the system are described as follows:

- **Data collection and pre-processing**: 
This project uses Prajna Bhandary’s dataset for training and testing the model. The dataset contains 690 images of people with masks and 686 images of people without masks. 75% of the images were used for training the model and the remaining were reserved for testing.
The data pre-processing step involved converting all images to grayscale and resizing them to 56x56 for consistency. One hot encoding was then performed, and the data was split into the training and testing set.

- **Building the CNN classification model**:
A CNN model was built using the sequential API. The network consists of an input layer, multiple hidden layers, and an output layer. The architecture contains two groups of convolution layers followed by an activation and max pooling layer. This results in a simplified network. A flatten and dropout layer reshapes the information and prevents the network from overfitting. Finally, a dense layer distinguishes the classes.

- **Mask detection and alarm**: 
The main goal of the system is to make sure that no person enters a public place without wearing a mask. This model identifies such people and starts ringing an alarm. The alarm works as a denial for the person, and it continues until (s)he wears a mask.

## Conclusion

The proposed system will act as a valuable tool to monitor whether a person is wearing a mask or not. This will lessen the manual work and restrict the entry of people not wearing masks in public areas. The system will generate alerts to ensure that all people wear mask properly. The accuracy of the model is 93.41% which will be helpful to fulfil the motive of the system, i.e., to reduce the spread of coronavirus.
