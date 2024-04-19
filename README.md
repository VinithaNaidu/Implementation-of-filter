# EX NO-5
# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By   :S.Prema Latha
### Register Number:212222230112
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("paris.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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

![Screenshot 2024-03-19 103757](https://github.com/premalatha-sureshbabu/Implementation-of-filter/assets/120620842/e16124cc-bb01-4e7f-840c-1990b5d9e998)


ii) Using Weighted Averaging Filter

![Screenshot 2024-03-19 103805](https://github.com/premalatha-sureshbabu/Implementation-of-filter/assets/120620842/681aa19c-42d2-42c4-a638-4516e7b978a1)


iii) Using Gaussian Filter

![Screenshot 2024-03-19 103812](https://github.com/premalatha-sureshbabu/Implementation-of-filter/assets/120620842/f89ff184-1e52-436d-8fac-2a36a3c71238)


iv) Using Median Filter

![Screenshot 2024-03-19 103819](https://github.com/premalatha-sureshbabu/Implementation-of-filter/assets/120620842/28002ad3-0f4b-48fe-8076-ec7a0b154913)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-19 103828](https://github.com/premalatha-sureshbabu/Implementation-of-filter/assets/120620842/3724b0b0-30d7-435d-8f97-c345dee8e895)


ii) Using Laplacian Operator

![Screenshot 2024-03-19 103836](https://github.com/premalatha-sureshbabu/Implementation-of-filter/assets/120620842/32549ae9-4f98-40b0-b4cf-398f071e0da0)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
