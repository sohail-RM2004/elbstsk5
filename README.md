# Heart Disease Detection — Decision Tree & Random Forest

This project applies **Decision Tree** and **Random Forest** classifiers to predict heart disease from patient data.  
We explore model performance, overfitting control, feature importance, and cross-validation.

---

## Dataset
The dataset contains the following features:

- **age** — Age in years  
- **sex** — 1 = male, 0 = female  
- **cp** — Chest pain type (4 values)  
- **trestbps** — Resting blood pressure (mm Hg)  
- **chol** — Serum cholestoral (mg/dl)  
- **fbs** — Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)  
- **restecg** — Resting ECG results (0, 1, 2)  
- **thalach** — Maximum heart rate achieved  
- **exang** — Exercise induced angina (1 = yes, 0 = no)  
- **oldpeak** — ST depression induced by exercise relative to rest  
- **slope** — Slope of peak exercise ST segment  
- **ca** — Number of major vessels (0–3) colored by flourosopy  
- **thal** — 0 = normal; 1 = fixed defect; 2 = reversible defect  
- **target** — 1 = heart disease, 0 = no heart disease  

---

## Tasks & Results

### **1️. Train a Decision Tree Classifier & Visualize**
- Trained a `DecisionTreeClassifier` on the dataset.
- Visualized the decision tree using `matplotlib`.
- **Accuracy (full depth)**: Train = **1.000**, Test = **0.985**  

---

### **2️. Analyze Overfitting and Control Tree Depth**
- Limiting tree depth (`max_depth=4`) reduced complexity.
- **Accuracy (max_depth=4)**: Train = **0.883**, Test = **0.800**
- Observation: Full-depth tree performed better here due to simple dataset, but depth control is important for noisy/large datasets.

---

### **3️. Train a Random Forest and Compare Accuracy**
- Random Forest trained using default parameters.
- **Accuracy**: Train = **1.000**, Test = **0.9756**  
- More robust and stable than a single Decision Tree.

---

### **4️. Interpret Feature Importances**
Random Forest feature importance (top 5):
| Feature   | Importance |
|-----------|------------|
| cp        | 0.1351     |
| ca        | 0.1273     |
| thalach   | 0.1222     |
| oldpeak   | 0.1219     |
| thal      | 0.1105     |

Observation: Chest pain type, number of vessels, and exercise-related measures are the most predictive.

---

### **5️. Evaluate Using Cross-Validation**
| Model           | CV Mean Accuracy |
|-----------------|------------------|
| Decision Tree   | 0.8341           |
| Random Forest   | 0.9971           |

Random Forest achieved near-perfect and consistent accuracy across folds.

---

## Visualizations
- **Decision Tree Plot** — Shows the decision-making path.  
- **Feature Importance Chart** — Highlights most impactful features.

---


