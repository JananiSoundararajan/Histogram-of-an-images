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
# Developed By: JANANI
# Register Number: 212222230049
# Grayscale image and Color image
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("tomie.jpeg")
color_image = cv2.imread("nanno.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# Histogram of Grayscale image and color image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("tomie.jpeg")
Color_image = cv2.imread("nanno.jpg")
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
# Histogram equalization of Grayscale image
```python
import cv2
gray_image = cv2.imread("tomie.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

#### Grayscale Image
![tomiegray](https://github.com/JananiSoundararajan/Histogram-of-an-images/assets/119477549/312c0fb2-e04c-4fef-bdf5-51842a114b29)

#### Color Image
![nannocolor](https://github.com/JananiSoundararajan/Histogram-of-an-images/assets/119477549/a28f0ffa-1dfe-483b-9e08-00341e2e5894)


### Histogram of Grayscale Image and any channel of Color Image
![tomhis](https://github.com/JananiSoundararajan/Histogram-of-an-images/assets/119477549/ab330df5-d7ba-41c2-8c8c-5ada14d77651)
![tommhis](https://github.com/JananiSoundararajan/Histogram-of-an-images/assets/119477549/3e79db06-ede8-4fb6-8d5a-84e2c800eeb6)

![nannohis](https://github.com/JananiSoundararajan/Histogram-of-an-images/assets/119477549/8aac6865-8719-40c1-aa33-fa28500103dc)
![nannohiss](https://github.com/JananiSoundararajan/Histogram-of-an-images/assets/119477549/289b94d4-b900-43d9-b1e0-a7ef2ec3db53)


### Histogram Equalization of Grayscale Image.




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
