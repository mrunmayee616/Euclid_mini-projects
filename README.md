# Credit Card Fraud Detection Using Unsupervised Learning

## Overview
This project applies multiple unsupervised learning techniques to detect patterns and anomalies in credit card transaction data. The goal is to compare clustering algorithms and anomaly detection methods for identifying potentially fraudulent transactions.

## Dataset
The project uses the **Credit Card Fraud Detection Dataset** (`creditcard.csv`).
* Features: Transaction attributes (V1–V28, Amount, etc.)
* Target Column: `Class`
  * `0` → Normal Transaction
  * `1` → Fraudulent Transaction
For unsupervised learning, the target column is removed before training.

## Algorithms Used
### Clustering Algorithms
* K-Means Clustering
* Hierarchical Clustering
* DBSCAN

### Anomaly Detection
* Isolation Forest

### Dimensionality Reduction
* Principal Component Analysis (PCA)

## Project Workflow
1. Load and preprocess data
2. Scale features using StandardScaler
3. Apply K-Means clustering
4. Apply Hierarchical Clustering
5. Apply DBSCAN clustering
6. Visualize clusters using PCA
7. Detect anomalies using Isolation Forest
8. Compare clustering performance using:

   * Silhouette Score
   * Davies-Bouldin Score

## Results
| Method                  | Silhouette Score | Davies-Bouldin Score |
| ----------------------- | ---------------- | -------------------- |
| K-Means                 | 0.0800           | 2.5514               |
| Hierarchical Clustering | 0.1192           | 2.0974               |
| DBSCAN                  | 0.6503           | 0.4321               |
| Isolation Forest        | N/A              | N/A                  |

### Isolation Forest Results
* Normal Transactions Detected: 9900
* Anomalies Detected: 100

## Conclusion
* DBSCAN achieved the highest Silhouette Score and the lowest Davies-Bouldin Score, indicating the best clustering performance among the evaluated clustering algorithms.
* Isolation Forest successfully identified anomalous transactions and proved effective for fraud detection.
* PCA visualization helped in understanding cluster distribution and anomaly separation.

## Technologies Used
* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* SciPy

## Installation
Create a virtual environment:
```bash
python -m venv venv
```
Activate the environment:

### Windows
```bash
venv\Scripts\activate
```
Install dependencies:

```bash
pip install pandas numpy matplotlib scikit-learn scipy
```

## Run the Project
```bash
python ul_project.py
```

