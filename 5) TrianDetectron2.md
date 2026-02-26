5) Train Detectron2
- https://youtu.be/I7O4ymSDcGw?si=rLhoMmlN6aw0l8N4
- Detectron2 trained code: https://github.com/computervisioneng/train-object-detector-detectron2/tree/master

- <img width="709" height="554" alt="image" src="https://github.com/user-attachments/assets/c8accafd-789f-4692-8980-cfde47f60570" />
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
- <img width="663" height="328" alt="image" src="https://github.com/user-attachments/assets/e77032d4-3d1b-4a95-9df1-788f6caa816b" />
- <img width="535" height="686" alt="image" src="https://github.com/user-attachments/assets/5d2f6ba0-4abb-4e7b-8f90-81258a92889f" />
- Now we define ArgumentParser():
    - <img width="1096" height="383" alt="image" src="https://github.com/user-attachments/assets/994036ca-5289-4812-a91d-f49d7e29a9b2" />
    - Class.names is a text file that contains our class name , here is:
    - <img width="651" height="212" alt="image" src="https://github.com/user-attachments/assets/fbcb5580-65ff-4490-bfdf-fb358d3fc9f8" />
    - ./data is folders that contains annotations and images
    - It’s better that we define  all of the arguments here like iterations,batch-size,..
- What is ‘--model’ ? in this link there are different pretrained  model of Detectron2 model Zoo that are for different task like Object Detection, Person keypoints,Segmentation, ..
https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md
- <img width="906" height="336" alt="image" src="https://github.com/user-attachments/assets/9dfad3ca-04d1-4b65-aa0f-c967e23c5558" />
- and this is the model that we chose for our code:
- <img width="781" height="303" alt="image" src="https://github.com/user-attachments/assets/403057d0-2550-4ce3-b74f-2588f17d53ab" />
- <img width="297" height="294" alt="image" src="https://github.com/user-attachments/assets/f7bde4bc-58d0-451e-ab20-9abf19eabd69" />
- <img width="412" height="371" alt="image" src="https://github.com/user-attachments/assets/bc44b267-d74d-41c1-8e96-6114e246660a" />
- <img width="425" height="374" alt="image" src="https://github.com/user-attachments/assets/144fdb00-159f-4d12-9b35-06d1582c9605" />
- <img width="432" height="684" alt="image" src="https://github.com/user-attachments/assets/462bfecc-069a-4464-8c52-8c6b05d046a5" />

- <img width="387" height="642" alt="image" src="https://github.com/user-attachments/assets/ae580bb8-a103-47dc-9759-7c5314ea273d" />
- <img width="362" height="349" alt="image" src="https://github.com/user-attachments/assets/511f7848-75a3-4130-8623-091e981fa2c7" />
- We need to create util.py:
- <img width="1034" height="371" alt="image" src="https://github.com/user-attachments/assets/f7c6b945-f65c-4867-89c9-7f257ae38de0" />
- In Train.py file call train function which is in util.py:
- <img width="1025" height="559" alt="image" src="https://github.com/user-attachments/assets/95b912d5-4bce-4b66-8ce1-e2a208c84c47" />
- Also in util.py we need another function to read from dataset:
- <img width="1039" height="718" alt="image" src="https://github.com/user-attachments/assets/58a0478f-15c5-455d-8635-b6500360756c" />
- <img width="354" height="681" alt="image" src="https://github.com/user-attachments/assets/c1bcd0bb-6395-4947-ba5e-b0e8911685a7" />
- In util.py we define get_dicts function to read the annotation for dataset: 
- <img width="1356" height="460" alt="image" src="https://github.com/user-attachments/assets/7b6e292b-5e87-443a-902b-c5e6f09e85d8" />
- <img width="1324" height="279" alt="image" src="https://github.com/user-attachments/assets/ec281974-73e0-40b0-b42d-5122739ee9d6" />
- <img width="668" height="677" alt="image" src="https://github.com/user-attachments/assets/0925a19f-3c92-41c0-828e-c6db4340b136" />
- <img width="798" height="405" alt="image" src="https://github.com/user-attachments/assets/d2ec5610-00b8-42d9-afba-2a19f155f16a" />
- In util.py we need train function:
- <img width="1139" height="59" alt="image" src="https://github.com/user-attachments/assets/0631ff11-737a-4fcc-881a-158815aefc39" />
- <img width="1118" height="394" alt="image" src="https://github.com/user-attachments/assets/fd92103a-e1b2-472f-8823-dd84a82f5da0" />
- <img width="1300" height="657" alt="image" src="https://github.com/user-attachments/assets/5d151793-5330-4365-8e1c-a10b8d5a102f" />
trainer.resume_or_load(resume=false) ⇒ means run from scratch

- 0000000000000000000000000000000
- What is get_cfg function?
- We want to change the pretrained model configuration based on out desire configuration. So first we call _get_cfg() ⇒ then we modify our parameters with cfg.merge_from_file
- <img width="664" height="363" alt="image" src="https://github.com/user-attachments/assets/d58ebd5e-d6cd-4cb1-bf82-9bda1e91e960" />
- <img width="1228" height="540" alt="image" src="https://github.com/user-attachments/assets/cf9b7f69-01eb-4c9e-8f2b-60d1e3f90965" />
- <img width="969" height="605" alt="image" src="https://github.com/user-attachments/assets/50dacb4b-0e20-4192-a489-310b850859ab" />
- <img width="1084" height="592" alt="image" src="https://github.com/user-attachments/assets/08a76ae9-d311-40cf-aa46-bf534a721d50" />
- We need to create Validation loss function  into loss.py, because we have not that:
- <img width="787" height="471" alt="image" src="https://github.com/user-attachments/assets/d862a9bc-d1c8-4dee-8113-90c914db2715" />
- <img width="715" height="541" alt="image" src="https://github.com/user-attachments/assets/90f1a225-2ec0-4d61-8b7f-9eead144fc3e" />
<img width="763" height="676" alt="image" src="https://github.com/user-attachments/assets/d6270bf3-639f-4ef7-bfe7-2406b22ad274" />
- We also need to create plot_loss.py to plot percentage of loss function and validation of our Detectron2 model:
- <img width="868" height="479" alt="image" src="https://github.com/user-attachments/assets/f077a149-8349-4a4a-b3bf-fae8fb427241" />
- before deleting some plot code we have this plot:
- <img width="781" height="530" alt="image" src="https://github.com/user-attachments/assets/af22209c-668c-402a-9471-f54a610c1bfc" />
- But we need to disable this lines of code:
- <img width="834" height="219" alt="image" src="https://github.com/user-attachments/assets/a8ccd5cf-5e9d-41f6-9436-de5aa83561f5" />
- To have this plot:
- <img width="479" height="386" alt="image" src="https://github.com/user-attachments/assets/9870476e-daec-4895-b0d3-5e9ec3a7598f" />
- <img width="479" height="386" alt="image" src="https://github.com/user-attachments/assets/80c0f7a8-3d3c-4d01-a1ec-bf74b77f2bc2" />







# Running Detectron 2 pretrained model:
- Now, we want to run Detecron 2 on our data. We need to upload this 4 python code:
- util.py / train.py / loss.py / class.names
- we also need data file that contains train and val data(image and anotation files)
- <img width="678" height="586" alt="image" src="https://github.com/user-attachments/assets/a17d8967-c72f-4c02-96f1-aa7900b1b34d" />
- Now,in google colab: 
- <img width="731" height="401" alt="image" src="https://github.com/user-attachments/assets/7fec2abe-828d-4de3-a25e-be521439bc20" />
- we have to change our working directory to folder that contains detectron 2 files and data :
- <img width="893" height="153" alt="image" src="https://github.com/user-attachments/assets/d1ebbba8-e466-44cd-8169-a3df10d65a9a" />
- Then run this line to train Detectron 2 model (that we already created train file and define these arguments with argparse Library ):
- <img width="906" height="142" alt="image" src="https://github.com/user-attachments/assets/d854bfec-7bd4-4e93-a5b9-a3579e76b395" />
the output files save  into output folders:
- <img width="539" height="349" alt="image" src="https://github.com/user-attachments/assets/a5fb0871-35e8-42aa-8a9f-404a8cf8951f" />
- We defined check point=500 to check the validation of file after 500 epoc and we can see the output: 
- <img width="209" height="321" alt="image" src="https://github.com/user-attachments/assets/52661a03-676b-4339-9164-68f0e75c5493" />
The validation information is  in metrics.json file:
- <img width="377" height="146" alt="image" src="https://github.com/user-attachments/assets/d2efc669-6025-47ea-81d7-ff5d153f9510" />



























































