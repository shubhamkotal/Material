
mri #09: (a) missing framework for handling differences between development and monitoring metrics; (b) lack of clarity on sensitivity testing approach
severity: MEDIUM (New)

description
The monitoring framework does not contain a defined section on how to manage situations where monitoring metrics differ from those applied during development, nor does it provide justification for such differences. This creates ambiguity in ensuring that performance evaluation remains consistent with original benchmarks. In addition, there is a lack of clarity on how sensitivity testing will be conducted, particularly regarding the role of PSI/CA in assessing model robustness under data shifts.

business risk / consequence and justification of severity and classification
The absence of a framework for handling differences in metrics reduces transparency and risks undermining comparability of model performance over time. Similarly, the lack of a clear sensitivity testing methodology introduces uncertainty in evaluating the model’s resilience to variations in input data. These gaps weaken the overall monitoring framework and may delay detection of emerging issues, though existing stability and strength checks provide partial mitigation. Therefore, the issue is classified as medium severity.



---

MRI #06: Model documentation limitations observed in Monitoring Framework

Severity: MEDIUM (New)

Description
The review of the Customer Selection Binary Classifier Model Monitoring Framework highlights multiple documentation gaps and unclear definitions. These limit transparency, consistency, and traceability in monitoring outcomes. The following issues were observed:

1. Lack of clarity on monitoring exceptions (Query 2 – Section 3.1):
The framework does not define a minimum number of events or minimum observation period required for monitoring tests to be valid. Similarly, no process is documented for providing a rationale when certain monitoring tests cannot be performed due to insufficient data. This gap is observed in Section 3.1, where the phrase “earliest available period for which measures are available” is used without further clarification.


2. Absence of rationale for metric thresholds (Query 6 – Section 4.4.4):
Thresholds such as “25% deterioration in KS from benchmark = RED” are included in Section 4.4.4 but not justified. The absence of rationale creates ambiguity on whether thresholds are aligned with business objectives, regulatory expectations, or statistical significance.


3. Unclear baseline definition for monitoring (Query 13 – Section 3.1):
In Section 3.1, the framework states that benchmarks will be based on the “earliest available period”, but it does not specify whether this refers to model development data, validation data, or the first monitoring window. This lack of clarity may lead to inconsistent benchmark selection.


4. Missing rationale for Model Lift thresholds (Query 14 – Section 4.3.1):
The framework defines categories of Lift in Section 4.3.1 (Minor/No, Moderate, Significant) using percentage thresholds. However, there is no explanation of why these thresholds were chosen or how they are linked to business objectives such as improved targeting or financial benefit.


5. Ambiguity in overall model strength aggregation (Query 15 – Section 4.3.4):
Section 4.3.4 states that overall model strength is based on KS, Lift, and Rank Ordering. However, the method for aggregating these metrics into a final RAG is not clearly defined. For example, KS could be Red while Lift and RO are Amber, yet the overall status is Amber. Without a transparent rule, reviewers may misinterpret how conflicting signals are resolved.


6. Conservative vs. non-conservative RAG treatment not justified (Query 16 – Section 4.4.4):
In Section 4.4.4, non-conservative rules are applied (e.g., Green + Amber = Green) instead of the more typical conservative approach (which would classify as Amber). The lack of justification for this methodology introduces subjectivity in RAG assessment.


7. Incomplete action plan definition (Query 18 – Section 6.4):
Section 6.4 mentions that a persistent breach occurs when the model receives a Red overall status for two consecutive monitoring cycles, requiring suspension or rebuild. However, it does not define:

What action is required if one Red outcome occurs.

What action is required if consecutive Amber outcomes are observed.
This omission may delay timely remediation in early warning situations.




Business risk / Consequence and justification of severity and classification
The above gaps increase the risk of inconsistent monitoring outcomes, weak governance, and potential regulatory scrutiny. Lack of documented rationale and rules reduces transparency for independent validation and could lead to delayed corrective actions when weaknesses emerge. While these gaps are significant for governance and compliance, they primarily concern documentation and process clarity rather than the model’s predictive performance. Therefore, the severity is classified as Medium.


---
