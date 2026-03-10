
# 4) Text detection: Tesseract vs Easyocr vs AWS Textract | What is the best OCR?

https://youtu.be/CcC3h0waQ6I?si=s-4CkD5yroNw45qD

# prepare data
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
