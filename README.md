# Histogram-of-an-images

## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread().

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: DELLI PRIYA L
# Register Number: 212222230029
```

## Output:
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("vijay.png")
color_image = cv2.imread("ajith.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/ae0b0a58-8e75-4aa4-9f5f-b77cfe97de87)

### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("vijay.png")
Color_image = cv2.imread("ajith.png")
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
```
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/428daeb2-b3ce-4bc8-ab7c-03038c860280)

### Grayscale Image
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/9d3dec91-04a6-4fc8-8d07-87006399915e)
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/d4e46a61-7592-4c45-b014-7b61acec963a)

### Colour Image
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/52a5e15e-b3c4-4ce8-a449-9cbbebe95ef2)
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/f3e5d02e-453b-4b18-9caa-cfcae814fe34)
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/c9d04c24-d948-4f28-a0ee-29c4d42230f2)

### Histogram Equalization of Grayscale Image.
```
import cv2
gray_image = cv2.imread("vijay.png",0)
cv2.imshow('Gray Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Priya-Loganathan/Histogram-of-an-images/assets/121166075/91d31343-1e6c-4f7f-ba31-0051aee036f2)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
