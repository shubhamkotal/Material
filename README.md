


---

MRI #01: Missing model implementation details, limiting the ability to assess the accuracy, reliability, and compliance of the deployed model from a third-party perspective

Severity: MEDIUM (New)


---

Description

As stated in the GMRP Policy v5.0, Section 2.3, models must be implemented in a secure and suitable IT environment, with appropriate quality and change controls, ongoing testing, and documented evidence to allow independent review. The policy also requires that data inputs be accurate and representative, calculations be controlled and auditable, and outputs be accurate and fit for purpose. Furthermore, the Model Owner must provide comprehensive implementation and testing documentation to the Model Validator to confirm that the deployed model matches the developed and approved version.

In the current case, no such implementation documentation has been provided. There is no defined User Acceptance Testing (UAT) plan specifying the steps to be taken, metrics to be monitored, or thresholds for acceptance when validating the production model against the development version. The approach for output verification, feature-level checks, and resolution of discrepancies is not outlined. Similarly, there is no clarity on how IT controls will be maintained—such as access control, change management, and version tracking—or how data quality checks will be conducted to ensure completeness, accuracy, and representativeness in production. These omissions make it difficult for a third party to verify that the model has been correctly deployed, is operating within a controlled environment, and remains compliant with governance requirements.


---

Business risk / Consequence and justification of severity and classification

Without documented implementation testing, acceptance criteria, and control measures, discrepancies between the developed and deployed models may go undetected, leading to incorrect outputs, misclassification, and potential financial or operational losses. The lack of IT control documentation increases the risk of unauthorized changes or environment instability, while missing data quality validation can compromise the reliability of model outputs. These gaps reduce long-term model effectiveness, weaken governance compliance, and justify a Medium severity rating, with potential to escalate to High if they result in material business impact.


-
