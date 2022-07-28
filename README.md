# Traffic-Signs-Classification [![](https://camo.githubusercontent.com/2fb0723ef80f8d87a51218680e209c66f213edf8/68747470733a2f2f666f7274686562616467652e636f6d2f696d616765732f6261646765732f6d6164652d776974682d707974686f6e2e737667)](https://python.org)

Traffic Sign Classification is employed to detect and classify traffic signs to inform and warn a driver beforehand to avoid violation of rules. There are certain disadvantages of the existing systems, used for classification, like incorrect predictions, hardware cost and maintenance, which are to a great extent resolved by the proposed system. The proposed approach implements a traffic signs classification algorithm employing a convolutional neural network.

## View my deployed Model on Streamlit using Streamlit Sharing
Click here to see the deplyed model: 
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://tanu-shree-31-traffic-signs-classification-streamlit-app-cxrykd.streamlitapp.com/)

## Snapshot of the result:
![image](https://user-images.githubusercontent.com/69342524/181501087-cd4a1bdc-b378-4592-a84f-767d5f0db182.png)
![image](https://user-images.githubusercontent.com/69342524/181501151-9c02c63b-5bc6-4762-a386-f18fce3442ca.png)


The purpose of this project is to train and test an implementation of the Convolutional Neural Network for a classification task. The model will be used in an application, where the user can upload a photo of a traffic sign and get the prediction of its class.

## DATASET
The dataset was taken from The German Traffic Sign Recognition Benchmark (GTSRB) and was presented first-time at the single-image classification challenge at the International Joint Conference on Neural Networks (IJCNN) 2011. It was created from about 10 hours of video recorded while driving on different roads in Germany during the daytime. The Data consists of about 40.000 real colorful photos of traffic signs. 

## BUILDING THE MODEL

![image](https://user-images.githubusercontent.com/69342524/181505299-8a11cf1b-3e59-4513-82fb-9b0aad687569.png)

Initially, the CNN model architecture is built. The following steps are followed :
1. Sequentially add the layers in the order: two convolutional layers, one pooling layer, dropout layer, again two convolutional layers, one pooling layer, dropout layer, flattening layer, dense layer, again a dropout layer and finally the dense layer.

2. In the convolutional layer, number of filters is specified. It performs the convolution operation on the original image and generates a feature map.

3. The ReLU performs the maximum function to convert the negative values to zero without changing the positive ones and generate a rectified feature map. 

4. The Pooling layer takes the rectified feature map and performs a down-sampling operation (like Max Pooling or average pooling) and thus reduces the dimensionality of the image.

5. The flattening layer is used to convert the input feature map to a 1-dimensional array.

6. The dropout layer is used to avoid over fitting by setting some of the input neurons to 0 during the training process. The dense layer, on the other hand, feeds all the outputs from the preceding layer to all its neurons and perform the matrix- vector multiplication (the row vector of the output from the preceding layer should be equal to the column vector of the dense layer), to generate a m-dimensional vector.

7. After addition of the layers, the model is to be compiled (final step in the creation of model to define the loss function and apply optimization techniques) and assign the loss function as “categorical_crossentropy” and use the “Adam optimizer”. The reason for specifying this loss function is that the proposed system is a multiclass classification problem, where multiple classes are considered but one image belongs to exactly one class.

8. Next, the model is trained using the training dataset, by passing the pre-processed images from the training dataset.

9. Finally, the predictions on the test data are done using the trained model and the traffic sign name along with the class Id is shown as an output.

![image](https://user-images.githubusercontent.com/69342524/181504317-1f8a1ccc-16ec-4d60-a209-8e7f335a1e79.png)  ![image](https://user-images.githubusercontent.com/69342524/181505723-6ca3a10b-f062-48c8-8320-52763ae252ac.png)

## LIBRARIES USED
<img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/0815ce7a7b769f0316037a76cc866d7239ed2ab1/Numpy.PNG" width="200"> <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/0815ce7a7b769f0316037a76cc866d7239ed2ab1/Pandas.PNG" width="200"> <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/0815ce7a7b769f0316037a76cc866d7239ed2ab1/Jupyter%20notebook.PNG" width="200">   <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/16b327faf7a88b9a93fcfe5c167d482baa4b0702/Matplotlib.PNG" width="200">  <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/16b327faf7a88b9a93fcfe5c167d482baa4b0702/Sklearn.PNG" width="200"> <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/16b327faf7a88b9a93fcfe5c167d482baa4b0702/Visual%20studio.PNG" width="200"> <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/16b327faf7a88b9a93fcfe5c167d482baa4b0702/Streamlit.PNG" width="200">  <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/main/keras.png" width="200">  <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/main/pillow.png" width="200">  <img target="_blank" src="https://github.com/Tanu-Shree-31/Technology/blob/main/tensorflow-ar21.png" width="200"> 

## RESULT:
![image](https://user-images.githubusercontent.com/69342524/181503724-d6e7c1f1-601c-4920-bc67-c0e8e9e17a24.png)

Epochs: 20
Therefore, Obtained an accuracy of 94.86% on the testing data.

##FUTURE SCOPE:
Can be used to detect the traffic signals in live and the environmental constraints including lighting, shadow , distance (sign is quite far), air pollution, weather conditions in addition to motion blur, and vehicle vibration which are common in any real time system may affect the detection and thus the classification. Hence, there is a need for further research and advancements to deal with these issues. Also, there are certain traffic signs that may not be predicted accurately. For this, augmentation and one hot encoding techniques can be used. Augmentation involves shifting of the image, zoom in and rotate the images (if required).

## Connect with me! 🌐
Known on internet as **Tanushree Shetty**


[<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/linkedin.png" title="LinkedIn">](https://www.linkedin.com/in/tanushree-b-s-9153951b1/)   [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/github.png" title="Github">](https://github.com/Tanu-Shree-31)   [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/telegram-app.png" title="Telegram"/>](https://web.telegram.org/z/)   [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/instagram-new.png" title="Instagram">](https://www.instagram.com/lltanu.shettyll/)

## Email Me :e-mail:

[<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/secured-letter.png" title="Mail me">](mailto:bstanushree@gmail.com)


PS: Please do not forget to drop a star if you like it !!
