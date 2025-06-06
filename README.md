
MRI #XX: Missing a) HSBC-specific model performance testing limits and b) accuracy-based metrics assessment for third-party model performance
Severity: HIGH (Vendor)

Description:
As per sections 11.3.1 of GMF Policy v12 & MRM Policy v12, model development and assessment must include HSBC-specific performance thresholds and accuracy-based evaluation metrics. However, the current performance evaluation is entirely reliant on the vendor.

a) Missing HSBC-specific performance testing thresholds
The vendor has assessed model performance (for instance, using AUROC) without considering HSBC’s internal threshold framework. No HSBC-calibrated benchmark or acceptance criteria (e.g., minimum AUROC, KS, FPR/FNR thresholds) has been applied, which weakens HSBC's ability to judge the model’s business fitness and compliance with internal policies.

b) Missing accuracy-based metrics for performance
The vendor's performance insights are largely based on discriminatory power (e.g., AUROC), with no evidence of accuracy-based metrics such as misclassification rate, accuracy, confusion matrix, FPR/FNR, etc. This limits visibility into how the model performs in real-world classification scenarios—especially relevant for fraud detection, where false positives and negatives have significant business implications.

Business Risk / Consequence and Justification of Severity and Classification:
Relying solely on vendor-shared metrics dilutes HSBC’s ability to objectively validate and defend the effectiveness of the model. Without internal thresholds and robust accuracy-based assessments, model risk increases significantly—especially in high-impact use cases like fraud detection. Incomplete performance insight could lead to poor customer experience, operational losses, and regulatory scrutiny.

Given that both issues restrict HSBC’s ability to fully evaluate model reliability and performance, and the model is critical (fraud monitoring), this observation is marked as high severity.
