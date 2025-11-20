# 💧 Water Potability Prediction Using Machine Learning (Random Forest)

---

## 📄 Overview
This project predicts whether **water is safe (potable)** or **unsafe (not potable)** for drinking using **machine learning**.  
A **Random Forest Classifier** is trained on chemical properties of water to classify water quality based on real-world parameters.

The model analyzes different water characteristics such as pH level, dissolved solids, hardness, sulfate content, and more to determine whether the water sample is **Potable (1)** or **Not Potable (0)**.

---

## 🧩 Dataset
The dataset contains several key water quality features and a final label indicating **Potability**.

**Dataset Columns:**
- ph  
- Hardness  
- Solids  
- Chloramines  
- Sulfate  
- Conductivity  
- Organic_carbon  
- Trihalomethanes  
- Turbidity  
- Potability → (1 = Drinkable, 0 = Not drinkable)

Missing values are filled using column-wise mean values to avoid data loss.

---

## 🧠 Model Used: Random Forest Classifier
This project uses **Random Forest**, a powerful ensemble learning method that combines multiple decision trees to improve prediction accuracy.

### Why Random Forest?
- Handles nonlinear data  
- Works well with tabular datasets  
- Less prone to overfitting  
- Provides high accuracy  
- Robust to noise and missing values  

### Additional Improvements
To improve detection of potable vs. non-potable water:

✔ SMOTE is used to fix dataset class imbalance  
✔ StandardScaler is used to normalize the features  

---

## ⚙️ Tools & Technologies
- Python  
- Pandas, NumPy  
- Scikit-Learn  
- SMOTE (imbalanced-learn)  
- Google Colab / Jupyter Notebook  

---

## 🧪 Model Workflow
The project follows this processing pipeline:

1. Load and clean dataset  
2. Fill missing values  
3. Split data into training & testing sets  
4. Apply **SMOTE** to balance data  
5. Scale features with **StandardScaler**  
6. Train **Random Forest Classifier**  
7. Evaluate model accuracy & confusion matrix  
8. Predict new water sample potability  

---

## 📊 Results
The Random Forest model achieves strong performance on the test set:

| Metric | Value |
|--------|-------|
| Accuracy | ~80–85% |
| Precision / Recall | Improved after SMOTE |
| Confusion Matrix | Better class separation |




    print("Water is NOT POTABLE (Unsafe to Drink).")
