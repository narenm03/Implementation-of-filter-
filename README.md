# Implementation-of-filter
## NAME:NARENDHARAN M
## REG NO:212223230134
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
### Developed By   :
### Register Number:
</br>

### 1. Smoothing Filters

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
<img width="724" height="362" alt="image" src="https://github.com/user-attachments/assets/76c482cc-205d-4a1a-9926-bf10a6bd3e2d" />
<img width="403" height="406" alt="image" src="https://github.com/user-attachments/assets/835b33fe-0517-4dad-977e-be961ebe4661" />
<img width="438" height="417" alt="image" src="https://github.com/user-attachments/assets/38ef6528-ca73-4279-a7d1-b8d198a040fe" />
<img width="411" height="411" alt="image" src="https://github.com/user-attachments/assets/fe8d6474-41c6-44e0-a8ff-b44aba8a23d6" />
<img width="412" height="409" alt="image" src="https://github.com/user-attachments/assets/1fe2f406-961d-4dd4-9416-48001847ead2" />
<img width="417" height="404" alt="image" src="https://github.com/user-attachments/assets/c76b46fc-d6a2-465c-992f-d51b79091cf3" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.





