# Color Conversion
## AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 library and upload the image or capture an image.

### Step2:

Read the saved image using cv2.imread("filename.jpg").

### Step3:

Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:

Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])

### Step5:

Output the image using cv2.imshow("OUTPUT", image)

## Program:

## Developed By: KAYALVIZHI M
## Register Number: 212220230024

# i) Convert BGR and RGB to HSV and GRAY
```python

import cv2
house_color_image = cv2.imread("img.jpg")
cv2.imshow('212220230024',house_color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)

hsv_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)

gray_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
# ii) Convert HSV to RGB and BGR
```python

RGB_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV TO RGB',RGB_image)

BGR_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV TO BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii) Convert RGB and BGR to YCrCb
```python

YCrCb_image = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB to YCrCb',YCrCb_image)

YCrCb_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR to YCrCb',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iv) Split and Merge RGB Image
```python

blue = RGB_image[:,:,0]
green = RGB_image[:,:,1]
red = RGB_image[:,:,2]
cv2.imshow("R plane",red)
cv2.imshow("G plane",green)
cv2.imshow("B plane",blue)
p=cv2.merge((blue,green,red))
cv2.imshow("merged",p)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
# iv) Split and merge HSV Image
```python

h, s, v = cv2.split(hsv_image)
cv2.imshow("h plane",h)
cv2.imshow("s plane",s)
cv2.imshow("v plane",v)
merged = cv2.merge((h,s,v))
cv2.imshow("merge",merged)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### i) BGR and RGB to HSV and GRAY

![img2](https://user-images.githubusercontent.com/75413726/162756260-5c59e483-0548-4049-96d2-2e0de53265d8.jpg)
![img3](https://user-images.githubusercontent.com/75413726/162756291-5fff6aac-54bc-4ef7-8695-0ff4622b364f.jpg)


### ii) HSV to RGB and BGR

![img4](https://user-images.githubusercontent.com/75413726/162756398-70898eb7-77c4-4bae-b806-db63e066342c.jpg)


### iii) RGB and BGR to YCrCb

![img5](https://user-images.githubusercontent.com/75413726/162756449-cac1aa29-9a74-4bc8-a741-fccd39f4a21a.jpg)

### iv) Split and merge RGB Image

![img6](https://user-images.githubusercontent.com/75413726/162756511-8ebd5bfc-3fb9-4103-ba48-691eaab6ba3f.jpg)


### v) Split and merge HSV Image

![img7](https://user-images.githubusercontent.com/75413726/162756561-13cd6412-5947-4116-a156-c2e869461565.jpg)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
