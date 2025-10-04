### INSURANCE RISK & CLAIMS ANALYSIS ###
DOMAIN DOCUMENT
This dataset contains detailed information about car insurance policyholders, their vehicles, and their claim history. Each record represents an individual customer with demographic details such as birthdate, gender, marital status, education level, household income, and parental status. These attributes provide a strong basis for understanding customer profiles and how personal characteristics may influence driving behaviour and insurance risk.
The dataset also captures rich details about the insured vehicle, including car make, model, colour, year of manufacture, and usage type (personal, commercial, or commuting). Combined with the coverage zone, this information helps in assessing environmental and vehicle-related risk factors. For example, an older car used for commercial purposes in an urban area may carry a different risk profile compared to a new personal car in a rural zone.
On the financial and claims side, the dataset includes claim amount (total cost of claims filed), claim frequency (number of claims filed), and household income. These fields are critical in evaluating customer value and risk. High-frequency claimants may signal higher risk, while high claim amounts could indicate severe accidents or expensive repairs. The Kids Driving field adds another dimension, reflecting household driving behavior, since households with multiple young drivers are typically considered riskier by insurers.
Overall, this dataset offers a comprehensive view of customers, vehicles, and claims. It can be used to build Power BI dashboards for claims analysis, customer segmentation, risk profiling, and premium optimization. Insights derived from the data can help insurance companies design fairer pricing models, identify high-risk segments, detect potential fraud, and improve customer targeting strategies.

### MATERIALS TO DO THIS PROJECT: ### 
1. Excel Link: https://srmist-my.sharepoint.com/:x:/r/personal/gp6066_srmist_edu_in/_layouts/15/doc2.aspx?sourcedoc=%7BD712891C-6F99-407B-BF10-67546B156414%7D&file=insurance_policies_data%201.xlsx&action=default&mobileredirect=true&wdOrigin=SEARCHENGINE.GOOGLE%2CAPPHOME-WEB.BANNER.UPLOAD&wdPreviousSession=720632dc-2586-4a5c-a0d3-527590652469&wdPreviousSessionSrc=AppHomeWeb&ct=1759615587569
2. Domain Document Link: 
3. Business Requriements Document Link:

### 1. ID ###
Definition: A unique identifier assigned to each policyholder or insurance record.
Type: Numeric or text (Primary Key).
Details:
Ensures each policy/customer record is unique.
Not used directly in analysis but essential for data integrity, relationships, and avoiding duplicates.
Business Use: Helps track individual policyholders across multiple datasets (e.g., linking claims, payments, or renewals).

### 2. Birthdate ###
Definition: Date of birth of the policyholder.
Type: Date.
Details:
Used to calculate the Age of the policyholder.
Age is a strong factor in insurance risk assessment (younger drivers may have more accidents, older drivers may have slower reflexes).
Business Use:
Segment customers into age groups (e.g., <25, 25–40, 40–60, 60+).
Age-based pricing of premiums and risk profiling.

### 3. Car Color ###
Definition: The exterior color of the insured car.
Type: Categorical (text).
Details:
Although color doesn’t directly affect risk, it can influence car visibility, theft probability, and customer preferences.
Business Use:
Explore patterns (e.g., some studies suggest red cars might be involved in more speeding cases).
Insights for fraud detection (unusual color-claim patterns).

### 4. Car Make ###
Definition: The manufacturer/brand of the car (e.g., Toyota, Ford, BMW).
Type: Categorical.
Details:
Different makes have varying repair costs and accident likelihood.
Business Use:
Analyze claims by car brand.
Identify which brands have higher claim frequency (riskier) vs lower claims (safer).
Useful for underwriting and premium adjustments.

### 5. Car Model ###
Definition: Specific model of the car (e.g., Toyota Corolla, BMW X5).
Type: Categorical.
Details:
Provides deeper granularity beyond car make.
Claim risk can vary significantly between models of the same make.
Business Use:
Compare claims for luxury vs economy models.
Useful for loss ratio analysis by vehicle type.

### 6. Car Use ###
Definition: The primary purpose of the car (e.g., Personal, Commercial, Commute).
Type: Categorical.
Details:
Commercial and commuting cars usually have higher claim rates due to greater exposure (more time on the road).
Business Use:
Pricing policies differently for personal vs commercial use.
Risk profiling based on usage patterns.

### 7. Car Year ###
Definition: The manufacturing year of the car.
Type: Numeric.
Details:
Helps calculate Car Age = Current Year – Car Year.
Older cars may break down more often or have lower resale/repair costs.
Business Use:
Assess claim likelihood by vehicle age.
Create segments like New (<3 years), Mid-age (3–10 years), Old (>10 years).

### 8. Coverage Zone ###
Definition: The geographic risk area where the policyholder resides/uses the car (e.g., Zone A, Urban, Rural).
Type: Categorical.
Details:
Location impacts accident probability, theft risk, and repair costs.
Urban areas → higher claim frequency, rural areas → fewer accidents but possibly more severe damage.
Business Use:
Compare performance across regions.
Useful for mapping dashboards in Power BI.

### 9. Education ###
Definition: The highest education level attained by the policyholder (e.g., High School, Graduate, Postgraduate).
Type: Categorical.
Details:
Education level often correlates with income and risk behavior.
Business Use:
Check claim frequency by education group.
Insights for marketing campaigns and segmentation.

### 10. Gender ###
Definition: Gender of the policyholder (Male, Female, Other).
Type: Categorical.
Details:
Gender differences in claim patterns may exist.
Business Use:
Risk analysis by gender group.
Demographic breakdowns in dashboards.

### 11. Marital Status ###
Definition: Marital status of the policyholder (Single, Married, Divorced, etc.).
Type: Categorical.
Details:
Married people are often seen as more stable, potentially lower risk.
Business Use:
Compare claims between singles vs married customers.
Factor in pricing and risk adjustment.

### 12. Parent ###
Definition: Whether the policyholder has children (Yes/No).
Type: Boolean / Categorical.
Details:
Parents may drive differently compared to non-parents.
Business Use:
Segment claims and policies by parent status.
Combine with Kids Driving for more detailed household analysis.

### 13. Claim Amt ###
Definition: Total monetary value of claims filed by the policyholder.
Type: Numeric (currency).
Details:
A critical measure of insurance losses.
Business Use:
Used to calculate total losses, average claim amount, and claim ratios.
Identify high-cost claims for fraud detection.

### 14. Claim Freq ###
Definition: The number of claims filed by the policyholder.
Type: Numeric (integer).
Details:
Frequency of claims indicates risk behavior.
Business Use:
KPI for customer risk assessment.
Combined with Claim Amt → identifies whether risk is due to high frequency or high severity.

### 15. Household Income ###
Definition: Annual income of the policyholder’s household.
Type: Numeric.
Details:
Income level affects affordability of premiums and vehicle type.
Business Use:
Segment customers into income bands.
Compare claim patterns across income groups.
Target marketing/policy offers (e.g., premium insurance for high-income households).

### 16. Kids Driving ###
Definition: Number of kids in the household who are licensed drivers.
Type: Numeric (integer).
Details:
Values (1, 2, 3…) indicate number of kids driving.
More kids driving generally = higher accident probability.
Business Use:
Analyze claims by number of kids driving.
Group into categories (e.g., None, 1 Kid, 2 Kids, 3+ Kids).
Helps insurers estimate family household risk.



### BUSINESS REQUIREMENT ###
An insurance company is looking to better understand its policyholder base and claim patterns to make data-driven business decisions. Currently, policy and claims data are scattered across multiple sources, making it difficult for stakeholders to track performance and identify trends.
The company requires a centralized interactive dashboard in Power BI that can provide a clear overview of:

### KPI’s Requirements: ###
1. Total Policies – to measure the size of the active customer base. 
     ![Total Policies](https://github.com/user-attachments/assets/71a87aef-1e6b-477d-ae69-75c9c9d9fd5c)
   2. Total Claim Amount – to track the overall financial impact of claims.
    ![Total Claim Amount](https://github.com/user-attachments/assets/c28e4a06-3108-4502-b68b-7b7da7ce9f54)
3. Claim Frequency – to analyse how often claims are being made. 
4. Average Claim Amount – to assess claim severity and potential risk exposure. 
    ![Avg Claim Amount](https://github.com/user-attachments/assets/aad1b7e0-d071-43c8-be0b-7cefbca90952)
5. Gender-wise Total Policies – to understand customer distribution across genders for better segmentation and policy targeting.
    ![Gender-wise Total Policies ](https://github.com/user-attachments/assets/75d43a49-9c58-4d20-8b73-dc68c3b25858)
    

### Chart’s Requirements: ###
To deep dive into the data, we need to go beyond KPIs and analyse different aspects of insurance policies and claims. Charts help us visually explore patterns, relationships, and anomalies across customer demographics, car details, and claim behaviours. By analysing charts, stakeholders can identify risk factors, understand customer segments, and optimize policy decisions.

For this report, all visualizations are designed around two key dynamic measures:
  - Total Claim Amount
  - Total Policies
These measures provide the foundation to compare, filter, and segment the data effectively.


### Visualization Requirements: ###
1. By Car Use (Donut Chart) – To analyse policy distribution and claim amounts based on how cars are being used (e.g., personal, commercial).
    ![Total Claim Amount by Car Use](https://github.com/user-attachments/assets/af959791-2936-49f6-b200-0bc46043d259)
2. By Car Make (Bar Chart) – To identify which car brands have higher policies and claims, highlighting brand-based risks.
    ![By Car Make (Bar Chart)](https://github.com/user-attachments/assets/7740dc84-57dc-42ac-aa36-fad5e6565bc8)
3. By Coverage Zone (Donut Chart) – To evaluate policies and claims by geographic zones, useful for regional risk analysis.
    ![By Coverage Zone (Donut Chart)](https://github.com/user-attachments/assets/67c1afa7-e396-4a13-8a71-dfbb670c3aaf)
4. By Age Group (Frequency Chart/Histogram) – To assess policyholders’ age distribution and identify which age brackets file more claims.
    ![By Age Group (Frequency Chart or Histogram)](https://github.com/user-attachments/assets/26e5c3e8-e134-423e-a59e-d7fa90a390bb)
5. By Car Year (Area Chart) – To analyse how the car’s age (year of manufacture - from 1990's) impacts policy counts and claim amounts.
    ![By Car Year (Area Chart)](https://github.com/user-attachments/assets/30bf0416-b0bf-44ec-9f04-a88c2579029f)
6. By Kids Driving (Ribbon Chart) – To compare the impact of young drivers in households on policy count and claim amounts.
    ![By Kids Driving (Ribbon Chart)](https://github.com/user-attachments/assets/70c253b4-af24-4bc5-ace2-40d0681b3589)
7. By Education (Pie Chart) – To understand how education levels correlate with insurance policy adoption and claims.
    ![By Education (Pie Chart)](https://github.com/user-attachments/assets/bcca76fe-2f96-4a24-a50e-4dbad7cc5fad)
8. By Education & Marital Status (Matrix Heat Grid) – To explore the combined effect of education and marital status on policies and claims, highlighting customer profiles.
    <img width="606" height="329" alt="By Education   Marital Status (Matrix Heat Grid)" src="https://github.com/user-attachments/assets/1830370b-c2ca-4e65-9d5c-8c6dd6469647" />




### Conclusion ###

The Insurance Risk & Claims Analysis project provides a comprehensive understanding of policyholder demographics, vehicle characteristics, and claim behaviors through an interactive Power BI dashboard. By consolidating scattered datasets into a single, visual platform, this analysis empowers insurers to make data-driven decisions with clarity and precision.

The dashboard’s KPIs and visual insights reveal crucial trends such as high-risk customer segments, claim frequency variations, and car usage impact on claim costs. Through detailed segmentation by factors like age group, car make, coverage zone, education, and family composition, insurance professionals can identify patterns that drive risk and profitability.

Overall, this project enables insurance companies to:
    - Optimize premium pricing based on real risk profiles.
    - Enhance fraud detection through anomaly identification.
    - Improve customer targeting using demographic insights.
    - Strengthen operational efficiency by monitoring key performance metrics in real time.

By integrating analytics and visualization, this solution transforms raw data into actionable intelligence—helping insurers move from reactive claim management to proactive risk mitigation.



### Overall Dashboard Image: ###
![Overall Dashboard Image](https://github.com/user-attachments/assets/28254118-0d35-4015-99d9-5361713937d6)

