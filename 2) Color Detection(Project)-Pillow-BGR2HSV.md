
# 2) Color Detection Project
https://youtu.be/eDIj5LuIL4A?si=bR4lJ_LpMnDHkpSy
- <img width="699" height="394" alt="image" src="https://github.com/user-attachments/assets/a40b7b80-10f5-4170-b488-b5da76a570f7" />

<img width="531" height="157" alt="image" src="https://github.com/user-attachments/assets/6b682a1a-7a7a-460b-9808-01bb5ac66bf8" />

- We need to install below library with this command, I saved this in txt file:
  - opencv-python==4.6.0.66
  - numpy==1.23.4
  - Pillow==9.2.0
- Now, I install using this command:

- # Pip install -r requirements.txt
- We read image from webcam:
- <img width="451" height="377" alt="image" src="https://github.com/user-attachments/assets/842a6416-1f93-4b15-86de-c2115974d8b3" />
- <img width="408" height="203" alt="image" src="https://github.com/user-attachments/assets/ea107809-bd90-4d8e-917e-801604e21e90" />
- Below image is a top view of above image:
- <img width="206" height="205" alt="image" src="https://github.com/user-attachments/assets/70081bdb-875c-4667-9d7b-35794a7ae20b" />
- We don’t ave only one yellow color , but we have an interval of different yellow color that we have to define:
- <img width="263" height="237" alt="image" src="https://github.com/user-attachments/assets/b1d3676f-03d6-4f2b-a741-24a75bff1fb2" />
- Opencv read images in BGR format ⇒ in order to use a range of color we have to convert color to HSV
- We create this file as util.py ⇒ because we need it alot:
    - this is a color detection helper function used for HSV thresholding in OpenCV.
    - <img width="880" height="401" alt="image" src="https://github.com/user-attachments/assets/2dd10d34-5b7d-4c9f-8e84-9f76dd5a7387" />
 - def get_limits(color):
     - c = np.uint8([[color]])
     - hsvC = cv2.cvtColor(c, cv2.COLOR_BGR2HSV)
     - lowerLimit = hsvC[0][0][0] - 10, 100, 100
     - upperLimit = hsvC[0][0][0] + 10, 255, 255
     - lowerLimit = np.array(lowerLimit, dtype=np.uint8)
     - upperLimit = np.array(upperLimit, dtype=np.uint8)
     - return lowerLimit, upperLimit
  
##🎯 What This Function Enables
- This function is typically used for:
    - Real-time color tracking
    -  Object detection by color
    -   Ball tracking
    -   Marker detection
    -   Traffic light detection
    -   Simple segmentation tasks
## 🎯 What This Function Does
- It converts a given BGR color into HSV, then creates a range (lower and upper limits) around that color for masking.
This is typically used with:
<img width="689" height="97" alt="image" src="https://github.com/user-attachments/assets/aa58f1ba-f111-4275-8454-17be3ab084f1" />
- to detect objects of a specific color.
- ## 🧠 Step-by-Step Explanation
- <img width="586" height="506" alt="image" src="https://github.com/user-attachments/assets/e2e56554-025e-4cb8-8980-313a691e7f14" />
- <img width="623" height="721" alt="image" src="https://github.com/user-attachments/assets/8b130ba3-1b53-4b8c-9717-a97bb0422648" />
- <img width="584" height="797" alt="image" src="https://github.com/user-attachments/assets/af732b88-74bb-425a-b1b3-eceb899225c6" />
- <img width="625" height="637" alt="image" src="https://github.com/user-attachments/assets/0172cca3-db24-4967-a459-aa844877d5fe" />
- <img width="685" height="411" alt="image" src="https://github.com/user-attachments/assets/72266f38-b330-4d97-8bcc-4e0e0d9c1993" />
- <img width="602" height="695" alt="image" src="https://github.com/user-attachments/assets/95ba0d52-dda3-4a9d-8a13-6230e8e730b1" />
- 🔥##  Why Use HSV Instead of BGR?
- HSV is better for color detection because:
-  Hue isolates the color itself
-  Lighting changes affect BGR heavily
-  HSV is more robust to brightness variation
-  <img width="512" height="530" alt="image" src="https://github.com/user-attachments/assets/24f7236e-a8e7-4387-913b-69c3d5a1e94d" />
- <img width="797" height="723" alt="image" src="https://github.com/user-attachments/assets/9520d639-5af3-4bb2-86a9-a749cb97f277" />
- cv2.inrage()
- <img width="606" height="104" alt="image" src="https://github.com/user-attachments/assets/20f455c8-ecc4-4400-a146-e75d24442a53" />
- This creates a binary mask that isolates pixels within a specified HSV color range.
- <img width="476" height="782" alt="image" src="https://github.com/user-attachments/assets/9cf5c30f-3b72-4f90-8943-5bedeed062a6" />
- <img width="429" height="694" alt="image" src="https://github.com/user-attachments/assets/28237bdf-547f-4556-80d6-5d6419ab49ac" />
- Now ⇒ we want draw a rectangle  around yellow object
- First we have to find the mask coordinate:
- <img width="288" height="36" alt="image" src="https://github.com/user-attachments/assets/49f84865-1ccc-4e01-881b-3398bde2aaf4" /> ==> pillow library
- mask_=Image.fromarray(mask)
- bbox=_mask.getbbox() ⇒ this has 4 value to draw rectangle
- <img width="697" height="599" alt="image" src="https://github.com/user-attachments/assets/e5a38f02-3180-46e2-9358-453a7d9b5f80" />
- <img width="699" height="394" alt="image" src="https://github.com/user-attachments/assets/a40b7b80-10f5-4170-b488-b5da76a570f7" />
