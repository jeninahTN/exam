# AI Exam - Question 3: Customer Segmentation Pipeline

This project implements a complete clustering pipeline for customer segmentation using the Nigerian E-Commerce Dataset. The goal is to group customers based on their purchasing behavior to enable targeted marketing strategies.

## Project Overview

The pipeline performs the following steps:
1.  **Data Loading**: Loads the `Nigerian E-Commerce Dataset.xlsx`.
2.  **Data Cleaning**: Handles duplicates and missing values.
3.  **Feature Engineering**: Calculates RFM (Recency, Frequency, Monetary) metrics for each customer.
4.  **Scaling**: Standardizes the features using `StandardScaler`.
5.  **Clustering**:
    *   Uses **K-Means** clustering.
    *   Determines the optimal number of clusters ($k$) using the Elbow Method.
    *   Applies **DBSCAN** for density-based clustering comparison.
6.  **Visualization**: Visualizes clusters using PCA (Principal Component Analysis) to reduce dimensions to 2D.
7.  **Evaluation**: Computes the Silhouette Score to measure cluster quality.
8.  **Profiling & Recommendations**: Analyzes cluster characteristics and provides actionable marketing recommendations.

## Files

*   **`AI_Exam_Question_3.ipynb`**: The main Jupyter Notebook containing the full analysis and code.
*   **`create_structured_notebook.py`**: A Python script that programmatically generates the `AI_Exam_Question_3.ipynb` notebook.
*   **`check_k.py`**: A helper script to quickly run the Elbow Method on simulated data to check for the optimal $k$.
*   **`run_notebook.py`**: A script to execute the notebook programmatically.
*   **`Nigerian E-Commerce Dataset.xlsx`**: The input dataset used for analysis.
*   **`cluster_assignments.csv`**: The output file containing the original data with assigned cluster labels.

## Prerequisites

Ensure you have Python installed with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl notebook
```

## Usage

### Running the Notebook
You can open and run the notebook using Jupyter:

```bash
jupyter notebook AI_Exam_Question_3.ipynb
```
 Generating the Notebook
If the notebook is missing or you want to regenerate it from the source script:

```bash
python create_structured_notebook.py
```

### Quick K-Check
To quickly check the inertia values for different $k$ (Elbow Method) using simulated data:

```bash
python check_k.py
```

## Results

The analysis identifies distinct customer segments (e.g., "Low Value", "Loyal Customers", "VIPs") and outputs the results to `cluster_assignments.csv`.
