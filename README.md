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
I looked at what hours fraudulent transactions occurred the most. It was clear that fraud activity increased significantly during late-night and early morning hours (22:00 - 03:00) with minimal to no fraud activities during business hours.

<img width="867" height="734" alt="Screenshot (177)" src="https://github.com/user-attachments/assets/6de51e35-0433-4b62-bf76-dc3f647b891f" />

This suggests that fraud detection and prevention applications should be implemented duting high-risk hours so as to limit cost to the bank.
