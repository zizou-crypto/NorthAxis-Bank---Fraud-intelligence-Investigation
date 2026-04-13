# NorthAxis-Bank---Fraud-intelligence-Investigation
### SQL based risk analysis of suspicious $2.3M outflows | Q3 2024

----

## Project Background
NorthAxis Bank's compliance hotline recorded a 340% spike in fraud related complaints in Q3 2024. 
Internal audit flagged an estimated $2.3M  in suspicious outflows concentrated in a 6 week window. 
As a Junior Data analyst on Risk intelligence team, I was tasked with investigating transaction patterns, profiling
high-risk accounts and delivering a data backed risk report to the executive team ahead of board risk committe meeting.

----

## Tools used
- SQL server
- Power BI (Visualization)
- Github (Documentation)

-----

## Data model
The analysis was conducted on a gold layer data warehouse with a star schema consisting of 6 tables:

| Table | Description |
| ---   | ---- |
| fact_transactions | Core transaction ledger - amounts, channels, fraud flags |
| dim_customer | Customer profiles, KYC status, fraud target flag | 
| dim account | Account types, balance tiers, credit limits | 
| dim_merchant | merchant details, shell merchant flag, risk rating |
| dim_location | Geographical data, high risk country flag |
| dim_date | Calendar table with weekend and month end flags |

----

## Analytical deliverables

### 1. Transaction overview & Baseline KPIs
Established what normal looks like before hunting anomalies 
Volume, value, channel breakdown and daily trend across Q3 2024
![Daily transaction](Daily_transaction.png)


### 2. Anomaly detection & Velocity checks 
Flagged rapid repeat transactions, off hours spikes and statistical outliers using z score analysis. 


### 3. Customer risk profiling 
Built behavioral baselines per customer and surfaced daviations from thheir own transactions history

### 4. Executive risk report
Board ready summary of estimated exposure, top accounts recommended for freezing, channels to restrict and merchants to blacklist. 

### Key findings summary
