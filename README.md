

MRI #01: Insufficient information in submitted CVQ documentation

Severity: MEDIUM (New)

Description

As per Section 2.7 of the GMR Policy v5.0, “All models must be documented to demonstrate that the model is fit for purpose and performing as intended, with the level of detail commensurate with the Model Tier.”

The model was implemented prior to the effective date of the Group Model Risk Policy (May 2020). Accordingly, the use of MRG-approved global model documentation templates was waived, and the necessary approvals from the relevant Model Sponsors were obtained. As a result, the documentation made available for validation is limited to the Core Validation Questionnaire (CVQ), Model Technical Document (MTD), and monitoring results.

However, the CVQ does not adequately cover key aspects of the model, as outlined below:

Assumptions regarding business scope, model scope, and data usage are not documented:
Although the XGBoost model does not rely on strong statistical assumptions, key business-related assumptions—such as intended use, scope, and input data considerations—have not been documented. These assumptions are critical for appropriate model application and interpretation. Their absence increases the risk of misalignment with business objectives.

Model limitations are not documented:
Clear articulation of model limitations is required to assess their potential impact on model outputs. In the absence of such documentation, there is a risk of misinterpretation of results or use of the model beyond its intended scope, which could lead to incorrect or suboptimal decisions.

Data preprocessing steps are not documented:
Key data preparation activities, including data quality checks, missing value treatment, variable exclusion due to high missingness, duplicate record removal, outlier detection or treatment, and sampling methodology, have not been described in the CVQ documentation.

Insufficient disclosure of model explainability:
While the CVQ states that qualitative testing was performed through a review of the top ten model features to assess explainability, the results of this review have not been included in the CVQ.


Business risk / Consequence and justification of severity and classification

The lack of proper documentation introduces risks related to model transparency, validation, and compliance. The long-term impact of these documentation gaps may lead to difficulties in model validation, adaptation, and auditability. Nevertheless, these issues are not likely to directly impact the model’s functionality or the outputs produced and hence are classified as medium severity.


--



Below is a professionally written MRI, aligned in structure, tone, and depth with your earlier example.
Changes are minimal, severity is justified as Medium, and both Description and Business Consequence are kept to one paragraph each, as requested.


---

mri #02: lack of transparency in model monitoring results

Severity: MEDIUM (New)

Description

As per the approved model monitoring plan, model performance is required to be assessed using Lift and Population Stability Index (PSI). For the most recent monitoring cycle, the model owner has reported a Lift value of 2.84 and a PSI value of 0.09, both of which are within the predefined monitoring thresholds and indicate satisfactory model performance. However, only the final metric values have been provided, without any supporting calculation details or evidence. Specifically, no calculation tables, decile-wise performance results, response rate summaries, definition of the target population (e.g., top 20%), PSI calculation methodology, or baseline/reference distribution used for PSI have been shared. In the absence of this supporting information, the reported monitoring results cannot be independently reviewed or validated, resulting in a lack of transparency around how these metrics were derived.

Business risk / Consequence and justification of severity and classification

The absence of detailed monitoring calculations limits the ability of independent reviewers to validate the accuracy, robustness, and consistency of reported model performance metrics, thereby reducing transparency and auditability of the monitoring process. While the reported Lift (2.84) and PSI (0.09) indicate that the model is currently performing within acceptable thresholds and no immediate performance deterioration is observed, the lack of evidentiary support poses governance and validation risks over time. As the issue does not indicate an adverse impact on current model performance or outputs, it is classified as medium severity.


---

