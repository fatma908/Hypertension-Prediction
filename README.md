Overview
High blood pressure is a major risk factor for cardiovascular disease. This project uses the **Hypertension Risk Prediction Dataset** to predict individual risk of hypertension. The objective is to develop a model that stratifies patients by risk, enabling healthcare stakeholders to make informed decisions about early intervention and preventive care.

Dataset
- **Source:** [Kaggle - Hypertension Risk Prediction Dataset](https://www.kaggle.com/datasets/miadul/hypertension-risk-prediction-dataset?resource=download)  
- **License:**[Kaggle Dataset License]  
- **Collection:** Patient health data collected from surveys and clinical measurements.  
- **Schema / Fields:** Includes features like `Age`, `Gender`, `BMI`, `Cholesterol`, `Glucose`, `Smoking`, `Alcohol intake`, `Physical activity`, and `Hypertension label`. Units vary: numerical values for measurements, categorical for lifestyle indicators.  
- **Filters / Joins:** No joins applied. Some missing values were imputed.  

Methods
- **Preprocessing:** Imputed missing values, encoded categorical features (e.g., Gender, Smoking), and scaled numerical features (e.g., Age, BMI, Glucose).  
- **Feature Engineering:** Created BMI categories, combined lifestyle indicators into a single risk score, and derived interaction terms between Age and BMI.  
- **Baseline Model:** Unsupervised learning using **K-Means clustering** to group patients by risk.  
- **Improved Model:** Random Forest classifier trained on labeled data to predict hypertension risk.  
- **Validation Plan:** 80/20 train-test split, 5-fold cross-validation for hyperparameter tuning.  
- **Hyperparameter Search:** Grid search for number of clusters (unsupervised), max depth, number of trees, and learning rate (Random Forest).  
- **Leakage Prevention:** Preprocessing steps fit only on training data; clustering and prediction applied on separate validation/test sets to prevent data leakage.

Results
- **Metrics:** Random Forest: Accuracy, F1-score; K-Means: Silhouette score.  
- **Figures:** PCA 2D cluster visualization, confusion matrix, and Random Forest feature importance plot.  
- **Comparison:** Random Forest improved predictive accuracy over K-Means alone, providing better risk stratification.  
- **Practical Meaning of Errors:** Misclassifying high-risk patients delays intervention, while false positives may trigger unnecessary lifestyle changes.
Reproducibility
- **Environment:** Python, Pandas, Scikit-learn, Matplotlib, Seaborn 
Poster
Place the PDF in results/ and link it here. Ensure figures match repository outputs.
Acknowledgments 
-## Acknowledgments
- Dataset provided by Kaggle  
- **Mentors:** **Ashley Scruse, Whitney Nelson, Robert Briggs, Jr., David Cherry, Chris Thomas**  
- **Program support and institution:** **Morehouse College**
