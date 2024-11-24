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
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
# Display the image using Matplotlib
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
   ### output:
![image](https://github.com/user-attachments/assets/c368a995-70f3-4635-a669-b6727630cc55)

   


### ii)Draw Shapes and Add Text
Step2:
o Draw a line from the top-left to the bottom-right of the image.

o Draw a circle at the center of the image. 

o Draw a rectangle around a specific region of interest in the image. 

o Add the text "OpenCV Drawing" at the top-left corner of the image.
```



i) draw a square 
# Load the image
image = cv2.imread('img.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (770, 490), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()

```
### output :



![image](https://github.com/user-attachments/assets/f9482dac-6e0a-4d3a-9f9b-a5d193795ab0)



```
ii)draw a circle at the center of image
# Load the image
image = cv2.imread('img.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
circle_img = cv2.circle(img_rgb,(400,250),150,(25,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

### output:
![image](https://github.com/user-attachments/assets/ea4d0195-3742-45b6-bc42-e3da588f9331)







iii) draw a line from the top-left to bottom-right of the image

```
# Load the image
image = cv2.imread('img.jpeg') # Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb.shape
# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (790, 500), (25, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

### output :

![image](https://github.com/user-attachments/assets/cdbd3950-1b09-4273-96c3-2321b447e6a8)



```
iv)Add the text "OpenCV Drawing" at the top-left corner of the image

# Load the image
image = cv2.imread('img.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
# Add text to the image
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 40), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

### output:

![image](https://github.com/user-attachments/assets/a5f2104a-c0cb-4778-adeb-cc6ee16a7302)


### iii)Image Color Conversion


Step3:
o Convert the image from RGB to HSV and display it.
    
o Convert the image from RGB to GRAY and display it. 

o Convert the image from RGB to YCrCb and display it. 
    
o Convert the HSV image back to RGB and display it.

```
# Load the image
image = cv2.imread('img.jpeg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
# Original RGB Image
plt.imshow(image_rgb)
plt.title("RGB - ORG ")
plt.axis("off")
```
## output :

![image](https://github.com/user-attachments/assets/dd145814-e58f-418b-b306-7f9d7ee46c0d)

```
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
# output

![image](https://github.com/user-attachments/assets/dd6d2288-2932-41ef-84ff-a571d9a348c0)

# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")


# output

![image](https://github.com/user-attachments/assets/357b697c-6455-4d3c-8da1-64d89354ee58)

```
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)

# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```
# output 
  ![image](https://github.com/user-attachments/assets/361181c5-0fa7-43fb-9a66-6f8be18ed608)



```
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```
# output

 
![image](https://github.com/user-attachments/assets/86be7a28-d3e9-4379-b722-eb9c513156dc)



Step4:
o Access and print the value of the pixel at coordinates (100, 100). 

o Modify the color of the pixel at (200, 200) to white.

```
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[100:350, 300:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()

```

# output

![image](https://github.com/user-attachments/assets/239cd20d-6319-4abf-a299-d65facd2c707)


Step5:
o Resize the original image to half its size and display it.


```

# Load the image
image = cv2.imread('img.jpeg')
image.shape
# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)
# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
 # output
 
![image](https://github.com/user-attachments/assets/6cbf7f41-03e1-4a20-9c51-6173ffc27e61)

Step6:
o Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
# Load the image
image = cv2.imread('img.jpeg') 
image.shape
# Crop a 300x300 region starting from (50, 50)
roi = image[100:350, 250:550]  # Rows: 50-349, Columns: 50-349

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()


```


# output

![image](https://github.com/user-attachments/assets/8997bc41-b101-4a09-8589-6cf1cfd44dcb)


Step7:
o Flip the original image horizontally and display it. 

o Flip the original image vertically and display it.
```

# Load the image
image = cv2.imread('img.jpeg') 
# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)
# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")

# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)
# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
# output

![image](https://github.com/user-attachments/assets/2459693a-3fdd-41bd-98fb-636bc21c90b8)

# output

![image](https://github.com/user-attachments/assets/8ea2993f-1871-4b82-b4b4-1fa07becc9fc)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







