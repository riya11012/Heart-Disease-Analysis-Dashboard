
💓 Heart Disease Analysis Dashboard 

1. Problem

Cardiovascular diseases are a leading cause of death worldwide, yet healthcare providers often struggle to quickly identify high-risk patient groups from large, complex datasets.
Hospitals and research institutions need a clear, interactive, and data-driven way to analyze survival rates across demographics and medical factors to guide early intervention strategies.

2. Strategy

I aimed to design an interactive Power BI dashboard that not only displays heart disease survival statistics but also makes it easy for healthcare professionals to explore the impact of key health factors across age groups and genders.
My approach included:
Data Cleaning & Modeling to ensure accuracy.
Creating custom DAX measures for meaningful metrics.
Designing gender-toggle views for comparative analysis.
Building visual narratives for storytelling with data.

3. Execution
Tools & Technologies:

Power BI – Dashboard creation and interactivity

DAX – Custom measures for survival rate, deaths, and age averages

Data Cleaning – Removing inconsistencies and preparing the dataset for modeling

Key DAX Measures:

  Avg Age of Survival = CALCULATE(
    AVERAGE(heart_Disease_clinical_records_[age]),
    heart_Disease_clinical_records_[DEATH_EVENT] = 0
  )

  Survival Rate = 1 - DIVIDE(
    SUM(heart_Disease_clinical_records_[DEATH_EVENT]),
    COUNT(heart_Disease_clinical_records_[count])
  )

  Total Deaths = CALCULATE(
    COUNT(heart_Disease_clinical_records_[count]),
    heart_Disease_clinical_records_[DEATH_EVENT] = 1
  )

  Total Survivals = CALCULATE(
    COUNT(heart_Disease_clinical_records_[count]),
    heart_Disease_clinical_records_[DEATH_EVENT] = 0
  )


Dashboard Features:

Overall Analysis View – Total deaths, survivals, survival rate, average age of survivors.

Gender Toggle – Switch between male, female, or combined data.

Key Visuals:

Survival rate by age group

Death count vs. serum creatinine levels

Death count vs. ejection fraction

Spline charts for comorbidities like anaemia, smoking, and diabetes


📁 Dashboard Views

1. Overall Population Analysis
   
   <img width="1322" height="736" alt="image" src="https://github.com/user-attachments/assets/7b2b875d-34c8-4436-9182-d6e0bc66d426" />
   
2. Female-Only Analysis
   
    <img width="1326" height="736" alt="image" src="https://github.com/user-attachments/assets/d259f49f-7896-4be9-830c-668151d86289" />

3. Male-Only Analysis

   <img width="1312" height="732" alt="image" src="https://github.com/user-attachments/assets/1c7a390e-dbde-4723-8c43-0adf9f408bde" />



 4.📎 Results

The final dashboard:
Improved clarity for identifying high-risk patient groups by age and gender.
Allowed interactive exploration of medical and lifestyle factors impacting survival.
Enabled quick data-driven decisions for targeted healthcare interventions.
Served as a ready-to-use analytical tool for medical researchers and hospitals.
Potential Use Cases:
Hospital cardiac departments for patient risk assessment.
Public health agencies for targeted prevention programs.
Medical researchers studying gender-specific heart disease patterns.


