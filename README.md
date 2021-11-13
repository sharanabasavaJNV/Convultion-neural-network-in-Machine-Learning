# Convultion-neural-network-in-Machine-Learning
The proposed idea is to create an autonomous system which segregates the waste. 
The system segregates the waste using CNN algorithm in ML. 
The algorithm detects and classifies the waste according to data set provided to CNN. 
The algorithm accordingly classifies the waste as organic and recyclable.

**process**
First of all, we collect image data set from Kaggle website. Then dataset will be sent to training, where it goes under several processes through several layers.
After sending into training set, image will be pixelated. Where whole image will be shared as patch/pixel ranging from 0-255 value (Since RGB value ranges from 0-255). Then image will go through 3 layers such as **Conv2D**, **max pooling**, fixed layer.
Layers 


**i. Conv2D**
after pixelating the images, the image will be an input for conv 2D layer, in conv2D layer image will  undergo some filter such as weights, parameters no of filters, and axis that convolutes the input image. If the image value is zero, then there is no image (explain filtering)

**Padding **
After applying filters in result, we can see that we are losing 2/2 pixels 
So, to avoid loss of information we will add some strides to the original image 
After strides to original image again we apply filter, now we can see result, we got 6/6-pixel image information which is original images pixel.

**ii. Max pooling**
in this layer mainly 2 things will happen 
a)	It reduces the no of parameters or pixels with in the model
b)	It generalizes the result from a CNN layer, and again sent to CNN layer 
c)	In this we will extract sharp edges of the image as well as characteristic features from image set

**_RELU_** 
After extracting we will not be sure about image, which section it belongs to 
So Relu comes to act 
RELU is nothing but Rectified linear unit which brings non-linearity.
If I am holding this pen, now I captured its image and named it as pen. Now I am looking this pen in different angle but still I am able to recognize that this is pen. 
It sets an image with angle say from centre or by width, height shift or horizontal shift. So, like this image is treated and then it is sent to next flatten 
Flatten 
Flatten is a layer where each neuron is connected to one another.
In this layer all the neurons which are in 3D are converted to 1D neurons 

**iii. Fully-connected layer**
Before going to this layer, I would like to explain what is meant by _**Drop out and overfitting_** 
_Drop out_ is nothing but releasing some unwanted neurons from image set.

**How it is released and why**? 
If an image set is complex which is nothing but overfitting to avoid over fitting system releases neurons for easy classifications
This is the last layer where image will go through process.
In this layer it takes the output image of an output max pooling layer and then determines according to its layer, which is nothing but categorical cross-entropy.
So finally, we will be able to separate the waste into section/category with the help if machine learning.

_What are the pros?_
No money is spent on expensive sensors 
We will be able to avoid disease caused by hand picking waste 
_What are cons?_
System be accurate up to 88% if image has complex features 


