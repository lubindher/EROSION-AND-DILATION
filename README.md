# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).
<br>


### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.
<br>

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.
<br>

### Step4:
Display the eroded image using cv2.imshow.
<br>

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
<br>

 
## Program:
```
DEVELOPED BY: Lubindher S
REG NO: 212222240056
```
```python
# Import the necessary packages


import cv2
import numpy as np



# Create the Text using cv2.putText

img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"ALDRIN LIJO J E",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image

cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("ALDRIN LIJO J E",image_erode)
cv2.waitKey(0)



# Dilate the image

image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("ALDRIN LIJO J E",image_dilatel)
cv2.waitKey(0)



```
## Output:

### Display the input Image


![Screenshot 2023-11-06 204106](https://github.com/lubindher/EROSION-AND-DILATION/assets/119559904/034ae193-0ed4-4328-8fde-f1a2efb3f0cf)


<br>

### Display the Eroded Image


![Screenshot 2023-11-06 204145](https://github.com/lubindher/EROSION-AND-DILATION/assets/119559904/e7ac3c90-c2d1-46fe-8bd4-45872ca8f4c3)


<br>

### Display the Dilated Image

![Screenshot 2023-11-06 204106](https://github.com/lubindher/EROSION-AND-DILATION/assets/119559904/fa91b01c-0e58-4c33-98b8-34fd76abc4cd)



<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
