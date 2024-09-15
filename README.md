# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

 i) Read and Display an Image
 ii) 	Draw Shapes and Add Text.
iii) Image Color Conversion.
iv) Access and Manipulate Image Pixels.
v) Image Resizing
vi) Image Cropping
vii) Image Flipping
viii)	Write and Save the Modified Image

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program and Output:

### Developed By:priyadharshini E
### Register Number:212223230159 


### i)Read and Display an Image
```
!pip install matplotlib
pip install opencv-contrib-python
import cv2
import matplotlib.pyplot as plt
import cv2
image=cv2.imread('img1.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('kakashi',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### output:






### ii)Draw Shapes and Add Text
```
i) draw a square from the left corner of the image
import cv2
img = cv2.imread("img1.jpg")
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

ii)draw a circle at the center of image
import cv2

img = cv2.imread("img1.jpg")

res=cv2.circle(img,(320,295),150,(255,0,0),10)

cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii) draw a line from the top-left to bottom-right of the image
import cv2

img = cv2.imread("img1.jpg")
res = cv2.line(img,(550,600),(0,0),(220,120,205),10)

cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

iv)Add the text "OpenCV Drawing" at the top-left corner of the image

import cv2
image = cv2.imread("img1.jpg")
image = cv2.resize(image, (400, 300))
text = "kakashi"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### iii)Image Color Conversion

```
import cv2
img = cv2.imread('img1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
YCrCB2 = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCB',YCrCB2)
rgb = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('RGB2YCrCB',rgb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output :


### iv)Access and Manipulate Image Pixels

(i) Access and print the value of the pixel at coordinates (100, 100)

```
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
## output:


(ii) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('img1.jpg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output



### v)Image Resizing

```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## output



### vi)Image Cropping

```
import cv2
image = cv2.imread('img1.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### output



### vii)Image Flipping

i)Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("img1.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## output



ii)Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("img1.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output




### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("img1.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('boat_pic.jpg',img)

```
### output:





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







