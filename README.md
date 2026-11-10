# Task 1: Netflix Content Recommendation System

## 📌 Project Overview
This project was completed as part of the Auspify Technologies Machine Learning Internship. The goal was to build a Content-Based Recommendation System that suggests similar Netflix titles based on their genres and categories. 

## 🛠️ Tech Stack & Libraries
- **Python 3**
- **Pandas:** Data manipulation and cleaning.
- **Scikit-Learn:** `TfidfVectorizer` for NLP (text vectorization) and `cosine_similarity` for distance calculation.
- **Regex (re):** For advanced text cleaning.

## 🧠 Methodology
1. **Robust Data Preprocessing:** 
   - Handled missing values (`NaN`) in the `listed_in` column.
   - Used Regular Expressions to remove weird characters and normalize spaces.
   - Converted titles to lowercase and stripped whitespace to handle messy user inputs (e.g., `' sAnKoFa '`).
2. **NLP Vectorization:** 
   - Utilized `TfidfVectorizer` (Term Frequency-Inverse Document Frequency) to convert text genres into a 44-dimensional numerical matrix. This penalizes overly common words and rewards rare genres.
3. **Similarity Calculation:** 
   - Computed a pairwise `cosine_similarity` matrix (8790 x 8790) to find the angle between movie vectors.
4. **Recommendation Engine:** 
   - Built a highly robust function that handles edge cases:
     - Missing movie titles (returns a clean error message).
     - Case insensitivity and extra spaces.
     - Returns a structured DataFrame with the `title`, `listed_in`, and `similarity_score` (0.0 to 1.0).

## 📸 Project Screenshots
*(See the Screenshots folder in this directory)*
- Data Sanity Check (`df.head`)
- Data Cleaning Output
- TF-IDF Matrix Shape
- Edge Case Testing (Normal, Messy, Non-existent inputs)
