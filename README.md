# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step 2:
Create the Text using cv2.putText

### Step 3:
Create the structuring element

### Step 4:
Use Opening operation

### Step 5:
Use Closing Operation

### Step 6:
end the program.
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
img1=np.zeros((70,300),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,' Pallavi ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)
# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))
# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)
# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)
```
## Output:

### Display the input Image
![output](https://github.com/Pallavi-Raveendranadreddy/Opening-and-Closing/blob/a36578860831aaa648ec5e8dfe2c04dd954c3c8d/11a.PNG)
### Display the result of Opening
![output](https://github.com/Pallavi-Raveendranadreddy/Opening-and-Closing/blob/41389e02cb56964d67aad534382246de0decfd4b/11b.PNG)
### Display the result of Closing
![output](https://github.com/Pallavi-Raveendranadreddy/Opening-and-Closing/blob/1c1a8b858f368f3839899c9a0597af49cc8ee0cb/11c.PNG)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
