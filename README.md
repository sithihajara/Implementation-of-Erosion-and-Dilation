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
```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,560),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"SITHI HAJARA I ",(5,70),font,2,(255),5,cv2.LINE_AA)
# cv2.imshow("nameimg",text_image)
# cv2.waitKey(0)
# cv2.destroyAllWindows()
plt.title("Original Image")
plt.imshow(text_image,'RdGy_r')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'RdGy_r')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'RdGy_r')
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/sithihajara/Implementation-of-Erosion-and-Dilation/assets/94219582/4430504f-7c2f-41f8-890d-6e119a922eca)
### Display the Eroded Image
![image](https://github.com/sithihajara/Implementation-of-Erosion-and-Dilation/assets/94219582/6e86a5d5-edad-4120-97d4-8e833404d052)
### Display the Dilated Image
![image](https://github.com/sithihajara/Implementation-of-Erosion-and-Dilation/assets/94219582/bce7cc28-2bf2-4880-8669-c104e083b222)
## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
