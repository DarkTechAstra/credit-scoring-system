### 💸 DeFi Wallet Behavior Clustering with Feature Engineering & KMeans

This project focuses on analyzing and clustering DeFi wallet behaviors using unsupervised learning. By parsing and feature-engineering deeply nested transaction logs (e.g., deposits, withdrawals, liquidations), we extract meaningful behavioral patterns across wallets and cluster them using **KMeans**.

#### 🚀 Key Highlights

* **Raw Data:** Wallet-wise records of DeFi actions like `deposits`, `withdraws`, `borrows`, `repays`, and `liquidates` (nested JSON format).
* **Feature Engineering:**

  * Parsed and flattened complex nested structures.
  * Extracted metrics like `deposits_count`, `withdraws_count`, `liquidates_total_usd`, etc.
  * Converted all string-based numerical values into usable floats.
* **Handling Edge Cases:**

  * Managed `NaN`s and missing values smartly (e.g., no liquidations → assigned 0s).
  * Filtered out irrelevant sub-keys (like asset symbols).
* **Unsupervised Clustering:**

  * Applied **KMeans** to engineered features.
  * Interpreted cluster profiles: whales, inactive wallets, high-risk liquidators, etc.
* **Scoring System:**

  * Designed a custom wallet score (`1–100`) based on behavioral metrics and cluster importance.
* **Visualization:**

  * Used **PCA** to reduce features and visualize cluster separability in 2D.

#### 📂 Tech Stack

`Pandas`, `NumPy`, `Scikit-learn`, `Matplotlib`, `Seaborn`, `PCA`, `KMeans`

#### 🧠 Why This Matters

This clustering approach helps in:

* Risk profiling for DeFi protocols.
* Detecting behavioral patterns (e.g., frequent liquidators or power users).
* Prioritizing wallets for marketing, rewards, or fraud detection.


