
# 4) Text detection: Tesseract vs Easyocr vs AWS Textract | What is the best OCR?

https://youtu.be/CcC3h0waQ6I?si=s-4CkD5yroNw45qD

# prepare data:
- !scp  '/content/drive/MyDrive/archive.zip' '/content/archive.zip'
- !unzip '/content/archive.zip' -d '/content/'

  - !scp => Secure Copy the file in google colab
  - !unzip => Unzip the zip file and put in d path (destination folder)
-!apt install tesseact-ocr
- !apt install libtesseract-dev
- !pip install pytesseract
- !pip install Pillow
- !pip install easyocr
- !pip install boto3
    - Pillow is a Python library used for opening, manipulating, and saving image files.
  # Text Detection:
  1 ) pytesseract:
     
- import pytesseract
- from PIL import Image
- image_path="/content/images/10.jpg"
- text=pytesseract.image_to_string(Image.open(image_path), lang='eng') #language=English
- print(text)
- output:
- <img width="280" height="182" alt="image" src="https://github.com/user-attachments/assets/2cdaf776-25fd-42be-8ca9-ff6d910e63fd" />

    -  We don’t need any preprocessing for below text detection

2 ) easyocr :
- from easyocr import Reader
- reader=Reader(['en'])
- results=reader.readtext(image_path)
- for result in results:
-   print(result[1])
- output:
- <img width="387" height="277" alt="image" src="https://github.com/user-attachments/assets/15a3e93a-a9b4-4b10-a2f7-9459afb3ac42" />

3 ) Amazon Textract:

- We have to connect to AWS account:
- <img width="600" height="444" alt="image" src="https://github.com/user-attachments/assets/2cd02cf8-c39f-4ddc-8df4-84cb795cbbdf" />
- IAM
- <img width="309" height="250" alt="image" src="https://github.com/user-attachments/assets/9c1d4e19-26f5-46ac-bd62-ed54c1a9e4dc" />
- User > create User
- <img width="234" height="339" alt="image" src="https://github.com/user-attachments/assets/87f4712a-e532-43c2-aa3d-452559afcc37" />
- <img width="285" height="201" alt="image" src="https://github.com/user-attachments/assets/37eb1b4a-80b3-4875-8562-76a385d3f705" />
- next > attach policies directly
- <img width="877" height="186" alt="image" src="https://github.com/user-attachments/assets/31b09372-fec5-47fd-a502-c508c4d448ef" />
- Search for AmazonTextractFullAscces
- <img width="432" height="180" alt="image" src="https://github.com/user-attachments/assets/8925ba4e-cb71-46da-8389-66d3ae50edb1" />
- Next > create user
- select the desire user that we created:
- <img width="347" height="253" alt="image" src="https://github.com/user-attachments/assets/d77f132f-34a3-4635-b922-c0dd37c2e1f0" />
- Click on Security credentials
- <img width="381" height="261" alt="image" src="https://github.com/user-attachments/assets/9258d956-5c84-4066-b5fc-c3905fae86c6" />
- create access key
- <img width="902" height="124" alt="image" src="https://github.com/user-attachments/assets/fb6ff25a-0dd5-405d-8859-a230d6ad6099" />
-local code
- <img width="307" height="175" alt="image" src="https://github.com/user-attachments/assets/3db910da-04d9-46e9-a7a1-d1f554f04812" />
- <img width="117" height="77" alt="image" src="https://github.com/user-attachments/assets/0acd3f36-2b21-4249-a5bb-885cf410cc95" />
-  next> create access key
-  Tip: we have to pay for using this aws service
-  Now, we supposed that we created an access key > go into google colab and write a python code
-  <img width="604" height="301" alt="image" src="https://github.com/user-attachments/assets/c7ade84d-454f-42da-901a-707846d0f131" />
- output: <img width="189" height="31" alt="image" src="https://github.com/user-attachments/assets/433ca335-750a-4727-872c-96e8705cf22d" />

# Compare performances for 3 different wat for text extraction:

















- 




  
