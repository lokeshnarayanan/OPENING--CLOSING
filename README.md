# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries: OpenCV (cv2), NumPy (np), and Matplotlib (plt).
### Step2:
Use cv2.putText to add the text "THE BOYS" to the image at coordinates (10, 70) with a font size of 2 and white color (255).


### Step3:
Use cv2.getStructuringElement to create a kernel (structuring element) for morphological operations. In this case, it's a rectangular kernel of size (9, 9).


### Step4:
Use cv2.morphologyEx with the cv2.MORPH_CLOSE operation to perform a closing operation on the original image.



### Step5:

Use plt.show() to display the entire figure with the subplots
 
## Program:

``` Python

import cv2
import numpy as np
import matplotlib.pyplot as plt


img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'LOKESH N',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)

kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
cv2.imshow("Opening image",image_open)

image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
cv2.imshow("Closing Image",image_close)

cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image
![Screenshot from 2023-10-11 16-18-06](https://github.com/lokeshnarayanan/OPENING--CLOSING/assets/119393019/e0109211-bb02-494d-9d54-865c057e1bde)


### Display the result of Opening

![Screenshot from 2023-10-11 16-17-48](https://github.com/lokeshnarayanan/OPENING--CLOSING/assets/119393019/4e457dad-b4e1-4c7d-aa52-36df578bbaf1)

### Display the result of Closing
![Screenshot from 2023-10-11 16-17-37](https://github.com/lokeshnarayanan/OPENING--CLOSING/assets/119393019/f946ba0c-3ddb-4dbf-80c4-57de0ccb6c66)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
