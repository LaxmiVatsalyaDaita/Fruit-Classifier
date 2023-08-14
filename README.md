# Fruit-Classifier

# INTRODUCTION

India is an agriculture country. Different types of fruits and vegetables are produced where all the pre-harvest and post-harvest processes are done manually with the help of labor. Separating fruits of lower quality from fresh fruits manually can become a tedious task when done on a larger scale. It takes a lot of man-power to segregate the fruits into batches based on quality  before they can be packaged and shipped. One of the most common ways in which segregation is done is by identifying spots on the fruit. Most of the fruits have a tendency to develop brown (or) black spots on the surface as a result of rotting from the inside. Our project aims at developing a model that can classify a fruit and label it as defective, on the identification of any spots on its surface using a machine learning approach. This reduces the need for human interference in the process.

DESIGN
PROPOSED MODEL

  
The project consists of 3 stages. In the first stage, a deep learning model is designed and is trained and tested on the static dataset consisting of 8120 images of both good and bad quality of fruits of the type Apple, Banana and Guava. In the second stage, an image of the fruit is captured by the Raspberry Pi camera connected to the Raspberry Pi Zero 2 W and is uploaded to the google drive. In the final stage, the uploaded image is taken as input to the deep learning model and the output class is predicted.

 

The dataset used is the FruitNet dataset consisting of 6 types of fruits (apple, Banana, Guava, Lime, Pomegranate and Orange) and 3 quality types per fruit (good, mixed, bad).
 
The pre-processing of the data is carried out in two stages.
1)	Data Augmentation: The dataset was highly imbalanced and had to be balanced to avoid overfitting or underfitting of the model. 
2)	Image-processing: The images are first converted from BGR to Gray scale and then sharpened using a kernel ( [  [0,-1,0] , [0,4,0] , [0,-1,0] ] ) before the images are fed into the neural network. This is done to identify the black/brown spots in the bad quality fruits.  
 


The deep learning model used for the problem is a Convolution Neural Network with 3 convolution layers, 2 pooling layers and 1 dropout layer.  The dataset has been split as 80% training data and 20% testing data.
  
The model achieved an accuracy of 94% after training for 10 epochs. 

RESULTS

VISUALIZATION OF THE BALANCED DATASET:
  

CLASSIFICATION REPORT:
 
 CONFUSION MATRIX:

 







Testing the model with image:
  
Testing the model with image taken by Pi Camera:
 

FUTURE SCOPE

•	A setup that can revolve the camera to capture the images of the fruit from all direction to provide better results. 
•	The use of a bounding box that can detect individual fruits in an image of multiple fruits and classify them individually.
•	 Automatic segregation of fruits with the help of actuators and motors.

REFERENCES

•	FruitNet: Indian fruits image dataset with quality for machine learning applications (By Vishal Meshram , Kailas Patil Vishwakarma University, India)
•	Automatic Fruit Quality Inspection System (By Manali R. Satpute, Sumati M. Jagadle)
•	A Real-Time Smart Fruit Quality Grading System Classifying by External Appearance and Internal Flavor Factors (By Han Suk Choi, Je Bong Cho, Sang Gyun Kim, Hong Seok Choi)
•	Real-time visual inspection system for grading fruits using computer vision and deep learning techniques, Information Processing in Agriculture (By N. Ismail and O. A. Malik)

APPENDIX

Components:
1.	Raspberry Pi Zero 2 W
2.	Pi Camera 5MP
3.	Pi Cable
4.	SD Card 8GB (for loading the raspberry pi OS)
Software:
1.	Google Colab
2.	PuTTY
3.	VNC Viewer
