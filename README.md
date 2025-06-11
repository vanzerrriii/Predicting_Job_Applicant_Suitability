# Predicting Job Applicant Suitability

![Hiring Banner](Images/We%20Re%20Hiring%20Clipart%20Transparent%20Background,%20Modern%20Design%20We%20Are%20Hiring%20To%20Join%20Work%20Team%20In%20Geometric%20Style,%20Join,%20Advertisement,%20Carreer%20PNG%20Image%20For%20Free%20Download.jpeg)

## Project Goal  
The objective of this project is to build a machine learning model that predicts whether a job applicant is suitable for a particular role based on their background. This supports recruitment platforms and HR tech firms in streamlining candidate screening, reducing manual effort, and improving the quality of shortlisted applicants.

---

## Overview  
This analysis explores a dataset of job applicants to classify them as "suitable" or "not suitable" for a job role. The dataset, obtained from Kaggle, includes a variety of candidate attributes such as education, major, years of experience, and company background. The project applies several classification algorithms to create a predictive model that can assist hiring platforms and HR systems in making faster, data-driven decisions.

### Key Activities:
- Data cleaning and preprocessing  
- Exploratory data analysis (EDA) to identify patterns  
- Classification modeling and evaluation  
- Hyperparameter tuning and feature importance analysis  

---

## Business Problem  
Recruiters are overwhelmed by large volumes of job applications, making manual resume screening inefficient, inconsistent, and prone to bias. Companies need a solution to:
1. Automate early-stage screening
2. Identify top candidates faster
3. Reduce time-to-hire and hiring costs

This project seeks to answer:
- Can we predict applicant suitability reliably?
- Which candidate features are most predictive?
- Which classification model performs best for this task?

---

## Data  
The dataset is sourced from [Kaggle - HR Analytics Job Change of Data Scientists](https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists) and includes:
- **Features**: Education level, major, years of experience, gender, company type, university enrollment, etc.
- **Target**: Suitability (1 = Suitable, 0 = Not Suitable)

### Data Preprocessing:
- Combined training and test sets for exploratory analysis  
- Handled missing values and performed categorical encoding  
- Balanced the dataset to account for class imbalance  

---

## Methods  
We applied both descriptive analysis and classification modeling.  
### Models Used:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting

### Evaluation Metrics:
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC Score  

---

## Results  

### Model Comparison Summary:

| Model              | Accuracy | Precision (Class 1) | Recall (Class 1) | ROC-AUC |
|-------------------|----------|---------------------|------------------|---------|
| Logistic Regression | 75.2%   | 53%                | 36%             | 0.70    |
| Decision Tree       | 71.8%   | 49%                | 38%             | 0.66    |
| Random Forest       | 76.3%   | 54%                | 39%             | 0.71    |
| **Gradient Boosting** | **77.1%** | **56%**             | **40%**          | **0.72** |

![Confusion Matrix](Images/confusion%20matrix.png)

---

## Key Data Insights  

### 1. Relevant Experience  
Applicants with relevant experience are significantly more likely to be labeled suitable.  
![Relevant Experience](Images/experience%20vs%20suitability.png)

### 2. Suitability Distribution  
Clear class imbalance exists — fewer candidates are marked suitable.  
![Suitability Distribution](Images/relevance%20vs%20suitability.png)

### 3. University Enrollment  
Those enrolled in full-time programs show higher suitability scores.  
![University Enrollment](Images/university%20vs%20suitability.png)

### 4. Company Type  
Suitable applicants mostly come from private companies; missing data correlates with unsuitability.  
![Company Type](Images/company%20vs%20suitability.png)

---

## Conclusion  

1. **Feature Importance**  
   - Relevant experience, education, and company background are strong predictors of suitability.

2. **Model Effectiveness**  
   - Gradient Boosting performed best overall. It had the highest accuracy and balanced precision-recall for suitable applicants.

3. **Business Value**  
   - This model can help automate early-stage applicant filtering, saving time and improving shortlisting quality.

---

## Recommendations  

1. **Integrate the Gradient Boosting model** into recruitment platforms for initial screening.  
2. **Use key features (experience, education, company type)** to prioritize applicants.  
3. **Periodically retrain the model** with new data to adapt to changing hiring trends.  
4. **Include human oversight** for final candidate decisions to avoid missing qualified applicants.

---

## Further Analysis  

- **Fairness & Bias Testing**: Evaluate the model's performance across gender and university tiers.  
- **Model Deployment**: Build an applicant scoring dashboard.  
- **Feature Expansion**: Include skill tags or resume text (via NLP) to improve accuracy.  
- **Hyperparameter Tuning**: Further refine Gradient Boosting for optimal performance.  

---

## For More Information  
- [View Presentation Slides (PDF)](Predicting_Job_Applicant_Suitability.pdf)  
- [View Full Jupyter Notebook](Predicting_Job_Applicant_Suitability.ipynb)

