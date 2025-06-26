
Here’s the MRI issue written in the same structure and tone as your example:


---

mri #XX: missing insight into high-value fraud detection coverage
severity: medium (vendor)
description:
The current model is designed with a specific objective—to detect high-value fraud transactions. While the model’s performance metrics (e.g., overall accuracy, AUROC, recall) have been shared and indicate acceptable results, a critical gap remains in understanding how effectively the model captures the intended target: high-value frauds. Specifically, there is no analysis provided on:

How many high-value fraud observations were present in the test data.

Out of those, how many were correctly identified by the model.


This omission significantly limits our ability to assess whether the model is achieving its intended business goal. A model that shows strong recall overall may still fail to identify rare but high-impact events if those events are underrepresented in the evaluation. For instance, if the test data contains only a few high-value frauds and the model detects only one of them, the reported metrics may overstate the model's effectiveness in real-world scenarios.

Furthermore, there is no stratified performance insight or segment-wise breakdown based on fraud amount tiers. This is particularly important for high-value fraud detection use cases where the business priority lies in minimizing financial loss from large transactions, not just maximizing overall fraud detection.

business risk / consequence and justification of severity and classification:
Given that the model’s current reported performance shows improved classification and an increased Value Detection Rate (VDR), the model appears to meet general expectations. However, without visibility into the high-value fraud capture rate, the validation lacks completeness and auditability. This raises concern about the model’s actual effectiveness in protecting against high-risk losses. Due to the strategic importance of high-value fraud detection and the lack of critical output insights for this segment, the issue is classified as medium severity. The business performance is currently acceptable, but the missing granularity in model evaluation prevents a thorough and confident validation.
