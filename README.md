# Microsoft-AI-Challenge-2018-Week-3

Aim of this challenge was to find a cartoon character (refered as Waldo) from bunch of other cartoon characters given in challenge images. Participents were free to use any of the available techniques to find out the location of character in image.


![alt text](https://github.com/nkjadhav/Microsoft-AI-Challenge-2018-Week-3/blob/master/Announcement%20LinkedIn%20Winner.png = 640x380)

      

## To solve this challenge, I tried in three different approaches.

### Approach 1: Face API – Facial Recognition Software | Microsoft Azure
__Reference Link__ - https://azure.microsoft.com/en-in/services/cognitive-services/face/

__Reason__ - The Azure Face API is a cognitive service that provides algorithms for detecting, recognizing, and analyzing human faces in images. This approach was not suitable for this challenge as the face image which was meant to be detected was at very low resolution.

__Lesson learnt__ – I tried Face API and could detect faces from normal resolution images and it worked. But, Azure Face API is well suited for cases where image resolution is good enough to identify face. 


### Approach 2: Tensorflow Object Detection API
__Reference Link__ - https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md

__Reason__ - Deep learning provides yet another way to solve such problem. But unlike traditional image processing computer vision methods, it works using only a handful of labelled examples that include the location of object in an image.

__Lesson learnt__ - I was able to detect object in first image of competition but was unable to locate object in other images as it was not trained for new images. Considering target image resize/crop will disturb the trained model and inclusion of new test image may need retraining of model to accommodate it. Hence, this approach was kept aside. Also, little bit complex.


### Approach 3: NumPy and OpenCV
__Reference Link__ - https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_imgproc/py_template_matching/py_template_matching.html

__Reason__ – Simple approach and easy to setup experimentation. Requires NumPy and OpenCV. No need to train/retrain model, kind of brute force search.

__Lesson Learnt__ - Template matching using Python and OpenCV is actually quite simple. To start, one just need two images — an image of the object which we want to match and an image that contains the object. Then we just need to make calls to cv2.matchTemplate and cv2.minMaxLaoc.
