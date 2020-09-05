# **Traffic Light Classfier**

## Computer Vision to build a Traffic Light Classifier

### Using openCV techniques for computer vision

---

**Traffic Light Classifer Project**

The goals / steps of this project are the following:

* Use knowledge of computer vision techniques to build a classifier for images of traffic lights:
  - Greater than 90% accuracy
  - Never classify red lights as green
 
* Dataset of traffic light images in which one of three lights is illuminated: red, yellow, or green
  - All images come from this [MIT self-driving car course](https://deeplearning.mit.edu/) and are licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

* 1. Loading and visualizing the data.
* 2. Pre-processing.
* 3. Feature extraction.
* 4. Classification and visualizing error.
* 5. Evaluate the model.


[//]: # (Image References)

[image1]: ./Result_Images/1.png "1"
[image2]: ./Result_Images/2.png "2"
[image3]: ./Result_Images/3.png "3"
[image4]: ./Result_Images/4.png "4"
[image4]: ./Result_Images/5.png "5"

### README

- The implementation of the traffic light classifier can be found in [project code](./Traffic_Light_Classifer.ipynb). 

- The classifier gave an accuracy of *92.92%* and *never* classify red lights as green.

- An example of the process:

![alt text][image5]

### Steps used to build traffic sign classifier.

#### 1. Loading and Visualizing the Traffic Light Dataset

* This traffic light dataset consists of 1484 number of color images in 3 categories - red, yellow, and green:

  - 904 red traffic light images
  - 536 green traffic light images
  - 44 yellow traffic light images

* All 1484 of the traffic light images are separated into training and testing datasets.

  - 80% of these images are training images, to create a classifier.
  - 20% are test images, which will be used to test the accuracy of the classifier.

Example of data:
![alt text][image1]
![alt text][image2]

#### 2. Pre-process the Data

* Input 
  - same format, of the same size, and so on.

* Output
  - one-hot encoded labels: 
   - red light label: [1, 0, 0]
   - yellow light label: [0, 1, 0]
   - green light label: [0, 0, 1]

* Standardize the input images
  - Resize each image to the desired input size: 32x32px

![alt text][image3]

#### 3. Feature Extraction

* Created a brightness feature that uses HSV color space

![alt text][image4]

* Created few more features such as red masking, cropping, etc.

#### 4. Classification and Visualizing Error

* Using training images from [here](./traffic_light_images/training)
* Using all the features, function that takes in an RGB image and, using extracted features, outputs whether a light is red, green or yellow as a one-hot encoded label.
 

#### 5. Testing the Classifier

* Using test images from [here](./traffic_light_images/test)
* above 90% classification accuracy.
* never classify a red light as a green light.


