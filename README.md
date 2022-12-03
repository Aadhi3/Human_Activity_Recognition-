# Human_Activity_Recognition-
Traits of LRCN over LSTM with Fast and optimum code  


Using youtube videos to train and test the Human Activity we'll check the best performing model other than LSTM in final to CNN+LSTM
Convolutional Neural Networks (CNN) are great for image data and Long-Short Term Memory (LSTM) networks are great when working with sequence data


Approach 1
----------
ConvLSTM recurrent layers are used to create the model:-
An LSTM network is specifically designed to work with a data sequence as it takes into consideration all of the previous inputs while generating an output
This approach is very well defined, takes in the number of filters and kernel size required for applying the convolutional operations softmax is used as optimizing layer

we got an average of 17s/epoch in the given model with an accuracy of nearly 70%

Approach 2
-----------
Implement the LRCN Approach:-

The CNN model can be used to extract spatial features from the frames in the video, and for this purpose, a pre-trained model can be used, that can be fine-tuned for the problem. And the LSTM model can then use the features extracted by CNN, to predict the action being performed in the

Long-term Recurrent Convolutional Network (LRCN)
which combines CNN and LSTM layers in a single model. The Convolutional layers are used for spatial feature extraction from the frames, and the extracted spatial features are fed to LSTM layer(s) at each time-steps for temporal sequence modeling.
network learns spatiotemporal features directly in an end-to-end training, resulting in a robust model

Conv2D layers will be then flattened using the Flatten layer and will be fed to a LSTM layer. The Dense layer with softmax activation will then use the output from the LSTM layer to predict the action being performed

Here obtained a super efficient model which took
1s/epoch with accuracy of 91%

