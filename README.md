## EX 1: COLOR_CONVERSIONS_OF-IMAGE
## DATE:
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
### Developed By: KANCHARLA NARMADHA
### Register Number: 212222110016



### i) Read and display the image
```
import cv2
image=cv2.imread('image.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('Narmadha',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:
![DIP](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/d5156a93-8fca-49c7-90fc-c3b4e412aed7)


### ii)Write the image

```
import cv2
image=cv2.imread('image.jpg',0)
cv2.imwrite('cat.jpg',image)

```
### OUTPUT:

<br>![DIP 2](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/d072068c-36f4-44eb-b79b-0e9666fecd5b)

### iii)Shape of the Image

```
    import cv2
    image=cv2.imread('image.jpg',1)
    print(image.shape)
```
### OUTPUT:
![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/0e993f32-b545-4b18-9801-043c044d0c53)

### iv)Access rows and columns
```
 import random
    import cv2
    image=cv2.imread('image.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/203cbe4f-467d-4487-9696-5641debfddda)



### v)Cut and paste portion of image
```
 import cv2
   image=cv2.imread('image.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
### OUTPUT:
![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/74786eaf-2d81-4c82-9084-f3660b9d2c4b)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('image.jpg',1)
img = cv2.resize(img,(300,200))
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
### OUTPUT:

![dip 6 1](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/ed2f3e1c-14a8-4176-ab79-7112a63da785)

![dip 6 2](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/c4c7c983-e8a8-4040-8cb8-51ca09e421f6)

![dip 6 3](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/5e2a99af-93a9-4934-a080-e3da8277d149)

![dip 6 4](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/af07144e-eda9-49c9-b29b-7cec77a14b24)

![dip 6 5](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/d91e9a85-ffb6-4379-ba79-f6354c107606)

### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('image.jpg')
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
### OUTPUT:
![dip 7 1](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/444a43b6-4cf5-46c6-b2f6-ae02ce42c83e)

![dip 7 2](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/faf4dc11-d338-4fca-81da-e58472efbb39)

![dip 7 3](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/07db5a4b-fc86-4dbb-ac3f-de8a896bc106)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('image.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![dip 8 1](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/740ed729-3ccd-45df-a365-269b4c5835ad)

![dip 8 2](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/398be87e-9d7f-4224-a26a-32e3661f3bbe)

![dip 8 3](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/d10b5c60-40cc-4d54-a519-062f613cf618)

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('image.jpg',1)
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
### OUTPUT:

![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/19f59a0a-c699-41bb-9fb4-c935c491b4bb)

![dip 9 2](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/d99d425e-85cc-4e29-8b49-649d16bb569b)

![dip 9 3](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/46d42137-294c-47af-9266-758753779fce)

![dip 9 4](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/0bb06c50-e2df-4cae-83c6-2ba00a1e6df8)


### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("image.jpg",1)
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
### OUTPUT:
![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/a63ddea8-cfa9-4fe5-b6a9-372d0ab5880c)


![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/afbc9ba4-fc8f-4927-bd1d-02205b6967fd)

![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/402d211e-cbff-4fc5-97df-2b0dc2fb5f79)

![image](https://github.com/kancharlaNarmadha/COLOR_CONVERSIONS_OF-IMAGE/assets/119559316/e0e59dea-0f29-4ccf-a8ba-8bfb1104309c)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







