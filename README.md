yoMRI #05: Absence of Model Assumptions and Limitations Documentation. Severity: HIGH (New)

Description
No documentation has been provided outlining the key assumptions and limitations of the model. Understanding these factors is essential to ensure that the model is sound, fit for purpose, and appropriately interpreted. Without explicitly identifying and assessing assumptions, there is no validation that they are reasonable, valid, or well-supported.

Similarly, model limitations must be clearly defined to understand their impact on model outputs. Without this, stakeholders may misinterpret results or apply the model beyond its intended scope, leading to incorrect or suboptimal decisions. The lack of transparency around assumptions and limitations also makes it difficult to assess model robustness and reliability over time.

Business Risk / Consequence and Justification of Severity and Classification
Failing to document assumptions and limitations increases the risk of misinterpretation and misuse of the model. If key assumptions are flawed or untested, model predictions may be unreliable, potentially leading to incorrect business decisions. Additionally, an unclear understanding of limitations can result in applying the model to scenarios where it is not valid, further compromising its effectiveness.

Given these risks, the issue is classified with a Severity level of HIGH, as it directly impacts model governance, interpretability, and decision-making reliability. Clearly defining assumptions and limitations is crucial for ensuring model transparency, validity, and long-term usability.

MRI #06: Incomplete Model Performance Monitoring and Undefined Thresholds. Severity: HIGH (New)

Description
The current model performance monitoring framework includes metrics such as PSI, CSI, KS, rank ordering, and model lift. While PSI and CSI assess model stability, and KS, RO, and model lift evaluate model strength, these metrics alone do not provide a complete view of model performance. Additional confusion matrix-based metrics like AUC, Recall, and Precision should be incorporated to demonstrate that the model is performing within expected levels.

Furthermore, no thresholds have been defined for the existing stability and strength metrics. Without clear thresholds, breaches in performance cannot be identified, making it unclear when corrective actions are needed. Additionally, no action plan has been documented to address threshold breaches, further limiting proactive model management.

The latest monitoring results for November 2024 have also not been provided, making it impossible to assess the model's current status and effectiveness. Without up-to-date monitoring data, stakeholders cannot determine whether the model remains reliable or if performance degradation has occurred.

Business Risk / Consequence and Justification of Severity and Classification
The lack of comprehensive model performance evaluation, undefined metric thresholds, and missing latest monitoring results introduce significant risks. Without additional performance metrics like AUC, Recall, and Precision, the model’s classification effectiveness remains unclear, increasing the risk of misclassifications. Undefined thresholds prevent timely identification of performance deterioration, leading to delayed corrective actions. Moreover, the absence of recent monitoring results leaves decision-makers without crucial insights into the model’s current reliability.

Given these risks, this issue is classified with a Severity level of HIGH, as it impacts model transparency, governance, and long-term effectiveness. Establishing a robust performance monitoring framework with well-defined thresholds and updated results is essential to ensure continued model reliability and effectiveness.

