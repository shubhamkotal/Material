mri #03: missing evidence that model development data is representative of hsbc’s portfolio
Severity: MEDIUM (New)

Description
Model validation requires confirmation that the data used to develop the model is representative of HSBC’s portfolio and business context. This ensures that the model is expected to behave reliably when applied to the bank’s actual customer base or transaction data. However, the Model Documentation Template (MDT) does not contain any test results or supporting analysis to demonstrate that the development data reflects HSBC’s portfolio characteristics.

Without this confirmation, it is not possible to assess whether the model is suitable for the intended use case. This becomes especially critical for third-party models, where the development process is external and visibility into the data used is limited. The absence of such analysis creates a significant gap in verifying model applicability and effectiveness within HSBC’s operational environment.

Business risk / Consequence and justification of severity and classification
The lack of evidence confirming the representativeness of the development data introduces risk to model accuracy, reliability, and overall performance. If the data used to create the model differs significantly from HSBC’s portfolio, the model may generate inaccurate predictions or outputs when deployed, potentially leading to poor business decisions or compliance issues.

This risk is heightened in the case of third-party models, where transparency is already limited and assumptions cannot be directly verified. The absence of this validation undermines confidence in the model's design and raises the likelihood of failure when used on internal data. Due to the importance of development data alignment in assessing model suitability, IMR is raising a medium severity MRI.
