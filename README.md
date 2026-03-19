# World Happiness Report 2019: Predictive Modeling & Analysis

##  Overview

This project delves into the **World Happiness Report 2019** dataset to identify key factors influencing happiness scores across countries and to build predictive machine learning models. Although the full dataset spans from 2015 to 2019, this analysis focuses exclusively on the 2019 data, which comprises 156 clean rows with no missing values. Initial Exploratory Data Analysis (EDA) has been performed to understand the dataset's structure and relationships.

## Table of Contents

1.  [Dataset Description](#dataset-description)
2.  [Analytical Logic & Methodology](#analytical-logic--methodology)
3.  [Key Findings & Model Performance](#key-findings--model-performance)
4.  [How to Run the Notebook](#how-to-run-the-notebook)
5.  [Dependencies](#dependencies)

## Dataset Description

The 2019 World Happiness Report dataset includes 156 countries and features several crucial parameters:

*   **Country or region:** The name of the country.
*   **Score:** The continuous happiness score (target for Regression models).
*   **GDP per capital:** Economic output per person.
*   **Social support:** Perceived social support from family/friends.
*   **Healthy life expectancy:** Average years of healthy life.
*   **Freedom to make life choices:** Perceived freedom in life choices.
*   **Generosity:** Involvement in charitable acts.
*   **Perceptions of corruption:** Perceived level of corruption.
*   **Score_class:** A categorical happiness class ('Low', 'Medium', 'High'), derived from 'Score' (target for Classification models).

## Analytical Logic & Methodology

This notebook follows a standard machine learning workflow:

1.  **Data Loading & Initial Exploration:** Initial checks, descriptive statistics, and unique value analysis.
2.  **Feature Engineering & Visualization:** Correlation heatmaps, 3D scatter plots, and pivot tables to uncover relationships.
3.  **Data Preprocessing:** One-Hot Encoding for categorical variables and StandardScaler for numerical feature scaling.
4.  **Regression Modeling:** Training and evaluating Linear Regression, Random Forest Regressor, and Gradient Boosting Regressor to predict the continuous 'Score'. Hyperparameter tuning was applied.
5.  **Classification Modeling:** Transforming 'Score' into 'Score_class' and training Logistic Regression, Decision Tree, Random Forest Classifier, Gradient Boosting Classifier, and K-Nearest Neighbors (KNN). Hyperparameter tuning was performed, and models were evaluated using Accuracy, F1-score, Confusion Matrices, and Classification Reports.

## Key Findings & Model Performance

### Regression Models

After hyperparameter tuning, the **Gradient Boosting Regressor** emerged as the best-performing model, achieving the lowest Mean Squared Error (MSE) and highest R-squared (R2) score.

### Classification Models

The **K-Nearest Neighbors (KNN)** model, after hyperparameter tuning (with `n_neighbors=29`), demonstrated the best performance for predicting happiness categories, achieving the highest Accuracy and F1-score among all tested classification models.

*   **KNN Model Performance:**
    *   **Accuracy:** 0.81
    *   **F1-score (weighted):** 0.81
    *   The model showed excellent recall for the 'High' happiness class but some challenges in recalling 'Low' happiness instances, occasionally misclassifying them as 'Medium'.

## How to Run the Notebook

This project is implemented in a Google Colab notebook. To run it:

1.  **Clone the Repository:**
    ```bash
    git clone <your-repository-url>
    cd <your-repository-name>
    ```
2.  **Open in Google Colab:** Upload the `.ipynb` file to Google Colab.
3.  **Upload Dataset:** The notebook expects the `2019.csv` file. You will be prompted to upload it during execution (e.g., `files.upload()`).
4.  **Execute Cells:** Run all cells sequentially.

## Dependencies

Key libraries used in this project include:

*   `pandas`
*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `scikit-learn`

## Dataset Source

This dataset is sourced from Kaggle. You can find the original dataset [here](https://www.kaggle.com/datasets/unsdsn/world-happiness). *Please replace this with the exact link to the 2019 dataset if it's different or if you have uploaded it to your Kaggle profile.*

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and distribute this work. 
The primary author is Fidan Bannayeva [LinkedIn](https://www.linkedin.com/in/fbannayeva/).