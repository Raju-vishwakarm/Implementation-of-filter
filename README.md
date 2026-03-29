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
```
 Developed By:D.Raju 
 Register No: 212224240128 
```

### 1. Smoothing Filters

## i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
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
## ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
## iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
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
## iv)Using Median Filter
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
## i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
## ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
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


## i) Using Averaging Filter
<img width="960" height="768" alt="Screenshot 2025-09-06 104426" src="https://github.com/user-attachments/assets/74b17529-058c-4a75-ba61-673ff25797c2" />


## ii)Using Weighted Averaging Filter
<img width="668" height="517" alt="Screenshot 2025-09-06 104435" src="https://github.com/user-attachments/assets/0d82338e-b5de-4fb1-a5d6-bedd02ae93b9" />


## iii)Using Gaussian Filter

<img width="654" height="516" alt="Screenshot 2025-09-06 104444" src="https://github.com/user-attachments/assets/a812ffca-765b-4487-a882-813a792c1091" />

## iv) Using Median Filter

<img width="961" height="764" alt="Screenshot 2025-09-06 104457" src="https://github.com/user-attachments/assets/66473b63-e82d-4b04-90ae-b509c6c6c9ed" />

### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="685" height="519" alt="Screenshot 2025-09-06 104505" src="https://github.com/user-attachments/assets/7f5a2d2a-a6ca-42a1-95f7-13b8ad63dcd3" />

## ii) Using Laplacian Operator
<img width="652" height="508" alt="Screenshot 2025-09-06 104512" src="https://github.com/user-attachments/assets/c895ebe1-f89d-4383-870c-f779d099ddea" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.

