# 6) Image classification-Scikit learn
- https://youtu.be/il8dMDlXrIE?si=Ujijjoz10yHQnbvd
-  We need these 3 library:
-  <img width="232" height="97" alt="image" src="https://github.com/user-attachments/assets/92438ff3-89f4-4837-bd7c-1d0d2f38b2ad" />

- define libraries:
- <img width="551" height="296" alt="image" src="https://github.com/user-attachments/assets/7184877c-0eb3-4b3a-8f11-2d1f5fabe54a" />
- prepare data:
- <img width="680" height="508" alt="image" src="https://github.com/user-attachments/assets/c6a19206-b838-4b89-9463-eee5863dfcd3" />
- train / test split:
- <img width="1135" height="79" alt="image" src="https://github.com/user-attachments/assets/8007ae1a-2378-41f8-a31f-6dfd0ff72a19" />
   - what is stratify?
  
  - <img width="360" height="268" alt="image" src="https://github.com/user-attachments/assets/73d048c4-b75f-4e01-8d13-2399509209d5" />
- train classifier:
-  We don’t define the parameter for SVC because we want to use default parameters value only C and gamma
classifier = SVC() : اینجا ما یک مدل یادگیری ماشین می‌سازیم. مدل: SVC (Support Vector Classifier)  این مدل مثل یک معلم است که یاد می‌گیرد چطور چیزها را دسته‌بندی کند. مثلاً: - عکس گربه  عکس سگ - مدل یاد می‌گیرد تشخیص دهد.
- در اینجا دو تنظیم داریم:
-  C  کنترل می‌کند مدل چقدر سختگیر باشد.
     -  C کوچک → مدل ساده‌تر
     -  C بزرگ → مدل پیچیده‌تر
- Gamma  کنترل می‌کند مدل چقدر به جزئیات توجه کند.
     - gamma بزرگ → توجه زیاد به جزئیات
     - gamma کوچک → نگاه کلی‌تر
     - 



