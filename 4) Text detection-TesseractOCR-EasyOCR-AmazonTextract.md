
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
- import pytesseract
- from PIL import Image
- image_path="/content/images/10.jpg"
- text=pytesseract.image_to_string(Image.open(image_path), lang='eng') #language=English
- print(text)
- output:
- <img width="280" height="182" alt="image" src="https://github.com/user-attachments/assets/2cdaf776-25fd-42be-8ca9-ff6d910e63fd" />
    -  We don’t need any preprocessing for below text detection





  
