# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

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
### i)Image Translation

![dipexp51](https://user-images.githubusercontent.com/94165415/232819541-8e7ce83d-1a4b-4ac1-906a-61ba7423e24e.png)

### ii) Image Scaling

![dipex512](https://user-images.githubusercontent.com/94165415/232819632-344fcb56-d84b-47d1-bd60-7e0067a59f36.png)

### iii)Image shearing



### iv)Image Reflection


### v)Image Rotation


### vi)Image Cropping


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
