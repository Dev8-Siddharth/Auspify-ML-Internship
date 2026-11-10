# Task 2: Netflix Content Type Prediction (Binary Classification)

## 📌 Project Overview
This is Task 2 of the Auspify Technologies Machine Learning Internship. The objective is to build a supervised Machine Learning model that predicts whether a Netflix title is a **Movie** or a **TV Show** based on its features.

## 🛠️ Tech Stack
- **Python 3**
- **Pandas & NumPy:** Data manipulation.
- **Scikit-Learn:** `LabelEncoder`, `TfidfVectorizer`, `RandomForestClassifier`, and `Train/Test Split`.
- **Matplotlib:** Feature Importance visualization.

## 🧠 Methodology
1. **Feature Engineering:** 
   - Extracted numerical values from the `duration` column (e.g., "90 min" -> 90, "2 Seasons" -> 2).
   - Cleaned the `listed_in` (genres) column by removing the word "TV" to prevent **Data Leakage**.
2. **Data Preprocessing:** 
   - Vectorized genres using `TfidfVectorizer`.
   - Combined genre vectors and duration into a sparse matrix (`hstack`).
3. **Model Training:**
   - Split data into **80% Training / 20% Testing**.
   - Trained a **Random Forest Classifier** with `class_weight='balanced'` to handle the 70/30 class imbalance (6,126 Movies vs 2,664 TV Shows).
4. **Evaluation & Explainability:**
   - Achieved **99.89% Accuracy**.
   - Used `feature_importances_` to prove that `duration_num` (45.7%) was the most impactful feature, followed by specific genre keywords.

## 📸 Output Screenshots
*(See the Screenshots folder in this directory)*
- Classification Report & Accuracy
- Feature Importance Bar Chart
- Live Prediction Function Tests