# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## ALGORITHM:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use gaussian filter for smoothing the image to reduce the noise.
### Step4:
Apply the respective filters - Sobel, Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
## Program:

# Import the packages

``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("images.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
```

# Load the image, Convert to grayscale and remove noise
``` Python
gray_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```

# SOBEL EDGE DETECTOR
## Sobel X:
``` Python
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()
```
## Sobel Y:
``` Python

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()
```
## Sobel XY:
``` Python
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()
```

# LAPLACIAN EDGE DETECTOR
``` Python
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()
```
# CANNY EDGE DETECTOR
``` Python
canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()



```
## Output:
### orinigal image 
![image](https://github.com/praveenst13/EDGEDETECTION/assets/118787793/a27fdfcb-1020-4de8-8fc7-4c0464f13d10)
### SOBEL EDGE DETECTOR
<br>
<br>

## Sobel X:
![image](https://github.com/praveenst13/EDGEDETECTION/assets/118787793/d0f3bf36-9cf5-403b-9b92-e72fb1e6c190)

## Sobel Y:
![image](https://github.com/praveenst13/EDGEDETECTION/assets/118787793/6fe41a39-43b2-41ea-b2f7-5758385f7b83)
<br>

## Sobel XY:

![image](https://github.com/praveenst13/EDGEDETECTION/assets/118787793/48bf152f-fb77-42a0-b543-d7f2bcaf7b8b)

<br>
<br>
<br>


### LAPLACIAN EDGE DETECTOR
<br>
<br>
<br>

![image](https://github.com/praveenst13/EDGEDETECTION/assets/118787793/48e9bfd9-2b46-4da4-924f-97e003921117)


<br>
<br>
<br>


### CANNY EDGE DETECTOR
<br>
<br>
<br>

![image](https://github.com/praveenst13/EDGEDETECTION/assets/118787793/b311c9ae-cd8a-4ef7-aa2a-5803f6b4af14)

<br>
<br>
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
