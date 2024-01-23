# Workplace case Study

This report delves into the analysis of absenteeism in the workplace, based on the Jupyter Notebook titled "Case study (1)" from the GitHub repository "Absenteeism in The Workplace". The study aims to predict absenteeism at work, focusing on the likelihood of an employee being absent for a certain number of hours during a workday. This prediction is crucial for enhancing company productivity by efficiently reorganizing workflow and managing workforce resources. [Absenteeism at Work]([https://github.com/Juantonios1/Absenteeism-Analysis-to-Improve-Work-Performance/blob/main/Absenteeism%20Analysis%20ipynb/Absenteeism%20Analysis%20to%20Improve%20Work%20Performance.ipynb](https://github.com/farahzak/Absenteeism-in-The-Workplace/blob/main/Absenteeism%20-%20Data%20Preprocessing.ipynb)).

## Summary Process
<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Content</summary>
  <ol>
    <li>
      <a href="#business-background">Business Background</a>
    </li>
    <li>
      <a href="#data-understanding">Data Understanding</a>
    </li>
    <li>
      <a href="#exploratory-data-analysis">Exploratory Data Analysis</a>
    </li>
    <li>
      <a href="#data-preprocessing">Data Preprocessing</a>
    </li>
    <li>
      <a href="#data-transformation-and-feature-engineering">Data Transformation and Feature Engineering</a>
    </li>
    <li>
      <a href="#machine-learning-algorithm-predicting-absenteeism">Machine Learning Algorithm: Predicting Absenteeism</a>
    </li>
    <li>
      <a href="#conclusion">Conclusion and Recommendation</a>
    </li>
  </ol>
</details>

## Business Background
**Context :**  
Organizations for years have been looking for ways to improve human resource management by paying attention to aspects such as work organization, organizational environment, or personal issues to reduce employee absenteeism at work and to reduce high employee turnover. However, with the various ways that have been done so far, the absenteeism rate in some organizations still tends to be high. Absenteeism defined as any failure of an employee to report for or remain at work as scheduled, regardless of reason, expresses a monetary implication. The term ‘as scheduled’ is very significant, for this automatically excludes vacations, holidays, jury duty, and the like. It also eliminates the problem of determining whether the absenteeism is excusable or not. The absence of workers from the workplace can be disruptive and increase costs for the organization and is an indication that there is poor work adjustment for employees.

**Problem Statement :**  
From a business perspective, employees who are not present to do their jobs will cost more than they should. The absence is a big problem because it reduces output and is annoying because it requires rescheduling and changing programs which is one of the contributing factors to the failure of a department's organization to meet performance targets.

**Objective :**  
The primary objective of this report is to develop a predictive model for absenteeism in the workplace. In today's fast-paced and competitive business environment, understanding and anticipating employee absenteeism is crucial for maintaining productivity and efficient workflow management. The goal is to analyze various factors that contribute to absenteeism and use this information to predict the likelihood and duration of an employee's absence from work.

## Data Understanding

| Feature      | Description                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| ID           | Unique ID for customer                                                                        |
| Reason of absence | Reasons 1-21 are registered in the International Classification Diseases (ICD)               |
| Date         | Date of Absence                                                                               |
| Transportation Expense | Cost related to business travel (fuel, parking, meals, etc)                                   |
| Distance to work | Distance measured in km                                                                       |
| Age          | Years of age                                                                                  |
| Daily workload average | Measured in minutes                                                                           |
| Body Mass Index | Number based on your weight and height                                                        |
| Education    | Representing different levels of education                                                    |
| Children     | Number of children in the family                                                              |
| Pets         | Number of pets in the family                                                                  |
| Absenteeism time in hours | Time that employee doesn't do their task                                                      |

## Exploratory Data Analysis
The exploratory data analysis focuses on understanding the patterns and distributions within the data. Key steps include:

**Analyzing 'Reason for Absence':** This involves examining the range and uniqueness of reasons provided for absenteeism.
**Quantitative Analysis:** The transformation of nominal values into dummy variables is performed to aid in regression analysis.
**Classification of Absence Reasons:** The reasons for absence are classified into distinct groups to simplify the analysis.
![correlation](Image/Correlation.png)

## Data Preprocessing
The analysis utilizes a dataset based on a pre-existing study about absenteeism at work. The data is processed using Python, SQL, and Tableau for cleaning, analysis, and visualization. The preprocessing steps include:

**Data Loading:** The data is loaded into a pandas DataFrame for manipulation and analysis.
**Initial Data Overview:** The dataset is examined for missing values and column data types.
**Dropping Unnecessary Columns:** Columns not relevant to the analysis, such as 'ID', are removed.
**Creating Dummy Variables:** For categorical data, dummy variables are created to facilitate quantitative analysis.
**Grouping Reasons for Absence:** The reasons for absence are categorized into groups for a more structured analysis.

## Data Transformation and Feature Engineering
Several transformations and feature engineering steps are undertaken:

**Date Processing:** The 'Date' column is converted into a datetime object for easier manipulation.
**Extracting Month and Day of the Week:** New columns are created to represent the month and day of the week of each absence.
**Reordering Columns:** The DataFrame columns are reordered for better organization and analysis.
**Final Data Checkpoint:** A final checkpoint is created to save the state of the DataFrame after significant transformations.

## Machine Learning Algorithm: Predicting Absenteeism
Introduction
In the realm of human resource management, understanding and predicting absenteeism in the workplace is crucial. The GitHub repository "Absenteeism in The Workplace" presents a comprehensive analysis using a logistic regression model to address this issue. This report summarizes the key findings and insights derived from the machine learning algorithm implemented in the notebook titled "Logistic Regression model to predict absenteeism."

**Methodology**
The approach involved several critical steps:

**Target Variable Definition:** The continuous variable 'Absenteeism Time in Hours' was transformed into a binary classification - 'moderately absent' and 'excessively absent'. This categorization was based on the median value of absenteeism hours.

**Data Balancing Check:** The dataset's balance was assessed, revealing a near ideal split for logistic regression purposes, with 46% of the data falling into the 'excessively absent' category.

**Standardization of Data:** To enhance the model's performance, data standardization was carried out, excluding dummy variables. This step is essential for logistic regression models to function optimally.

**Model Training and Evaluation**
The logistic regression model underwent training and subsequent evaluation:

**Training and Accuracy:** The model achieved an accuracy of approximately 79% on the training set, indicating a high level of proficiency in predicting absenteeism.

**Coefficient Analysis:** An examination of the model's coefficients was conducted to understand the influence of each feature. Higher coefficients indicated a stronger impact on the likelihood of excessive absenteeism.

**Feature Selection via Backward Elimination:** This technique was employed to refine the model by removing features with minimal impact, slightly improving the model's accuracy.

**Testing on Unseen Data:** The model's generalizability was tested on a separate dataset, where it achieved a 74% accuracy, demonstrating its effectiveness on new data.

**Probability Estimation:** Beyond binary classification, the model provided probabilities for each classification, offering a more detailed perspective on absenteeism likelihood.

## Conclusion
The analysis in the "Case study (1)" notebook provides a comprehensive approach to predicting absenteeism in the workplace. By preprocessing the data, performing exploratory analysis, and engineering relevant features, the study lays the groundwork for building a predictive model. This model can potentially help organizations in making informed decisions related to workforce management, considering various factors like proximity to the workplace, family size, and educational background.
