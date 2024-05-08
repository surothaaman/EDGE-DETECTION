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

## PROGRAM :
**DEVELOPED BY : SUROTHAMAN R**
**REGISTER NO : 212222103003**
### Convert image to grayscale and remove noise
```P
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("rose.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```p
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y AXIS :**
```p
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY AXIS :**
```p
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```p
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```p
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR

**SOBEL X AXIS :**
![Screenshot 2024-04-02 114317](https://github.com/Harish2404lll/EDGE-DETECTION/assets/141472096/2545ef0e-2b85-46f5-b4dc-24dec6a51b4c)



**SOBEL Y AXIS :**
![Screenshot 2024-04-02 114330](https://github.com/Harish2404lll/EDGE-DETECTION/assets/141472096/0a0d8941-d688-4032-8cf9-19d442559098)


**SOBEL XY AXIS :**
![Screenshot 2024-04-02 114340](https://github.com/Harish2404lll/EDGE-DETECTION/assets/141472096/558084b9-e71e-4df9-a030-ef6f72001e4f)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-02 114355](https://github.com/Harish2404lll/EDGE-DETECTION/assets/141472096/1d22b7d2-d574-47d2-a5ba-dd3e50ebeecf)


### CANNY EDGE DETECTOR
![Screenshot 2024-04-02 114408](https://github.com/Harish2404lll/EDGE-DETECTION/assets/141472096/3f87e0e6-f17d-418d-be6a-298dc28ca822)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
