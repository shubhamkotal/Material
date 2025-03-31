Severity: HIGH (MRI)

Description
As per section 2.8 of GMR Policy:
"h. The Model Owner must submit relevant model implementation and testing documentation to the Model Validator for independent review."

Model implementation testing, such as User Acceptance Testing (UAT), lacks sufficient documentation for a third party to understand the process and results. The provided test documents do not clearly outline the implementation steps, making it difficult to validate that the developed and deployed models are identical. Additionally, there is no clear assessment of implementation results, limiting the ability to compare expected vs. actual model performance. Performance deterioration (over-fitting) has been observed during out-of-time testing, characterized by high recall and very low precision values. Without detailed documentation, discrepancies between the development and implemented models may go unnoticed, significantly impacting overall model reliability.

Business Risk / Consequence and Justification of Severity and Classification
Unclear implementation testing and documentation introduce significant business risks. If the deployed model differs from the developed version or does not perform as expected, it may lead to incorrect classifications, resulting in financial losses, regulatory compliance issues, and operational inefficiencies. The observed performance deterioration, particularly the high recall with very low precision, increases the risk of incorrect decisions, amplifying business impact. Without proper assessment, issues in model performance may remain undetected, reducing long-term effectiveness and reliability. Given the observed degradation in model performance and the associated risks, the severity is classified as HIGH (MRI). Ensuring comprehensive testing and clear documentation is critical for maintaining model accuracy, compliance, and operational confidence.


