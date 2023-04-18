# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output.

### Step5:
End the program.

## Program:
```python
Developed By: DHANASHREE M
Register Number: 212221230018

import cv2
import numpy as np
import matplotlib.pyplot as plt
img=cv2.imread('mount.jfif')
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(img)
plt.show()
rows,cols,dim=img.shape

i)Image Translation

m=np.float32([[1,0,100],[0,1,200],[0,0,1]])
t_img=cv2.warpPerspective(img,m,(cols,rows))
plt.axis('off')
plt.imshow(t_img)
plt.show()


ii) Image Scaling

n=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
s_img=cv2.warpPerspective(img,n,(cols*2,rows*2))
plt.axis('off')
plt.imshow(s_img)


iii)Image shearing

o_x=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
p_y=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sh_x=cv2.warpPerspective(img,o_x,(int(cols*1.5),int(rows*1.5)))
sh_y=cv2.warpPerspective(img,p_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sh_x)
plt.imshow(sh_y)
plt.show()



iv)Image Reflection

rows,cols,dim=img.shape
q_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
q_y=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
r_img=cv2.warpPerspective(img,q_x,(int(cols),int(rows)))
r_img1=cv2.warpPerspective(img,q_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(r_img)
plt.show()
plt.imshow(r_img1)
plt.show()

v)Image Rotation

angle=np.radians(40)
r=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
ro=cv2.warpPerspective(img,r,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(ro)
plt.show()


vi)Image Cropping

c_img = img[120:600,120:600]
plt.axis('off')
plt.imshow(c_img)
plt.show()


```
## Output:


![dipexp51](https://user-images.githubusercontent.com/94165415/232819541-8e7ce83d-1a4b-4ac1-906a-61ba7423e24e.png)

### i)Image Translation

![dipex512](https://user-images.githubusercontent.com/94165415/232819632-344fcb56-d84b-47d1-bd60-7e0067a59f36.png)

### ii) Image Scaling

![dipex513](https://user-images.githubusercontent.com/94165415/232824890-53fc0909-81c0-4c51-92e7-65f59ce88f16.png)

### iii)Image shearing

![dipex54](https://user-images.githubusercontent.com/94165415/232828115-ba9ea210-f499-4229-bd81-75d41cae54d4.png)

### iv)Image Reflection

![dipex55](https://user-images.githubusercontent.com/94165415/232829794-7303fe8e-9f03-4416-99e6-8ed3a3e22068.png)

### v)Image Rotation

![dipex56](https://user-images.githubusercontent.com/94165415/232830329-c676bb3d-3e2b-49b9-b9f6-27521f00720d.png)

### vi)Image Cropping

![sodapdf-converted](https://user-images.githubusercontent.com/94165415/232830789-4d0779ee-fd93-47ad-a0d0-ce849abe0701.jpg)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
