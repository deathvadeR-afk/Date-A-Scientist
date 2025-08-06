# Date-A-Scientist

## 📚 Project Overview

This project delves into a dataset of user profiles from the dating platform OKCupid. The primary goal is to perform a comprehensive exploratory data analysis (EDA) to understand the demographics and characteristics of the users. Following the analysis, a machine learning model is developed to predict a user's zodiac sign based on their profile information, including demographics and lifestyle choices.

This project showcases a complete data science pipeline, from data cleaning and preprocessing to feature engineering, model training, and evaluation.

## 📊 The Dataset

The data used in this project is the `profiles.csv` dataset, which contains anonymized data for approximately 60,000 OKCupid users. The dataset includes a wide range of features, such as:

*   **Demographics:** `age`, `sex`, `orientation`, `body_type`, `diet`, `education`, `location`, `ethnicity`, `religion`.
*   **Lifestyle:** `drinks`, `drugs`, `smokes`, `pets`, `speaks`.
*   **User Essays:** Ten open-ended essay responses, including `essay0` (My self-summary), `essay1` (What I’m doing with my life), and more.
*   **Target Variable:** `job`.

## 🎯 Project Goal

The main objective is to build and evaluate a classification model that can accurately predict a user's zodiac sign from their profile information. This involves analyzing how various demographic and lifestyle choices might correlate with astrological signs, potentially helping to enhance the matchmaking process for users who haven't disclosed their sign.

## ⚙️ Methodology

The project follows these key steps:

1.  **Data Cleaning & Preprocessing:**
    *   Handling missing values in categorical and numerical columns.
    *   Standardizing data formats and correcting inconsistencies.

2.  **Exploratory Data Analysis (EDA):**
    *   Visualizing distributions of key features like age, sex, and orientation using Matplotlib and Seaborn.
    *   Analyzing relationships between different variables to uncover initial insights.
    *   Exploring the distribution of job categories.

3.  **Feature Engineering:**
    *   Converting categorical variables into numerical format using one-hot encoding.
    *   Handling missing values in the dataset.
    *   Creating dummy variables for categorical features.

4.  **Model Building & Training:**
    *   Splitting the dataset into training and testing sets.
    *   Training several classification models to find the best performer. Models explored include:
        *   Logistic Regression
        *   K-Nearest Neighbors (KNN)
        *   Decision Tree Classifier
    *   Using `Scikit-learn` pipelines to streamline the preprocessing and modeling workflow.

5.  **Model Evaluation:**
    *   Evaluating the models on the test set using metrics like accuracy, precision, recall, and F1-score.
    *   Analyzing the classification report and confusion matrix to understand model performance across different zodiac signs.

## 🛠️ Technologies Used

*   **Python 3**
*   **Pandas:** For data manipulation and analysis.
*   **NumPy:** For numerical operations.
*   **Matplotlib & Seaborn:** For data visualization and EDA.
*   **Scikit-learn:** For machine learning, including text feature extraction (TF-IDF) and classification models.

## 🚀 How to Run

To replicate this project on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/deathvadeR-afk/Date-A-Scientist.git
    cd DateAScientist
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv .venv
    # On Windows
    .\.venv\Scripts\activate
    # On macOS/Linux
    source .venv/bin/activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the analysis:**
    *   If the project is in a Jupyter Notebook (e.g., `analysis.ipynb`), start Jupyter Lab:
        ```bash
        jupyter lab
        ```
    *   If the project is a Python script (e.g., `main.py`), run it from the terminal:
        ```bash
        python main.py
        ```
