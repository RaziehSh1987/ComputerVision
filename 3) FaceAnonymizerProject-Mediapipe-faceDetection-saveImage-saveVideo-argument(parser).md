# 3)FaceAnonymizerProject-Mediapipe-faceDetection-saveImage-saveVideo-argument(parser)
- <img width="614" height="154" alt="image" src="https://github.com/user-attachments/assets/a0e61b62-0bb1-43eb-81ec-3741fe4251bb" />
- These are the steps:
- <img width="257" height="158" alt="image" src="https://github.com/user-attachments/assets/96d3eb30-235a-4304-a6e8-0588d6a8cc0e" />

# Mediapipe : 
- MediaPipe is an open-source framework developed by Google for building real-time computer vision and perception pipelines.
-  It is designed for:
  - Face detection
  - Face mesh (468 facial landmarks)
  - Hand tracking
  - Pose estimation (body skeleton)
  - Object detection
  - Gesture recognition
- It works in: Python , Android , iOS , Web

- <img width="754" height="500" alt="image" src="https://github.com/user-attachments/assets/d881dea6-dbf8-4990-aa02-2593557e46f8" />
- ## Different between Mediapipe and Yolo:
- <img width="762" height="323" alt="image" src="https://github.com/user-attachments/assets/9e3feb8c-b7e6-42da-b688-ec2c15c154b2" />

## Face Detection:
- We need to call mediapipe Library ⇒ to
-  mp.solutions.FaceDetection() have 2 parameters:
    - Model_selection ⇒ use when:
        - Use 0 → For webcam / close-up applications
        - Use 1 → For surveillance / long-distance detection
    - Min_detection_confidence ⇒ Defines the minimum confidence score required for a detection to be considered valid. Range: 0.0 → 1.0
        - 0.5 (default) → Balanced detection
        - Higher value (e.g., 0.7–0.8) → Fewer false positives, stricter detection
        - Lower value (e.g., 0.3–0.4) → More detections, but higher false positives
    - face_detection .process(img) ⇒ give us the location_data and coordinated information about the face that detected

- <img width="881" height="700" alt="image" src="https://github.com/user-attachments/assets/fdac2681-4461-47b2-88b9-573617c23772" />
- <img width="412" height="512" alt="image" src="https://github.com/user-attachments/assets/bc7f703d-805f-4f6e-9278-f14dbf06b104" />
## blur image:
- img= cv2.blur(img,(50,50))
- cv2.imshow(“img”,img)
- <img width="386" height="464" alt="image" src="https://github.com/user-attachments/assets/4e771975-ef5c-45a1-a30d-d2ed0ca5ce3e" />
- Now just blur the face selection:
- <img width="875" height="196" alt="image" src="https://github.com/user-attachments/assets/6a682fc7-c295-482f-8cf5-9fafbd5e46b1" />
- <img width="370" height="467" alt="image" src="https://github.com/user-attachments/assets/eecc81da-e5eb-48a1-ba7d-63fc4ded6dd6" />
## Save image:
- Use os library to address to the output location
- Use cv2.imwrite ⇒ to save an image
- <img width="597" height="371" alt="image" src="https://github.com/user-attachments/assets/2e343b05-bb32-4e73-8c45-2bb945560172" />
- <img width="873" height="200" alt="image" src="https://github.com/user-attachments/assets/f7b38971-6b9c-4178-a016-06582f32b47c" />
- <img width="587" height="244" alt="image" src="https://github.com/user-attachments/assets/d02bde80-609d-43f7-955c-d9040b853b9b" />
- Entire code for face detection and Blur its:
- <img width="916" height="767" alt="image" src="https://github.com/user-attachments/assets/8646fcc7-a9f6-46b1-8072-4774c5780a38" />
## face Detection on Video:
- To solve this problem , we have to create a function of above operations that we have done to detect and blur face ⇒ so we can call this function for each frame of webcam
- <img width="914" height="497" alt="image" src="https://github.com/user-attachments/assets/fcc14c20-bf2a-49b0-8e19-bc882522ae19" />
- And the rest of the code become like this:
- <img width="912" height="363" alt="image" src="https://github.com/user-attachments/assets/eb6d7b0d-cc72-4d5b-a354-b77d753ea78d" />

## Now, we want to write codes to define different mode to read from image or video or webcam ⇒ so we use the argparse library :
- <img width="315" height="110" alt="image" src="https://github.com/user-attachments/assets/7833de84-42e9-4ee2-8c42-5f216a7c891a" />
- <img width="802" height="244" alt="image" src="https://github.com/user-attachments/assets/4795c570-20b6-443c-8d70-e0740bfa9d4f" />
- <img width="913" height="506" alt="image" src="https://github.com/user-attachments/assets/81be5ea6-d063-4696-b609-81adc1ecd65b" />
## Read video :
- To Read video  we have to change these lines:
- <img width="836" height="219" alt="image" src="https://github.com/user-attachments/assets/efb69082-5c23-4a69-af8e-31d933171be3" />
- And also we have to add these lines, that if “mode=video” ⇒ read from videoCapture
- <img width="901" height="625" alt="image" src="https://github.com/user-attachments/assets/65c0bc07-2c94-4dde-8349-6580583eb098" />
- Output is:
- <img width="661" height="569" alt="image" src="https://github.com/user-attachments/assets/8347672a-42c4-4167-8b7e-ffcc6903ce83" />

## Read from webcam:
- If we have one camera ⇒ we must choose VideoCApture(0)
- <img width="695" height="455" alt="image" src="https://github.com/user-attachments/assets/574f43a0-01d3-42cc-b828-3aabd6a820fa" />
- We also have to change this below code to read from webcam:
- <img width="633" height="249" alt="image" src="https://github.com/user-attachments/assets/4743999a-9902-4817-b2cf-246a26560b37" />
- It means:
    - We want to read from webcam
    - There is not path to read from.



















- 


- 



- 
















- 



