# IMPLEMENTATION-OF-FILTERS

## Aim:

To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:

Anaconda - Python 3.7

## Algorithm:

### Step1

Import the required modules.

### Step2

Convert the image from BGR to RGB.

### Step3

Apply the required filters for the image separately.

### Step4

Plot the original and filtered image by using matplotlib.pyplot

### Step5

End the program.

## Program
```
Developed By : DHANUMALYA D

Register Number:212222230030
```
### 1. Smoothing Filters
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("road.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```

i) Using Averaging Filter
```
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()

```

iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![Screenshot from 2023-09-06 19-11-31](https://github.com/Dhanudhanaraj/IMPLEMENTATION-OF-FILTERSS/assets/119218812/8bebae3f-67cc-4e88-8a1e-b55fde3f597c)

ii) Using Weighted Averaging Filter

![Screenshot from 2023-09-06 19-11-39](https://github.com/Dhanudhanaraj/IMPLEMENTATION-OF-FILTERSS/assets/119218812/41f35240-49dd-4d19-b14a-17bc258b6a8e)

iii) Using Gaussian Filter

![Screenshot from 2023-09-06 19-11-49](https://github.com/Dhanudhanaraj/IMPLEMENTATION-OF-FILTERSS/assets/119218812/b4850994-907a-4d66-8dee-4a4a5dc759f2)

iv) Using Median Filter

![Screenshot from 2023-09-06 19-12-01](https://github.com/Dhanudhanaraj/IMPLEMENTATION-OF-FILTERSS/assets/119218812/3ae00490-016b-44f3-9129-156a584139e1)

### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot from 2023-09-06 19-12-08](https://github.com/Dhanudhanaraj/IMPLEMENTATION-OF-FILTERSS/assets/119218812/b19fffa1-e31e-46d0-92d2-42bb2276123a)

ii) Using Laplacian Operator

![Screenshot from 2023-09-06 19-12-16](https://github.com/Dhanudhanaraj/IMPLEMENTATION-OF-FILTERSS/assets/119218812/49594bda-6cb9-4bb4-bae6-d897ca6e16aa)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
