# Task 4: Netflix Content Segmentation (Unsupervised Clustering)

## 📌 Project Overview
This is Task 4 of the Auspify Technologies Machine Learning Internship. The objective is to group Netflix titles into meaningful clusters using Unsupervised Machine Learning. Unlike previous tasks, we did not have an "Answer Key" (no target variable). The algorithm had to discover the patterns on its own.

## 🛠️ Tech Stack
- **Python 3**
- **Pandas & NumPy:** Data manipulation.
- **Scikit-Learn:** `StandardScaler` (Feature Scaling) and `KMeans` (Clustering).
- **Matplotlib:** Elbow Curve and Scatter Plot visualization.

## 🧠 Methodology
1. **Data Preprocessing:** 
   - Extracted numerical duration from the `duration` column (e.g., "90 min" -> 90, "2 Seasons" -> 2).
   - Selected `release_year` and `duration_num` as our clustering features.
2. **Feature Scaling:** 
   - Applied `StandardScaler` to normalize the data. This was critical because `release_year` (e.g., 2020) and `duration_num` (e.g., 90) are on completely different scales. Without scaling, K-Means would have been biased by the year.
3. **Finding the Optimal K:** 
   - Used the **Elbow Method** to plot inertia against the number of clusters (K=1 to 10). The sharp bend occurred at **K=3**, indicating that 3 is the optimal number of segments.
4. **K-Means Clustering:** 
   - Trained `KMeans(n_clusters=3)` and assigned labels to the original DataFrame.

## 📊 Business Insights (Interpreting the Clusters)
By analyzing the average release year and duration of each cluster, we discovered:
- **Cluster 0 (Modern TV Shows):** Average Year 2017, Average Duration 5.8 (Seasons). This represents the recent surge in episodic content.
- **Cluster 1 (Modern Movies):** Average Year 2015, Average Duration 102 (Minutes). This is the massive library of contemporary films.
- **Cluster 2 (Classic Movies):** Average Year 1987, Average Duration 108 (Minutes). This is the archive of older, classic cinema.

## 📸 Output Screenshots
*(See the Screenshots folder in this directory)*
- Elbow Method Curve
- Cluster Summary Table
- Final Scatter Plot (Release Year vs. Duration)