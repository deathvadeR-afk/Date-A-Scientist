# Date-A-Scientist: OKCupid Profile Analysis & Prediction

## 📚 Project Overview

This project delves into a dataset of user profiles from the dating platform OKCupid. The primary goal is to perform a comprehensive exploratory data analysis (EDA) to understand the demographics and characteristics of the users. Following the analysis, a machine learning model is developed to predict a user's job category based on their profile information, with a special focus on the text from their self-summary essays.

This project showcases a complete data science pipeline, from data cleaning and preprocessing to feature engineering, model training, and evaluation.

## 📊 The Dataset

The data used in this project is the `profiles.csv` dataset, which contains anonymized data for approximately 60,000 OKCupid users. The dataset includes a wide range of features, such as:

*   **Demographics:** `age`, `sex`, `orientation`, `body_type`, `diet`, `education`, `location`, `ethnicity`, `religion`.
*   **Lifestyle:** `drinks`, `drugs`, `smokes`, `pets`, `speaks`.
*   **User Essays:** Ten open-ended essay responses, including `essay0` (My self-summary), `essay1` (What I’m doing with my life), and more.
*   **Target Variable:** `job`.

## 🎯 Project Goal

The main objective is to build and evaluate a classification model that can accurately predict a user's `job` category from the other available features, particularly the text data in their essays. This involves natural language processing (NLP) techniques to convert unstructured text into meaningful features for the model.

## ⚙️ Methodology

The project follows these key steps:

1.  **Data Cleaning & Preprocessing:**
    *   Handling missing values in categorical and numerical columns.
    *   Standardizing data formats and correcting inconsistencies.

2.  **Exploratory Data Analysis (EDA):**
    *   Visualizing distributions of key features like age, sex, and orientation using Matplotlib and Seaborn.
    *   Analyzing relationships between different variables to uncover initial insights.
    *   Exploring the distribution of job categories.

3.  **Feature Engineering & NLP:**
    *   Combining all ten essay columns into a single text corpus for each user.
    *   Processing the text data: removing stop words, punctuation, and applying lemmatization.
    *   Converting the cleaned text into numerical vectors using TF-IDF (Term Frequency-Inverse Document Frequency).
    *   Combining the TF-IDF text features with other categorical and numerical features from the dataset.

4.  **Model Building & Training:**
    *   Splitting the dataset into training and testing sets.
    *   Training several classification models to find the best performer. Models explored could include:
        *   Naive Bayes
        *   Logistic Regression
        *   Random Forest Classifier
    *   Using `Scikit-learn` pipelines to streamline the preprocessing and modeling workflow.

5.  **Model Evaluation:**
    *   Evaluating the models on the test set using metrics like accuracy, precision, recall, and F1-score.
    *   Analyzing the classification report and confusion matrix to understand model performance across different job categories.

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