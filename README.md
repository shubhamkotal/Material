
documentation issue: Gaps and limitations in model documentation
Severity: MEDIUM (New)

Description:

Several critical aspects of model documentation are missing, which may impact transparency, interpretability, and long-term usability. The absence of these details limits the ability to validate fraud classification, assess model reliability, and ensure proper business alignment. Below are the identified gaps:

1. Event and non-event definition not documented:
The documentation does not specify the parameters or descriptions used to classify transactions as fraudulent (event) or non-fraudulent (non-event). Clear labeling criteria are essential for model validation and regulatory compliance. Without this, it is unclear whether the model is learning from correctly classified fraud cases, leading to potential bias or misinterpretation.


2. Fraudulent transactions: 1st party vs. 3rd party classification missing:
It is not documented whether the fraudulent transactions are initiated by first-party fraudsters (genuine account holders committing fraud) or third-party fraudsters (external attackers). This distinction is crucial, as detection strategies and risk mitigation measures vary significantly for each case. The lack of clarity may lead to inappropriate model tuning and response strategies.


3. Assumptions regarding business scope, model scope, and data usage not documented:
Although LightGBM does not rely on strong statistical assumptions, the model owner has not documented key business-related assumptions, such as scope, intended usage, and input data considerations. These assumptions influence how the model should be applied and interpreted. The absence of this documentation could lead to misalignment with business goals or improper model deployment.


4. Scoring equation missing from model documentation:
The model documentation does not include the equation used to transform probability outputs into risk scores. This is essential for understanding how risk levels are assigned to transactions and ensuring consistency across different model versions. Without this equation, there is a lack of transparency in decision-making, making it difficult to validate the model’s scoring mechanism.


5. SHAP test assessment not documented:
Although the model owner has performed the SHAP test for explainability, the assessment and interpretation of the results have not been documented. SHAP values help identify feature importance and ensure that the model’s decisions align with business logic. The absence of this documentation reduces trust in the model’s decision-making process and limits interpretability for stakeholders.



Business risk / Consequence and justification of severity and classification:

The lack of proper documentation introduces risks related to model transparency, validation, and regulatory compliance. Missing details on fraud labeling criteria and scoring mechanisms can lead to inconsistent fraud detection, potential regulatory scrutiny, and challenges in model monitoring. Additionally, unclear assumptions may result in business misalignment, reducing the effectiveness of the model in real-world applications.

This issue is classified with a Severity level of MEDIUM, as the model is currently functional with no immediate misclassification concerns. However, the long-term impact of these documentation gaps may lead to difficulties in model validation, adaptation, and auditability. Comprehensive documentation is necessary to ensure that the model remains interpretable, maintainable, and aligned with business needs.

