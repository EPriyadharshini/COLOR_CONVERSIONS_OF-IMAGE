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

   
![Screenshot 2024-09-15 233910](https://github.com/user-attachments/assets/7d915ff3-50ce-4adc-a9f7-43db7a6a4e6d)


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
```
### output :



![Uploading Screenshot 2024-09-15 234302.png…]()



```
ii)draw a circle at the center of image
import cv2

img = cv2.imread("img1.jpg")

res=cv2.circle(img,(320,295),150,(255,0,0),10)

cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### output:


![Uploading Screenshot 2024-09-15 234756.png…]()



```
iii) draw a line from the top-left to bottom-right of the image
import cv2

img = cv2.imread("img1.jpg")
res = cv2.line(img,(550,600),(0,0),(220,120,205),10)

cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### output :


![image](https://github.com/user-attachments/assets/9b87a7cd-93d5-4cde-99c6-7c8f961423e5)


```
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

### output:

<img width="301" alt="image 5 dip ex 1" src="https://github.com/user-attachments/assets/cf11c98a-a681-45db-9e70-689fd98188d1">


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


![Uploading img6 dip exe1.png…]()



### iv)Access and Manipulate Image Pixels

(i) Access and print the value of the pixel at coordinates (100, 100)

```
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
## output:

<img width="442" alt="img 7 dip exe1" src="https://github.com/user-attachments/assets/f3d225c4-b5cd-45b6-9894-bba04fea0466">


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

![image](https://github.com/user-attachments/assets/2f94c1d7-c59e-4a1e-92c3-7a2def6b8cd3)


### v)Image Resizing

```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## output

<img width="473" alt="img9 dip exe1" src="https://github.com/user-attachments/assets/1e01a94c-bbf9-42e5-af2b-762652565d68">


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

<img width="91" alt="img 10 dip" src="https://github.com/user-attachments/assets/f3b0b572-407d-4892-b443-b7165d3c6435">


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

<img width="460" alt="img 11 dip" src="https://github.com/user-attachments/assets/27196546-bc4b-4d22-a6bf-3053c4660c76">


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

![Screenshot 2024-09-16 001342](https://github.com/user-attachments/assets/5a579f03-11ca-4403-9434-8b3d90439942)



### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("img1.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('boat_pic.jpg',img)

```
### output:

<img width="425" alt="dip last img exe 1" src="https://github.com/user-attachments/assets/ec9fc8e3-ae73-4134-b3d7-8ba9f0b27abc">




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







