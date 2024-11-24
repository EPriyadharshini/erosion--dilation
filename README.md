# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary pacakages

## Step2:
Create the text using cv2.putText

## Step3:
Create the structuring element

## Step4:
Erode the image

## Step5:
Dilate the Image
 
## Program:

### NAME : Priyadharshini E 
### REF_NO : 212223230159

```

import cv2
import numpy as np
import matplotlib.pyplot as plt# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'priya', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```

## Output:

### Display the input Image


![image](https://github.com/user-attachments/assets/f6d7c2c1-4bac-4286-873c-7b53f902e352)

### Display the Eroded Image


![image](https://github.com/user-attachments/assets/852ce064-cdc6-4354-8842-096882125e4c)

### Display the Dilated Image


![image](https://github.com/user-attachments/assets/492dc2e7-d65b-433f-9cb3-e8cf7a13b171)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
