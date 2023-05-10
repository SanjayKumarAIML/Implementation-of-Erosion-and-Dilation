# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Erode and Dilate the image.

### Step 5:
End Program.
 
## Program:

``` Python
# Developed By   : Sanjay Kumar S S
# Register Number: 212221240048


# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1 = np.zeros((100,225), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Sanjay',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')


# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
cv2.erode(img1, kernel)


# Erode the image
image_erode1 = cv2.erode(img1,kernel)
plt.imshow(image_erode1, 'gray')


# Dilate the image
image_dilate1 = cv2.dilate(img1, kernel)
plt.imshow(image_dilate1, 'gray')
```
## Output:

### Display the input Image:
<br>
<img src='https://github.com/SanjayKumarAIML/Implementation-of-Erosion-and-Dilation/assets/93427246/e1c4233f-5acc-4b14-82fc-98691aca55b2'>
<br>


### Display the Eroded Image:

<br>
<img src='https://github.com/SanjayKumarAIML/Implementation-of-Erosion-and-Dilation/assets/93427246/332e7139-1c7c-4091-8ebe-527bdc9de90e'>
<br>


### Display the Dilated Image:

<br>
<img src='https://github.com/SanjayKumarAIML/Implementation-of-Erosion-and-Dilation/assets/93427246/26c47d11-1c19-4d04-bc2a-9595f61e4911'>
<br>


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
