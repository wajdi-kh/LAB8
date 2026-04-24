# K-Nearest Neighbors (KNN) Classification Project

## Project Overview
This project implements a **K-Nearest Neighbors (KNN)** machine learning model to classify data from an artificial dataset. The goal is to predict the 'TARGET CLASS' based on several anonymous feature variables. The project follows a standard data science workflow, including data preprocessing, exploratory data analysis (EDA), model training, and optimization using the Elbow Method.

## Dataset
The dataset `KNN_Project_Data` contains:
* **Features:** 10 numerical variables (labeled with anonymous codes like XVPM, GWYH, etc.)
* **Target:** `TARGET CLASS` (Binary: 0 or 1)

## Workflow

### 1. Exploratory Data Analysis (EDA)
Used `seaborn` to create a large pairplot to visualize relationships between features, with the hue defined by the Target Class to check for cluster separation.

### 2. Data Preprocessing
* **Feature Scaling:** Since KNN relies on the distance between points, all feature variables were standardized using Scikit-Learn's `StandardScaler`. This ensures that features with larger scales do not disproportionately influence the model.

### 3. Model Training
* Split the data into training and testing sets (70/30 split).
* Initially trained a KNN classifier with $K=1$.

### 4. Choosing the Optimal K (Elbow Method)
To improve performance, I iterated through $K$ values from 1 to 40 and plotted the **Error Rate**. This "Elbow Plot" helped identify the point where the error rate stabilizes.
* **Optimal K identified:** $K \approx 31$

## Results
The model performance significantly improved after tuning the $K$ parameter:

| Metric | K = 1 | K = 31 |
| :--- | :--- | :--- |
| **Accuracy** | ~72% | **~84%** |
| **Precision (Avg)** | 0.72 | **0.84** |
| **Recall (Avg)** | 0.72 | **0.84** |

## Technologies Used
* **Python**
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Data Visualization)
* **Scikit-Learn** (Machine Learning)

## How to Run
1. Ensure you have the `KNN_Project_Data` file in the same directory.
2. Run the Jupyter Notebook `02-K Nearest Neighbors Assignment.ipynb`.
