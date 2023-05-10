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
End the Program.
 
## Program:

```
Developed by : Sithi Hajara I
Register number :212221230102
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img1 = np.zeros((100,230), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'anusha',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image_erode1=cv2.erode(img1, kernel)
plt.imshow(image_erode1, 'gray')
```

# Erode the image
```
image_erode1=cv2.erode(img1, kernel)
plt.imshow(image_erode1, 'gray')
```

# Dilate the image
```
image_dilate1 = cv2.dilate(img1, kernel)
plt.imshow(image_dilate1, 'gray')

```
## Output:

### Display the input Image
![image](https://github.com/sithihajara/Implementation-of-Erosion-and-Dilation/assets/94219582/a8a2927d-cd9d-434c-b3e1-6f99d3c792f6)

### Display the Eroded Image
![Screenshot 2023-05-11 002434](https://github.com/sithihajara/Implementation-of-Erosion-and-Dilation/assets/94219582/9e6c5d6b-807f-43f8-bdd4-8ffa38913984)

### Display the Dilated Image
![image](https://github.com/sithihajara/Implementation-of-Erosion-and-Dilation/assets/94219582/0f4fdd29-ce7a-4b2f-be51-0c1787d29916)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
