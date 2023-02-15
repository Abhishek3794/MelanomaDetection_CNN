# Project Name
> ## Melanoma Detection using CNN



## Table of Contents
* [General Info](#general-information)
* [Problem Statement](#problem-statement)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)



## General Information
- ***Melanoma*** is a type of malignant skin cancer which if not detected early, can prove to be fatal.

- Melanoma accounts for almost 75% of skin cancer related deaths and hence, it is imperative that it be detected early to allow the time for proper treatment and recovery. Thus, a solution which can evaluate images and detect the presence of melanoma can be very helpful.

- The dataset used for building the multi-class classification model for achieving this were formed from the ***International Skin Imaging Collaboration (ISIC)*** and has ***2357*** images spanning across 9 skin cancer classes.



## Problem Statement
- ***Melanoma***, a type of skin cancer, accounts for almost 75% of skin cancer related deaths. Thus, it becomes essential to detect it early to prevent it from becoming fatal. This notebook aims to build a multi-class classification model (Convolutional Neural Network (CNN)) for the detection of Meanoma.



## Technologies Used
- ***Python*** - version ***3.x***
- ***pandas*** - version ***1.3.5***
- ***numpy*** - version ***1.21.6***
- ***matplotlib*** - version ***3.5.1***
- ***tensorflow*** - version ***2.11.0***
- ***keras*** - version ***2.11.0***



## Conclusions
- Three models were built and the results recorded.

- The first model has convolutional layers, pooling layers, a flatten layer and dense layers. The model was overfitting and hence, the second model was built taking this into consideration.

- The second model has convolutional layers, pooling layers, batch normalization layers, dropout layers, a flatten layer and dense layers. The dense layers are L2 regularized. Also, the images were transformed (rotation, zoom, translation and contrast) to make the model robust and generalise well on the important features. The overfitting reduced but was still not acceptable.

- The third model has convolutional layers, pooling layers, batch normalization layers, dropout layers, a flatten layer and dense layers. The dense layers for this model are L2 regularized as well. Class imbalance was handled in the data (using the augmentor module) before training the third model. That further reduced the margin of overfitting.

- As we can see, handling the class imbalance did help in reducing overfitting and as well as underfitting to some extent. The model can be further improved by using more training data (diverse and with very little class imbalance), different architectures (more CNN and pooling layers, different activation functions, different initializers), different hyperparameter value combinations for each hyperparameter, and training the model for more number of epochs. With all the mentioned steps, the accuracy of the model can be increased further and a well generalised model can be built for Melanoma detection. Also, the first two models were trained for 20 epochs each and the third one for 30 epochs - with a higher number of epochs the accuracy can be further improved. Last but not the least, transfer learning can be used to train a model for this specific task from a pre-existing trained model (either by changing the last few layers and keeping the weights of the initial layers unchanged or, by using the weights of the trained model as the starting point instead of random initialisation).
