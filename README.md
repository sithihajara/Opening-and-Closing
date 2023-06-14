# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

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
Use Opening operation.
### Step5:
Use Closing Operation.
### Step 6:
Print the output and end the program.

## Program:

```
DEVELOPED BY : SITHI HAJARA I
REGISTER NO : 212221230102
```
```
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"HAJARA I",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/sithihajara/Opening-and-Closing/assets/94219582/25e31490-14ba-4126-a124-5e6f6f65a97b)

### Display the result of Opening
![image](https://github.com/sithihajara/Opening-and-Closing/assets/94219582/be6429a0-b0c6-479e-9d71-b211976f3278)
### Display the result of Closing
![image](https://github.com/sithihajara/Opening-and-Closing/assets/94219582/94bae4b3-48cd-4c87-9965-d17f799a2606)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
