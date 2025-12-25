> **Hackathon context**  
> This project was developed during a time-limited hackathon as part of an AI bootcamp.  
> The focus was on rapid exploration, analysis, and collaborative problem-solving rather than building a production-ready system.


# fraude-credit-hackathon
Hackathon 23-10-2025 – Credit Card Fraud Detection and Prevention
1. Project Overview

This project was developed during the Hackathon 23-10-2025 by our team of three members, with the objective of detecting and preventing fraudulent credit card transactions.

Fraudulent transactions represent only ~0.17% of all records, which makes them very hard to detect but extremely important to monitor.
Our analysis highlights patterns in amounts, timing, and anonymized features that can guide prevention strategies.

2. Exploratory Data Analysis (EDA)

The dataset is highly imbalanced: most transactions are genuine.

Transaction amounts are usually small, but fraud tends to cluster in specific ranges.

Fraudulent activity appears disproportionately at unusual hours (night/early morning).

Correlation analysis shows some anonymized features (e.g., V14, V10, V12) are strongly linked to fraud.

Scatter plots confirm that fraudulent transactions form visible clusters in certain feature combinations.

3. Data Preprocessing

No missing values were detected in the dataset.

Transaction amounts were log-transformed to better visualize distributions.

The extreme class imbalance is a challenge. Techniques like oversampling, undersampling, or SMOTE are recommended before modeling.

4. Feature Analysis

Even though features are anonymized (V1–V28), some carry much stronger signals for fraud.

These top predictors can be prioritized in monitoring systems or combined into aggregated risk scores.

This focus helps improve prevention efforts by targeting the most informative parts of the data.

5. Predictive Modeling (Next Step)

While this notebook focused mainly on analysis and visualization, predictive models can be applied to classify fraud vs. genuine transactions.

Evaluation should prioritize:

Maximizing fraud detection (recall/sensitivity).

Minimizing false alarms (precision).

Accuracy alone is not sufficient because of the class imbalance.

6. Visualization Highlights

We created clear and intuitive visualizations using Matplotlib and Seaborn:

Class imbalance (0 = genuine, 1 = fraud).

Distribution of transaction amounts overall and by class.

Fraud occurrence by hour of the day.

Correlation heatmaps and top features.

Scatter plots showing clusters of fraudulent transactions.

These visuals make the problem easy to understand for both technical and business stakeholders.

7. Fraud Prevention Strategy

Real-time monitoring: transactions scored instantly, with alerts for high-risk cases.

Dynamic rules: focus on unusual hours, suspicious amount ranges, and repeated transactions.

Step-up authentication: high-risk transactions require additional customer verification.

Data enrichment: integrating location, device/browser fingerprint, and merchant information.

Business value: combines data-driven detection with clear rules → practical and trustworthy for financial institutions.

8. Conclusion

Our analysis confirms that fraud is rare but not random.
Patterns in amount, time, and specific anonymized features strongly increase fraud likelihood.
Combining machine learning models with business rules offers the most effective fraud detection strategy.

9. Team Contributions
Catherine Maameri: Exploratory Data Analysis, Data Preprocessing, PowerPoint presentation

Adel Zituni: Feature Engineering, Predictive Modeling.

Cristina Moussoungedi: Project setup (repository & main branch), Fraud Prevention Strategy, visualizations, README draft.

10. Dataset

The dataset used is creditcard.csv from Kaggle
.
It contains anonymized features (V1–V28), transaction Amount and Time, and the Class label (0 = genuine, 1 = fraud).
