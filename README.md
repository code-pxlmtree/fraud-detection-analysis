# Fraud Detection Analysis
## Executive Overview
Financial institutions process millions of transactions daily. Even a small percentage of fraudulent transactions can result in:
- Significant financial losses
- Reputational damage
- Regulatory penalties
- Loss of customer trust

The objective of this project is to analyse transaction data to:
- Identify patterns that distinguish fraudulent from legitimate transactions
- Detect high-risk transaction characteristics
- Develop rule-based risk flags

## Dataset
The dataset was obtained from kaggle on this link: https://www.kaggle.com/datasets/priyamchoksi/credit-card-transactions-dataset

## Analysis and Key Findings
After the dataset was cleaned by removing duplicates and filling in null values, I started analysing the data.
### Fraud Distribution
Fraud represented a very small proportion of total transactions confirming a class imbalance problem, with fraudulent transactions representing 0.57% of total transactions.
Note:
0 = Legitimate transaction
1 = Fraudulent transaction

<img width="1373" height="208" alt="Screenshot (176)" src="https://github.com/user-attachments/assets/dc752f80-2a60-4185-8198-37fae7f12d40" />

### Time of Day Fraud Spikes
I looked at what hours fraudulent transactions occurred the most. It was clear that fraud activity increased significantly during late-night and early morning hours (22:00 - 03:00) with minimal fraud activities during business hours.

<img width="867" height="734" alt="Screenshot (177)" src="https://github.com/user-attachments/assets/6de51e35-0433-4b62-bf76-dc3f647b891f" />

This suggests that fraud detection and prevention applications should be implemented during high-risk hours so as to limit cost to the bank.

### Amount Anomalies
The boxplots did not reveal any outliers for fraud activities. Which shows that the bank has not suffered a high amount fraud transaction therefore measures put in place for fraud prevention are working as designed for the most part.

<img width="914" height="713" alt="Screenshot (178)" src="https://github.com/user-attachments/assets/70094db5-fcd1-43b0-9945-81f5b0a8b85a" />

### Risk Flags
We looked at two rule-based fraud indicators in order to see what is the probability for a fraudulent transaction to occur in these fraud risk situations 1. High Amount Risk Flag and 2. Night Transction Risk Flag.

The high amount risk flag showed that amounts that were classified as High Amounts (In the 95th percentile of transaction amount) had a fraud probability of **8.68%** while normal transactions only had a fraud probability of 0.15%. This demonstrates that there is a substantial increase (~59x increase) in fraud probability when transaction amounts exceed a risk threshold.

The night transaction risk flag showed similar findings with transactions in the late-night and early morning period (22:00 - 05:00) had a fraud probability of **10.37%**, while transactions in the other hours of the day had a fraud probability of 0.46% 

<img width="741" height="574" alt="Screenshot (179)" src="https://github.com/user-attachments/assets/dc086820-9933-4520-8262-6631ffb8005b" />

## Business Recommendations
Based on the findings, the bank could:
- Trigger step-up authentication for high-value transactions
- Increase monitoring intensity during high-risk hours (22:00 - 05:00)
- Assign higher fraud scores to transactions meeting multiple risk conditions
- Implement anomaly-based alerts for extreme amount deviations

## Skills Demonstrated
This project simulates how banks and fintech institutions may approach fraud detection and it showcases practical skills in:
1. Python (Pandas, Matplotlib)
2. Feature engineering
3. Risk analysis
4. Business interpretation of data

## References
- Quang Dong, 2023 https://medium.com/quant-ai-lab/fraud-credit-card-transaction-dataset-feature-engineering-exploratory-data-analysis-63001299d429
