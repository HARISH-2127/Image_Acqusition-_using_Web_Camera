# Image_Acqusition-_using_Web_Camera
## Name: HARISH S
## Register no:212224040105

## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program:
### Developed By: HARISH S
### Register No: 212224040105


## i) Write the frame as JPG file

```PYTHON
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()

```


## ii) Display the video

```PYTHON
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iii) Display the video by resizing the window

```PYTHON

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  

```


## iv) Rotate and display the video

```PYTHON
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 
```

## Output

### i) Write the frame as JPG image
</br>
<img width="615" height="489" alt="image" src="https://github.com/user-attachments/assets/70b5e1c7-051a-410c-a1eb-7ebd02db582c" />

</br>


### ii) Display the video
</br>
<img width="611" height="465" alt="image" src="https://github.com/user-attachments/assets/8b1a8e6c-40bf-4656-a642-b158f0b17a05" />

</br>


### iii) Display the video by resizing the window
</br>
<img width="318" height="465" alt="image" src="https://github.com/user-attachments/assets/9e7184e5-d957-43bc-8514-075d07c612f6" />

</br>



### iv) Rotate and display the video
</br>
<img width="359" height="461" alt="image" src="https://github.com/user-attachments/assets/b843380f-a190-4e64-a0df-a70e2cadd6cd" />

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
