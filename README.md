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
```
 Developed By: Kamesh D
 Register Number: 212222240043
```

### Input Grayscale Image and Color Image :
```py
import cv2
import matplotlib.pyplot as plt
from google.colab.patches import cv2_imshow

# Load the images
gray_image = cv2.imread("luffy.jpg", 0)
color_image = cv2.imread("luffy.jpg")

# Display the images
cv2_imshow(gray_image)
cv2_imshow(color_image)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```py
import numpy as np
import cv2
Gray_image = cv2.imread("luffy.jpg")
Color_image = cv2.imread("luffy.jpg")
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
```py
import cv2
gray_image = cv2.imread("luffy.jpg",0)
cv2_imshow(gray_image)
equ = cv2.equalizeHist(gray_image)
cv2_imshow(equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-20 100945](https://github.com/KameshLeVI/Histogram-of-an-images/assets/120780633/d3cca3fb-0550-4a6b-9aaf-9076421a8fa8)
![Screenshot 2024-03-20 100958](https://github.com/KameshLeVI/Histogram-of-an-images/assets/120780633/b17f04b3-8724-475e-aa0e-42542b698097)



### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-20 101050](https://github.com/KameshLeVI/Histogram-of-an-images/assets/120780633/2f1e9c52-473b-4e15-a84d-5f34f6dd482a)


### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-20 101206](https://github.com/KameshLeVI/Histogram-of-an-images/assets/120780633/5b0fc188-1bef-4154-a72c-bad21077f557)
![Screenshot 2024-03-20 101224](https://github.com/KameshLeVI/Histogram-of-an-images/assets/120780633/5ea38e22-880b-4519-92df-d6995b88e757)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
