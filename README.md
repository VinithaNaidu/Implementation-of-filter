# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
```py
Developed By   : VINITHA NAIDU
Register Number: 212222230175
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("kholi.png")
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
```Python
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
```Python

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
```Python

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
```Python

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
```Python


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

![Screenshot 2024-03-15 132703](https://github.com/SHARAN-MJ/Implementation-of-filter/assets/119560305/8d70f800-a567-471e-a0f5-2435c8a1e727)


ii) Using Weighted Averaging Filter

![Screenshot 2024-03-15 132726](https://github.com/SHARAN-MJ/Implementation-of-filter/assets/119560305/ab683d10-bbcb-40a1-be9f-dd8fc64f0a35)

iii) Using Gaussian Filter

![Screenshot 2024-03-15 132742](https://github.com/SHARAN-MJ/Implementation-of-filter/assets/119560305/3c2b4599-c2c6-446f-937c-ee35966e584e)


iv) Using Median Filter

![Screenshot 2024-03-15 132755](https://github.com/SHARAN-MJ/Implementation-of-filter/assets/119560305/a27c2cd1-387d-46cc-aee4-60096dd17d42)



### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-15 132809](https://github.com/SHARAN-MJ/Implementation-of-filter/assets/119560305/91193e78-1ab9-4609-8d5b-186b39b91697)

ii) Using Laplacian Operator

![Screenshot 2024-03-15 132823](https://github.com/SHARAN-MJ/Implementation-of-filter/assets/119560305/a526edc4-a3bf-4bab-9fd4-9836d055caf8)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
