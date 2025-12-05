## Project Background
​Metro Bank is a high-street retail bank dedicated to providing personalized service alongside modern financial products. Like many growing institutions, Metro Bank faces the constant challenge of balancing rapid customer acquisition, maintaining profitability across a large branch network, and minimizing risk from fraud and service failures.
​This project originates from a genuine need for executive leadership to move past siloed reports. The objective was to create a single source of truth, a comprehensive, 5-page analytical dashboard built in Advanced Microsoft Excel—that integrates the entire customer and operational journey.

The analysis is structured around the following Key Business Questions:

* **Customer Segmentation:** Who are our most valuable customer segments (e.g., Boomers vs. Millennials, Corporate vs. Retail)?

* **​Product Health:** How are our core products (Savings, Checking, Loans, Credit Cards) performing, and what is the typical customer relationship?
  
* **Operational Efficiency:** Which branches are the most profitable, and how can we optimize staff allocation?

*  **Risk & Trust:** What are the primary sources of customer complaints and fraud exposure, and how quickly are we resolving them?
   **Interactive Dashboard:** The full Power BI Sales Performance dashboard can be accessed [here]().

#### Tools & Technologies
​Primary Tool: Microsoft Excel (Advanced)
​Techniques: Excel Data Model (Power Pivot), Custom Calculated Measures/Fields, Pivot Tables, Advanced Conditional Formatting, and multi-sheet dashboard integration.

## Data Structure & Initial Checks
​This complex, multi-page dashboard was built on a robust, denormalized data model within Microsoft Excel's Power Pivot. This approach was essential for connecting raw data from four separate sheets/tables and enabling complex, cross-table calculations.
#### ​Data Model Structure:
​The core tables used to power the analysis, as derived from the Excel Data Model viewer, include:
* ​**accounts:** Contains individual account status (`AccountID`, `CustomerID`, `Account Type`, `Balance`, `Loan Amount`, `Credit Score`).
* **Customers:** Contains primary customer and branch attributes (`CustomerID`, `Age Group`, `Region`, `Income`, `Tenure`, Branch operational metrics like `Profit Margin` and `Revenue per Staff`).
* **transactions:** Captures all activity (`TransID`, `AccountID`, `Date`, `Transaction Type`, `Channel`, `Merchant`).
* **Complaints:** Contains all risk and service data (`ComplaintID`, `CustomerID`, `Complaint Type`, `Status`, `Resolution Time`, `Urgency Flag`).

* ![Image](https://github.com/user-attachments/assets/fcdf3f1e-9dd9-4204-b11f-0c48a35c21ef)

 #### Data Preparation & Calculation Highlights

* ​**Custom Calculated Measures:** The entire analysis, including key metrics like `Profit Margin` (64%), `Average Tenure` (5yrs), `Cost-to-Income Ratio`, and `YOY changes` was created using custom calculated measures and fields within the Power Pivot Data Model. This ensures dynamic accuracy across all Pivot Table and Slicer filters.
* **Relationship Management:** The model uses one-to-many relationships (e.g., Customer`[CustomerID]` to transactions`[CustomerID]`) to link transactional and complaint data back to the core customer and demographic tables.
* **Segmentation:** Data was enriched to categorize customers by `Generation` (Boomers, GenX, Millennials) and `Wealth Segment` (High, Low, Medium, Premium) for targeted analysis.
* **Efficiency Metrics:** Complex ratios like `Profit Margin` and `Branch Cost-to-Income Ratio`  were calculated to assess operational health.
![Image](https://github.com/user-attachments/assets/8dd2e0b4-6545-4f05-97f9-9b5ff1f459dc)

## Executive Summary
​Metro Bank is characterized by a strong, loyal customer base (`Average Tenure`: 5 Years) and healthy profitability (`Profit Margin`: 64%). However, two critical areas demand immediate executive focus: Digital Adoption and Risk Management.
* **Customer & Product Health:** `Savings` (38%) is the most dominant product, yet `Millennials`, despite having the highest wealth, show a less loyal profile than `Boomers`. Total Deposit is $145M, but the `Average Credit Score` is 580, suggesting moderate credit risk exposure in the current portfolio.
  
![Image](https://github.com/user-attachments/assets/22e696b0-673d-4ef2-a393-fae6524815f1)

* **Operational Efficiency**: The bank maintains a `high Profit Margin` (64%), driven by top-performing `branches` like Lisaville ($4.2M Profit). However, the `Cost-to-Income Ratio` is highly volatile, and 40% of branches have ratios above 100%, indicating widespread inefficiency.

![Image](https://github.com/user-attachments/assets/96b59e5e-e73e-4f51-8f95-a51364d7a76f)

* **Risk Exposure**: Despite a 28% decrease in total `complaints YOY`, 81% of `Premium Customers` are affected by fraud and service issues. Furthermore, 41% of complaints remain unresolved, highlighting a critical failure in customer service follow-through.

![Image](https://github.com/user-attachments/assets/2ecf4f0c-24fb-4f84-a795-7c2dbb3d203a)
  
## Insights Deep Dive (Page-by-Page)
​The dashboard is divided into five analytical modules:
 #### Customer Base Analysis
***Loyalty & Tenure**: The customer base shows strong retention with an `Average Tenure` of 5 Years. 167 customers are categorized as Loyal.

***Wealth Distribution**:`Millennials` ($114,590 Avg Income) hold the highest average income, surpassing Boomers and GenX, positioning them as the key demographic for future high-value product sales.

***Segmentation**: `Corporate customers` have the highest average wealth, but the `Private` and `Retail` segments are crucial due to their higher transaction volumes.
![Image](https://github.com/user-attachments/assets/f1547a1c-784a-4fe8-a332-b9c7ba08df86)


#### Product Performance
***Product Mix**:  `Savings ` (38%) and  `Checking ` (31%) accounts dominate the portfolio.

***Lending & Risk**:  `Approved Loan` Amount stands at $43.7M with an  `Average Credit Score ` of 580. The chart "Does Credit Card Drive Loan Decisions?" shows a slight rejection bias (592 Rejected vs 581 Approved), suggesting tight, risk-averse lending criteria.
![Image](https://github.com/user-attachments/assets/49b4f94a-4a11-4d79-903a-616a4a14af27)

#### Transaction Behavior
***Digital Adoption Gap**:  `Premium customers ` prefer Digital Channels (Online/POS), but  `low-wealth  `customers rely on Branch & ATM, highlighting an uneven digital transition and potential cost center in physical banking.

***Cash Flow**: The largest cash movements are split evenly between  `Withdrawal `,  `Payment `, and  `Deposit ` activities.

***Merchant Activity**: Top merchants driving the biggest cash flow are  `Airbnb ` ($3.0M),  `LocalStore ` ($2.6M), and  `Apple ` ($2.5M), confirming a high volume of consumer spending via digital payments.
![Image](https://github.com/user-attachments/assets/9b80950f-4be4-414f-9baf-978c72ec2ca1)

#### Branch Performance & Efficiency

​***Profitability:** `Total Profit` is $38.2M, with a healthy 64% `Profit Margin.`

***​Top Branches:** `Lisaville` ($4.2M Profit) and `Michaeltown`($3.6M Profit) are the highest-performing branches.

***​Efficiency Crisis:** The Branch `Cost-to-Income` Ratio plot shows that approximately 40% of branches are operating at a ratio above 100%, making them net loss centers for the bank.
![Image](https://github.com/user-attachments/assets/56a73334-1f05-41b8-890f-01ef650ddb85)

#### Complaints & Risk Analytics

​***Complaint Volume:** `Total fraud cases` are 142. Overall `complaints`decreased by -28% VS 2024, which is a positive trend.

***​Service Failure:** The `Avg. Resolution Time` is 34 Days, which is excessively long and a major drag on customer satisfaction. 41% of all complaints remain `unresolved.`

***​Premium Customer Risk:** 81% of `Premium Customers` are affected by service issues, meaning the bank is failing to provide adequate service to its most valuable segment. `Charges Disputes` (184) and `Fraud` (142) are the top two complaint types.
![Image](https://github.com/user-attachments/assets/9bab4318-ef21-4458-8e85-9c1200107d4b)

## Business Recommendations

​The following strategic recommendations are based on the need to stabilize the core banking functions, improve efficiency, and protect the high-value customer base:
​Immediate Resolution Initiative:

**Customer Segmentation:** Who are our most valuable customer segments (e.g., Boomers vs. Millennials, Corporate vs. Retail)

**​Targeted Digital Migration**: Develop specific incentives and education programs to shift low-wealth customers from high-cost Branch/ATM use to Online/POS channels to reduce operational costs.

**​Branch Restructuring & Investment:**
​Prioritize investment and expansion in high-profit branches like Lisaville.

**​Review:** Place all branches with a Cost-to-Income ratio above 100% under immediate cost review and restructuring to eliminate loss centers.

**​Millennial Wealth Strategy**: Design and market personalized savings/investment products directly to the Millennial segment, leveraging their high average income and wealth to convert them into Loyal and Legacy customers.

**​Fraud and Dispute Workflow Optimization**: Given that Charges Disputes and Fraud are the top concerns, implement a specialized, fast-track workflow for these specific product-related issues to reduce exposure and protect customer assets
