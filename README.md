# EDGE-DETECTION
### Name : SAI HRISHI M
### Reg No : 212224240140
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r'C:\Users\admin\Desktop\DIPT\DIPT SAI IMG.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
### ORIGINAL IMAGE
<img width="340" height="462" alt="image" src="https://github.com/user-attachments/assets/7f6c92b6-7cf7-48a0-836b-c6fbea3d14fa" />

### SOBEL EDGE DETECTOR

<img width="337" height="461" alt="image" src="https://github.com/user-attachments/assets/1b262958-e488-4c7a-9e26-41c19703bb52" />

### LAPLACIAN EDGE DETECTOR
<img width="614" height="495" alt="image" src="https://github.com/user-attachments/assets/e37318f5-1d12-4484-83d9-075d5b09ddb8" />


### CANNY EDGE DETECTOR
<img width="628" height="501" alt="image" src="https://github.com/user-attachments/assets/ab7b3178-774c-488e-899d-5f28d94f1c97" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
