# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, "Hanshika", (5, 150), font, 3, (255), 5, cv2.LINE_AA)
cv2.imshow("Original", img)
cv2.waitKey(0)

# Create the structuring element
kernel_open = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
kernel_close = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))

# Use Opening operation
opened = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel_open)
cv2.imshow("Opening", opened)
cv2.waitKey(0)

# Use Closing Operation
closed = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel_close)
cv2.imshow("Closing", closed)
cv2.waitKey(0)

```
## Output:

### Display the input Image
<img width="537" height="266" alt="Screenshot 2025-11-17 105853" src="https://github.com/user-attachments/assets/dcc09e0f-59b1-45f7-bc76-ff9e2dcbbb15" />


### Display the result of Opening

<img width="537" height="266" alt="Screenshot 2025-11-17 105853" src="https://github.com/user-attachments/assets/3265437e-3f8f-4e45-956a-414465e442a4" />

### Display the result of Closing
<img width="541" height="266" alt="Screenshot 2025-11-17 105959" src="https://github.com/user-attachments/assets/f3b4d629-0109-4ec6-98d4-067d567d4fe0" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
