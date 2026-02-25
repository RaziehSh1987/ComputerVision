5) Train Detectron2
https://youtu.be/I7O4ymSDcGw?si=rLhoMmlN6aw0l8N4
<img width="709" height="554" alt="image" src="https://github.com/user-attachments/assets/c8accafd-789f-4692-8980-cfde47f60570" />
- I need to install these libraries:
    - If we couldn't install it ⇒ Maybe the Python version is too high and we need to add a new interpreter (for example, Python 3.9 or 3.10) and install it.
- <img width="618" height="164" alt="image" src="https://github.com/user-attachments/assets/ea98e03b-0b2a-4414-9e1d-1c343672c98a" />
- Also we need to create these python files:
<img width="837" height="70" alt="image" src="https://github.com/user-attachments/assets/12cb0061-730a-4ff7-8ae9-00b9a642e482" />

# Train.py file:
- <img width="699" height="69" alt="image" src="https://github.com/user-attachments/assets/10914346-1f7b-4638-b9c9-ab1d9467a8fb" />
- Detectron 2 use of Yolo format for annotation ==> class is class id and xc , yc are position of the center of bounding box of annotation and  w,y are width and height of the bounding box.example:
- <img width="857" height="93" alt="image" src="https://github.com/user-attachments/assets/1de96885-bb2f-461d-873d-7342c8f8d409" />
- Annotation is the process of labeling data — such as drawing bounding boxes, marking keypoints, or defining segmentation masks — to create ground-truth information for training and evaluating machine learning models.
- We saved images and their annotation in Data folders:
- <img width="490" height="360" alt="image" src="https://github.com/user-attachments/assets/5ca1b2a7-85f0-4092-8584-268c73ab7141" />
annoation for training ==> <img width="483" height="218" alt="image" src="https://github.com/user-attachments/assets/9c7270ff-ecae-4264-ae29-7095c112dea2" />
- images for training ==> <img width="652" height="288" alt="image" src="https://github.com/user-attachments/assets/e11a35e3-74f6-4197-8a19-15d6dcd4f5bf" />
- Also we have these folders Validation test after training.
-This is what exactly we want to access them - the structure of name must be the same in train and val folders:
- <img width="535" height="686" alt="image" src="https://github.com/user-attachments/assets/5d2f6ba0-4abb-4e7b-8f90-81258a92889f" />
- Now we define ArgumentParser():
    - <img width="1096" height="383" alt="image" src="https://github.com/user-attachments/assets/994036ca-5289-4812-a91d-f49d7e29a9b2" />
    - Class.names is a text file that contains our class name , here is:
    - <img width="651" height="212" alt="image" src="https://github.com/user-attachments/assets/fbcb5580-65ff-4490-bfdf-fb358d3fc9f8" />
    - ./data is folders that contains annotations and images
    - It’s better that we define  all of the arguments here like iterations,batch-size,..
- What is ‘--model’ ? in this link there are different model of Detectron2 model Zoo that are for different task like Object Detection, Person keypoints,Segmentation, ..
https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md
- <img width="906" height="336" alt="image" src="https://github.com/user-attachments/assets/9dfad3ca-04d1-4b65-aa0f-c967e23c5558" />
























