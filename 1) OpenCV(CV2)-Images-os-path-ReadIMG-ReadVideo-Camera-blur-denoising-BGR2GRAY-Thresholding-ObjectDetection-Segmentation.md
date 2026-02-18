# Day 2) OpenCV(CV2)-Images-os-path-ReadIMG-ReadVideo-Camera

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

#Read from Webcam:
- Read webcam:
- cv2.videoCapture(webcam’s number like 2) ⇒ here we have more than 1 webcam attached to our computer so we chose number 2 that is id of our webcam
- <img width="366" height="146" alt="image" src="https://github.com/user-attachments/assets/8dcc7f31-3fc5-47e3-ab9b-63fea0fa0ca7" />
- Visualize webcam:
- While True ⇒ means until webcam works













 
















