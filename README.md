# ML-C63-March-2024
Loan Dataset Analysis

**Columns for Risk Analysis:**
Identified Columns:loan_status
term
purpose
subgrade
home_ownership
pub_rec_bankruptcies
revol_util


**Dataset Columns and Descriptions**

Status : Indicates the current status of the loan.
Term: The loan term in months.
Purpose: The purpose of the loan.
Subgrade: A finer classification of the loan grade.
Home_ownership: Home ownership status (Rent, Own).
pub_rec_bankruptcies: Number of public record bankruptcies.
revol_util: Revolving credit utilization rate.

**Data Cleaning**
Removing Rows with Missing Values
Handling Blank Entries
Ensuring Data Consistency
Filter out columns with NA values and blanks.
	
	df_cleaned = df.dropna()
	df_cleaned = df_cleaned.replace("", pd.NA).dropna()

**Data Filtering Conditions**
High revol_util (greater than 50%) is associated with an increased risk of loan default. 
Term : To fetch the loan end date and compare with the last payment date.
Purpose : Bankruptcies and Home Ownership Renters have a higher occurrence of public record bankruptcies compared to homeowners.
 Subgrade Analysis: Lower subgrades (e.g., D1 and below) show a higher incidence of defaults.

**Key Findings**
High revol_util (> 50%) is associated with higher default risk.
Lower subgrades (e.g., D1 and below) show a higher incidence of defaults.
Renters have a higher occurrence of public record bankruptcies compared to homeowners.










