# Insurance Fraud Prediction

This project uses Machine Learning to predict fraudulent insurance claims based on policyholder data and incident details.

## Technical Highlights
- **Data Cleaning:** Handled missing values in features like `authorities_contacted`.
- **Feature Engineering:** Transformed date-based features into numerical durations and extracted incident timing.
- **Statistical Analysis:** Used **Variance Inflation Factor (VIF)** to detect and remove multicollinearity among claim amount features.
- **Modeling:** Implemented **Logistic Regression** to classify claims as fraudulent or legitimate.

## Technologies Used
- Python (Pandas, NumPy, Scikit-learn)
- Visualization (Matplotlib, Seaborn)
- Statsmodels (for VIF analysis)

## Results
The model helps identify key indicators of fraud, such as incident severity and specific hobbies of the insured, providing a baseline for automated fraud detection systems.