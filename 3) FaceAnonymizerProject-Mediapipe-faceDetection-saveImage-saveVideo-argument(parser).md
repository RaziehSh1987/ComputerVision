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







- 



