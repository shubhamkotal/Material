
This table presents the performance met purics of a logistic regression model across different datasets: Train, Test, OTV1 (Out-of-Time Validation 1), and OTV2 (Out-of-Time Validation 2). Below is an explanation of each KPI (Key Performance Indicator) and its interpretation:

1. Target = 1 / Target = 0

Represents the count of positive (1) and negative (0) cases in each dataset.

The imbalance is noticeable, as Target = 1 is very low compared to Target = 0. This suggests a highly imbalanced dataset, which can impact model performance.



---

2. KS (Kolmogorov-Smirnov Statistic)

Measures the separation between the positive and negative class distributions.

Higher KS means better model discrimination.

37.1% in Test, 34.2% and 34.4% in OTVs → Model maintains discrimination across different datasets.

Conclusion: Satisfying, as KS values are relatively stable.



---

3. KS Variation

Shows how KS changes relative to the training set.

Low variation (-3.4% and -2.8%) suggests model performance is stable across OTV datasets.



---

4. MAPE (Mean Absolute Percentage Error)

Measures the error in probability predictions.

Higher MAPE indicates worse calibration.

MAPE in OTV2 (27.0%) is higher than in OTV1 (17.8%) → suggests some calibration issues over time.

Conclusion: Medium variation, meaning calibration is somewhat inconsistent.



---

5. ROB (Robustness)

Likely measures model stability across different periods (robustness metric).

Lower values indicate potential instability.

0% in OTV1 and 4% in OTV2 → Model struggles with robustness in unseen data.

Conclusion: Low satisfying, meaning model robustness is weak.



---

6. PSI (Population Stability Index)

Measures distributional shift in input features between datasets.

< 0.1 is ideal, < 0.25 is acceptable, > 0.25 is concerning.

PSI = 1% in Test, 0.5% in OTV1, and 0.4% in OTV2 → No significant data drift.

Conclusion: Satisfying, as there is no major shift.



---

7. %RR (Rejection Rate)

Measures how many cases the model rejects (if rejection criteria exist).

Stable across datasets (0.06% to 0.1%), meaning no significant rejection bias.

Conclusion: Satisfying.



---

8. %Error

Likely represents classification error.

Negative values in OTVs (-9.7% and -13.2%) suggest improvement over time.

Conclusion: Satisfying, as error is reducing.



---

9. LogLoss

Measures model uncertainty in probability predictions (lower is better).

LogLoss is stable across datasets (0.49% to 0.57%), meaning model predictions remain consistent.

Conclusion: Satisfying.



---

Final Takeaway

The model performs well overall, with good discrimination (KS), low data drift (PSI), and stable log loss.

Issues to consider:

Higher MAPE in OTV2 → Indicates potential calibration drift.

Low robustness (ROB) → Model stability may be weak in some scenarios.



If this model is used for production, periodic recalibration and feature monitoring may be needed.

Potential Calibration Drift refers to a situation where the predicted probabilities from a model become less reliable over time. This means that the relationship between predicted probabilities and actual outcomes changes, making the model’s probability estimates less accurate.

How It Relates to MAPE in Your Table?

MAPE (Mean Absolute Percentage Error) measures the error in probability predictions.

In your case, MAPE is 16.9% (Train), 23.1% (Test), 17.8% (OTV1), and increases to 27.0% in OTV2.

This suggests that over time (OTV2), the model's predicted probabilities deviate more from actual outcomes.


Why Does Calibration Drift Happen?

1. Changing Data Patterns – The relationship between features and outcomes might shift over time.


2. Feature Distribution Shift – Even if PSI is stable, small variations in feature distributions may affect calibration.


3. Regulatory or Economic Changes – If this model is used in finance, market conditions may change, impacting prediction accuracy.


4. Overfitting to Past Data – The model may have learned past relationships too well, making it sensitive to new patterns.



Impact of Calibration Drift

If not corrected, the model overestimates or underestimates risk, leading to poor decision-making.

Example: In credit risk, a miscalibrated model may assign lower probabilities to defaults, leading to incorrect risk pricing.


How to Fix It?

1. Recalibrate the Model – Use Platt Scaling or Isotonic Regression to correct probability outputs.


2. Monitor Model Performance – Regularly check KS, MAPE, and PSI to detect drift early.


3. Retrain with Recent Data – Incorporate new data periodically to adapt to changing patterns.


4. Use Stability Constraints – Ensure model features remain stable over time.



Would you like a step-by-step guide on how to recalibrate a model if drift is detected?

