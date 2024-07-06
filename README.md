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
- **Univariate Analysis**: Distribution plots, box plots.
- **Multivariate Analysis**: Correlation matrix, pair plots.
- Plots representing various aspects such as count of people in different sectors, marital status, age, BMI, and glucose levels in relation to stroke occurrence.

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

