# Fifa-players-analysis
Analysis of 19,630 professional soccer players (men's and women's) from the FIFA 22 dataset. The project is split into two parts: predicting player rank using linear regression, and classifying a player's preferred foot using K-Nearest Neighbors.
Part 1 — Predicting Player Rank (Linear Regression)
Using four player attributes — passing, attacking, defending, and skill — to predict overall player rank.
Key findings:

R² = 0.705 — the model explains 70.5% of variance in player rank
RMSE of ~3.74, meaning predictions are off by ~3–4 ranking positions on average
attacking is the strongest and most statistically significant predictor
skill was not statistically significant (p = 0.465); its confidence interval includes zero
Coefficients were validated by comparing statsmodels and sklearn outputs — differences were less than 0.002
Part 2 — Classifying Preferred Foot (KNN)
Using 10 skill-based features (shooting, passing, dribbling, attacking, defending, skill, movement, power, mentality, goalkeeping) to classify whether a player is left- or right-footed.
Key findings:

Overall accuracy: 72%
The model is heavily biased toward predicting right-footed players due to class imbalance (74.8% of players are right-footed)
Recall for left-footed players: only 17% — the model correctly identifies left-footed players just 1 in 6 times
Potential improvements: SMOTE oversampling or class weighting to address imbalance
