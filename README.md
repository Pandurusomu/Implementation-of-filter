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
### Developed By : Panduru somu
### Register Number: 212223240111
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nature.jpg")
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
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters
</br>

### i) Using Averaging Filter
<img width="722" height="222" alt="image" src="https://github.com/user-attachments/assets/00741da6-3812-49df-8972-8e8624062a11" />


### ii)Using Weighted Averaging Filter
<img width="548" height="309" alt="image" src="https://github.com/user-attachments/assets/6e71f9d4-c27b-49a3-b1ab-7d80757259e9" />


### iii)Using Gaussian Filter
<img width="548" height="309" alt="image" src="https://github.com/user-attachments/assets/38690d08-5bf9-46ad-bee7-c8cbbbd64bd1" />


### iv) Using Median Filter
<img width="581" height="315" alt="image" src="https://github.com/user-attachments/assets/df0d1622-efba-4bad-8e5d-ac333dc8f621" />


### 2. Sharpening Filters
</br>

### i) Using Laplacian Kernal
<img width="511" height="316" alt="image" src="https://github.com/user-attachments/assets/cbb5d3ae-3230-48a9-94ef-8d7e4b072e57" />


### ii) Using Laplacian Operator
<img width="529" height="312" alt="image" src="https://github.com/user-attachments/assets/8862967d-7e47-43ac-a334-5df1445ff082" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
