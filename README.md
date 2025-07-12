# 🩺 Diabetes Prediction using Decision Tree Classifier

## 📌 Project Overview

This project uses a **Decision Tree Classifier** to predict whether a patient has diabetes based on various health metrics. The model is trained using a labeled dataset and evaluated for classification accuracy.

---

## 📁 Dataset Information

- **📄 File Name**: `diabetes.csv`  
- **🎯 Target Variable**: `Outcome`  
  - 0 = Non-diabetic  
  - 1 = Diabetic  
- **📊 Features**:
  - `Pregnancies`
  - `Glucose`
  - `BloodPressure`
  - `SkinThickness`
  - `Insulin`
  - `BMI`
  - `DiabetesPedigreeFunction`
  - `Age`

---

## 🧹 Data Preprocessing

1. ✅ Loaded the dataset using `pandas`  
2. 📤 Split the data into:
   - `X` → Features (`data.drop('Outcome', axis=1)`)
   - `y` → Labels (`data['Outcome']`)  
3. 🔀 Performed train-test split using:
   ```python
   train_test_split(X, y, test_size=0.2, random_state=0)
   ```

---

## 🛠️ Model Training

- 🧠 Algorithm: **DecisionTreeClassifier** from `sklearn.tree`  
- 📌 Criterion: `'entropy'` (uses information gain for splitting)  
- ✅ Model trained using:
  ```python
  Classifier.fit(xtrain, ytrain)
  ```

---

## 📈 Evaluation

- 📍 Made predictions using `Classifier.predict(xtest)`  
- ✔️ Accuracy measured with:
  ```python
  accuracy_score(ytest, ypred)
  ```

---

## 🌳 Tree Visualization

- 📉 Used `export_graphviz()` to visualize the decision tree  
- Rendered using `graphviz.Source()` with:
  - Feature names
  - Filled colors for better readability

> To view the tree on GitHub or export it:
```python
export_graphviz(Classifier, out_file='tree.dot', feature_names=x.columns, filled=True)
```

---

## 📌 Key Observations

- Decision trees are intuitive and easy to interpret  
- No feature scaling or encoding was needed for this dataset  
- The model’s performance depends on depth and criteria (e.g., entropy or gini)

---

## 🧰 Libraries Used

- `pandas` 🐼  
- `numpy` 🔢  
- `sklearn` 🤖  
- `graphviz` 🌐

---

## 🚀 Future Enhancements

- 🌲 Tune tree depth and pruning to avoid overfitting  
- 🎯 Compare with other models (Random Forest, Logistic Regression, SVM)  
- 🔍 Perform cross-validation for more robust evaluation  
- 📊 Visualize confusion matrix and ROC-AUC

---

## 🙏 Acknowledgments

- Dataset is publicly available and widely used for ML classification demos  
- Inspired by real-world applications of machine learning in healthcare

---

## 📜 License

This project is licensed under the **MIT License** ✅
