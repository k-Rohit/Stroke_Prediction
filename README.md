# Strok Prediction using Machine Learning 

This project aims to identify potential and possible risk factors contributing to brain stroke and predict its occurrence using various data analysis and machine learning techniques. The dataset contains 5109 samples from Kaggle.

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Types of Stroke](#types-of-stroke)
- [Symptoms and Causes](#symptoms-and-causes)
- [Machine Learning Overview](#machine-learning-overview)
- [Data Collection and Dataset Description](#data-collection-and-dataset-description)
- [Data Preprocessing](#data-preprocessing)
  - [Null Value Identification and Imputation](#null-value-identification-and-imputation)
  - [Feature Engineering and Encoding](#feature-engineering-and-encoding)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Training and Selection](#model-training-and-selection)
- [Evaluation of Models](#evaluation-of-models)
- [Conclusion](#conclusion)
- [Future Scope](#future-scope)
- [How to Run](#how-to-run)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The main objective of this project is to analyze and predict brain strokes using data analysis and machine learning techniques. This involves identifying risk factors, preprocessing data, exploring the data, training various models, and evaluating their performance.

## Problem Statement
To identify potential and possible risk factors contributing to brain stroke and predict its occurrence through various data analysis and machine learning techniques.

## Types of Stroke
- **Ischemic Stroke**: Occurs when a blood clot blocks or narrows an artery leading to the brain.
- **Hemorrhagic Stroke**: Occurs due to bleeding into the brain by the rupture of a blood vessel.

## Symptoms and Causes
### Symptoms
- Trouble speaking and understanding what others are saying.
- Paralysis or numbness of the face, arm, or leg.
- Problems seeing in one or both eyes.
- A sudden and severe headache.
- Trouble walking.

### Causes
- Being overweight or obese.
- Diabetes or increased blood sugar levels.
- Cardiovascular disease, including heart failure and heart defects.
- Age: People aged 60 or older have a higher risk of stroke.


## Data Collection and Dataset Description
The dataset was collected from Kaggle and contains 5109 samples and 12 features.

## Data Preprocessing
### Null Value Identification and Imputation
- **Null Values**: The dataset contains 1745 null values (1544 in smoking status, 201 in BMI).
- **Imputation Strategy**: Mean imputation was used for the BMI column, replacing NaN values with the mean BMI of both males and females separately.

### Feature Engineering and Encoding
- Feature encoding was done using mapping and OneHotEncoder for categorical variables.

## Exploratory Data Analysis
## Insights

1. **Work Sector and Stroke Risk**: 
   - Individuals working in the private sector exhibit a higher incidence of stroke, followed by those who are self-employed. The data shows a significantly higher number of stroke cases among private sector employees compared to other sectors.

2. **Age and Gender Impact**:
   - The likelihood of experiencing a stroke increases with age for both genders. Specifically, males aged above 70 years and females aged above 72 years are at higher risk. Notably, some extreme outliers were identified in females, with children aged 1 and 14 also experiencing strokes. These cases showed BMI values far above the normal range for those ages.

3. **BMI and Stroke Correlation**:
   - Males with strokes have a median BMI close to 29, aligning with scientific data that indicates men with a BMI of 30 or higher are at greater risk of stroke. Females with strokes have a median BMI touching 30, also indicating elevated stroke risk compared to the normal BMI range.

4. **Glucose Levels and Stroke Risk**:
   - Elevated blood glucose levels are an early indicator of potential stroke risk. Individuals with an average glucose level above 115mg/dL are at higher risk. The median average glucose level for males with strokes is above 115mg/dL, while for females, it is close to 100mg/dL. Some outliers with extremely high glucose levels do not have strokes, indicating variability in stroke risk factors.

5. **Age and Glucose Level Relationship**:
   - As age increases, average glucose levels tend to rise due to decreased insulin production by the pancreas, increasing stroke risk. This trend is evident as most individuals in the 60-80 age group with high glucose levels have experienced strokes.

6. **Age and Stroke Incidence**:
   - The majority of stroke cases in both males and females occur in the 60-80 age group. Some individuals with normal average glucose levels but high BMI values also experience strokes, suggesting BMI as a significant risk factor.

7. **BMI Variability and Stroke**:
   - In males, nearly all individuals with strokes have a BMI above 27 to 27.5. In contrast, females with strokes show a wide range of BMI values. Outliers with extremely high BMI values are mostly in the 20-40 age group, where stroke risk is generally lower.

8. **Marital Status and Stroke Risk**:
   - Married individuals have a higher incidence of stroke compared to unmarried individuals. The data shows a greater number of married people experiencing strokes.

9. **Weight Category and Stroke Risk**:
   - A significant number of individuals in the overweight and obese categories experience strokes. This is consistent with research indicating that obesity and overweight conditions increase stroke risk due to higher triglyceride levels and the potential for blood clot formation.



## Model Training and Selection
### Algorithms Used
1. **RandomForestClassifier**
2. **Naive Bayes**
3. **KNNClassifier**
4. **SupportVectorMachine**

### Splitting the Dataset
- The dataset was split into training (80%) and testing (20%) sets.
- Stratified K-Folds Cross Validation was used to handle class imbalance.

## Evaluation of Models
- Evaluation was based on recall as the suitable metric due to class imbalance.
- RandomForestClassifier performed the best with the lowest number of false negatives.

## Conclusion
The main features affecting stroke prediction are average glucose level, Body Mass Index (BMI), and age. RandomForestClassifier was the most effective model for predicting strokes.

## Future Scope
- Improving data entry and balancing the dataset.
- Exploring more features to enhance model accuracy.
- Initiating further research on brain stroke prediction, particularly relevant to the Indian population where 60% of global stroke patients are from India.

## How to Run
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/stroke-analysis-and-prediction.git
    ```
2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
3. **Run the Streamlit Application**:
    ```bash
    streamlit run app.py
    ```

## Contributing
Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before getting started.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

<iframe src="https://www.kaggle.com/embed/nisargpatel13/brain-stroke-prediction-eda-multiple-models?cellIds=86-100&kernelSessionId=124968785" height="500" style="margin: 0 auto; width: 100%; max-width: 950px;" frameborder="0" scrolling="auto" title="Brain Stroke Prediction(EDA &amp; Multiple Models)"></iframe>

