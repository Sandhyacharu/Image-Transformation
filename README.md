### EX NO: 02
### DATE:
# <p align="center">IMAGE TRANSFORMATION</p>

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and image for transformation.

### Step2:
Perform operations on the image like translaton, rotation and other.

### Step3:
Use the warpPerspective(image , matrix, (rows, columns)) function.

### Step4:
Plot the Image and Transformed Image on the graph using matplotlib for identifying changes.

### Step5:
Diifferent operations has been performed on the image.

## Program:
```
### Developed By: N Sandhya Charu
### Register Number: 212220230041
```
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("cock.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
```
### i)Image Translation
```python
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
```
### ii) Image Scaling
```python
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
### iii)Image shearing
```python
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
### iv)Image Reflection
```python
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```
### v)Image Rotation
```python
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
### vi)Image Cropping
```python
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![image](https://user-images.githubusercontent.com/75235167/166093715-8ed53cfd-546f-4327-baf0-45c119f4091a.png)

### ii) Image Scaling
![image](https://user-images.githubusercontent.com/75235167/166093735-21b4aaca-8f01-4b01-b10c-d1d615e043f2.png)

### iii)Image shearing
![image](https://user-images.githubusercontent.com/75235167/166093754-b6cbcb16-ad93-4af2-a1de-ac76c7b11a88.png)

### iv)Image Reflection
![image](https://user-images.githubusercontent.com/75235167/166093765-0194d90a-ad8c-4392-a2b9-be00b14bab61.png)

### v)Image Rotation
![image](https://user-images.githubusercontent.com/75235167/166093794-a96090f7-e9e8-4f57-932f-baa7cba07330.png)

### vi)Image Cropping
![image](https://user-images.githubusercontent.com/75235167/166093811-914762e6-534d-48ed-a87d-cf2cc40c513d.png)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
