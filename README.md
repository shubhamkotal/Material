
mri #03: missing evidence that model development data is representative of hsbc’s portfolio
Severity: MEDIUM (New)

Description
Model validation requires confirmation that the data used to develop the model is representative of HSBC’s portfolio and business context. This ensures that the model is expected to behave reliably when applied to the bank’s actual customer base or transaction data. However, the Model Documentation Template (MDT) does not contain any test results or supporting analysis to demonstrate that the development data reflects HSBC’s portfolio characteristics.

Without this confirmation, it is not possible to assess whether the model is suitable for the intended use case. This becomes especially critical for third-party models, where the development process is external and visibility into the data used is limited. The absence of such analysis creates a significant gap in verifying model applicability and effectiveness within HSBC’s operational environment.

Business risk / Consequence and justification of severity and classification
The lack of evidence confirming the representativeness of the development data introduces risk to model accuracy, reliability, and overall performance. If the data used to create the model differs significantly from HSBC’s portfolio, the model may generate inaccurate predictions or outputs when deployed, potentially leading to poor business decisions or compliance issues.

This risk is heightened in the case of third-party models, where transparency is already limited and assumptions cannot be directly verified. The absence of this validation undermines confidence in the model's design and raises the likelihood of failure when used on internal data. Due to the importance of development data alignment in assessing model suitability, IMR is raising a medium severity MRI.

mri #05: limited model performance insights due to absence of accuracy-based metrics
Severity: MEDIUM (New)

Description
The model owner has not provided performance testing results based on accuracy-based metrics such as precision, recall, F1-score, or confusion matrix. The current performance assessment is limited to gain chart analysis, which, while useful for understanding rank-ordering capability, does not provide a comprehensive view of the model’s predictive accuracy or classification strength.

While the gain chart indicates that the model is able to capture approximately 65% of the fraud amount, it does not offer insights into false positives, false negatives, or overall classification quality. Accuracy-based metrics are essential to understand trade-offs between detection and misclassification, which directly impact operational decision-making and resource allocation.

Business risk / Consequence and justification of severity and classification
Relying solely on gain chart analysis limits the ability to fully evaluate the model’s effectiveness, especially in high-risk areas like fraud detection where both missed frauds and false alarms have significant consequences. The absence of comprehensive performance metrics creates a partial understanding of the model’s strengths and weaknesses, reducing confidence in its practical use.

Given that gain chart results indicate moderate performance, and the model is able to capture a substantial portion of fraud value, the immediate business impact is not critical. However, without more detailed accuracy-based evaluation, there is a risk of suboptimal model tuning and ineffective deployment strategies over time. Therefore, IMR is raising a medium severity MRI to emphasize the need for a more complete performance assessment..

mri #04: missing monitoring framework and change governance plan for third-party model
Severity: MEDIUM (New)
Description
The model documentation does not include a monitoring framework specific to this third-party model. It is also unclear whether the common monitoring framework used for retail fraud mitigation models will be applied. Additionally, there is no information provided regarding the vendor’s plan for ongoing monitoring or governance practices.
A defined monitoring framework is essential to ensure that the model’s performance is tracked effectively post-implementation and that any deterioration is detected and addressed in a timely manner. It also serves as a mechanism to validate whether the model continues to function as intended under changing portfolio conditions. Moreover, the monitoring framework should include a model change log to track any modifications made over time, providing transparency into changes, rationale behind updates, and evidence that governance and controls are in place to manage such changes.
This lack of clarity on monitoring responsibilities and absence of a change governance structure weakens HSBC’s ability to ensure model sustainability and accountability once it enters production.
Business risk / Consequence and justification of severity and classification
The absence of a monitoring framework and model change governance plan at the implementation stage presents a moderate risk to ongoing model performance and integrity. Without a clear monitoring approach, performance degradation may go undetected, potentially impacting business decisions or compliance outcomes. Additionally, a missing change log limits transparency into updates made by the vendor, reducing HSBC’s ability to evaluate the rationale for model modifications and whether such changes improve performance or introduce new risks.
This issue is particularly relevant for third-party models, where internal visibility is limited and formal control mechanisms must be explicitly defined. Given the model is currently in the implementation stage and this framework is required before full deployment, IMR is raising a medium severity MRI.
