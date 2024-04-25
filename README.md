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

## Program:
### DEVELOPED BY: CHAITANYA P S
### REGISTER NUMBER: 212222230024
``` python

import cv2
import matplotlib.pyplot as plt
img=cv2.imread("rog.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### ORIGINAL IMAGE

![download](https://github.com/chaitanya18c/EDGE-DETECTION/assets/119392724/a39735d9-36c4-4dbf-99f4-8db9385dd692)


### SOBEL EDGE DETECTOR

![download](https://github.com/chaitanya18c/EDGE-DETECTION/assets/119392724/ca1be246-03bc-4da1-8807-a134f3af3df6)
![download](https://github.com/chaitanya18c/EDGE-DETECTION/assets/119392724/73c3068c-c0bd-4a37-868d-d444af4ffd0a)
![download](https://github.com/chaitanya18c/EDGE-DETECTION/assets/119392724/56b3c5bc-5ffd-499d-857d-b993c99dc619)

### LAPLACIAN EDGE DETECTOR

![download](https://github.com/chaitanya18c/EDGE-DETECTION/assets/119392724/a78b6bba-567f-4919-a30e-0e8ce68c7ff4)


### CANNY EDGE DETECTOR

![download](https://github.com/chaitanya18c/EDGE-DETECTION/assets/119392724/c84fcd79-aed9-4795-9282-59120d203d73)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
