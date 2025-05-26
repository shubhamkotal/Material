mri #03: missing evidence that model development data is representative of hsbc’s portfolio
Severity: MEDIUM (New)

Description
Model validation requires confirmation that the data used to develop the model is representative of HSBC’s portfolio and business context. This ensures that the model is expected to behave reliably when applied to the bank’s actual customer base or transaction data. However, the Model Documentation Template (MDT) does not contain any test results or supporting analysis to demonstrate that the development data reflects HSBC’s portfolio characteristics.

Without this confirmation, it is not possible to assess whether the model is suitable for the intended use case. This becomes especially critical for third-party models, where the development process is external and visibility into the data used is limited. The absence of such analysis creates a significant gap in verifying model applicability and effectiveness within HSBC’s operational environment.

Business risk / Consequence and justification of severity and classification
The lack of evidence confirming the representativeness of the development data introduces risk to model accuracy, reliability, and overall performance. If the data used to create the model differs significantly from HSBC’s portfolio, the model may generate inaccurate predictions or outputs when deployed, potentially leading to poor business decisions or compliance issues.

This risk is heightened in the case of third-party models, where transparency is already limited and assumptions cannot be directly verified. The absence of this validation undermines confidence in the model's design and raises the likelihood of failure when used on internal data. Due to the importance of development data alignment in assessing model suitability, IMR is raising a medium severity MRI.


mri #04: missing model-specific monitoring framework and vendor monitoring details
Severity: HIGH (New)

Description
Ongoing monitoring is a critical control to ensure that models continue to perform as expected in a dynamic environment. For this model, the model owner has not provided a model-specific monitoring framework, nor clarified whether the existing Retail Fraud models’ monitoring approach will be applied. Furthermore, there is no information regarding the vendor’s monitoring practices, planned interventions, or how model updates and modifications will be managed over time.

This lack of clarity creates a significant oversight, as it prevents the establishment of clear accountability, monitoring triggers, and response mechanisms. The absence of both internal and vendor-side monitoring expectations weakens the bank’s ability to detect performance deterioration, data drift, or emerging risks in a timely manner.

Business risk / Consequence and justification of severity and classification
The absence of a defined monitoring framework and vendor oversight introduces a high risk to the ongoing reliability, compliance, and integrity of the model. Without robust monitoring, there is a strong possibility that changes in input data, customer behavior, or market conditions could lead to undetected degradation in model performance. This can result in incorrect risk assessments, operational failures, or regulatory non-compliance.

For third-party models, where HSBC does not control the development lifecycle, this risk is significantly magnified. The inability to ensure or verify timely vendor updates or corrective actions further weakens model governance. Given the potential for substantial business impact and failure to meet internal and regulatory expectations, IMR is raising a high severity MRI.
