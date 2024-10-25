# AAI_500_Group7 (Statistical Analysis and Predictive Modeling for AIDS Virus Infection)
This project is a part of the AAI_500_Group7 course in the Applied Artificial Intelligence Program at the University of San Diego (USD) with the objective of developing an end-to-end statistical analysis of a dataset.

## Project Status: [Completed]

**Title of the Project**: Statistical Analysis and Predictive Modeling for AIDS Virus Infection.

**Short Description of the Project**: This project performs a Statistical Analysis and Predictive Modeling for AIDS Virus Infection

**Objectives of the Project:** 
1) To develop a predictive model for AIDS virus Infection using the clinical data.
2) We aim to identify the key risk factors associated with HIV infection and assess their impact through probability and statistical analysis.
3) We aim to perform statistical analysis to gain insights into the central tendency and dispersion of numerical variables such as age, gender, and clinical data to understand the characteristics of the population.
4) We aim to compute Inferential statistics in different groups (for example: infected vs non-infected patients) and derive conclusions about the broader population based on the sample data
5) We aim to perform predictive modeling to establish the relationship between explanatory variables and response variables using classification algorithm.

**Partner(s)/Contributor(s)**  
•	Ananya Chandraker, Sethuraman Krishnasamy, Suman Senapathi

**Partners contact:**
•	Ananya Chandraker :https://www.linkedin.com/in/ananyachandraker/,
•	Sethuraman Krishnasamy: , 
•	Suman Senapathi: webjdi.github.io 

**Methods Used**
•	Machine Learning

**Technologies**
•	Python

**Project Description:** 
This project performs a Statistical Analysis and Predictive Modeling for AIDS Virus Infection.
We have used  the AIDS classification dataset which encapsulates a broad spectrum of clinical and Demographic variables related to AIDS patients.

**Details of Dataset:**
This is an AIDS classification dataset that encapsulates a broad spectrum of clinical and Demographic variables related to AIDS patients.

Data Source: - OpenML- AIDS_Virus_Infection_Prediction (https://www.openml.org/search?type=data&status=active&id=46076&sort=runs)

Number of Variables: 23

Number of Instances: 50000

Size of dataset: 5.35 MB

**Data Dictionary:**
attribute description here for reference:
time: Time since the baseline measurement, in days.
trt: Treatment code (0, 1, 2), where each number signifies a different treatment regimen.
age: Age of the patient in years.
wtkg: Weight of the patient in kilograms.
hemo: Presence of Hemophilia (0 = No, 1 = Yes).
homo: Homosexual behavior (0 = No, 1 = Yes).
drugs: Drug use (0 = No, 1 = Yes).
karnof: Karnofsky score indicating patient's functional impairment (scores range from 0 to 100).
oprior: Number of opportunistic infections prior to the study.
z30: Presence of Z30 gene (0 = No, 1 = Yes).
preanti: Months before receiving antiretroviral therapy.
race: Race (0 = Non-white, 1 = White).
gender: Gender (0 = Female, 1 = Male).
str2: Stratification variable 2.
strat: Overall stratification.
symptom: Presence of specific AIDS-related symptoms (0 = No, 1 = Yes).
treat: Treatment response (0 = No, 1 = Yes).
offtrt: Off treatment (0 = No, 1 = Yes).
cd40: CD4 count at the baseline.
cd420: CD4 count at 20 weeks.
cd80: CD4 count at 8 weeks.
cd820: CD4 count at 20 weeks post the 8-week measurement.
infected: HIV infection status (0 = Negative, 1 = Positive).

**Visualizations:**

1. Distribution of Age: A histogram with a kernel density estimate (KDE) was created to visualize the age distribution. The plot shows a normal
distribution centered around 34 years, with most participants falling between their late teens and late forties.

2. Distribution of Weight A similar histogram was generated for weight, revealing that most participants have weights clustered around the
mean of 74.7 kg, with fewer individuals at both extremes.

3. Boxplot of Age by Infection Status: This boxplot illustrates th3e age distribution among infected and non-infected individuals. It indicates
that infected individuals tend to be slightly older on average compared to those not infected.

4. Boxplot of Weight by Infection Status: This visualization shows weight distributions across infection statuses. It highlights that there are no
significant differences in weight between infected and non-infected groups.

5. Correlation Heatmap: A correlation matrix has been visualized using a heatmap to assess relationships between numerical variables.
Notably, there are moderate correlations between age and infection status, suggesting that older individuals may have higher infection rates.

6. Conclusion The EDA reveals important insights into the dataset

Concerning HIV infection patterns:
i) The age distribution suggests that older individuals are likely to be infected more compared to younger individuals.
ii) Weight does not appear to have a significant impact on infection status based on the boxplot analysis.
iii) The correlation heatmap indicates potential relationships worth exploring further in predictive modeling.


**Model Selection:**

i) Initial Selection of Logistic Regression Model
Initially, Logistic Regression was chosen as a baseline for its simplicity andinterpretability in binary classification.

ii) Final Selection of Adaptive Boost Model
However, Adaboost was later adopted to improve model performance bycombining multiple weak learners, offering better accuracy and robustness in handling complex patterns.

**Model Analysis:**

**i) Analysis of Initial Model - Logistic Regression**

Analysis of Logistic Regression Model Output for AIDS Dataset, the output provided summarizes the performance metrics of a logistic regression model applied to an AIDS dataset. Here’s a breakdown of the key components and their implications:

1. Precision, Recall, F1-Score, and Support

Precision:
For class 0.0: 0.73
For class 1.0: 0.58
Precision indicates the proportion of true positive results in relation to all positive predictions made by the model.

A precision of 0.73 for class 0.0 means that when the model predicts a negative outcome (not having AIDS), it is correct 73% of the time.
Conversely, a precision of 0.58 for class 1.0 indicates that the model is correct only 58% of the time when predicting a positive outcome (having AIDS).

Recall:
For class 0.0: 0.93
For class 1.0: 0.21
Recall measures the ability of the model to identify all relevant instances (true positives).

A recall of 0.93 for class 0.0 suggests that the model successfully identifies 93% of actual negatives, while a recall of only 0.21 for class 1.0 indicates that it only identifies 21% of actual positives.

F1-Score:
For class 0.0: 0.82
For class 1.0: 0.31
The F1-score is the harmonic mean of precision and recall, balancing the two metrics.
The F1-score for class 0.0 (0.82) is relatively high, indicating good performance in identifying negatives, whereas the score for class 1.0 (0.31) shows poor performance in identifying positives.

Support:
Class 0.0: 4615 instances.
Class 1.0: 2025 instances.
Support refers to the number of actual occurrences of each class in the dataset, suggesting that there are more negative cases than positive cases in this dataset.

2. Overall Accuracy
The overall accuracy of the model is reported as 71%, meaning that it correctly predicts the outcome for approximately three-quarters of all instances in the dataset.

3. Macro and Weighted Averages
Macro Average:
Precision: 0.65
Recall: 0.57
F1-Score: 0.56
The macro average treats all classes equally, regardless of their support.

Weighted Average:
Precision: 0.68
Recall: 0.71
F1-Score: 0.66
The weighted average considers the support (number of true instances) for each class, providing a more balanced view when dealing with imbalanced datasets.

**Implications and Recommendations**:

Imbalanced Classes: The significant disparity between precision and recall for class 1.0 suggests that the model struggles to identify positive cases effectively, which may be critical in medical contexts like AIDS diagnosis.

**Model Improvement:**

Needed to consider techniques such as oversampling the minority class (class with HIV), undersampling the majority class, or using synthetic data generation methods like SMOTE to balance the dataset.

Needed to experiment with different algorithms or ensemble methods (e.g., Random Forests or AdaBoost) that might better capture complex patterns in imbalanced datasets.

Threshold Adjustment: Adjusting the classification threshold could help improve recall for class 1.0 at the cost of precision, which may be acceptable depending on clinical needs (e.g., prioritizing identifying as many positive cases as possible).

Further Evaluation: Utilizing additional metrics such as ROC-AUC can provide further insights into model performance across different classification thresholds.

Conclusion:
The logistic regression model shows strong performance in predicting negative outcomes but struggles significantly with positive predictions in this AIDS dataset context, highlighting areas for potential improvement and further analysis to ensure effective clinical decision-making.

**ii) Analysis of the Adaptive Boost Model**

Description of the Classification Report Output for AdaBoost with Decision Tree Estimator The classification report provides a comprehensive overview of the performance of the Adaptive Boosting (AdaBoost) model using a decision tree as the base estimator. The report includes key metrics such as precision, recall, F1-score, and support for each class.

Conclusion

The classification report indicates that the AdaBoost model with a decision tree estimator performs reasonably well in distinguishing between infected and non-infected individuals in this dataset. While precision and recall for both classes are relatively high, there is room for improvement, particularly in recall for the infected class (1.0), which is crucial in medical contexts to minimize false negatives.

Overall, this output suggests that AdaBoost effectively combines weak learners (in this case, decision trees) to create a strong classifier capable of handling classification tasks related to HIV infection status while adapting to misclassifications through its boosting mechanism.

**Conclusion and Recommendations:**

The classification report indicates that the AdaBoost model with a decision tree estimator performs reasonably well in distinguishing between infected and non-infected individuals in this dataset. While precision and recall for both classes are relatively high, there is room for improvement, particularly in recall for the infected class (1.0), which is crucial in medical contexts to minimize false negatives.

Overall, this output suggests that AdaBoost effectively combines weak learners (in this case, decision trees) to create a strong classifier capable of handling classification tasks related to HIV infection status while adapting to misclassifications through its boosting mechanism.

The classification report for the AdaBoost model using a decision tree estimator indicates that the model performs well in distinguishing between infected and non-infected individuals. Key metrics show:

Overall Accuracy: The model achieves an accuracy of 77%, suggesting that it correctly predicts the infection status for the majority of cases.

Precision and Recall: The precision for both classes is relatively high, particularly for the infected class (1.0), which is at 80%. However, recall for the infected class is lower at 70%, indicating that while the model is good at identifying positive cases when it predicts them, it misses some actual positive cases.

F1-Scores: The F1-scores of 0.78 for non-infected (0.0) and 0.75 for infected (1.0) reflect a balanced performance but highlight the need for improvement in capturing more true positives in the infected class.

**Model Evaluation:**

Implementation of cross-validation ensures that the model's performance is consistent across different subsets of the data.
It is better to consider using additional metrics such as ROC-AUC to evaluate model performance comprehensively, especially in medical contexts where false negatives can have serious consequences.

Deployment and Monitoring:
If this model is intended for real-world application, establish a monitoring system to track its performance over time and make adjustments as necessary based on new data or changing patterns in infection rates.

## License: MIT License. 

## Acknowledgment:

We want to express our heartfelt gratitude and appreciation to all the individuals who have contributed to the successful completion of our college group project.
We would also like to thank our professors, Dr. Zahid Hussain Wani and Dr. Vinay for their guidance and support. Their expertise and mentorship have been instrumental in shaping our project and pushing us toward excellence.

We want to thank our fellow group members for their hard work, dedication, and cooperation throughout the project. Each team member played a crucial role, bringing unique skills and perspectives, greatly enriching our work.

We are truly grateful for the collaboration, guidance, support, and resources provided. Thank you all for making this project a fulfilling and rewarding experience.
