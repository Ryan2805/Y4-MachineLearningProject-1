# Diabetes Prediction using Machine Learning 

This project explores a **binary classification problem** using a diabetes dataset.
The goal is to analyse patient health metrics and build machine learning models capable of predicting whether a patient is likely to have diabetes.

The notebook covers the full data science workflow including **data exploration, preprocessing, model training, hyperparameter tuning, and evaluation**.

---

# Dataset

The dataset contains medical diagnostic measurements for patients.
Each row represents an individual patient, and the target variable indicates whether the patient has diabetes.

### Target Variable

`Outcome`

* `0` → No diabetes
* `1` → Diabetes diagnosis

### Example Features

* Glucose level
* Blood pressure
* Skin thickness
* Insulin level
* Body Mass Index (BMI)
* Age
* Diabetes pedigree function

These medical indicators are used to train predictive models.

---

# Project Workflow

The project follows a typical machine learning pipeline:

1. **Data Quality Checks**
2. **Exploratory Data Analysis**
3. **Data Preprocessing**
4. **Train / Validation / Test Split**
5. **Model Training**
6. **Model Comparison**

---

# Exploratory Data Analysis 

Initial analysis was performed to understand the structure and quality of the dataset.

Steps included:

* Checking dataset shape and variable types
* Identifying missing values
* Detecting invalid values (e.g. medical measurements recorded as `0`)
* Generating histograms for feature distributions
* Computing mean and standard deviation
* Creating a **correlation heatmap**
* Checking class balance for the diabetes outcome

These steps help identify potential issues before modelling.

---

# Data Preprocessing 

Some medical measurements contain **invalid zero values**, which represent missing data.

For selected features:

* Glucose
* BloodPressure
* SkinThickness
* Insulin
* BMI

Zeros were treated as missing values and handled using **median imputation**.

Additional preprocessing included:

* Feature scaling using **StandardScaler**
* Building preprocessing pipelines with **scikit-learn**

---

# Data Splitting

The dataset was split using a **stratified 60/20/20 approach**:

* **60% Training**
* **20% Validation**
* **20% Test**

Stratified sampling ensures the class distribution remains consistent across datasets.

---

# Machine Learning Models 

Three classification models were trained and compared.

### Logistic Regression

A baseline linear model used for binary classification.

Hyperparameters tuned:

* `C` (regularisation strength)
* Solver type

---

### Support Vector Machine (RBF Kernel)

A nonlinear classifier capable of capturing complex decision boundaries.

Hyperparameters tuned:

* `C`
* `gamma`

---

### Decision Tree

A tree-based model that splits the dataset based on feature thresholds.

Hyperparameters tuned:

* Maximum tree depth
* Minimum samples per leaf

---

# Model Evaluation

Models were compared using several evaluation metrics:

* Accuracy
* Precision
* Recall
* F1 Score

The best model was selected using the **validation F1 score**, then retrained on the combined training and validation data before final evaluation on the test set.

A performance comparison table and visualisation are included in the notebook.

---

# Technologies Used 

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# Repository Structure

```
diabetes-classification
│
├── DiabetesAssignment.ipynb
├── dataset.csv
└── README.md
```

---

# How to Run the Project

1. Clone the repository

```
git clone https://github.com/yourusername/diabetes-classification.git
```

2. Install dependencies

```
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Launch the notebook

```
jupyter notebook DiabetesAssignment.ipynb
```

---

# Key Skills Demonstrated

* Data cleaning and preprocessing
* Exploratory data analysis
* Feature engineering
* Machine learning model training
* Hyperparameter tuning
* Model evaluation and comparison

---

# Possible Improvements

Future work could include:

* Random Forest and Gradient Boosting models
* Cross-validation for more robust evaluation
* Feature importance analysis
* Hyperparameter optimisation with GridSearch or RandomSearch
* Deployment as a prediction API

---

# Author
Ryan Daly | rdaly2610@gmail.com | S00237889@atu.ie
Ryan Daly
Software Development Student
