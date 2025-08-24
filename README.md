# Credit EDA & Default Prediction

This project performs **Exploratory Data Analysis (EDA)** and builds a **machine learning model** to predict credit default risk.  
It is based on the Home Credit Default Risk dataset, which is **imbalanced** (more non-defaulters than defaulters).  

To handle this imbalance, we used **XGBoost**, which is robust and works well even with skewed datasets.

---

## 📌 Project Overview
- Perform in-depth EDA to understand borrower profiles.
- Visualize distributions of key features (loan amount, income, annuity, etc.).
- Detect patterns between clients who repay vs. those who default.
- Handle **imbalanced dataset** problem.
- Train ML models with a focus on **XGBoost**.

---

## 📊 Key EDA Insights
(Add your own insights here once you finalize all visualizations)

- **Loan Amount Distribution**: Most loans are between **200k–600k**; very few exceed **1M**.  
  👉 Example: In a bank, most people borrow ₹5–10 lakhs, but very few borrow ₹50+ lakhs.

- **Income Distribution**: Majority of applicants earn between X and Y, but a small group has very high income.

- **Credit Term (Annuity vs Credit)**: Longer-term loans tend to default more.

- **Imbalance Observation**: Defaulters are much fewer than non-defaulters (dataset skewed).  
  This imbalance is why **XGBoost** was chosen.

---

## 📷 Visualizations (Sample Captions)
These are captions you can directly use under your screenshots in GitHub:

1. **Credit Amount Distribution**  
   Most borrowers take moderate loans (200k–600k). Very few loans exceed 1M.

2. **Income Distribution**  
   Income is right-skewed — majority of applicants earn low to medium income, with very few very high earners.

3. **Age Distribution**  
   Most applicants are between 30–50 years old.

4. **Default vs Non-Default Ratio**  
   Dataset is highly imbalanced: very few defaults compared to non-defaults.

<img width="1920" height="1080" alt="Screenshot (63)" src="https://github.com/user-attachments/assets/937a00a9-2128-44e2-8b8a-399bb2175b8d" />
Applicant Income Distribution (AMT_INCOME_TOTAL)

Most people earn between 100k – 300k annually (around ₹10k–25k/month if in INR).
Very few earn very high (500k+).
Example: Most borrowers are average salaried employees, not very rich people.
This helps us understand who the typical borrower is.



<img width="1920" height="1080" alt="Screenshot (62)" src="https://github.com/user-attachments/assets/ae09bc16-71c0-459c-8c91-6d9c09a624e3" />
Correlation Heatmap with Target
Strongest predictors of default are EXT_SOURCE_1, 2, 3 (external credit scores).
These are negatively correlated → higher external score = less chance of default.
Other features: Age (DAYS_BIRTH), ID publish date, phone change date, goods price also matter.
Example: Think of EXT_SOURCE as a "credit rating from another agency" → higher rating = safer borrower.
So, credit history/ratings are most important in predicting loan default.



<img width="1920" height="1080" alt="Screenshot (61)" src="https://github.com/user-attachments/assets/d2bb3214-9d63-4d02-bd2c-25cc028acef9" />
Default Rate by Gender
Both men and women mostly repay, but women are slightly more likely to repay than men.
Defaults are low overall, but you see more defaults among men proportionally.
Example: If 100 men and 100 women borrow → maybe 10 men default, but only 7 women default.
This suggests gender has some influence, but not the main factor.



<img width="1920" height="1080" alt="Screenshot (60)" src="https://github.com/user-attachments/assets/8e08a527-0006-48ed-9985-5b2bb3cf112e" />
Credit Amount Distribution (AMT_CREDIT)
Distribution shows most loans are small to medium (peak around 200k–600k).
Very few loans are very large (1M+).
Example: In a bank, most people borrow ₹5–10 lakhs, but very few borrow ₹50+ lakhs.
This tells us most borrowers take moderate loans.



<img width="1920" height="1080" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/71360a44-4ecc-412c-9c5a-6e22f488f994" />
Loan Repayment Distribution (TARGET)
Graph shows most loans are repaid (0), very few are default (1).
Numbers: about 92% repaid, 8% default.
Example: Imagine 1000 people take loans → about 920 repay, 80 default.
This shows class imbalance (data is uneven).


---

## ⚙️ Requirements
To run this project, install dependencies:

```bash
pip install -r requirements.txt
