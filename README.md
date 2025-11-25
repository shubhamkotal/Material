
mri #XX: incomplete and insufficient monitoring against defined framework

Severity: HIGH (New)

Description:

The monitoring framework clearly defines required checks across Accuracy, Stability, and Unintended Bias, including moving averages, UCL/LCL limits, CCL bands, amber/red triggers, PSI/CSI measures, and segment-level fairness diagnostics. However, the monitoring results provided do not include any of these components. Instead, only directional deviation scores for FAR, FRR, and a composite score are shared, with no supporting calculations, threshold logic, baseline values, trend charts, or statistical evidence. This prevents verification of how the deviation scores were derived or whether they meaningfully reflect model drift.

Due to the absence of charts, distributions, and methodology for calculating accuracy, stability, and bias indicators, the monitoring cannot be validated against the framework. No information is provided on temporal drift, feature stability, population shifts, or protected-segment fairness. As a result, the current monitoring output is incomplete, does not meet the framework requirements, and provides insufficient information to confirm whether the model remains stable, accurate, or unbiased in production.

Business risk / consequence and justification of severity:
Incomplete monitoring limits the ability to identify emerging issues in model accuracy, stability, or unintended bias. Without the required diagnostics, there is a heightened risk that model drift, performance degradation, or fairness concerns remain undetected. This can directly impact customer experience, operational efficiency, and compliance expectations. Given the absence of evidence to demonstrate that ongoing monitoring aligns with the approved framework, the residual risk remains High.

_____

---

MRI #XX: Lack of periodic review and validation of monitoring framework parameters

Severity: HIGH (New)

Description:

The monitoring framework specifies that key parameters—including the optimal time window for moving averages, the three-month window for establishing the Central Control Line (CCL), and the eight-month window used to derive Amber and Red control limits—must be reviewed and validated within defined post-implementation periods (3–6 months). However, although the model has been live for a considerable period and routine monitoring results have been produced, no evidence has been provided to confirm that these reviews were ever performed. There is no documentation showing assessment of alternative window lengths, recalibration of control limits, or verification that the originally assumed distributions and volatility patterns remain appropriate.

Furthermore, no summary, analysis, or recommendation has been shared to demonstrate whether the monitoring framework still reflects the current transaction mix, market behaviour, or model performance characteristics. The absence of such periodic validation implies that monitoring continues to rely on initial parameters that may no longer be statistically sound or operationally relevant, reducing confidence in the accuracy of RAG triggers and breaching expected model-risk governance practices.

Business risk / consequence and justification of severity:

Without review and validation of the monitoring framework’s core parameters, there is a significant risk that control limits and thresholds do not reflect actual model behaviour. This may lead to inaccurate detection of performance deterioration, delayed identification of drift, and insufficient oversight of bias or stability issues. As a result, potential issues may remain hidden, negatively affecting customer outcomes, operational risk, and regulatory expectations. Due to the absence of required governance reviews, the residual risk is assessed as High.


---

Business risk / consequence and justification of severity:

While the required periodic review of monitoring parameters has not been evidenced, the originally selected time windows and control limit assumptions appear to have been sufficiently robust for the model’s observed performance to date. Current partial monitoring results indicate stable behaviour with no material deviations that would suggest immediate performance or fairness concerns. However, the absence of formal review reduces assurance that the framework remains fully aligned to current data patterns and operational conditions. This creates a moderate risk that potential emerging issues may not be detected as early as intended. Given that present indicators remain satisfactory but governance expectations have not been fully met, the residual risk is assessed as Medium.
