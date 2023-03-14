## Mental Health
**Author: Ivan Santaella Martinez**

### Executive summary
- Executive Presentation: [mental-health-executive](https://github.com/ivan-troy-2001/Mental-Health/blob/main/mental-health-executive.pdf)

### Rationale
Mental health is important at every stage of life, from childhood and adolescence through adulthood, and it is a problem that can affect anyone.

### Research Question
What are the contributing factors to seek treatment for mental health at workplace?

### Data Sources
  - Dataset:
    - https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey
    - This dataset is from a 2014 survey that measures attitudes towards mental health and frequency of mental health disorders in the tech workplace.

### Methodology
- Machine Learning: This project presents a classification problem, therefore, the following models will be used and evaluated.
  - K-Nearest Neighbors
  - Logistic Regression
  - Decision Tree
  - Support Vector Machine
- Metrics:
  - Accuracy: This was the chosen metric since this is a classification problem and the goal is to identify as many opportunities for treatment as possible.
- Project:
  - CRISP-DM

### Results
- Exploratory Data Analysis
  - The majority of the respondents reported working for an organization.
  - The data was mostly collected in the U.S. and we won't be able to infer something about the country of origin.
  - Treatment column was selected as the target variable.
  - Target class is balanced, so there was no need to down sampling nor up sampling the dataset.
  - Respondents with a family history of mental illness are more likely to seek treatment.
  - Respondents who feel a mental condition interferes with their work are more likely to seek treatment.
  - The majority of individuals surveyed work in tech companies.
- Data Preparation
  - Object types were convented to category types for a more efficient memory usage and faster training.
  - Comments column was removed since it is mostly empty.
  - Timestamp column was removed since it is not relevant to the target model.
  - Age column contained outliers which were removed.
  - Gender column was standardized since it presented different values to identify gender.
  - Dataset was filtered for U.S. based respondents since the data was mostly collected in the U.S.
  - NAN values were imputed for work_interfere and self_employed columns.
  - One-hot encoding was applied to categorical columns.
  - Age column was scaled.
- Modeling
  - A dummy estimator was used to establish the baseline obtaining a test accuracy score of: 0.54
  - Logistic Regression was used to build the first model obtaining a test accuracy score of: 0.86
- Model comparison
  - Logistic Regression and Support Vector Machine performed the best among all the models evaluated.
  - As expected, Decision Tree tends to overt fit the training dataset.
  - After performing grid search and cross-validation, Logistic Regressions performed the best.
- Final model
  - The final model was built using Logistic Regression with parameters: C=0.09, penalty=l1, solver=liblinear
  - The final test accuracy score was: 0.88
- Findings: After identifying the importance of the model features.
  - These are the top predictors for an individual to seek treatment in case of experiencing a mental health issue.
    - The employer offers care options for mental health.
    - The individual has a family history of mental illness.
    - The individual feels that a mental condition interferes with work.
    - The employer provides benefits for mental health.
  - The following factors do not influence whether individuals who experience a mental condition seek treatment or not.
    - They are self-employed.
    - They work for a tech company.
    - They work remotely.

### Outline of project
- Jupyter Notebook: [mental-health-final](https://github.com/ivan-troy-2001/Mental-Health/blob/main/mental-health-final.ipynb)

### Contact and Further Information
[Contact ME](mailto:itsantaella@gmail.com)
