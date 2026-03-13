# 6) Image classification-Scikit learn
- https://youtu.be/il8dMDlXrIE?si=Ujijjoz10yHQnbvd
-  We need these 3 library:
-  <img width="232" height="97" alt="image" src="https://github.com/user-attachments/assets/92438ff3-89f4-4837-bd7c-1d0d2f38b2ad" />

- define libraries:
- <img width="698" height="533" alt="image" src="https://github.com/user-attachments/assets/116c4ad7-e4b0-42b3-971f-5933ec6bade2" />

- prepare data:
- <img width="680" height="508" alt="image" src="https://github.com/user-attachments/assets/c6a19206-b838-4b89-9463-eee5863dfcd3" />
- train / test split:
- <img width="1135" height="79" alt="image" src="https://github.com/user-attachments/assets/8007ae1a-2378-41f8-a31f-6dfd0ff72a19" />
   - what is stratify?
  
  - <img width="360" height="268" alt="image" src="https://github.com/user-attachments/assets/73d048c4-b75f-4e01-8d13-2399509209d5" />
- train classifier:
-  We don’t define the parameter for SVC because we want to use default parameters value only C and gamma
Below is a **clean GitHub / README.md format** you can directly paste into your repository.

````markdown
## Support Vector Classifier (SVC) Model

```python
classifier = SVC()
````

Here we create a **machine learning classification model** called **SVC (Support Vector Classifier)**.

The goal of this model is to **learn patterns from training data and classify new data into categories**.
For example, the model can learn to distinguish between:

* Cat images
* Dog images

After training, the model can predict the correct category for new unseen data.

---

## Model Hyperparameters

In this example, we tune two important hyperparameters:

### C

`C` controls how strict the model is when separating the classes.

* **Small C → Simpler model**
  Allows more classification errors but improves generalization.

* **Large C → More complex model**
  Tries to classify training data more accurately but may overfit.

---

### Gamma

`gamma` controls how much the model focuses on individual data points.

* **Large gamma → Focus on very close data points**
  Creates more detailed decision boundaries.

* **Small gamma → Focus on overall data distribution**
  Produces smoother and simpler boundaries.

---

## Hyperparameter Tuning with GridSearch

Since we **do not know the best values for `C` and `gamma`**, we test multiple combinations using **GridSearchCV**.

Example parameter grid:

```python
parameters = {
    'C': [1, 10, 100, 1000],
    'gamma': [0.01, 0.001, 0.0001]
}
```

GridSearch will try **all possible combinations** of these values and select the best performing model.

Total models tested:

```
4 C values × 3 gamma values = 12 models
```

---

## Why These Values?

The values are chosen on a **logarithmic scale**:

```
0.0001 → 0.001 → 0.01
1 → 10 → 100 → 1000
```

This allows the search to efficiently explore **small, medium, and large parameter values**.

Using logarithmic scales for hyperparameter tuning is a **standard practice in machine learning**.


<img width="1108" height="259" alt="image" src="https://github.com/user-attachments/assets/a1ed4a1d-5947-4624-bed2-d170e2c36382" />

- Test Performance:
     -  Now we must predict test data based on best option that Grid search selected:
<img width="919" height="395" alt="image" src="https://github.com/user-attachments/assets/86aa8c8d-d457-4f99-9982-30ca66a4c4f4" />

output:
<img width="553" height="58" alt="image" src="https://github.com/user-attachments/assets/6c182673-f828-4ee5-a8c5-37c37525c43f" />




