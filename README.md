# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode and Dilate the image.

### Step5:
End Program.
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the Text using cv2.putText
cv2.putText(img1,' LISHA ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')

```
## Output:

### Display the input Image
![Capture1](https://user-images.githubusercontent.com/75237886/171336135-c5b76be8-4c71-486b-9a62-3edf829e3554.PNG)

### Display the Eroded Image
![Capture2](https://user-images.githubusercontent.com/75237886/171336194-8324aadc-ae49-4cf9-b343-ef31b444c8e0.PNG)


### Display the Dilated Image
![Capture3](https://user-images.githubusercontent.com/75237886/171336203-f75f023e-fac1-465f-b8e9-e718113747c0.PNG)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
