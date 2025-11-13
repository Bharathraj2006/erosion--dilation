# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = np.zeros((600, 600))
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ABCD', (100,300), font,5, (255, 255, 255), 25, cv2.LINE_AA)


plt.imshow(img, cmap='gray')
plt.axis('off')
plt.show()

kernel = np.ones((5,5),np.uint8)
kernel

erosion = cv2.erode(img,kernel,iterations=4)
plt.imshow(erosion, cmap='gray')
plt.axis('off')
plt.show()

dilution = cv2.dilate(img,kernel,iterations=4)
plt.imshow(dilution, cmap='gray')
plt.axis('off')

```
## Output:

### Display the input Image
![alt text](output/input.png)

### Display the Eroded Image
![alt text](output/erosion.png)

### Display the Dilated Image
![alt text](output/dilution.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
