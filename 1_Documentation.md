This file contains detailed description about each of the datasets to be considered for checking TabPFN performance.

---
# Industrial Domain - Manufacturing


## 1. `AI4I 2020 Predictive Maintenance Dataset`
- **Description:** The AI4I 2020 Predictive Maintenance Dataset is a synthetic dataset that reflects real predictive maintenance data encountered in industry.
- **Source:** <a href="https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset">UCIMLR</a>
- **File:**  ![CHANGE.csv](datasets/Industry_Manufacturing/AI4I_2020_Predictive_Maintenance.csv)
- **#Rows:** 10000
- **#Features:** 14
- **Target:** `Machine Failure`
- **#Views:** 85066 (as of October 21, 2025)
- **Additional Description:** "Since real predictive maintenance datasets are generally difficult to obtain and in particular difficult to publish, we present and provide a synthetic dataset that reflects real predictive maintenance encountered in industry to the best of our knowledge."
- **Features:** <br>
`UDI`: Unique ID <br>
`Product ID`: Unique Product ID<br>
`Type`: Product Quality Variant. L: Low, M: Medium, H: High<br>
`Air Temperature [K]`: Generated with random walk process normalised to a standard deviation of 2K<br>
`Process Temperature [K]`: Generated with random walk process normalised to a standard deviation of 1K added to air temperature plus 10K<br>
`Rotational Speed [rpm]`: Calculated from power of 2860W, overlaid with normal noise<br>
`Torque [Nm]`: Torque values are normally distributed around 40Nm with a σ = 10 Nm and no negative values<br>
`Tool Wear [min]`: Quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process<br>
`TWF (Tool Wear Failure)`: Tool will be replaced or fail at a randomly selected tool wear time between 200 – 240 mins<br>
|- Case for 120 data points <br>
`HDF (Heat Dissipation Failure)`: Heat dissipation causes a process failure, if the difference between air and process temperature is 
below 8.6 K and the tool’s rotational speed is below 1380 rpm<br>
|- Case for 115 data points <br>
`PWF (Power Failure)`: Product of torque and rotational speed (in rad/s) equals the power required for the process. If this power is below 3500 W or above 9000 W, the
process fails <br>
|- Case for 95 data points <br>
`OSF (Overstrain Failure)`: If the product of tool wear and torque exceeds 11,000 minNm for the L product variant (12,000 for M, 13,000 for H), the process fails due
to overstrain<br>
|- Case for 98 data points <br>
`RNF (Random Failures)`: Each process has a chance of 0,1 % to fail regardless of its process parameters<br>
|- Case for 19 data points <br>
`Machine Failure (Target)`: Did the machine fail at this particular datapoint due to any to above five failure categories?<br>


## 7. `credit-risk`
- **Description:** This dataset contains columns simulating credit bureau data
- **Source:** <a href="https://www.kaggle.com/datasets/laotse/credit-risk-dataset/">Kaggle</a>
- **File:**  ![credit_risk_dataset.csv](./datasets/credit_risk_dataset.csv)
- **#Rows:** 32581
- **#Features:** 12
- **Target:** `loan_status`
- **#Views:** 271000 (as of September 29, 2025)
- **#Downloads:** 46100  (as of September 29, 2025)
- **Additional Description:**
- **Features:** <br>
`person_age`: Age of the individual applying for the loan.<br>
`person_income`: Annual income of the individual.<br>
`person_home_ownership`: Type of home ownership of the individual.<br>
    |- rent: The individual is currently renting a property.<br>
    |- mortgage: The individual has a mortgage on the property they own.<br>
    |- own: The individual owns their home outright.<br>
    |- other: Other categories of home ownership that may be specific to the dataset.<br>
`person_emp_length`: Employment length of the individual in years.<br>
`loan_intent`: The intent behind the loan application.<br>
`loan_grade`: The grade assigned to the loan based on the creditworthiness of the borrower.<br>
    |- A: The borrower has a high creditworthiness, indicating low risk.<br>
    |- B: The borrower is relatively low-risk, but not as creditworthy as Grade A.<br>
    |- C: The borrower's creditworthiness is moderate.<br>
    |- D: The borrower is considered to have higher risk compared to previous grades.<br>
    |- E: The borrower's creditworthiness is lower, indicating a higher risk.<br>
    |- F: The borrower poses a significant credit risk.<br>
    |- G: The borrower's creditworthiness is the lowest, signifying the highest risk.<br>
`loan_amnt`: The loan amount requested by the individual.<br>
`loan_int_rate`: The interest rate associated with the loan.<br>
`loan_percent_income`: The percentage of income represented by the loan amount.<br>
`cb_person_default_on_file`: Historical default of the individual as per credit bureau records.<br>
    |- Y: The individual has a history of defaults on their credit file.<br>
    |- N: The individual does not have any history of defaults.<br>
`cb_preson_cred_hist_length`: The length of credit history for the individual.<br>
`loan_status (Target)`: Loan status, where 0 indicates non-default and 1 indicates default.<br>
    - 0: Non-default - The borrower successfully repaid the loan as agreed, and there was no default.
    - 1: Default - The borrower failed to repay the loan according to the agreed-upon terms and defaulted on the loan.<br>
<!-- - **Model Performance:** 
![Model Performance](./results/plot_7_credit_risk.png) -->