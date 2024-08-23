# COLOR_CONVERSIONS_OF-IMAGE
## AIM:
To write a python program using OpenCV to do the following image manipulations.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
```
1. Read and Display an Image:

Load an image from your local directory and display it.

2. Draw Shapes and Add Text:

Draw a line from the top-left to the bottom-right of the image.

Draw a circle at the center of the image.

Draw a rectangle around a specific region of interest in the image.

Add the text "OpenCV Drawing" at the top-left corner of the image.

3. Image Color Conversion:

Convert the image from RGB to HSV and display it.

Convert the image from RGB to GRAY and display it.

Convert the image from RGB to YCrCb and display it.

Convert the HSV image back to RGB and display it.

4. Access and Manipulate Image Pixels:

Resize the original image to half its size and display it.

6. Image Cropping:

Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

7. Image Flipping:

Flip the original image horizontally and display it.

Flip the original image vertically and display it.

8. Write and Save the Modified Image:

Save the final modified image to your local directory.
```

# Program:
```
Developed By: P KEERTHANA
Register Number: 212223240069
```


### 1.) Read and display the image

```Python
import cv2
image=cv2.imread('c.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
 

### OUTPUT:

![image](https://github.com/user-attachments/assets/3e6eb6c9-9fc6-4dc9-b50c-bba9b398ba39)


 

### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
import cv2
img = cv2.imread("C.JPG")
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```


### OUTPUT:


![image](https://github.com/user-attachments/assets/119ec99b-5d64-42b1-ba6f-9d171f0e0dee)


 
### ii)Draw a circle at the center of the image.
```Python
import cv2

# Load the image
img = cv2.imread("C.JPG")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


### OUTPUT:

![image](https://github.com/user-attachments/assets/25d75ce6-44d8-4650-93b3-ec1e9e3b64a5)


      
### iii)Draw a rectangle around a specific region of interest in the image.
```Python
import cv2

img = cv2.imread("C.JPG")
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 

### OUTPUT:


![image](https://github.com/user-attachments/assets/181ea2fb-9875-4272-8e4c-ac807d0bf87f)


      
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
import cv2

# Load the image
img = cv2.imread("C.JPG")

# Define the text to be added and its position
text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

    
### OUTPUT:

![image](https://github.com/user-attachments/assets/6783d68b-f362-438a-b811-7a1166410517)


### 3.)Image Color Conversion:
i)Convert the image from RGB to HSV and display it.
```Python
import cv2
img = cv2.imread('c.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![image](https://github.com/user-attachments/assets/b6793dc9-61c8-4e4a-b77e-902b090046fe)


#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('c.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:

![image](https://github.com/user-attachments/assets/59c99bbe-3eb8-4aae-b010-62e8a0911c77)


#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('c.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:

![image](https://github.com/user-attachments/assets/a355d992-b7a4-421a-913c-1b92192554e4)


#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('c.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:

![image](https://github.com/user-attachments/assets/5f7a25e5-1875-4ec7-8eff-f3ed3cad0534)


## 4. Access and Manipulate Image Pixels:
```Python
import cv2

# Load and resize the image
img = cv2.imread('c.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:

![image](https://github.com/user-attachments/assets/6e6f8673-05fd-457c-a1f0-8f8d56afa3a1)


![image](https://github.com/user-attachments/assets/7e5a11c1-95a2-467d-ae0c-dabb652b3354)


## 5. Image Resizing:
```Python
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:

![image](https://github.com/user-attachments/assets/6f8dff87-6857-4f70-b9a8-70a2bd95e780)


## 6.Image Cropping:
```Python
import cv2

# Load the image
image1=cv2.imread('c.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:

![image](https://github.com/user-attachments/assets/721313df-7f14-4842-8596-c8feaf60b5c8)


## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python

import cv2
img = cv2.imread("c.JPG")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:

![image](https://github.com/user-attachments/assets/934acd3f-2299-4132-ad23-70a6d9abe8a8)


#### ii.)Flip the original image vertically and display it.

```Python
import cv2

img = cv2.imread("c.JPG")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:

![image](https://github.com/user-attachments/assets/16950684-3e2e-44e0-bc05-781199574df0)


## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread("c.JPG")
img = cv2.resize(img,(300,200))
cv2.imwrite('sunny1.jpg',img)
```
### Output:

![image](https://github.com/user-attachments/assets/ac1b5d54-6919-439e-9dbc-33c2944fcb7d)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.


