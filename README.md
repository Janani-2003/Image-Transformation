# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the required packages.

### Step2:
<br>load the image file in the program.

### Step3:
<br>Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
<br>Display the modified image output.

### Step5:
<br>End the program.

## Program:
```python
Developed By: JANANI R
Register Number: 212221230039

import cv2
import numpy as np
import matplotlib.pyplot as plt
image=cv2.imread('minion.jpg')
img=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
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
### Original image
![org](https://user-images.githubusercontent.com/94288340/235204143-6ac29c6e-451c-472e-8bfb-1ff1b0ff1676.png)

### i)Image Translation
![trans](https://user-images.githubusercontent.com/94288340/235203266-837807e7-e106-4db6-b209-4a006bc82b38.png)


### ii) Image Scaling
![scl](https://user-images.githubusercontent.com/94288340/235203298-6e832394-3d95-4f19-9429-9cd7258efcdb.png)



### iii)Image shearing
![shear](https://user-images.githubusercontent.com/94288340/235203337-00a62302-e73a-4dc7-82e4-dd3646687552.png)



### iv)Image Reflection
![rotate](https://user-images.githubusercontent.com/94288340/235203376-ebabf5d3-de0a-485e-87ee-7e8acfc5311b.png)




### v)Image Rotation
![rot](https://user-images.githubusercontent.com/94288340/235203412-24537318-8c4e-4143-ae10-77dae54e9033.png)




### vi)Image Cropping
![crop](https://user-images.githubusercontent.com/94288340/235203437-eadc7048-d4fa-4123-886d-75bdc002847f.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
