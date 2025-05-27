

mri #XX: absence of user acceptance testing limits model reliability assessment prior to implementation

Severity: HIGH (Proposed)

Description
The model under review is intended to detect fraud for a new payment type that HSBC is engaging with for the first time. As this payment type has not been previously processed by HSBC, there is no internal data available to assess model performance on HSBC-specific portfolio. Therefore, no implementation report or internal performance validation is possible at this stage. The model is developed by a third-party vendor using external data representative of the new payment type, and the bank is considering using it for production deployment.

Given the absence of HSBC-specific data and the criticality of ensuring the model functions as intended, it is essential to conduct a User Acceptance Test (UAT). This may involve evaluating model outputs using vendor-provided proxy data or by generating simulated data by the model owner team to mimic HSBC-like scenarios. This step is vital to understand the model’s behavior on out-of-time and out-of-sample data before moving to a production environment. Additionally, current artifacts such as gain charts alone are insufficient to provide complete insights into model effectiveness or risk segmentation performance.

Business risk / Consequence and justification of severity and classification
Skipping UAT prior to production deployment of a third-party model built on proxy data introduces significant model risk. Without clear evidence of model behavior on test scenarios that approximate HSBC’s operational conditions, there is no assurance the model will perform reliably once implemented. This lack of validation undermines model governance standards and increases the likelihood of misclassification, undetected fraud, or operational disruption.

The absence of UAT effectively means the bank is relying on unverified assumptions of model robustness, which can lead to major losses if the model fails upon go-live. Given the lack of historical data and the novelty of the payment type, UAT becomes the only viable way to de-risk the initial implementation. Therefore, IMR is raising a high severity MRI to reflect the urgent need for rigorous UAT and validation prior to model acceptance and deployment.

