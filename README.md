
The model documentation correctly sums Alerts, Scam Captured, and Scam Captured Amount across April’25 and May’25. However, Recall and VDR metrics have been incorrectly summed instead of averaged, resulting in a false claim of a 14% uplift in VDR, whereas the actual trend shows a 14% decrease. This misrepresentation is inconsistent and inappropriate, potentially misleading stakeholders about model performance.


MRI #03: Model performance degradation, result inconsistency, and missing training-time metrics
Severity: HIGH (New)

Description:
A significant degradation in model performance has been observed during out-of-time (OOT) evaluation compared to the out-sample (development) period. At a fixed alert volume (~3,000 alerts), both VDR and Recall have declined notably while FPR remained stable, indicating the model is now producing a higher proportion of false alerts for the same alert capacity. This suggests score calibration drift and potential loss of discriminatory strength against evolving fraud patterns.

Additionally:

The Excel file containing OOT results does not match the performance table included in the model documentation, leading to inconsistency between reported and actual values. The documentation incorrectly states an increase of VDR by 14%, which is actually a decrease of 14%, raising concerns about the accuracy and transparency of model performance reporting.

The model development documentation lacks essential transparency on training-time performance metrics (in-sample results). Only validation and test phase metrics (out-sample and OOT, e.g., VDR, AUC-ROC, recall) have been shared, with no details on training performance. This restricts the ability to assess the bias-variance trade-off, a fundamental step in evaluating whether the model is underfitting, overfitting, or generalizing appropriately.


Business risk / consequence and justification of severity and classification:
Since the model’s effectiveness directly impacts fraud detection accuracy and operational efficiency, such degradation without supporting evidence from consistent documentation limits the ability to validate model stability and reliability. The inconsistency in provided results further undermines confidence in reported metrics and may lead to incorrect business or governance decisions based on incomplete or inaccurate information.

Moreover, the absence of training-time results hampers a complete and defensible validation process, introducing uncertainty in the model’s generalizability and audit readiness. Hence, IMR is raising a High severity MRI to emphasize the critical need for transparent, aligned, and validated performance reporting—including development, validation, and OOT phases—before the model can be relied upon for production decision-making.


---


MRI #04: Lack of representativeness and sampling adequacy in model development data
Severity: HIGH (New)

Description:
Post random sampling and data treatment, no analysis has been provided to confirm whether the sample remains representative of the population. Similarly, no test results or diagnostic checks have been shared to demonstrate that no systemic bias or distortion in variable relationships has been introduced during data treatment. The event rate used for model development is also undocumented. Given that at a comparable alert volume (~3,000 alerts), Recall and VDR have reduced significantly while FPR has decreased, it raises concern that the model may have been trained on insufficient fraud events and possibly required upsampling of the minority class. The observed performance trend and potential overfitting further align with data representativeness and event sufficiency gaps.

Business risk / consequence and justification of severity and classification:
A non-representative or biased training dataset directly undermines model stability, generalizability, and fraud detection accuracy in production. Missing evidence on event rate and representativeness prevents validation of data integrity and raises concern over the completeness of model development. Given the current performance degradation where Recall and VDR have decreased despite lower FPR, IMR is raising a High severity MRI to highlight the critical need for validated, unbiased, and sufficiently representative training data before model deployment.
