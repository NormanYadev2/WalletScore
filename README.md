# 💳 Aave Wallet Credit Scoring using Machine Learning (KMeans)

This project assigns DeFi credit scores (100–900) to Aave V2 wallet addresses by analyzing transaction behavior using unsupervised learning (KMeans clustering).

---


## 📖 Overview

Aave users interact with DeFi protocols without credit scores or historical risk assessments. This project aims to solve that by analyzing wallet behavior and clustering users into groups based on their repayment, borrowing, and activity patterns—ultimately assigning a credit score between **0 and 1000**.

---

## 📊 Features Used

The following wallet-level features are extracted and used to evaluate creditworthiness:

- `total_deposit`: Total deposited USD amount
- `total_borrow`: Total borrowed USD amount
- `total_repay`: Total repaid USD amount
- `repay_ratio`: Repay / Borrow
- `redeem_ratio`: Redeemed / Deposited
- `unique_assets`: Number of unique assets used
- `tx_count`: Number of wallet transactions
- `active_days`: Distinct days with wallet activity
- `avg_txn_value`: Average transaction value in USD

---

## 🧠 Machine Learning Approach

- **Preprocessing**
  - Raw JSON transaction data is converted to a pandas DataFrame.
  - Wallet-level features are extracted and scaled using `StandardScaler`.

- **Clustering**
  - `KMeans(n_clusters=5)` is used to group wallets into 5 clusters.
  - No labels are used, as this is an **unsupervised learning** task.

- **Scoring**
  - Each cluster is scored based on behavior:
    - High repay/redeem ratios
    - Higher total deposits
    - More active days
  - Clusters are ranked and assigned credit scores from 0 to 1000.

---

## 📁 Output

A CSV file is generated with the following columns:

- `wallet`: Wallet address
- `credit_score`: Score between 0-1000
- `cluster`: Cluster ID (0–4)
- Extracted feature columns (e.g., `total_deposit`, `repay_ratio`, etc.)

📄 **Output file**: `wallet_credit_scores.csv`

---


