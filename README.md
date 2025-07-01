# Credit Card Fraud Detection: Handling Imbalanced Data

This project explores the challenges of detecting fraudulent credit card transactions using machine learning techniques tailored to imbalanced datasets. With only 0.17% of transactions labeled as fraud, traditional models struggle to detect rare but costly fraudulent activity. The project compares sampling techniques and class balancing strategies to evaluate their impact on model performance.

## Highlights

- Dataset: Kaggle Credit Card Fraud dataset with 284,807 transactions (0.17% fraud)
- Baseline model: Random Forest Classifier
- Primary metrics: Recall, Precision, F1 Score
- Addressed class imbalance using:
  - Random Oversampling
  - Random Undersampling
  - SMOTE
  - SMOTE + Tomek Links
  - Class weight adjustments
  - Hyperparameter tuning via GridSearchCV

## Key Insights

- **Baseline model**: High accuracy, poor recall on minority class.
- **SMOTE**: Highest recall (85.2%) but with low precision.
- **SMOTE + Tomek Links**: Balanced F1 score (83.4%) with fewer false positives.
- **Class Weights**: Good recall (82.4%) with moderate F1 and precision.
- **Best method** depends on the business goal: catching more fraud (high recall) or avoiding false alarms (high precision).

## Project Structure

- **Exploratory Analysis**: Dataset characteristics, outlier handling
- **Data Splitting**: Stratified train-test split to prevent leakage
- **Baseline Model**: Random Forest on original data
- **Oversampling Methods**: Random oversampling, SMOTE
- **Undersampling Method**: Random undersampling
- **Hybrid Method**: SMOTE combined with Tomek Links
- **Model Evaluation**: Confusion matrices, recall/precision trade-offs
- **Tuning**: GridSearchCV for optimal hyperparameters

## Conclusion

Handling imbalance is crucial for fraud detection. This project shows how different resampling techniques affect performance, with SMOTE and class weighting offering strong results. Choosing the right method depends on whether minimizing false negatives or false positives is more important for your application. Want to learn more? read the pdf:)
