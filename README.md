# Histogram-of-Oriented-Gradients
Histogram of oriented gradients (HOG) is a feature descriptor used in computer vision and image processing for the purpose of object detection. The technique counts occurrences of gradient orientation in localized portions of an image. However, we can also use HOG descriptors for quantifying and representing both shape and texture.
## What is a Feature Descriptor ?
A feature descriptor is a representation of an image or an image patch that simplifies the image by extracting useful information and throwing away irrelevant information.
Typically, a feature descriptor converts an image of size width x height x 3 (channels ) to a feature vector / array of length n.

What is “useful” and what is “irrelevant” ? To define “useful”, we need to know that the informations (i.e features) are not useful for the purpose of viewing the image. But, are useful for tasks like image recognition and object detection. The features produced by this algorithm when fed into an image classification algorithms like Support Vector Machine (SVM) produce good results.
But, what kinds of “features” are useful for classification tasks ? 
### Let’s use an illustration. 
1. Suppose we want to build an object detector that detects buttons of shirts and coats. A button is circular ( may look elliptical in an image ) and usually has a few holes for sewing. You can run an edge detector on the image of a button, and easily tell if it is a button by simply looking at the edge image alone. In this case, edge information is “useful” and color information is not.
2. The images below shows how HOG extracted useful features (edges) and throw away the irrelevant feature (color etc.)
![EDGES OF CAR LOGOS PRODUCED FROM HOG](https://i.imgur.com/ZkkoBpK.jpg)
<fig>Figure 1: EDGES OF CAR LOGOS PRODUCED FROM HOG.</fig>
