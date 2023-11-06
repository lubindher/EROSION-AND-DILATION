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

![1](https://github.com/aldrinlijo04/EROSION-AND-DILATION/assets/118544279/ca756c79-cb5a-4000-938f-1e549817cbed)



<br>

### Display the Eroded Image

![2](https://github.com/aldrinlijo04/EROSION-AND-DILATION/assets/118544279/132692b7-7913-484e-95b6-d188f0b9d9a5)



<br>

### Display the Dilated Image

![3](https://github.com/aldrinlijo04/EROSION-AND-DILATION/assets/118544279/cef1b604-6025-4b8c-9298-eeceebf68d0f)



<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
