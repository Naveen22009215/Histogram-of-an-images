# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

```python
Developed By: NAVEEN KUMAR P
Register Number: 212222230092
```

### Input Grayscale Image and Color Image : 

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("tree.jpg")
color_image = cv2.imread("tree1.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```python
import numpy as np
import cv2
Gray_image = cv2.imread("tree.jpg")
Color_image = cv2.imread("tree1.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

### Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("tree.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Input Grayscale Image and Color Image
<img height=45% width=45% src="https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/bd70fff0-7e5d-4acc-b52e-04638bef264d">
<img height=47% width=45% src="https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/c05f706d-b1e8-48b6-8b65-2dee1fdee29d">

### Histogram of Grayscale Image and any channel of Color Image

#### Gray Scale -
![WhatsApp Image 2024-03-19 at 11 34 19_6bfe3884](https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/5fd1ffc3-7e4c-4faa-98c1-2e875341b559)
![WhatsApp Image 2024-03-19 at 11 34 18_f173d2f9](https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/228f3523-dbaf-47cc-8097-72947c3197b5)

#### Green Channel -
![WhatsApp Image 2024-03-19 at 11 34 19_695e904e](https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/e6cc39df-56e4-43d9-b84d-4b7043f77363)
![WhatsApp Image 2024-03-19 at 11 34 18_7ba3bd6f](https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/0e084d1f-cd05-49bd-89fe-ded5a7adadda)

### Histogram Equalization of Grayscale Image :
![WhatsApp Image 2024-03-19 at 11 34 19_695e904e](https://github.com/Naveen22009215/Histogram-of-an-images/assets/119401470/95670ee8-7a98-46fe-b111-ed8b205dec8a)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
