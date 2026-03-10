
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

# Compare performances by Similarity metrics for 3 different way for text extraction:
- we use Jaccard index:
- <img width="586" height="304" alt="image" src="https://github.com/user-attachments/assets/9f601dc5-9592-40ea-9041-16f2fbf8c748" />
- <img width="193" height="250" alt="image" src="https://github.com/user-attachments/assets/3b9b2513-bc01-463e-8923-183fc633643f" />
- We compare by counting the number of word that is detected
- we ask ChatGPT for:
- <img width="358" height="31" alt="image" src="https://github.com/user-attachments/assets/992ed2f5-03de-454f-9e43-ee5a2bbc0381" />
- <img width="478" height="386" alt="image" src="https://github.com/user-attachments/assets/3acf3905-af72-4fbb-b59c-d0434b41d3c3" />
- now , we put all of text detection code into 3 different function :
- <img width="453" height="147" alt="image" src="https://github.com/user-attachments/assets/f1474dca-654d-4ec7-b5ed-5228f04c7105" />
- <img width="337" height="115" alt="image" src="https://github.com/user-attachments/assets/83ec381b-b5a5-46c7-8b4d-929b5d19b074" />
- <img width="501" height="187" alt="image" src="https://github.com/user-attachments/assets/1ff0b118-d32f-46b8-a21d-dc1dbb828757" />
- And change Jaccard similarity function to read the 3 text extraction output:
- <img width="578" height="278" alt="image" src="https://github.com/user-attachments/assets/bc884787-47da-4039-8877-738f31552611" />
- <img width="332" height="41" alt="image" src="https://github.com/user-attachments/assets/035a5bd9-652c-4e0f-a05f-8941092ff437" /> 
- <img width="946" height="193" alt="image" src="https://github.com/user-attachments/assets/c93bf9e2-5c8d-4d7c-b7eb-81ccc99238cd" />
































- 




  
