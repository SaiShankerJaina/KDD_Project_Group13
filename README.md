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
Upon loading and inspecting the dataset, the following insights were gathered:

- The dataset consists of multiple features, both numeric and categorical.
- Initial exploration showed a varied age distribution with a mean around the older age group, which is expected in an Alzheimer's dataset.
- The gender distribution was relatively balanced.
- MMSE scores showed a wide range of values, indicating different levels of cognitive impairment among patients.

### Data Preparation:
1. *Handling Missing Values*: Identifying and imputing or removing missing values as appropriate.
2. *Data Transformation*: Normalizing and standardizing numeric features to ensure comparability.
3. *Feature Engineering*: Creating new features or modifying existing ones to enhance the dataset's predictive power.
4. *Data Splitting*: Dividing the dataset into training and testing sets for future modeling efforts.

Further steps in data preparation and modeling will be detailed in Deliverable 2.
