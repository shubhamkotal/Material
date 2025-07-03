

Thank you for your detailed feedback on the UK Payment MAL Classification model (GMIS-078502). I appreciate your observations and the opportunity to clarify a few areas where we may be viewing risk and control from different angles. Please find below my responses to the key points raised:


---

1. Assumptions Regarding Business Model, Scope, and Data Usage Not Documented
As you rightly noted, "assumptions influence how the model should be applied and interpreted." If any assumptions are incorrectly stated or unsupported by factual evidence, they will be removed during IMR review. That said, capturing these assumptions—even if business-aligned and dynamic—ensures traceability, context, and model alignment over time.


---

2. Scoring Equation Missing from Model Documentation
LightGBM, as a gradient boosting model, provides probabilistic outputs. However, the final score used for decisioning is derived through a transformation of these probabilities (e.g., scaling or applying thresholds). Understanding this scoring logic is critical because, as you mentioned, "Without the exact formula for the model, risk scoring is a black box mechanism." Our goal is not academic compliance, but ensuring interpretability, consistency across releases, and auditability of decision-making.


---

3. Undocumented Rules, MAL Acceptance Criteria, Cut-offs, and FPR Thresholds
While I understand that cut-offs and rule thresholds may evolve due to changing fraud patterns, documentation of the rationale behind their selection remains essential. These decisions define how observations are labeled as fraud or non-fraud, directly affecting model learning, monitoring, and governance.

Even if thresholds are flexible, a record of their business approval or operational logic should be maintained. This includes:

MAL acceptance criteria (e.g., why >10% XCP was chosen),

Score cut-off rationale,

Fraud team’s review capacity, and

Acceptable False Positive Rate (FPR).


This documentation enables meaningful performance reviews, prevents misinterpretation, and ensures alignment with risk appetite.


---

4. Platform-Level Compliance
You are right that the concern “is a platform challenge not a model issue”. However, since the platform forms part of the model's deployment and integration lifecycle, platform compliance (e.g., with Data Risk and Cyber Security Policies) is relevant to the overall model governance. If the platform has been audited, attaching the corresponding report would serve as strong evidence and closure.


---

5. Fraud Tagging and Model Output Usage
The reference to "fraud tagging" stems from the use of rules and score thresholds to label transactions. If these mechanisms are undocumented or vary in application, it could lead to inconsistent fraud detection, increased false positives, and hinder model monitoring (especially during backtesting or performance validation). Documenting these logic flows, even at a high level, ensures transparency and better alignment with the intended purpose of the model.


---

Conclusion
I truly value this discussion and am open to a follow-up call to align our understanding further. The intent behind these points is not to create overhead but to ensure we have strong, future-proof documentation that supports validation, monitoring, and audit readiness—ultimately reducing risk to “company, customer, shareholder, stakeholders or society.”

Thank you once again for your candid feedback and collaboration.

