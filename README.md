# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:
Create a black image of size 100x600 pixels.

### Step-2:
Use a specified font to write the word "Lifestyle" on the image at a defined position.

### Step-3:
Show the image containing the text without axis labels.

### Step-4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

### Step-5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.

### Step-6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.
 
## Program:

``` Python

import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'LOGU R' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output:

### Display the input Image
<br>
<img width="407" height="124" alt="image" src="https://github.com/user-attachments/assets/097fe687-33d9-432e-bcaf-7521f5ec259c" />

<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>
<img width="413" height="128" alt="image" src="https://github.com/user-attachments/assets/7178004d-8f91-458f-bbb3-3dca3ba96ca8" />

<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>
<img width="402" height="126" alt="image" src="https://github.com/user-attachments/assets/9c62e684-0c83-41df-b6dd-40fed84f986c" />

<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
