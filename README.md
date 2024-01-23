# Workplace case Study

In this project, I want to share how absenteeism can impact performance in an organization and the problem of it. To solve that problem I use data analytics to describe the pattern using Tableau and predict which employee will be absent so the organization can take action and prevent the problem using regression method (supervised learning).
![absent](Image/BLOG_Absent.jpg)

For full report of this project, please visit [Absenteeism at Work]([https://github.com/Juantonios1/Absenteeism-Analysis-to-Improve-Work-Performance/blob/main/Absenteeism%20Analysis%20ipynb/Absenteeism%20Analysis%20to%20Improve%20Work%20Performance.ipynb](https://github.com/farahzak/Absenteeism-in-The-Workplace/blob/main/Absenteeism%20-%20Data%20Preprocessing.ipynb)).

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
    <li><a href="#data-preprocessing">Data Preprocessing</a></li>
    <li><a href="#data-analytics">Data Analytics</a></li>
    <li><a href="#model-selection">Model Selection</a></li>
    <li><a href="#explainable-and-interpretable-machine-learning">Explainable and Interpretable Machine Learning</a></li>
    <li><a href="#preprocessing-new-dataset">Preprocessing New Dataset</a></li>
    <li><a href="#prediction-result">Prediction Result</a></li>
    <li><a href="#conclusion">Conclusion and Recommendation</a></li>
    <li><a href="#contributors">Contributors</a></li>
  </ol>
</details>

## Business Background
**Context :**  
Organizations for years have been looking for ways to improve human resource management by paying attention to aspects such as work organization, organizational environment, or personal issues to reduce employee absenteeism at work and to reduce high employee turnover. However, with the various ways that have been done so far, the absenteeism rate in some organizations still tends to be high. Absenteeism defined as any failure of an employee to report for or remain at work as scheduled, regardless of reason, expresses a monetary implication. The term ‘as scheduled’ is very significant, for this automatically excludes vacations, holidays, jury duty, and the like. It also eliminates the problem of determining whether the absenteeism is excusable or not. The absence of workers from the workplace can be disruptive and increase costs for the organization and is an indication that there is poor work adjustment for employees.

**Problem Statement :**  
From a business perspective, employees who are not present to do their jobs will cost more than they should. The absence is a big problem because it reduces output and is annoying because it requires rescheduling and changing programs which is one of the contributing factors to the failure of a department's organization to meet performance targets.

**Goals :**  
Based on these problems, this analysis is carried out to predict how long an employee will be absent from work and what factors affect the length of time someone is absent from work so that the organization can rearrange tasks to improve work performance and quality and find out which employees will be absent. To get answers to these problems, an analysis is carried out using supervised machine learning: regression.

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
At this stage, a brief analysis of the data will be carried out, as follows:
* Distribution Data
* Normal Test
* Data Cardinalities
* Identify Missing Values
* Data Correlation

![correlation](Image/Correlation.png)

## Data Preprocessing
At this stage, data preparation and processing will be carried out before being used as a data model, as follows:
* Casting Data Type
* Encode
* Categorization
* Extract Date Feature
* Splitting

## Data Analytics
At this stage, another information analysis will be carried out, as follows:
* Information Absenteeism in Company
![Information Absenteeism in Company](Image/Dashboard_1.png)
* Personal Information of Employee
![Personal Information of Employee](Image/Dashboard_2.png)
* Daily Work
![Daily Work](Image/Dashboard_3.png)

You can also see the full dashboard of analysis at [Analysis Tableau](https://public.tableau.com/app/profile/juan1691/viz/AnalysisAbseenteismProject/AnalysisAbseenteism).

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

##Conclusion
The logistic regression model presented in the "Absenteeism in The Workplace" repository is a potent tool for predicting absenteeism. Its balanced approach between accuracy and interpretability, coupled with its ability to provide probabilistic insights, makes it highly valuable for organizations aiming to understand and address workforce absenteeism. The model's adaptability to new data further underscores its practical utility in real-world scenarios.

