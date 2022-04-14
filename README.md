# Color Conversion
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
```
# Developed By:U.BHAVYA
# Register Number:212220230055
# i) Convert BGR and RGB to HSV and GRAY

import cv2
image=cv2.imread("cricket.jpg")
cv2.imshow("212220230055",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("212220230055",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("212220230055",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("212220230055",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![dip exp-3 image 1](https://user-images.githubusercontent.com/75235293/163441381-faa7063a-7c7b-452a-b48a-56ab24c6f79b.png)

![dip exp-3 image 2](https://user-images.githubusercontent.com/75235293/163441448-86a4bf94-c08b-43f8-8b58-0de061194c35.png)


### ii) HSV to RGB and BGR

![dip exp-3 image 3](https://user-images.githubusercontent.com/75235293/163441456-a2c60f2c-1356-4efa-92a5-a017dc38b302.jpg)


### iii) RGB and BGR to YCrCb

![dip exp-3 image 4](https://user-images.githubusercontent.com/75235293/163441469-fdb2783b-4336-4281-9df5-0d2dba110157.jpg)

### iv) Split and merge RGB Image

![dip exp-3 image 5](https://user-images.githubusercontent.com/75235293/163441499-2330e06e-26b0-4a5d-a0c4-352506bc38d4.jpg)

### v) Split and merge HSV Image

![dip exp-3 image 6](https://user-images.githubusercontent.com/75235293/163441520-793eef93-8ecb-476b-8266-4985423197e8.jpg)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
