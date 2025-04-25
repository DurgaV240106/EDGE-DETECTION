# EDGE-DETECTION
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

## program:
## NAME : DURGA V
## REG NO : 212223230052

Original
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("bird.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```


## Output:
### Original

![image](https://github.com/user-attachments/assets/c1456045-ce3a-451a-9730-7196787d4018)


### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/4146b5f2-deaa-46a6-8df6-efba55e93629)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/dd394817-59ad-4653-9704-1c93769fde1e)




### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/0d851043-a7c5-4c29-a7b0-c2a4f5106a77)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
