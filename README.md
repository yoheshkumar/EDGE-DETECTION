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
```
Developed by : YOHESH KUMAR R.M
Register no  : 212222240118
```

### Convert image to grayscale and remove noise:
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("yk.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### Sobel Edge Detector:
#### SOBEL X AXIS: 
```python
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

#### SOBEL Y AXIS:
```python 
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

#### SOBEL XY AXIS: 
```python 
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

### laplacian edge Detector:
```python
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

### Canny Edge Detector:
```python 
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
### SOBEL EDGE DETECTOR :
#### SOBEL X AXIS :
![xaxis](https://github.com/yoheshkumar/EDGE-DETECTION/assets/119393568/7fce7582-3eb6-48c8-8a4a-ca873f75b7c0)



#### SOBEL Y AXIS :
![yaxis](https://github.com/yoheshkumar/EDGE-DETECTION/assets/119393568/117bc91f-15bc-4666-ace9-73ab1b1093b2)

#### SOBEL XY AXIS :
![xyaxis](https://github.com/yoheshkumar/EDGE-DETECTION/assets/119393568/79dd0bba-7755-4ac6-b0ba-e8d862cfa47b)


### LAPLACIAN EDGE DETECTOR :
![lapacian](https://github.com/yoheshkumar/EDGE-DETECTION/assets/119393568/bddd85bd-17a1-4803-a86b-730b0b6d9a60)

### CANNY EDGE DETECTOR :
![canny](https://github.com/yoheshkumar/EDGE-DETECTION/assets/119393568/5be69729-dc1e-4fcc-a9e6-88cac9de8bdf)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
