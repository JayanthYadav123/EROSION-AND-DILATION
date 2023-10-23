# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
**Step1:** Import the necessary packages.

**Step2:** Create the text image using cv2.putText.

**Step3:** Then create the structuring image for dilation/erosion.

**Step4:** Apply erosion and dilation using plt.erode and plt.dilate.

**Step5:** Plot the images using plt.imshow.
 
## Program:
```
Developed By: G Jayanth Yadav
Reg No.: 212221230030

```

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"Jayanth",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Create the structuring element

kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image

image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()


# Dilate the image

image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()



```
## Output:

### Display the input Image

![image](https://github.com/JayanthYadav123/EROSION-AND-DILATION/assets/94836154/e4434077-bdbb-4aaf-acc0-6315b9f66df6)


### Display the Eroded Image

![image](https://github.com/JayanthYadav123/EROSION-AND-DILATION/assets/94836154/c210131e-3f0a-43fd-a7f8-36116529479e)


### Display the Dilated Image

![image](https://github.com/JayanthYadav123/EROSION-AND-DILATION/assets/94836154/0428b8ef-4d21-4c28-91ca-7e62facd6274)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
