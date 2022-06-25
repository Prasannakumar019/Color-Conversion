## EX NO:03
## DATE:11.4.22
# <p align="center">Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
### Step4:
Split and merge the image using cv2.split and cv2.merge commands
### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By: Prasanna kumar
# Register Number: 212220230035
# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('nat.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('nat.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('nat.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('nat.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('nat.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (226)](https://user-images.githubusercontent.com/75235090/162777823-3d2bd065-595c-4210-9f11-38e77be0ac20.png)

![Screenshot (227)](https://user-images.githubusercontent.com/75235090/162777838-d74819e0-c871-43fd-ac0e-8ec88f70a1a1.png)

### ii) HSV to RGB and BGR
![Screenshot (228)](https://user-images.githubusercontent.com/75235090/162778048-b075bc6e-2bcb-47de-8be5-1784d270a9ad.png)

![Screenshot (229)](https://user-images.githubusercontent.com/75235090/162778060-10936e55-4724-40cf-997a-d67be1eaea49.png)

### iii) RGB and BGR to YCrCb
![Screenshot (230)](https://user-images.githubusercontent.com/75235090/162778263-10396d90-afa1-43e3-8c22-412c90ca0bc5.png)

![Screenshot (231)](https://user-images.githubusercontent.com/75235090/162778279-b686889a-6782-4674-8a18-387a5207db5e.png)

### iv) Split and merge RGB Image
![Screenshot (234)](https://user-images.githubusercontent.com/75235090/162778910-65ab7be8-97e3-4346-af1d-42828cdd1a1d.png)

![Screenshot (235)](https://user-images.githubusercontent.com/75235090/162778933-f93ec04e-3990-4f07-9682-f5a329fc6860.png)

![Screenshot (236)](https://user-images.githubusercontent.com/75235090/162778952-1c5b2827-d2f6-4827-abcb-bedf95a6c45e.png)

![Screenshot (237)](https://user-images.githubusercontent.com/75235090/162778972-e945c5c8-c10b-4bcc-a48f-f8ccf71b8927.png)

### v) Split and merge HSV Image
![Screenshot (238)](https://user-images.githubusercontent.com/75235090/162779236-4401915c-d584-4459-b1a1-ecda9104dfef.png)

![Screenshot (239)](https://user-images.githubusercontent.com/75235090/162779254-e324e9dc-bfe4-43a5-a99c-db5dd429f727.png)

![Screenshot (240)](https://user-images.githubusercontent.com/75235090/162779320-1d10930c-0b51-4e46-acf4-76b55e29508d.png)

![Screenshot (241)](https://user-images.githubusercontent.com/75235090/162779347-63e7a03c-daa1-4190-ad29-a607e4314b84.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
