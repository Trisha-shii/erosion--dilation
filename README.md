# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step1:
Initialize a blank image and add text to it using cv2.putText().

Step2:
Create a kernel (structuring element) using np.ones() which defines the size and shape for erosion and dilation.

Step3:
Use cv2.erode() to shrink or thin out the white areas (text) of the image.

Step4:
Use cv2.dilate() to expand or thicken the white areas (text) of the image.

Step5:
Show the original, eroded, and dilated images (using cv2.imshow() or save them with cv2.imwrite()).
 
## Program:
TRISHA PRIYADARSHNI PARIDA
212224230293

``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'Trisha G' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))


# Dilate & Erode the image
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
![Screenshot 2025-05-06 094848](https://github.com/user-attachments/assets/79b1c82d-a690-4fa6-9f8b-4967717304e9)


### Display the Eroded Image
![Screenshot 2025-05-06 094900](https://github.com/user-attachments/assets/4d5e714d-453e-4948-909c-7befdfa9c5ca)


### Display the Dilated Image
![Screenshot 2025-05-06 094852](https://github.com/user-attachments/assets/6a22862c-a30d-47df-8161-1e6b6cae783b)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
