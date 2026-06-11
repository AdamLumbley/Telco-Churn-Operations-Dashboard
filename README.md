Telco Churn Operations Dashboard
Overview

This project analyzes customer churn within a telecommunications company using Power BI. The goal was to identify the primary drivers of churn and provide actionable recommendations to improve customer retention and reduce revenue loss.

In addition to dashboard development, the original 21-column flat dataset was redesigned into a lightweight dimensional model to improve report organization, scalability, and performance.

Data Model

The original dataset was transformed into a dimensional model consisting of:

1 Fact Table
2 Dimension Tables
1 Dedicated DAX Measures Table

This structure replaced a single 21-column table and improved model clarity while supporting faster report performance.

Data Model

Dashboard

The dashboard provides an operational overview of churn performance, customer behavior, and retention opportunities.

Operations Dashboard

Project Objectives
Measure overall customer churn performance
Identify the largest drivers of customer attrition
Quantify churn across customer segments
Generate actionable retention recommendations
Support telecom decision-making with data-driven insights
Key Findings
Contract Type

Contract length was the strongest predictor of churn:

Contract Type	Churn Rate
Month-to-Month	42.71%
One Year	11.27%
Two Year	2.83%

Customers on month-to-month contracts churn at dramatically higher rates than customers committed to longer-term agreements.

Recommendation: Increase customer migration into one- and two-year contracts to improve retention and stabilize recurring revenue.

Internet Service Type
Service Type	Churn Rate
Fiber Optic	41.89%

Fiber Optic customers exhibited significantly higher churn rates than expected.

Recommendation: Conduct further analysis to determine whether churn is driven by pricing, service quality, competition, customer expectations, or support issues.

Payment Method
Payment Method	Churn Rate
Electronic Check	45.29%
Credit Card (Automatic)	15.24%

Customers using electronic checks churned at nearly three times the rate of customers using automatic credit card payments.

Recommendation: Encourage customers to adopt automatic payment methods to reduce payment friction and improve retention.

Business Impact

The analysis identified three major opportunities to reduce customer churn:

Transition customers away from month-to-month contracts.
Investigate elevated churn among Fiber Optic customers.
Increase adoption of automatic payment methods, particularly credit card autopay.

Together, these initiatives have the potential to significantly improve customer retention and protect recurring telecom revenue.

Tools Used
Power BI
Power Query
DAX
Dimensional Data Modeling (Star Schema)
Data Visualization & Business Intelligence
