# Heart-disease-repo-using-ML
Predicting heart disease from clinical data using EDA, preprocessing and machine learning classification models.
Overview
Goal: predict the presence of heart disease (HeartDisease = 1 or 0)
Problem type: binary classification
Dataset: Heart Failure Prediction dataset (Kaggle), about 918 patient records with 11 features and 1 target
Tools: Python, pandas, NumPy, matplotlib, seaborn, scikit-learn
Notebook: notebooks/Heart.ipynb
Dataset Features
Feature	Description
Age	Age of the patient (years)
Sex	Sex of the patient
ChestPainType	Type of chest pain (e.g. ASY, ATA, NAP, TA)
RestingBP	Resting blood pressure (mm Hg)
Cholesterol	Serum cholesterol (mg/dl)
FastingBS	Fasting blood sugar (1 if above 120 mg/dl, else 0)
RestingECG	Resting electrocardiogram results
MaxHR	Maximum heart rate achieved
ExerciseAngina	Exercise-induced angina (Y/N)
Oldpeak	ST depression induced by exercise
ST_Slope	Slope of the peak exercise ST segment
HeartDisease	Target: 1 = heart disease, 0 = normal
Project Workflow
Exploratory data analysis
Checked shape, data types, summary statistics, duplicates and missing values
Plotted the target class distribution
Plotted histograms with KDE for Age, RestingBP, Cholesterol and MaxHR
Compared heart disease across Sex, ChestPainType and FastingBS using count plots
Used a box plot (Cholesterol), a violin plot (Age) and a correlation heatmap
Data cleaning
Found invalid zero values in Cholesterol and RestingBP, which are not physiologically possible
Replaced them with the mean of the valid (non-zero) values
Preprocessing
One-hot encoded categorical variables (pd.get_dummies, drop_first=True)
Standardized numerical features (Age, RestingBP, Cholesterol, MaxHR, Oldpeak) with StandardScaler
Modeling (in progress)
Train/test split, model training, cross-validation and evaluation
Key Findings

Add 3 to 4 findings from your own plots, for example:

How the heart disease rate differs between male and female patients
Which chest pain type is most associated with heart disease
How MaxHR and Age relate to the target
How many zero-value cholesterol records were found and how they were handled
Results

Results will be added once the models are trained.

Model	Accuracy	Precision	Recall	F1	ROC-AUC
Logistic Regression	-	-	-	-	-
Random Forest	-	-	-	-	-
Repository Structure
├── data/
│   └── heart.csv
├── notebooks/
│   └── Heart.ipynb
├── images/
├── requirements.txt
└── README.md
How to Run
bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
jupyter notebook notebooks/Heart.ipynb

requirements.txt:

numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter
Limitations
The dataset is small, so results may not generalize
Zero values in Cholesterol were imputed, which can affect the model
This is a learning project and must not be used for real medical decisions
Next Steps
Train and compare several classifiers with cross-validation
Tune hyperparameters
Add feature importance or SHAP analysis
Build a small Streamlit app for predictions
