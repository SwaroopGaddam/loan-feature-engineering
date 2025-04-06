# Loan Feature Engineering: "Able to Pay"

This project focuses on feature engineering to create a new feature called **"Able to Pay"**, which helps assess a applicant's likelihood of repaying their loan. Since existing features do not provide enough direct evidence to determine loan status, this feature is designed to improve loan risk assessment.

---

## Why This Project?  
Financial institutions rely on various factors to assess a applicant's ability to repay a loan. However, existing features may not be sufficient. This project introduces the **"Able to Pay"** feature to enhance loan risk assessment by incorporating financial ratios and credit scores.

---

## Installation & Setup  

### Steps  
1. **Clone this Repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/loan-feature-engineering.git
   cd loan-feature-engineering


2. **Install dependencies**
   ```bash
   pip install -r requirements.txt

3. **Run Feature Engineering**  

   This repository includes a **Colab Notebook** that directly loads the raw data from this repo and performs feature engineering.  

      #### **How to Run:**  
      1️. Open the **Colab notebook**: [Loan Feature Engineering Notebook](https://colab.research.google.com/github/SwaroopGaddam/loan-feature-engineering/blob/main/loan_feature_analysis.ipynb)  
      2. Ensure raw data is available in your repository ([Dataset Link](https://raw.githubusercontent.com/SwaroopGaddam/loan-feature-engineering/refs/heads/main/Cleaned_loan_data.csv))  

      ✅ No manual script execution required! The notebook handles everything for you. 

4. **Feature Engineering Logic**

   The "Able to Pay" feature is based on key financial indicators:
  
     - Credit Score  → Higher scores indicate a better likelihood of repayment.
     - Loan-to-Term Ratio (LTR)  → `LoanAmount / Loan_Amount_Term`  
     - EMI-to-Income Ratio (EIR)  → `(EMI / ApplicantIncome) * 100`  
   - A lower LTR and EIR suggest a higher ability to repay. 

5. **Derived Feature: Able_to_pay_EMI**  
   ```python
   # If 30% of Total Income is greater than EMI, the applicant is likely able to pay. 
   data["Able_to_pay_EMI"] = (data["TotalIncome"] * 0.3 > data["EMI"])
   
### Exploratory Data Analysis (EDA)
   - Visualized Loan Status distributions using countplot, boxplot, histplots and crosstab function.
   - Analyzed the impact of Income vs Loan Status.
   - Hypothesis testing is performed to check the significance between given fields and the target column: Loan Status.
   - Finally created a new feature **Able_to_pay_EMI** to check the combined impact of few impacting fields on Loan Status.

Made by **Swaroop Gaddam**  
📧 [swaroop.gaddam01@gmail.com](mailto:swaroop.gaddam01@gmail.com)  
🌐 [LinkedIn – swaroop-gaddam](https://www.linkedin.com/in/swaroop-gaddam/)
