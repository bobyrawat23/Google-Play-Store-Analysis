# Google-Play-Store-Analysis

# 🎯 Project Goal & Business Objective

The core objective was to analyze and model Google Play Store app ratings, aiming to: Understand the key features that influence app ratings.

Provide insights into how app characteristics (e.g., size, installs, price) impact user perception.

Build a predictive model that estimates an app's rating based on its attributes.

* Business motivation:

Help app developers and publishers make informed decisions on pricing, updates, and marketing.

Identify trends and patterns that differentiate successful apps.

# 🗃️ Data Overview

# 📌 Datasets Used:

Main Dataset (googleplaystore.csv): Contains details of over 10,000 apps including:

App, Category, Rating, Reviews, Size, Installs, Price, etc.

Review Dataset (googleplaystore_user_reviews.csv): Textual user reviews with associated sentiments (Positive, Negative, Neutral).

# 📌 Common Data Issues Encountered:

Missing values in columns like Rating, Size, and Price.

Inconsistent formatting:

Size: entries like "Varies with device", "13M", "500k".

Price and Installs: contained symbols like $, +, and ,.

# 🧹 Data Cleaning & Feature Engineering

✔️ Steps Taken:

Removed or imputed missing values (especially in Rating).

Cleaned numerical fields:

Installs converted from strings (e.g., "1,000+") to integers.

Size normalized (e.g., converted "13M" to 13, "500k" to 0.5).

Price cleaned from strings like "$4.99" to floats.

Converted categorical data:

One-hot encoded the Category feature to allow machine learning models to process it.

Filtered out anomalies:

Removed apps with extremely high prices, review counts, or outliers.

# 📊 Exploratory Data Analysis (EDA) – Insights

# 🔍 Key Findings:

Top Categories by App Count: FAMILY, GAME, TOOLS.

Highest Average Ratings: HEALTH, EDUCATION, BOOKS.

# Free vs Paid:

Over 90% of apps are free.

Paid apps don’t necessarily have higher ratings.

# Reviews & Installs Correlation:

More installs and reviews generally indicate better user engagement.

# App Size:

No strong correlation between app size and rating.

Users don’t penalize large apps if they are functional and engaging.

# 📈 Predictive Modeling

# 📌 Models Used:

# Linear Regression:

Simple baseline model to assess linear relationships.

R² Score: ~0.017 — explains ~1.7% of the variation in ratings.

RMSE: ~0.49 — shows average prediction error.

# Random Forest Regressor:

More complex, non-linear model.

R² Score: ~0.078 — explains ~7.8% of variation.

RMSE: ~0.47 — better prediction than linear regression.

# 🧠 Interpretation:

The models struggled to predict ratings accurately from numeric features alone.

Ratings are subjective and often influenced by user sentiment and app experience, which aren’t directly captured in the current dataset.

# 🚧 Limitations

Many important factors not included in the structured data:

App description, UI/UX quality, performance, update frequency.

Rating is a subjective measure, and tough to model from purely numeric fields.

Textual reviews were not used in modeling (reserved for future enhancement).

Temporal changes (e.g., updates over time) were not analyzed.

# 🚀 Future Enhancements

To improve the model and insights, the following steps are proposed:

# 📘 Sentiment Analysis:

Analyze user review sentiments (already available).

Derive text-based features (positive/negative tone) to predict ratings better.

Use NLP techniques like TF-IDF, BERT, or VADER.

# 📈 Time Series Analysis:

Study how app ratings change over time.

Evaluate how frequent updates, bug fixes, or new features affect user satisfaction.

# 🤖 Advanced Machine Learning:

Use models like XGBoost, Gradient Boosting, and Neural Networks to capture complex interactions.

Apply hyperparameter tuning for optimization.

# 🔍 Model Interpretability:

Use tools like SHAP or LIME to explain model decisions.

Helps stakeholders understand why a model predicts a certain rating.

# 📊 Dashboard or App:

Build a Streamlit dashboard or Power BI/Tableau report to present insights interactively.

Allow non-technical users to explore predictions and category-wise performance.

# 💼 8. Business Impact

Helps developers prioritize features and understand market dynamics.

Supports investment decisions in app monetization (free vs paid strategies).

Encourages data-driven marketing based on category trends and user preferences.

Enables early-stage developers to forecast performance before launching.

                                                                
# 🧾 Conclusion

    
This project provided a solid foundation in cleaning, analyzing, and modeling real-world app data.

Key factors like reviews, installs, and category do play a role, but are not sufficient alone.

There is a clear path forward using textual reviews, time-based data, and advanced ML techniques to enhance rating prediction and business insights.
