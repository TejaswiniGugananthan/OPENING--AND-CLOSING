# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:


# Import the necessary packages
```python
import cv2
import numpy as np
```


# Create the Text using cv2.putText

```python
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'Telecast', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)

```

# Create the structuring element

```python
struct_ele = np.ones((9, 9), np.uint8)

```

# Use Opening operation
```python
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)

```



# Use Closing Operation


```python
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)

```
## Output:

### Display the input Image

<img width="603" alt="image" src="https://github.com/TejaswiniGugananthan/OPENING--AND-CLOSING/assets/121222763/6d4777fb-c35e-423c-87c3-6695640dddc5">


### Display the result of Opening

<img width="571" alt="image" src="https://github.com/TejaswiniGugananthan/OPENING--AND-CLOSING/assets/121222763/de9b815c-5789-47f6-97dc-32610b49fe2e">


### Display the result of Closing

<img width="532" alt="image" src="https://github.com/TejaswiniGugananthan/OPENING--AND-CLOSING/assets/121222763/26d909f1-d571-41d1-8977-28ccf399dd85">


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
