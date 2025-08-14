<img width="1332" height="725" alt="image" src="https://github.com/user-attachments/assets/afa69a3c-a407-4172-9841-26794ccc0f6e" /><img width="1332" height="725" alt="image" src="https://github.com/user-attachments/assets/9b40d980-e907-482a-a6ca-b31986e6bc49" />
💓 Heart Disease Analysis Dashboard

This project is a **data-driven, interactive Power BI dashboard** designed to analyze **heart disease survival trends** across different age groups and genders. It provides **clear, actionable insights** into key medical and demographic factors influencing patient outcomes.

---

 🔍 Overview

The dataset contains **medical and demographic records** of heart disease patients. Through advanced **DAX calculations** and **visual storytelling**, the dashboard highlights:

* Total Deaths vs. Survivals
* Survival Rate & Average Age of Survival
* Gender-based Comparison (Female, Male, Combined)
* Impact of Key Health Factors

  * Serum Creatinine Levels
  * Ejection Fraction
  * High Blood Pressure
  * Anaemia
  * Smoking
  * Diabetes

---

 📊 Key Visuals

* Survival Rate by Age Group
* Death Count vs. Serum Creatinine
* Death Count vs. Ejection Fraction
* Spline Chart for comorbidities
* Gender Toggle to compare trends across M/F

---

## ⚙️ Tools & Technologies

* Power BI for dashboard design and interactivity
* DAX for custom measures:

  ```DAX
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
  ```
* Data Cleaning & Modeling** for accuracy and consistency

---

 📁 Dashboard Views

1. Overall Population Analysis
 <img width="1332" height="725" alt="image" src="https://github.com/user-attachments/assets/b0b6ed0d-6d64-441e-9291-436a4eb91317" />

   
3. Female-Only Analysis
4. Male-Only Analysis


 📎 Use Cases

* Health risk profiling by demographic group
* Identifying age groups at higher cardiac risk
* Comparative gender-based health analytics
* Storytelling in medical data with interactive visuals

---

If you want, I can expand this into a full portfolio project write-up** with a **project objective, methodology, dataset description, insights, and screenshots**, so it becomes a ready-to-upload **resume and LinkedIn showcase project**.

Do you want me to prepare that next?
