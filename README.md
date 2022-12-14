# Gesture-Recognition-with-3D-CNN-and-CNN-RNN

Gesture Recognition as the name suggests, we had to categorize the gestured provided to the camera. We considered 5 types of gestures in this viz. Thumbs up, thumbs down, swipe left, swipe right, and stop gesture (when use shows his/her palm). The data provided to us was in the form of sequential images in a separate folder and the name of the folder contained gesture type (class label). A CSV file was there which had folder name and gesture type. So the data was not exactly video but a sequence of images (frames).

We built a custom data generator for the data feeding purpose of the model. As this dataset was huge in size we had to build a data generator that would feed the data to the model in steps. Various preprocessing operations were involved in the data generator as you will see in the notebook below. Also, we considered alternate frames of the video so that memory utilization would be less. Image sizes have been resized so that all the images(frames) will be of the same size. 

Now comes the model-building part. We have build 2 types of models basically,
1. 3D CNN model
2. CNN + RNN stacked model

Model iterations are performed by altering hyperparameters and performance is compared for both the models and the best model is selected. 

For 3D CNN models, the procedure the straight forward but for CNN + RNN stacked models, it is somewhat tricky. Firstly we have used transfer learning for the CNN layers. We used ResNet50 and ResNet50V2 pre-trained models for transfer learning followed by RNN models like LSTM/GRU. It is advised to use GRU (Gated Recurrent Unit) as it has fewer parameters than LSTM (Long Short Term Memory) and similar accuracy. So we have proceeded with GRU.


