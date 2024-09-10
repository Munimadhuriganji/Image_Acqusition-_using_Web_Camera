# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera.

### Step 2:
Use cv2.imread to read the video or image.

### Step 3:
Use cv2.imwrite to save the image.

### Step 4:
Use cv2.imshow to show the video.

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:

### Developed By:GANJI MUNI MADHURI
### Register No: 212223230060
## i) Write the frame as JPG file
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('bottle',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()                  
```

## ii) Display the video
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('bottle',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


## iii) Display the video by resizing the window
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('Video',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```


## iv) Rotate and display the video
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('Rotated Video',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
## Output

### i) Write the frame as JPG image
![328526487-3d11e716-7055-434b-9f7c-5d0f73959aa9](https://github.com/Nethraa24/Image_Acqusition-_using_Web_Camera/assets/121215786/06d830bc-9692-409c-8450-cc11fe0be4d4)


### ii) Display the video
![328526487-3d11e716-7055-434b-9f7c-5d0f73959aa9](https://github.com/Nethraa24/Image_Acqusition-_using_Web_Camera/assets/121215786/a2e727a7-371e-4f3a-99d0-63983ae04e17)


### iii) Display the video by resizing the window

![328528088-6ff05ba2-38e9-4b8d-97d1-d9d34b3188cc](https://github.com/Nethraa24/Image_Acqusition-_using_Web_Camera/assets/121215786/b31dc810-b939-4814-b310-bdafc0fa1da1)

### iv) Rotate and display the video
![328528946-7e08e184-b339-46ad-8fb2-7b3af2213442](https://github.com/Nethraa24/Image_Acqusition-_using_Web_Camera/assets/121215786/5b97de36-f304-4bca-bcba-7833124d6b94)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
