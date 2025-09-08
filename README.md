
mri #06: missing adversarial stress testing to assess model robustness
severity: MEDIUM (New)

description
The vendor-provided fraud model has not been accompanied with evidence of adversarial stress testing, i.e., simulated probing to evaluate how fraudsters may adapt and bypass the model over repeated attempts. As per GMR Policy v5.0 section xx, “models exposed to external actors must be validated against adversarial manipulation to ensure robustness and resilience.” In the absence of such analysis, the model’s vulnerability to systematic gaming attempts remains unassessed, limiting visibility into potential weaknesses that could be exploited in real-world conditions.

business risk / justification of severity and classification
Current monitoring shows improved classification compared to previous model versions, with higher vendor detection rate (VDR) and reduced false positive rate (FPR). This suggests stable performance under normal operating conditions. However, without adversarial stress testing, the ability of the model to withstand fraudster probing remains unknown. This gap introduces governance and operational risk, as fraudsters may exploit predictable scoring behavior over time. Given the presently strong performance metrics, the severity is classified as medium rather than high.

