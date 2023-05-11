# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Plot the images using plt.imshow.
 
## Program:

```
Developed by :DEEPIKA.J
Registeration Number:212221230016
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"DEEPIKA.J",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')



# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))



# Use Opening operation
image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')




# Use Closing Operation
image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
![QQ1](https://github.com/21005688/Opening-and-Closing/assets/94747031/8c3f41f7-fccc-49db-9eef-7243f1ee09ea)


### Display the result of Opening

![QQ2](https://github.com/21005688/Opening-and-Closing/assets/94747031/14c83b5f-7fd4-41e7-957d-32462f2d9ed7)

### Display the result of Closing
![QQ3](https://github.com/21005688/Opening-and-Closing/assets/94747031/4905c1f7-5fc9-4a6c-b2ba-30bebb43f7f8)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
