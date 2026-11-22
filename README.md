# 🚀 Auspify Technologies: Machine Learning Internship Portfolio

Welcome to my Machine Learning Internship portfolio, completed as part of the 4-Week Practical Learning Program at **Auspify Technologies**. 

This repository contains 5 comprehensive, end-to-end Machine Learning projects. Rather than just running algorithms, this portfolio focuses on **production-ready code, data leakage prevention, edge-case handling, and extracting actionable business insights.**

## 🛠️ Technical Stack
- **Languages:** Python 3
- **Data Manipulation:** Pandas, NumPy, Regex
- **Machine Learning & NLP:** Scikit-Learn, Statsmodels, TF-IDF, XGBoost
- **Visualization:** Matplotlib, Seaborn

---

## 📂 Project Directory

### [Task 1: Netflix Content Recommendation System](./Task_1_Netflix_Recommendation_System)
*   **Type:** Unsupervised Learning (NLP)
*   **Core Concept:** Content-based filtering using TF-IDF Vectorization and Cosine Similarity.
*   **Highlight:** Built a robust recommendation engine that handles messy user inputs (case-sensitivity, extra spaces) and gracefully manages missing titles.

### [Task 2: Content Type Prediction Model](./Task_2_Content_Type_Prediction)
*   **Type:** Binary Classification (Supervised)
*   **Core Concept:** Random Forest Classifier predicting whether content is a Movie or a TV Show.
*   **Highlight:** Discovered and resolved **Data Leakage** by removing the word "TV" from the genre features, forcing the model to rely on true predictive features like `duration`.

### [Task 3: Audience Rating Classification](./Task_3_Netflix_Audience_Rating_Classification)
*   **Type:** Multi-Class Classification (Supervised)
*   **Core Concept:** Predicting Audience Ratings (TV-MA, PG-13, R, etc.) using a Voting Ensemble (Random Forest, Gradient Boosting, Logistic Regression).
*   **Highlight:** Handled highly imbalanced classes and utilized `GridSearchCV` for extensive hyperparameter tuning. Achieved a peak accuracy of **51.37%** (4.6x higher than random guessing) while documenting the inherent "Information Ceiling" of the dataset.

### [Task 4: Netflix Content Segmentation](./Task_4_Content_Segmentation)
*   **Type:** Unsupervised Learning (Clustering)
*   **Core Concept:** Grouping titles using K-Means Clustering based on Release Year and Duration.
*   **Highlight:** Applied `StandardScaler` to normalize data and used the **Elbow Method** to mathematically prove that content naturally segments into 3 distinct groups: *Modern TV Shows, Modern Movies, and Classic Movies.*

### [Task 5: Netflix Trend Forecasting Model](./Task_5_Trend_Forecasting)
*   **Type:** Time Series Forecasting
*   **Core Concept:** Predicting future content release trends using the ARIMA model.
*   **Highlight:** Identified and removed a **Data Artifact** (the incomplete 2021 dataset) to prevent false forecasting. Discovered the strategic business insight that Netflix is pivoting from Movies toward TV Shows.

*(Task 6: End-to-End Content Success Analytics Engine - Currently in Development)*

---

## 🧠 Key Engineering Takeaways
Throughout this internship, I have moved beyond basic scripting to embrace Master-level Engineering principles:
- **Preventing Data Leakage:** Ensuring models learn genuine patterns, not cheat codes.
- **Handling Data Artifacts:** Cleaning incomplete temporal data before time-series forecasting.
- **Edge Case Handling:** Writing functions that don't crash when a user types `"  sAnKoFa  "` or enters a movie that doesn't exist.
- **Business Translation:** Converting raw confusion matrices and feature importances into strategic business insights (e.g., *Why is duration the most important feature?*).

---
*Created by [Dev Siddharth] - ML Intern at Auspify Technologies.*
