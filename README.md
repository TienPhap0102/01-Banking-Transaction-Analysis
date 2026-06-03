# 🏦 Banking Transaction Analysis

<img width="1793" height="1004" alt="Ảnh chụp màn hình 2026-06-03 113918" src="https://github.com/user-attachments/assets/ad310a4c-e251-45b8-8cd1-4668d958f385" />

## 📖 Project Overview
In the highly competitive landscape of the financial services industry, understanding customer behavior, optimizing operational efficiency, and mitigating risks are paramount. This project involves the end-to-end development of a **Business Intelligence (BI) Dashboard** designed to transform raw retail banking transaction data into actionable insights. 

The system empowers management to monitor omnichannel transaction performance, evaluate customer loyalty, detect financial risks (fraud anomalies), and drive data-driven decision-making.

## 🎯 Business Objectives
*   **Customer Insights:** Analyze customer segment migration, demographics, and monitor the overall health of the customer base.
*   **Revenue & Product Performance:** Evaluate core revenue streams, with a focus on the Fee Burden across various financial products.
*   **Retention Tracking:** Measure Customer Lifetime Value (CLV) and monthly retention rates via Cohort Analysis.
*   **Risk & Fraud Management:** Monitor behavioral anomalies, credit risks, and isolate fraudulent transaction patterns.

## 🛠️ Tech Stack
*   **Data Visualization & BI:** Power BI
*   **Data Transformation:** Power Query, DAX (Data Analysis Expressions)
*   **Data Processing:** Google Colaboratory
*   **Analytical Models:** RFM (Recency, Frequency, Monetary), Cohort Analysis, Pareto Principle (80/20 Rule)

## 💾 Dataset Information
The dataset encompasses daily transactional records, customer financial profiles, and product details spanning from 2023 to 2025. 

Below is the data dictionary defining the core fields utilized in this analysis:

| Feature | Description |
| :--- | :--- |
| **TransactionID / CustomerID** | Unique identifiers for transactions and individual customers. |
| **TransactionDate** | The specific date the transaction was executed. |
| **TransactionType** | Categorization of the activity (`Deposit`, `Withdrawal`, `Transfer`, `Card Payment`, `Loan Payment`, `Fee`) |
| **Amount** | The total monetary value of the transaction. |
| **ProductCategory** | The financial product involved (`Loan`, `Credit Card`, `Checking Account`, `Savings Account`) |
| **Channel** | The platform or method used for the transaction (ATM, Branch, Mobile, Online). |
| **BranchCity** | The geographical location (city) of the branch where the transaction occurred. |
| **Fees & Penalties** | Quantitative metrics tracking additional costs (`CreditCardFees`, `InsuranceFees`, `LatePaymentAmount`) |
| **Customer Profile** | Socio-economic indicators including `CustomerScore`, `MonthlyIncome`, and derived `CustomerSegment` (Low, Middle, High Income) |
---

## 📊 Dashboard Architecture & Key Features

The dashboard is structured into 5 interactive pages:

**Business Overview:** Provides a high-level executive summary of Key Performance Indicators (KPIs) such as Total Customers, Total Transactions, and overarching revenue trends.
*   **Purpose:** Provides a high-level executive summary of the bank's overall performance.
*   **Key Analysis:** Tracks macro-level Key Performance Indicators (KPIs) such as Total Active Customers, Total Transaction Volume, and overarching revenue trends over the 2023-2025 period.

<img width="1788" height="1002" alt="Ảnh chụp màn hình 2026-06-03 114825" src="https://github.com/user-attachments/assets/ce222b8a-62a1-4d6e-bc99-dea9a370a017" />

-----
**Customer Behavior:** Analyzes the correlation between income segments and transaction values, omnichannel utilization, and the geographical distribution of transaction volumes utilizing Decomposition Trees and Map Visuals.
*   **Purpose:** Explores *who* the customers are, *where* they transact, and *how* they engage with the bank.
*   **Key Analysis:**
    *   **Geographical Distribution:** Utilizes Decomposition Trees and Map Visuals to trace transaction values down to specific cities (e.g., Murcia, Malaga).
    *   **Segment Correlation:** Analyzes the relationship between Income Segments (Low, Middle, High), Total Amount, and Average Customer Scores.
    *   **Omnichannel Utilization:** Evaluates the proportion of transactions across different platforms (ATM, Branch, Mobile, Online) to understand channel preferences.

<img width="1794" height="1007" alt="Ảnh chụp màn hình 2026-06-03 115909" src="https://github.com/user-attachments/assets/c5df2d03-a705-41b7-97f5-07ccfb05e5e1" />

-----
**RFM Analysis:** Evaluates dynamic customer segmentation based on Recency, Frequency, and Monetary metrics to pinpoint high-value "Champions" and churn-prone "At-Risk" groups.
*   **Purpose:** Dynamically segments the customer base to identify the most valuable users and those at risk of churning.
*   **Key Analysis:**
    *   **Customer Segmentation:** Maps users into distinct groups (e.g., *Champions, Loyal, At-Risk, Hibernating*) based on their R-F-M scores.
    *   **Pareto Analysis (80/20 Rule):** Demonstrates value concentration, revealing that the top segments consistently drive ~65% of the total monetary value.
    *   **Channel by Segment:** Breaks down how different segments (e.g., Champions vs. Lost Customers) utilize banking channels.
 
<img width="1794" height="1011" alt="Ảnh chụp màn hình 2026-06-03 120059" src="https://github.com/user-attachments/assets/4f553e32-dd41-416c-bdb2-0755ed12bd62" />

-----
**Revenue Analysis:** Tracks omnichannel transaction flows and assesses product-specific fee profitability and burdens (Loans, Credit Cards) across different income segments.
*   **Purpose:** Investigates the core revenue drivers and evaluates the financial burden placed on different customer groups.
*   **Key Analysis:**
    *   **Fee Burden Ratio:** Highlights the disparity in fee burdens across income groups, showing a significantly higher risk (1.87%) for Low-Income customers.
    *   **Product-Segment Matrix:** Identifies *Loans* and *Credit Cards* as the primary fee-generating products, especially within the Middle-Income segment.
    *   **Trend Analysis:** Tracks the total fee revenue by month and transaction type to identify seasonal peaks or drop-offs.

<img width="1791" height="997" alt="Ảnh chụp màn hình 2026-06-03 120208" src="https://github.com/user-attachments/assets/a443c07b-a8e9-4046-b7d3-4d1e0851692c" />

-----
**Cohort Analysis:** Visualizes the customer lifecycle, new user acquisition trends, and monthly Retention Rates to evaluate long-term engagement.
*   **Purpose:** Measures the effectiveness of customer acquisition and long-term retention strategies.
*   **Key Analysis:**
    *   **Acquisition Tracking:** Highlights the sharp decline in new user acquisition in 2025.
    *   **Retention Matrix:** Visualizes the month-over-month return rate of specific customer cohorts (starting from Jan 2023) to pinpoint exactly when users drop off.
    *   **Customer Lifetime Value (CLV):** Tracks the average revenue generated per user over their lifecycle, highlighting a critical drop in 2025.

<img width="1785" height="1005" alt="Ảnh chụp màn hình 2026-06-03 120251" src="https://github.com/user-attachments/assets/ade16cf0-12e9-45bd-888d-06ecb26f5e7c" />

-----
# 💡 Top Analytical Findings

*   **Primary Revenue Drivers:** The *Middle Income* segment and *Loan* products are the core engines generating the highest transaction volume and fee revenue.
*   **Retention Crisis (2025):** A sharp decline in New Customers (down 61.6% in 2025), a Retention Rate drop to 30.8%, and a declining CLV highlight critical bottlenecks in acquisition and long-term user engagement.
*   **Value Segmentation (Pareto Principle):** The top 3 segments (*Champions, Loyal, At Risk*) consistently contribute **65%** of the total monetary value. The *At Risk* group generates high revenue but poses a significant churn threat.
*   **Fee Burden Inequity:** The *Low Income* segment faces a disproportionately high fee burden ratio (**1.87%** compared to 0.41% for the high-income group), elevating churn risk.
*   **Fraud & Anomaly Signals:** Fraudulent transactions exhibit higher amounts and significantly higher fees, highly concentrated in *Loan Payment* transactions. The patterns are extreme and isolated, showing no dependency on specific channels or geographies.

---

## 🚀 Strategic Recommendations & Action Plan

### 1. Overhaul Acquisition & Onboarding
*   Conduct a deep dive into marketing channel performance to identify the root cause of the 61.6% acquisition drop in 2025.
*   Implement a **90-Day Onboarding Journey** with targeted incentives (e.g., waived fees for the first month) to prevent the massive user drop-off observed from Month 0 to Month 1 in the Cohort Matrix.

### 2. Alleviate the Low-Income Fee Burden
*   Introduce **Tiered Fee Structures** or "Maintenance-Free" digital-only accounts to encourage digital channel usage, reducing operational costs while easing the 1.87% fee burden on low-income customers.
*   Deploy automated proactive payment alerts to reduce late penalty fees and improve customer financial health.

### 3. Maximize Value from Top Segments
*   Leverage transaction history to offer hyper-personalized, pre-approved Loan and Credit Card products to the *Champions* and *Loyal* segments.
*   Introduce VIP Loyalty Programs to incentivize a higher frequency of transactions and increase CLV.

### 4. Mitigate Risk in 'At-Risk' Customers
*   Develop an early-warning system utilizing the anomaly detection results to flag *At-Risk* customers showing sudden transaction drops or unusual loan payment behaviors.
*   Offer dedicated account management or debt-restructuring options to save highly profitable relationships before they churn.

---

## 📂 Repository Structure
```text
📦 Retail-Banking-Analytics
 ┣ 📂 datasets               # Raw and cleaned data (if applicable)
 ┣ 📂 images                 # Dashboard screenshots and GIFs
 ┣ 📂 python_scripts         # Python code for cleaning data
 ┣ 📜 Bank_Transaction_Dashboard.pbix # Power BI Dashboard file
 ┗ 📜 README.md              # Project documentation


