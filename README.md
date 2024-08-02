### Project Title :
Unlocking the Potential of Data-Driven Diagnosis: Predicting Alzheimer's Disease Stages
### Team Members List :
1.Sai Shanker Jaina

2.Navya Vejalla

3.Sushma Kolli

4.Sri Gowthami Sunkavalli

### Project Introduction:
This project aims to analyze a dataset related to Alzheimer's disease, focusing on descriptive and diagnostic analytics to uncover patterns and insights within the data. The dataset, which includes information such as age, gender, BMI, blood pressure, cholesterol levels, MMSE scores, and diagnosis group, was sourced from a publicly available repository (link to be provided). The goal is to understand the relationships between these variables and identify any significant trends or correlations that may aid in further research or clinical practice.

Given the nature of the data and the research questions, the project will primarily use unsupervised learning techniques such as clustering to group similar patients and descriptive statistics to summarize and explore the data. Additionally, exploratory data analysis (EDA) will be conducted to visualize the distributions and relationships between variables. Classification models may be considered later to predict diagnosis groups based on the available features



### Research Question:
The primary research question for this project is: *What are the key factors associated with different diagnosis groups in Alzheimer's disease, and how do these factors interrelate?*

### Relevant Domain Information :
1. *Alzheimer's Disease Overview*: An article providing a comprehensive overview of Alzheimer's disease, including its symptoms, risk factors, and current research trends. [Alzheimer's Association](https://www.alz.org/alzheimers-dementia/what-is-alzheimers)

2. *MMSE and Its Use in Alzheimer's Diagnosis*: An article detailing the Mini-Mental State Examination (MMSE) and its relevance in diagnosing cognitive impairments, particularly Alzheimer's disease. [Journal of Alzheimer's Disease](https://www.j-alz.com/content/mini-mental-state-examination-mmse)

### Data Source and Description:  
Kaggle - Alzheimer's Disease Dataset : https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset

This dataset includes various attributes related to patients with Alzheimer's disease:

- *Age*: Age of the patient.
- *Gender*: Gender of the patient.
- *BMI*: Body Mass Index.
- *SystolicBP*: Systolic Blood Pressure.
- *DiastolicBP*: Diastolic Blood Pressure.
- *CholesterolTotal*: Total Cholesterol levels.
- *MMSE*: Mini-Mental State Examination score.
- *Diagnosis*: Diagnosis group (e.g., healthy, mild cognitive impairment, Alzheimer's disease).

### Data Understanding and EDA:
Here are the interpretations for the visualizations:
### 1. Age Distribution
**Interpretation:**
The age distribution histogram shows how the ages of patients are distributed within the dataset. The `kde` (kernel density estimate) line provides a smoothed version of the histogram. Peaks in the histogram and KDE indicate the most common age ranges. If the distribution is skewed, it may suggest a bias towards a particular age group within the dataset.

### 2. Gender Distribution
**Interpretation:**
The gender distribution count plot displays the number of patients of each gender. This helps to understand the gender balance in the dataset. A significant imbalance might suggest that the dataset is not fully representative of the general population.

### 3. MMSE Score Distribution
**Interpretation:**
The MMSE (Mini-Mental State Examination) score distribution shows the frequency of various MMSE scores in the dataset. The KDE line provides a smoothed estimate of the distribution. This visualization helps to identify the common range of cognitive scores among patients, which can be useful for understanding the severity distribution of cognitive impairment.

### 4. Pairplot for Numeric Features
**Interpretation:**
The pairplot shows pairwise relationships between selected numeric features (Age, BMI, Systolic Blood Pressure, Diastolic Blood Pressure, Total Cholesterol, and MMSE). The diagonal plots show the KDE of each individual feature, while the off-diagonal plots show scatter plots of feature pairs, providing insight into potential correlations or patterns between features.

### 5. Correlation Matrix
**Interpretation:**
The correlation matrix heatmap visualizes the Pearson correlation coefficients between numeric features. Values close to 1 or -1 indicate strong positive or negative correlations, respectively. This helps to identify which features are related to each other, providing insights into potential multicollinearity or redundant features.

### 6. MMSE Scores by Diagnosis Group
**Interpretation:**
The boxplot shows the distribution of MMSE scores across different diagnosis groups. The boxes represent the interquartile range (IQR), with the line inside the box indicating the median. Whiskers show the range, and any outliers are displayed as individual points. This visualization helps to compare cognitive function (as measured by MMSE) across different diagnostic categories.

### 7. Scatter Plot for SystolicBP vs. DiastolicBP
**Interpretation:**
The scatter plot visualizes the relationship between systolic and diastolic blood pressure, with points colored by diagnosis group. This helps to identify any patterns or differences in blood pressure readings across different diagnosis categories. Clusters or trends can indicate how blood pressure varies with different health conditions.

### Data Preparation:

**1. Data Cleaning:**
- Ensured that all numeric and categorical variables were correctly typed (e.g., age as integer, gender as categorical).
- Handled missing values by using median imputation for numeric features and mode imputation for categorical features to maintain the dataset's integrity.
- Removed any duplicate records to avoid skewed analysis.

**2. Feature Engineering:**
- Created additional features such as age groups (e.g., under 60, 60-75, over 75) to explore age-related trends in Alzheimer's disease.
- Generated interaction features like BMI * age to capture potential combined effects on cognitive health.
- Standardized numeric features like BMI, SystolicBP, DiastolicBP, and CholesterolTotal to ensure they are on a similar scale for better model performance.

**3. Encoding Categorical Variables:**
- Applied one-hot encoding to categorical features like Gender to prepare the data for machine learning models.

**4. Data Splitting:**
- Split the data into training and testing sets (e.g., 80% training, 20% testing) to evaluate model performance.
- Used stratified sampling for splitting to maintain the proportion of diagnosis groups in both sets.

**5. Data Transformation:**
- Applied log transformation to highly skewed features to reduce the impact of outliers and make the data more normally distributed.

### Modeling:

1. **K-Nearest Neighbors (KNN) Clustering**:
- Used KNN clustering to group patients based on similar features. The clustering helped in identifying patterns within the data and understanding group characteristics based on MMSE scores, BMI, and blood pressure.

2. **Logistic Regression**:
- Implemented logistic regression for classification of diagnosis groups based on available features.
- Used grid search and cross-validation to fine-tune hyperparameters, improving model accuracy.

3. **Decision Trees**:
- Applied decision tree algorithms to classify patients into different diagnosis groups.
- Used feature importance from decision trees to understand which factors play the most significant role in predicting Alzheimer’s disease stages.

4. **PyCaret**:
- PyCaret was used to quickly prototype multiple models, including Random Forest, Gradient Boosting, and Support Vector Machines (SVM).
- PyCaret's automated model comparison feature was utilized to identify the best-performing model based on accuracy, precision, recall, and F1-score.

### Evaluation:

1. **Model Evaluation Metrics**:
- Evaluated models using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC for binary/multiclass classification.
- Performed k-fold cross-validation to ensure the model's robustness and reduce the risk of overfitting.

2. **Best Performing Model**:
- The Random Forest model emerged as the best performer, with an accuracy of around 85% and a balanced precision and recall across diagnosis groups.
- The Decision Tree model also provided interpretable results, showing clear decision paths for different Alzheimer’s stages but with slightly lower accuracy.

### Conclusion/Results:

**Key Findings**:
- The analysis revealed that age, MMSE score, and cholesterol levels are significant predictors of Alzheimer’s disease stages.
- Patients in the higher age groups, with lower MMSE scores and higher cholesterol levels, were more likely to be diagnosed with Alzheimer’s disease.
- The clustering analysis showed distinct patient groups based on cognitive and physical health parameters, highlighting patterns that could inform targeted interventions.

**Learning Outcomes**:
- Data-driven techniques can effectively identify important factors related to Alzheimer’s disease.
- Feature selection and transformation play a critical role in enhancing model performance.
- PyCaret is a valuable tool for rapid model development and comparison.

Results Summary:

KNN Cross-Validation Accuracy: 0.7249720821813845 ± 0.019952718083979814
Logistic Regression Cross-Validation Accuracy: 0.838017021737952 ± 0.05212746897176803
Random Forest Cross-Validation Accuracy: 0.9301404022334255 ± 0.06426205709841978
Random Forest Test Accuracy: 0.9372093023255814
Known Issues:

1. Potential Bias: The dataset may have class imbalance, leading to biased model performance.
2. Missing Data: Imputation with mean might not be the best strategy for all features.
3. Encoding: Label encoding may not preserve ordinal relationships if they exist.
4. Model Overfitting: Random Forest model might be overfitting if not properly tuned
