# 📊 Wallet Credit Score Analysis


##  Introduction

The purpose of this analysis is to understand the behavioral distribution of blockchain wallets based on credit scores. The credit score is a proxy metric representing user reliability, repayment history, and risk behavior. 

---

**Key Observations:**

- The distribution is **multi-modal**, showing three major peaks:
  - **200–300**: The highest concentration of wallets.
  - **500–600**: A smaller but significant group of wallets.
  - **700–800**: A distinct, high-scoring minority.
  
- Very few wallets exist in the **0–100** and **900–1000** ranges.

- The KDE curve suggests **three behavioral clusters** based on usage and risk patterns.

---

## Clustered Behavior Insights

| Score Range | Behavior Summary                              | Risk Level   |
|-------------|------------------------------------------------|--------------|
| 200–300     | Most common wallets. Possibly new or average users with mixed activity and potential risk. | Moderate     |
| 500–600     | Active users with decent repayment behavior and fewer liquidations.                      | Low-Moderate |
| 700–800     | High-credit wallets, rarely liquidated, consistently repay.                              | Low          |

---

##  Interpretation

- The majority of wallet users are grouped in the **200–300** score range, suggesting a common pattern of behavior, possibly due to minimal activity which reflects risky, bot-like, or exploitative behavior.
- A secondary cluster at **500–600** likely represents more responsible users who show trustworthy patterns.
- The **700–800** range includes wallets with excellent behavior—potentially eligible for higher trust scores or protocol benefits.
- Sparse population in extreme ranges (very low or very high) may indicate **outliers** or **bot-like behavior**.

---


## Visual Summary

<img width="882" height="555" alt="Screenshot (4001)" src="https://github.com/user-attachments/assets/12d0eba1-6c6c-44bf-a6da-dd993d2fc686" />


📌 


