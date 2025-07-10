
f) Missing consolidated documentation of model assumptions
While the model is built using Logistic Regression, various assumptions (e.g., scope of model use, input data boundaries, business applicability) are scattered across multiple sections of the documentation. A dedicated section summarising all critical assumptions is missing. Lack of consolidated assumption documentation can lead to misinterpretation of model purpose, scope, and limitations—potentially resulting in misalignment with business objectives or misuse of the model.

g) Missing retraining frequency and criteria
The model documentation does not specify when or how often the model will be retrained to adapt to emerging fraud patterns. This omission weakens HSBC's ability to ensure the model remains relevant and effective over time, especially in dynamic fraud environments.

h) Missing scoring logic and calibration details
Although scores are used for decile analysis and are mentioned in the TOR, the documentation lacks clarity on how model outputs are translated into scores, the scoring range, and how fraud risk thresholds (e.g., score cut-offs) are determined. Absence of detailed scoring logic and calibration methodology reduces transparency for third-party reviewers and makes it difficult to validate how decisions are derived from model outputs.

i) Missing implementation (UAT) test results and performance assessment
While the implementation report states that background mode testing achieved a 100% match rate and has been signed off, no quantitative assessment or summary of UAT results has been provided. This lack of post-deployment validation limits the ability to compare actual outcomes versus expected performance, thereby hindering objective evaluation of model readiness and stability.



mri #05: lack of clarity in model output metrics – missing recall, false positive rate, and FPR tolerance threshold
severity: MEDIUM (New)

description
The current model performance is primarily evaluated using the GINI coefficient, which reflects the discriminatory power of the model. However, there is a lack of clarity on key performance indicators such as the value detection rate (VDR/Recall) and the false positive rate (FPR). These metrics are critical for understanding how well the model identifies actual fraudulent transactions and the extent to which it incorrectly flags legitimate ones.

Furthermore, the acceptable threshold or business tolerance level for FPR has not been defined. Without this benchmark, it is challenging to determine whether the current trade-off between fraud detection and alert volumes is aligned with operational capacity and business objectives. The absence of such metrics and benchmarks limits interpretability and transparency of the model’s effectiveness.

business risk / consequence and justification of severity and classification
Without visibility into the model’s recall and false positive rate, it is difficult to gauge how efficiently the model is detecting frauds versus overwhelming the investigation teams with false alerts. This could lead to under- or over-utilization of resources and potential dissatisfaction from stakeholders who require actionable insights. Moreover, without a defined FPR tolerance, it is unclear whether the model's operating point is optimized for business risk appetite.

However, the current model demonstrates stability in GINI scores across both out-of-sample and out-of-time datasets, indicating consistent classification performance over time. This stability suggests that the model is not exhibiting erratic behavior or sudden performance degradation, which helps mitigate immediate risk. Hence, the issue is classified as medium severity, as it affects model interpretability and operational alignment but does not indicate a critical failure in detection capability.





mri #02: missing training-phase performance metrics and model tuning parameter details
severity: MEDIUM (New)

description
The model design lacks key considerations from the development phase, specifically:

a) Training-time performance metrics (in-sample): Only test-phase metrics such as GINI have been assessed. There is no visibility into how the model performed on the training dataset. This restricts proper evaluation of the bias-variance tradeoff — a crucial diagnostic step to determine whether the model is underfitting, overfitting, or generalizing effectively.

b) Tuning parameter information: The decision threshold (cut-off) used to convert predicted probabilities into binary outcomes (event vs. non-event) in the logistic regression model has not been defined. No supporting analysis was presented to show how the cut-off was selected to optimize a trade-off between recall and precision or how it aligns with business risk tolerance.

These gaps represent design-level omissions that impact the interpretability and completeness of the model’s development process.

business risk / consequence and justification of severity and classification
Although the model exhibits acceptable test performance and shows stable GINI across validation and out-of-time datasets, the absence of training-phase metrics and decision threshold justification introduces uncertainty in the model’s ability to generalize across populations and time. It limits confidence in assessing model robustness and makes it difficult to validate that the model design is optimal under operational constraints.

Given that the current performance is stable and aligns with business expectations, but these design aspects are incomplete, the issue is classified as medium severity. It does not indicate an immediate failure but highlights important gaps that could impact model risk management and long-term reliability.


mri #06: missing monitoring results and inconsistent use of performance metrics
severity: HIGH (New)

description
The model was primarily evaluated using the GINI coefficient to assess discriminatory power. However, it is also stated that the F1 score will be used as the key metric to evaluate performance deterioration relative to the baseline (development sample). Despite this, no F1 score or accuracy-based metrics were applied or reported during the model development phase, leading to a disconnect between the defined monitoring strategy and the model’s original performance benchmarks.

Additionally, no model monitoring reports have been produced since the model went live, resulting in a lack of visibility into current performance or potential degradation in production. While the model owner has acknowledged this monitoring delay and raised an MSII (Managed Self-Identified Issue) to address it, and a plan is in place to complete the monitoring by end of July 2025, the specific monitoring gaps and risks remain undisclosed.

This lack of both actual monitoring output and consistency in selected performance metrics undermines transparency, risk tracking, and the ability to take timely corrective actions.

business risk / consequence and justification of severity and classification
Absence of ongoing monitoring results creates a significant risk, as the current model performance in live environments remains unknown. Without regular performance tracking, it is impossible to identify potential drift, shifts in data quality, or degradation in fraud detection capability. This can lead to delayed response to emerging threats, financial loss, or unnecessary operational effort due to undetected increase in false positives or false negatives.

Moreover, the inconsistent use of F1 score — proposed as the basis for performance comparison but not implemented during development — raises concerns about the coherence and integrity of the model lifecycle management.

Although an MSII has been raised and remediation is planned, the lack of transparency on existing gaps and absence of interim controls or performance insights justifies a classification of high severity. It reflects an elevated level of risk exposure due to monitoring failure and misaligned evaluation criteria.

