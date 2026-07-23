# Telco Churn Operations Dashboard

![Operations Dashboard](Telco%20Operations%20Dashboard.png)
![Data Model](Telco%20Data%20Model.png)

## Overview
This project analyzes customer churn within a telecommunications company using Power BI, identifying which customer segments and service attributes drive attrition, and what that means for retention strategy.

## Project Objectives
- Measure overall customer churn performance
- Identify the largest drivers of customer attrition
- Quantify churn across customer segments
- Generate actionable retention recommendations
- Support telecom decision-making with data-driven insights

## Data Model
The dataset was transformed into a dimensional model to support churn analysis in Power BI.

- 1 Fact Table (Customer Churn)
- 2 Dimension Tables (Customer, Service)
- 1 Dedicated DAX Measures Table

Relationships were structured using a star schema approach to enable efficient filtering and KPI calculations across churn segments.

## KPI Layer (DAX Measures)
I defined which KPIs the analysis needed, then used AI to help write the DAX syntax for them. I'm self-taught and still building fluency with DAX beyond core aggregation functions — using AI here is part of how I'm learning the language, not a substitute for understanding what each measure calculates and why.

| Measure | Purpose |
| :--- | :--- |
| `Total Customers` | Total customer count from the customer dimension. |
| `Total Revenue` | Total monthly charges across all customers. |
| `Customer Churn Rate %` | Share of customers who churned. |
| `Revenue Churn Rate %` | Share of monthly recurring revenue lost to churn. |
| `ARPU` | Average revenue per customer (Total Revenue ÷ Total Customers). |
| `Retained MRR` / `Churned MRR` | Monthly recurring revenue split between retained and churned customers. |

### Sample: Customer Churn Rate %
```dax
Customer Churn Rate % = 
DIVIDE(
    CALCULATE(COUNTROWS('Fact_Charges'), 'Fact_Charges'[Churn] = "Yes"),
    COUNTROWS('Fact_Charges'),
    0
)
```

## Dashboard
The dashboard provides an operational view of customer churn, highlighting risk segments, service-level drivers, and retention opportunities across customer groups.

## Findings & Business Impact

### Contract Type
| Contract Type | Churn Rate |
|--------------|------------|
| Month-to-Month | 42.71% |
| One Year | 11.27% |
| Two Year | 2.83% |

Month-to-month customers churn at more than 3x the rate of one-year contracts and 15x the rate of two-year contracts — the single clearest signal in the data, and a strong case for incentivizing longer commitments.

### Internet Service Type
| Service Type | Churn Rate |
|-------------|------------|
| Fiber Optic | 41.89% |

Fiber optic customers churn at a materially higher rate than other service types, suggesting a service quality or pricing issue worth investigating separately from contract structure.

### Payment Method
| Payment Method | Churn Rate |
|---------------|------------|
| Electronic Check | 45.29% |
| Credit Card (Automatic) | 15.24% |

Electronic check payers churn nearly 3x more than customers on automatic credit card billing — switching customers to autopay is a low-effort retention lever.

## Tools Used
- Power BI
- Power Query
- DAX (AI-assisted)
- Data Modeling (Star Schema)
- Data Visualization & Business Intelligence
