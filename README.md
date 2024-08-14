# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: P.Keerthana
### Register Number: 212223240069


## Output:

### i) Read and display the image

```
import cv2
image=cv2.imread('2.jpg',1)
image=cv2.resize(image,(400,400))
cv2.imshow('Flower',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/20c6bdef-3b79-429e-8cc8-982c8fd4fdba)

### ii)Write the image

```
image=cv2.imread('2.jpg',0)
cv2.imwrite('1.jpeg',image)
```
## OUTPUT:
![Screenshot 2024-08-14 214315](https://github.com/user-attachments/assets/ce308182-3bca-4649-b078-14655da7b111)


### iii)Shape of the Image
```
import cv2
image=cv2.imread('2.jpg',1)
print(image.shape)
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/894103bb-42e5-48d9-ae41-c5e7907fa6ab)


### iv)Access rows and columns
```
import random
import cv2
image=cv2.imread('2.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('Flower image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT :
![image](https://github.com/user-attachments/assets/c0823a88-c972-44cb-8695-14d9aadcaea8)


### v)Cut and paste portion of image
```
import cv2
image=cv2.imread('2.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('Flower',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/baba9033-c40e-417f-b04f-9865cf5ba814)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('2.jpg',1)
img = cv2.resize(img,(300,300))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/9ec36ab5-1476-4dea-89ca-22adce47824c)

![image](https://github.com/user-attachments/assets/80416d64-0fc2-458f-8d29-5320692a2c8c)

![image](https://github.com/user-attachments/assets/8ffa5dd2-454a-4ddc-9ce9-54d0a8c772a4)

![image](https://github.com/user-attachments/assets/ac23a976-1cd3-498b-bcef-122f06e90b2a)

![image](https://github.com/user-attachments/assets/b387aecb-5001-42d1-aa80-f548937f6446)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('2.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## OUTPUT:
![image](https://github.com/user-attachments/assets/1b96a439-9ebc-4f26-83f4-49ef8339c97a)
![image](https://github.com/user-attachments/assets/9774a257-8d56-442e-a6dc-7d3f0d2634b7)
![image](https://github.com/user-attachments/assets/ab544fed-b0a9-41c9-8aa4-65d83d736ecc)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('2.jpg')
img = cv2.resize(img,(300,300))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/392c8983-285e-4dd2-8f8f-0c1055e7357e)

![image](https://github.com/user-attachments/assets/d728ca83-5955-4d58-833d-8d345437c00d)
![image](https://github.com/user-attachments/assets/e064d49c-a560-43b1-8cb3-6bd6d3b86a08)


### ix) Split and merge RGB Image

```
import cv2
img = cv2.imread('2.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/94a1bd98-79b2-401e-923e-dc3ae68b1ee8)
![image](https://github.com/user-attachments/assets/47fb6520-63c0-4fd3-b8b2-7ee5692b5e8b)
![image](https://github.com/user-attachments/assets/1255cd92-0480-46d9-8bec-1fec8da74d06)
![image](https://github.com/user-attachments/assets/e4332999-20b7-4db6-99a0-df376a7ae021)



### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("2.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/bca5f1e9-fd70-4464-8304-0b8caafe5eee)

![image](https://github.com/user-attachments/assets/84b2fa83-3a6b-4035-b278-3499c8114bbf)

![image](https://github.com/user-attachments/assets/50364ca8-8ecb-4cb3-818c-f3446011e5b0)

![image](https://github.com/user-attachments/assets/be68f6f3-4c0d-4cef-8b1e-a92850b5adac)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







