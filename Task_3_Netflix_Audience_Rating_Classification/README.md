# Task 3: Netflix Audience Rating Classification (Multi-Class)

## 📌 Project Overview
This is Task 3 of the Auspify Technologies Machine Learning Internship. The objective is to predict the audience rating (e.g., TV-MA, PG-13, R) of Netflix content based on its features. This is a **Multi-Class Classification** problem.

## 🛠️ Tech Stack
- **Python 3**
- **Pandas & NumPy:** Data manipulation.
- **Scikit-Learn:** `TfidfVectorizer`, `RandomForestClassifier`, `GridSearchCV`, `VotingClassifier`, `GradientBoostingClassifier`, `LogisticRegression`.
- **Matplotlib & Seaborn:** Feature Importance and Confusion Matrix visualization.

## 🧠 Methodology
1. **Data Cleaning:** 
   - Grouped extremely rare ratings (NC-17, UR, TV-Y7-FV) into an "Other" category to prevent statistical noise. Focused on the top 8 most common ratings.
   - Cleaned genres using regex to remove the words "TV" and "Movie" to prevent data leakage.
   - Extracted numerical duration and filled missing release years.
2. **Feature Engineering:** 
   - Combined TF-IDF vectorized genres with Duration and Release Year.
3. **Model Training & Optimization:**
   - **Baseline Random Forest:** Achieved 48.01% accuracy.
   - **GridSearchCV (Aggressive Tuning):** Tested 24 combinations of hyperparameters (depth, max_features, n_estimators). Accuracy dropped to 45.05%, proving the model hit the **Information Ceiling**.
   - **Voting Ensemble (Soft Voting):** Combined Random Forest, Gradient Boosting, and Logistic Regression. 
   - **Weighted Ensemble:** Applied higher weights to tree-based models to achieve our best accuracy of **51.37%**.
4. **Evaluation:**
   - Analyzed the confusion matrix and discovered that the model frequently confuses adjacent classes (e.g., TV-14 vs TV-MA) because they share identical genres and durations.

## 📊 Key Learnings
- **Duration & Release Year** were the most important features (proving that modern Netflix shows are mostly TV-MA, while older content leans PG/R).
- **Genre keywords** like "Kids", "Family", and "Children" are highly predictive of safe ratings.
- **Ensemble Learning** (Voting) proved more powerful than a single Random Forest, even after hyperparameter tuning.

## 📸 Output Screenshots
*(See the Screenshots folder in this directory)*
- Final Weighted Ensemble Accuracy & Report
- GridSearchCV Best Parameters
- Feature Importance Bar Chart
- Confusion Matrix Heatmap