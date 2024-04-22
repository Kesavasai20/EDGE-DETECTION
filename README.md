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
### Developed By : K KESAVA SAI
### Register Number : 212223230105

### Importing packages,load and convert to gray image
```python
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('nature.jpg',0)
gray=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.imshow(gray)
```
### Sobel Edge Detector

### Sobel X  
```python
sobel_x = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobel_x,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### Sobel Y
```python
sobel_y = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobel_y,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### Sobel XY
```python
sobel_xy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobel_xy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### Laplacian Edge Detector
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### Canny Edge Detector
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### Gray Image
![image](https://github.com/Kesavasai20/EDGE-DETECTION/assets/138849303/8333f613-58a9-4f3c-ae6f-25e177307cce)

### SOBEL EDGE DETECTOR
### Sobel X
![image](https://github.com/Kesavasai20/EDGE-DETECTION/assets/138849303/025884bd-2210-4281-832e-6c1a6e53eceb)

### Sobel Y
![image](https://github.com/Kesavasai20/EDGE-DETECTION/assets/138849303/3ef12151-73ce-49e2-9156-9905db7866a0)

### Sobel XY
![image](https://github.com/Kesavasai20/EDGE-DETECTION/assets/138849303/d47d344e-53df-49ef-a7b7-a8777d0541b1)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Kesavasai20/EDGE-DETECTION/assets/138849303/201c452d-a735-4c1c-adc4-2fbf78176ffb)



### CANNY EDGE DETECTOR
![image](https://github.com/Kesavasai20/EDGE-DETECTION/assets/138849303/300aafa3-35b1-4eeb-9451-3523bf2f41c6)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
