# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
```
## Step 1: Import the necessary modules.

##Step 2: Perform smoothing operation on a image.
Average filter
Weighted average filter
Gaussian Blur
Median filter

## Step 3: Perform sharpening on a image.
Laplacian Kernel
Laplacian Operator

## Step 4: Display all the images with their respective filters.

```



## Program:
```
### Developed By   :RAKSHITHA DEVI J
### Register Number:212221230082
```
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("simp.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```


### 1. Smoothing Filters

i) Using Averaging Filter

```
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
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


![image](https://user-images.githubusercontent.com/94165326/230019107-cc65fed1-3d1a-414d-ab28-0d6cb84d6aeb.png)

ii) Using Weighted Averaging Filter


![image](https://user-images.githubusercontent.com/94165326/230020052-02731855-86fc-4ec6-8c05-4e9c3a01a5e2.png)


iii) Using Gaussian Filter


![image](https://user-images.githubusercontent.com/94165326/230020177-f21c3fd0-2d88-4c35-9751-e3550aba2ab9.png)

iv) Using Median Filter


![image](https://user-images.githubusercontent.com/94165326/230020472-b5857abc-46a6-4d5f-b021-a189efdc8617.png)

### 2. Sharpening Filters


i) Using Laplacian Kernal

![image](https://user-images.githubusercontent.com/94165326/230020832-1f8fc92c-ef76-4c5d-acd5-f77562685bc1.png)

ii) Using Laplacian Operator

![image](https://user-images.githubusercontent.com/94165326/230021019-090fb18e-1c4a-492c-b4ee-df2d28d62b5d.png)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
