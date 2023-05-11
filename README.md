# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the required packages.

### Step2:
Load the image to operate on.

### Step3:
Convert the image to grayscale image.

### Step4:
Use Sobel operator along x,y and xy directions.

### Step5:
Operate the image using Laplacian operator.

### Step6:
Operate the image using Canny Edge operator.

### Step7:
Show all the operated images output.

### step8:
End the program.
## Program:
``` Python
Developed by:shaik sameer basha
RegisterNumber:212222240093

# Import the packages
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("image1.png")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
# Load the image, Convert to grayscale and remove noise
# SOBEL EDGE DETECTOR
### SOBEL X:
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
### SOBEL Y:
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
### SOBEL XY:
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
# LAPLACIAN EDGE DETECTOR
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
# CANNY EDGE DETECTOR
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
### SOBEL EDGE DETECTOR
![Screenshot from 2023-05-11 11-11-49](https://github.com/shaikSameerbasha5404/Edge-Detection/assets/118707756/99e18011-94d5-42af-b5f4-704e964034c6)

![Screenshot from 2023-05-11 11-14-13](https://github.com/shaikSameerbasha5404/Edge-Detection/assets/118707756/5340e0a7-4fc7-4c5e-9e26-05ecd73a802d)

![Screenshot from 2023-05-11 11-14-55](https://github.com/shaikSameerbasha5404/Edge-Detection/assets/118707756/c9599a0d-b40a-466a-b319-4f2fc3641d85)

### LAPLACIAN EDGE DETECTOR
![Screenshot from 2023-05-11 11-15-31](https://github.com/shaikSameerbasha5404/Edge-Detection/assets/118707756/59eb2548-e1c5-4c4c-b0f4-e206f3669364)

### CANNY EDGE DETECTOR
![Screenshot from 2023-05-11 11-16-12](https://github.com/shaikSameerbasha5404/Edge-Detection/assets/118707756/0ead9aee-4b1b-496a-a075-e3f267e1c5a4)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
