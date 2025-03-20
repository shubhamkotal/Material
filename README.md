
MRI # 03: Lack of Portfolio Segmentation Analysis, Leading to Potential Model Bias

Severity: MEDIUM (New)

Description:
The current model is built on both credit and debit card transactions, covering six different portfolio segments (UK, CIIOM, CMB, MS, FD, and SVB). However, no statistical validation has been conducted to confirm whether combining these portfolios into a single model is appropriate. Different portfolios may exhibit distinct transactional behaviors, which, if unaccounted for, could lead to suboptimal model performance.

Key factors such as transaction size and spending patterns across debit and credit cards could vary significantly, introducing potential inconsistencies in customer classification. Statistical techniques such as clustering or Customer Similarity Index (CSI) should have been applied to assess the homogeneity of these portfolios before deciding on a unified model. Without this validation, the model may not be capturing critical nuances specific to each segment.

Business Risk / Consequence and Justification of Severity and Classification:
Failure to validate portfolio segmentation poses business risks, as model bias could lead to misclassification. If certain portfolios behave differently, the model might underperform for specific segments, leading to missed opportunities or inefficient resource allocation.

However, the current model has shown improved classification compared to its previous version, as evidenced by an increase in the Valid Detection Rate (VDR) and a reduction in the False Positive Rate (FPR). This indicates that, despite the potential risks, the model is performing satisfactorily at present. The long-term concern is whether model accuracy and stability can be maintained without proper portfolio segmentation analysis.

Given that the immediate impact is not critical, but long-term effectiveness could be compromised, this issue is classified as MEDIUM severity. Conducting statistical tests to confirm portfolio similarities would enhance confidence in the model’s robustness and ensure that customer selection is optimized across all segments.

