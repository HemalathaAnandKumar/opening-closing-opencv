# Opening and Closing Operations Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

- Morphological Opening
- Morphological Closing

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create or load an input image containing foreground objects.

### Step 3:

Display the original image.

### Step 4:

Create a structuring element (kernel) of suitable size.

### Step 5: Opening Operation

- Apply the Opening operation using the structuring element.
- Opening consists of Erosion followed by Dilation.
- Remove small foreground noises while preserving the shape of larger objects.
- Display the opened image.

### Step 6: Closing Operation

- Apply the Closing operation using the structuring element.
- Closing consists of Dilation followed by Erosion.
- Fill small holes and gaps within foreground objects.
- Display the closed image.

### Step 7:

Compare the original, opened, and closed images.

## Program

## Developed By

**Name:** Hemalatha.A

**Register No:**212224240056

## Output

### Original Image
```
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((300, 500), dtype=np.uint8)

cv2.putText(image, "MORPHOLOGY", (30, 150),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, 255, 5)

plt.imshow(image, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.show()
```
<img width="653" height="429" alt="639295754-7621a9d0-82ee-47e0-8e18-417d7d65d676" src="https://github.com/user-attachments/assets/575e6e3e-1d80-4bce-b2de-308794fca3df" />


### Opening Operation

```
kernel = np.ones((5, 5), np.uint8)

opening = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

plt.imshow(opening, cmap="gray")
plt.title("Opening Operation")
plt.axis("off")
plt.show()
```
<img width="665" height="427" alt="639295926-9ba5a735-ba37-468c-b66a-6bd7af05c84a" src="https://github.com/user-attachments/assets/39af4765-bf00-4cb8-aea9-3d42b0a1f10d" />

### Closing Operation

```
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

plt.imshow(closing, cmap="gray")
plt.title("Closing Operation")
plt.axis("off")
plt.show()
```
<img width="655" height="429" alt="639296059-85d2bce4-2a51-4603-a211-e60fe57340d2" src="https://github.com/user-attachments/assets/abc49b87-4cc8-43f8-a9b2-b6f7fc3174e0" />


- Original image is displayed.
- Closed image is displayed.
- Small holes and gaps inside objects are filled.
- Broken regions are connected.
- Object boundaries become more continuous.
## Comparison of three:
<img width="1198" height="269" alt="639296410-46f4a81c-9e5b-489c-9db1-208cad0630d9" src="https://github.com/user-attachments/assets/c03d5ae6-da5f-4c67-8f62-b0ad11243962" />


## Applications

### Opening

- Noise removal in binary images.
- Separation of connected objects.
- Preprocessing for object detection.

### Closing

- Filling small holes in objects.
- Connecting nearby components.
- Enhancing segmented regions.

## Advantages

### Opening

- Removes unwanted foreground noise.
- Preserves major object structures.
- Improves segmentation quality.

### Closing

- Restores object continuity.
- Eliminates small background gaps.
- Improves object representation.

## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV. 
