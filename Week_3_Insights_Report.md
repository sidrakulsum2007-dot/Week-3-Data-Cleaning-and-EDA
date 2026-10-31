
# Week 3 – Data Cleaning and Exploratory Data Analysis (EDA)

## 1. Project Overview

This project focuses on cleaning and analysing the Titanic passenger dataset using Python. The main objective is to identify and handle missing values, remove duplicate records, detect and handle outliers, encode categorical variables, perform feature scaling, and understand relationships between different features.

Exploratory Data Analysis (EDA) was performed to discover meaningful patterns and insights from the dataset.

## 2. Dataset Information

- **Dataset:** Titanic Passenger Dataset
- **Original Records:** 891 rows
- **Original Features:** 15 columns
- **Final Cleaned Records:** 775 rows
- **Final Cleaned Features:** 14 columns
- **Tools Used:** Python, Pandas, NumPy, Matplotlib, Seaborn and Scikit-learn
- **Environment:** Visual Studio Code with Jupyter Notebook

## 3. Data Cleaning Process

### 3.1 Handling Missing Values

The dataset contained missing values in the following columns:

- Age: 177 missing values
- Embarked: 2 missing values
- Deck: 688 missing values
- Embark Town: 2 missing values

The following methods were used:

- Missing values in the Age column were replaced with the median.
- Missing values in the Embarked column were replaced with the mode.
- Missing values in the Embark Town column were replaced with the mode.
- The Deck column was removed because it contained a large number of missing values.

After cleaning, no missing values remained in the dataset.

### 3.2 Removing Duplicate Records

Duplicate records were identified using the duplicated() function.

- Duplicate records found: 116
- Duplicate records removed: 116
- Final number of records: 775

Removing duplicates helped improve the consistency of the dataset.

### 3.3 Outlier Detection and Handling

Outliers were detected using the Interquartile Range (IQR) method.

The numerical columns analysed were:

- Age
- Fare
- Sibsp
- Parch

The detected outliers were:

| Column | Outliers Detected |
|---|---:|
| Age | 27 |
| Fare | 102 |
| Sibsp | 39 |
| Parch | 15 |

Outliers were handled using IQR-based capping. Values below the lower limit and above the upper limit were adjusted to their respective limits.

### 3.4 Encoding Categorical Variables

Categorical variables were converted into numerical form using One-Hot Encoding with the Pandas get_dummies() function.

The drop_first=True option was used to avoid unnecessary duplicate encoded columns.

The encoded dataset contained 18 columns.

### 3.5 Feature Scaling

StandardScaler from Scikit-learn was used to standardise the numerical features:

- Age
- Fare
- Sibsp
- Parch

Feature scaling helps bring numerical features onto a comparable scale.

## 4. Correlation Analysis

Correlation analysis was performed to understand the relationships between numerical features.

A correlation matrix was created using Pandas, and a heatmap was generated using Seaborn and Matplotlib.

Important observations:

- Passenger class and fare showed a negative correlation of approximately -0.74.
- Survival and male gender showed a negative correlation of approximately -0.52.
- Survival and adult male status showed a negative correlation of approximately -0.53.
- Survival and fare showed a positive correlation of approximately 0.31.

The correlation heatmap is saved in the visualizations folder as:

`11_correlation_heatmap.png`

## 5. Ten Analytical Questions and Findings

The following questions were analysed using Python:

1. **What is the total number of passengers?**  
   After data cleaning, 775 passenger records remained.

2. **What percentage of passengers survived?**  
   Approximately 41.29% of passengers survived.

3. **How many male and female passengers were there?**  
   Male passengers: 483.  
   Female passengers: 292.

4. **Which gender had a higher survival rate?**  
   Female passengers had a higher survival rate of approximately 73.97%, compared with 21.53% for male passengers.

5. **What was the survival rate in each passenger class?**  
   First class: 63.33%.  
   Second class: 50.61%.  
   Third class: 25.94%.

6. **What was the average age of passengers?**  
   The average passenger age was approximately 29.36 years.

7. **What was the average ticket fare?**  
   The average ticket fare was approximately 26.59.

8. **Which town had the highest number of passengers?**  
   Southampton had the highest number of passengers.

9. **How many passengers were travelling alone?**  
   The number was calculated using the alone column in the notebook.

10. **What was the survival rate of passengers travelling alone?**  
    Passengers travelling alone had a survival rate of approximately 33.64%, while passengers not travelling alone had a survival rate of approximately 51.18%.

## 6. Key Insights

The analysis revealed several interesting findings:

- Female passengers had a significantly higher survival rate than male passengers.
- First-class passengers had a higher survival rate than second- and third-class passengers.
- The overall survival rate was approximately 41.29%.
- The average passenger age was approximately 29.36 years.
- Passenger class and fare had a strong negative correlation.
- The survival rate of passengers travelling alone was lower than that of passengers not travelling alone.
- Data cleaning improved the consistency and quality of the dataset.

## 7. Project Files and Outputs

The project contains the following files:

- `dataset/titanic.csv` – Original dataset.
- `cleaned_data/titanic_cleaned.csv` – Cleaned dataset.
- `cleaned_data/titanic_encoded_scaled.csv` – Encoded and scaled dataset.
- `Week_3_Data_Cleaning_EDA.ipynb` – Complete Jupyter Notebook.
- `visualizations/11_correlation_heatmap.png` – Correlation heatmap.
- `README.md` – Project documentation.

## 8. Conclusion

This project provided practical experience in data cleaning and exploratory data analysis using Python.

Missing values were handled, duplicate records were removed, outliers were detected and capped, categorical variables were encoded, and numerical features were scaled.

Correlation analysis and visualisation helped identify relationships between passenger characteristics and survival.

Overall, this project improved my understanding of data preprocessing, data analysis, and the importance of preparing a dataset before applying machine learning algorithms.

## 9. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Visual Studio Code
