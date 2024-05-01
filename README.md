# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
```
DEVELOPED BY : PULI NAGA NEERAJ
REFERENCE NO : 212223240130
```
### Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'NEERAJ',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
### Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
### Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
### Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image

![image](https://github.com/PuliNagaNeeraj/erosion--dilation/assets/138849173/de881335-8714-4faa-8d3f-13c8e3aa2912)

### Display the Eroded Image

![image](https://github.com/PuliNagaNeeraj/erosion--dilation/assets/138849173/1a5827d3-5242-4c41-aa3f-76c708a61ffd)

### Display the Dilated Image

![image](https://github.com/PuliNagaNeeraj/erosion--dilation/assets/138849173/ad4e822d-5155-4eb6-9764-5090aa162718)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
