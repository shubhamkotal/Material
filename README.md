

mri #07: missing data quality reassessment report during monitoring
severity: MEDIUM (New)

description
While PSI and CSI are being performed at variable level to capture shifts in data distributions, there is no dedicated reassessment report to validate whether the preprocessing steps for handling missing data—defined during development—remain adequate under current production conditions. This creates a gap in ensuring that imputation or substitution logic continues to be appropriate as data quality evolves.

Such a reassessment is necessary because missing data patterns may change independently of distributional shifts captured by PSI/CSI. For example, an increase in null values for key predictors might still pass stability thresholds but render the predefined imputation logic insufficient, impacting data quality before it translates into visible model drift.

business risk / consequence and justification of severity and classification
Without periodic reassessment of missing data handling, there is a risk that predefined preprocessing rules may no longer be suitable, potentially leading to biased imputations, silent distortion of variable distributions, or weakening of model robustness over time. Although current performance metrics (e.g., KS) remain stable and PSI/CSI help detect shifts, the absence of targeted missing data quality checks leaves residual exposure. Given that immediate impact is limited but medium-term risks exist, the issue is classified as medium severity.

---
--

mri #08: absence of explainability reporting in monitoring
severity: MEDIUM (New)

description
While the model was developed with feature importance analysis and variable contribution checks, there is no ongoing explainability reporting integrated into monitoring. This creates a gap in validating whether the same features continue to drive model outcomes in production as originally intended. Without periodic explainability checks, changes in feature influence may go unnoticed, even if headline metrics such as KS or PSI/CSI appear stable.

Explainability reporting is particularly important to ensure model transparency and alignment with business logic. A shift in key drivers (e.g., less relevant predictors dominating risk scores due to hidden correlations) may signal underlying data drift or operational risk, which standard performance measures alone cannot capture.

business risk / consequence and justification of severity and classification
The absence of explainability monitoring creates risk of reduced transparency, undetected shifts in feature influence, and potential misalignment between model decisions and business expectations. This could lead to regulatory concerns, stakeholder challenges, or operational blind spots if the model starts relying on spurious drivers. While current performance indicators (e.g., KS) are stable, the lack of feature-level explainability tracking leaves a medium level of residual risk exposure. Hence, the issue is classified as medium severity.
