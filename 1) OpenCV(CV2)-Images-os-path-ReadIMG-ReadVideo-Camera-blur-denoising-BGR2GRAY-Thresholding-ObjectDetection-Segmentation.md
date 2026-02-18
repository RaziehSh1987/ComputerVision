# Day 2) OpenCV(CV2)-Images-os-path-ReadIMG-ReadVideo-Camera-blur-denoising-BGR2GRAY-Thresholding-ObjectDetection-Segmentation

- https://youtu.be/eDIj5LuIL4A?si=qztFKz0kD9dV_gD1
<img width="715" height="584" alt="image" src="https://github.com/user-attachments/assets/2cfd97fb-a43b-4573-958a-6166e639200c" />
<img width="694" height="674" alt="image" src="https://github.com/user-attachments/assets/4c8c9818-4387-46ae-90e8-43979e054fbb" />
<img width="684" height="422" alt="image" src="https://github.com/user-attachments/assets/00ff36e3-0b64-4d1e-9f42-3783ae6948eb" />
<img width="672" height="259" alt="image" src="https://github.com/user-attachments/assets/fe403b5c-e268-4b6a-ae71-8aa406283439" />
<img width="631" height="663" alt="image" src="https://github.com/user-attachments/assets/fb246384-87eb-4a7a-9577-9730d95b1107" />
 
# Access to Path with os:
- import OS:
- <img width="623" height="88" alt="image" src="https://github.com/user-attachments/assets/ee9ad098-f1ac-4533-804f-fde6a3f1fb57" />


 # Read Image with OpenCV
## Input and Output:
- cv2.imread()
- cv2.imwrite()
- Ex:
- <img width="705" height="668" alt="image" src="https://github.com/user-attachments/assets/895bcf42-0838-4302-8079-fae04e24a241" />
<img width="728" height="227" alt="image" src="https://github.com/user-attachments/assets/976105c0-a76f-4e43-b006-c9157b3ecb7c" />

##  Read & Write image⇒  cv2.imread() / .imwrite()
<img width="727" height="433" alt="image" src="https://github.com/user-attachments/assets/69122303-353f-4a79-9bb7-e301f0f2c1ab" />
## Visualize image:
<img width="335" height="154" alt="image" src="https://github.com/user-attachments/assets/3415f27f-7ad3-482f-b197-041ac7c127e3" />
- cv2.waitkey(5000)  ⇒ it means the image be open in 5 millisecond
# Read video:
<img width="650" height="333" alt="image" src="https://github.com/user-attachments/assets/4d9fd6ce-0830-40e6-b4cb-d7e37c1b133f" />
 ## Visualize video:
 - cv2.videocapture() ⇒ for read the video
- video.read() ⇒ return 2 values ⇒ frame and ret : when there is a frame so ⇒ ret=true otherwise ret=false
- cv2.wiatkey(40) ⇒
  - <img width="312" height="197" alt="image" src="https://github.com/user-attachments/assets/9f73616d-fdf5-4534-9a2e-27ee6a1ab5c5" />
<img width="458" height="317" alt="image" src="https://github.com/user-attachments/assets/a412b4a5-e3de-481a-a3b2-3c61600545eb" />
- video.Realease () ⇒ release memory from opencv ⇐ this is so important
- cv2.destroyAllWindows()
<img width="451" height="405" alt="image" src="https://github.com/user-attachments/assets/9399363e-34e6-488b-82ae-b28b0ec92618" />
- Ex:
- <img width="708" height="440" alt="image" src="https://github.com/user-attachments/assets/76426970-4603-4cba-9d44-1ba3c783b754" />
- Output:
- <img width="586" height="363" alt="image" src="https://github.com/user-attachments/assets/4adece10-ab7c-4be7-bf74-357643de640d" />

# Read from Webcam:
- Read webcam:
- cv2.videoCapture(webcam’s number like 2) ⇒ here we have more than 1 webcam attached to our computer so we chose number 2 that is id of our webcam
- <img width="366" height="146" alt="image" src="https://github.com/user-attachments/assets/8dcc7f31-3fc5-47e3-ab9b-63fea0fa0ca7" />
- Visualize webcam:
- While True ⇒ means until webcam works
- Read from webcam with id=2
- <img width="529" height="379" alt="image" src="https://github.com/user-attachments/assets/2c8c2c11-25af-4948-a879-608a13cdf601" />
- 0xFF ⇒ until the user press “q” for close webcam
- Ex:
- <img width="476" height="300" alt="image" src="https://github.com/user-attachments/assets/69576114-e797-4a4e-83b8-2659227f8031" />
- output:
- <img width="607" height="300" alt="image" src="https://github.com/user-attachments/assets/68650ae9-724d-426b-94b1-545f44c24da4" />
# Basic Operations:
## Resize image:
- cv2.resize(img,(x,y))
- <img width="625" height="720" alt="image" src="https://github.com/user-attachments/assets/b3d97792-c4aa-4f9a-9542-8875ea16685f" />
- Note: Dynamic Resize ⇒ using image.shape[:2]
- <img width="536" height="102" alt="image" src="https://github.com/user-attachments/assets/f8cd3bd7-8eea-46f4-ab6b-90ac4435013e" />
## Crop image:
- <img width="633" height="509" alt="image" src="https://github.com/user-attachments/assets/af4e5657-021e-4b49-8a74-67a804dd629b" />
## Colorspaces:
- <img width="437" height="30" alt="image" src="https://github.com/user-attachments/assets/76988fdf-aafc-475f-ac8a-8da7ce7e402d" />
<img width="621" height="546" alt="image" src="https://github.com/user-attachments/assets/716d7d8b-3eb5-415c-91e0-e889f2d018f2" />
<img width="619" height="220" alt="image" src="https://github.com/user-attachments/assets/249b93a2-bde1-473d-8f4e-ff96e954a465" />

## Bluring:
<img width="659" height="350" alt="image" src="https://github.com/user-attachments/assets/85813ab9-3b1e-4972-83d0-35ccd78370a6" />
# Denoising:
- <img width="635" height="278" alt="image" src="https://github.com/user-attachments/assets/0188bdca-cad9-4fed-ab4c-a97c8668b20d" />
<img width="532" height="460" alt="image" src="https://github.com/user-attachments/assets/fff32894-38d5-45d1-81ba-3811e80fcff2" />

## Image Thresholding:
- Image thresholding is a technique used to convert a grayscale image into a binary image (black and white).
- <img width="315" height="218" alt="image" src="https://github.com/user-attachments/assets/bc5ef59b-981b-456a-90eb-d75b193e82fb" />
- It helps separate objects from the background.
- We have 2 kind of thresholding:
 - Simple thresholding
 - Adaptive thresholding
- Simple Idea:
   - You choose a number (called threshold).
     - If pixel value > threshold → make it white
     - If pixel value ≤ threshold → make it black
- Example:
  - Grayscale pixel values range from 0 to 255:
     -  0 = black
     -  255 = white
  - If threshold = 127:
     - 200 → becomes white
     - 50 → becomes black
-  Why Use Thresholding?
   - It is used to:
      - Detect objects
      - Detect text
      - Segment foreground from background
      -  Prepare image for contour detection
      -  Improve computer vision processing
1)
## Simple Threshold:
- Ex:
   - first we have to convert RGB to GrayScale image
   - Next we use Threshold command to define:
      - 80 ⇒ is thresh that define the pixel  color value under this number convert to 0 that is black and above this value consider 255 that is white
      - It return 2 value ⇒ ret and final image after applying threshold
     <img width="621" height="299" alt="image" src="https://github.com/user-attachments/assets/9311d320-ac80-4f82-ae6e-1e736bd7ee7d" />
     - If we user Blur command with k_size=10  before Thresholding ⇒it seems we did image segmentation like:
 <img width="629" height="392" alt="image" src="https://github.com/user-attachments/assets/ec93baf0-8673-43f8-9ccb-49fcc4024dab" />
 
2)
## Adaptive thresholding:
<img width="757" height="197" alt="image" src="https://github.com/user-attachments/assets/6a9d354b-e6d2-4f1c-8697-3f61174cf1e7" />
<img width="669" height="455" alt="image" src="https://github.com/user-attachments/assets/9e9134b8-aaa5-4953-9934-a33e62baec28" />

## Function Signature

```python
cv2.adaptiveThreshold(src, maxValue,
                      adaptiveMethod,
                      thresholdType,
                      blockSize,
                      C)
````

---

## 🔹 Arguments Explained

### 1️⃣ `src`

Grayscale input image.

---

### 2️⃣ `maxValue`

Value assigned to white pixels.
Usually `255`.

---

### 3️⃣ `adaptiveMethod`

Defines how the threshold is calculated:

* `cv2.ADAPTIVE_THRESH_MEAN_C`
  → Uses the **mean** of the neighborhood area.

* `cv2.ADAPTIVE_THRESH_GAUSSIAN_C`
  → Uses a **weighted (Gaussian) mean** of the neighborhood.

---

### 4️⃣ `thresholdType`

* `cv2.THRESH_BINARY`
* `cv2.THRESH_BINARY_INV`

---

### 5️⃣ `blockSize`

Size of the local neighborhood area used to calculate the threshold.

* Must be an **odd number**
* Example values: `11`, `15`, `21`
* Larger block size → smoother threshold result

---

### 6️⃣ `C`

Constant subtracted from the calculated mean.

**Formula:**

```
Threshold = local_mean − C
```

Used to fine-tune the threshold result.

---

## 🔹 Example

```python
th = cv2.adaptiveThreshold(
    img,
    255,
    cv2.ADAPTIVE_THRESH_MEAN_C,
    cv2.THRESH_BINARY,
    11,
    2
)
```






 






























 
















 
















