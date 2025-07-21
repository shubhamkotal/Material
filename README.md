

For Pointer 1 – FPR Thresholds:
Thanks for the explanation. We agree that FPR in fraud models is dynamic and changes based on fraudster behavior and business needs. However, this explanation looks more like a mitigation. What we are looking for is to have this clearly documented in the model documentation, so that third-party reviewers can understand the approach taken for FPR handling in this specific model.

For Pointer 2 – Model Acceptance Criteria:
While model usage has been approved by the sponsor, owner, and user, our comment was specifically about the defined acceptance criteria in the documentation—i.e., €0.5M annualized fraud loss savings. We couldn’t trace this threshold in the approval records, and we also noted that the MRF approval is still pending.

For Pointer 3 – Third-Party Arrangements:
The documentation mentioned the use of a vendor platform (Feedzai-DSE), which gave the impression of third-party involvement. Now that you've clarified it runs on GCP under the HSBC instance, we understand it falls fully under HSBC control and can be considered internal. We’ll take down the MRI related to third-party arrangements. It would be helpful if this was clearly mentioned in the documentation.

Here is a concise version of the Business Risk / Consequence and Justification of Severity and Classification section — summarized without losing key points:


Business Risk / Consequence and Justification of Severity and Classification:
The lack of formal monitoring since go-live poses a significant risk, as model performance in production remains untracked. This limits the ability to detect performance degradation, data quality issues, or misalignment with risk appetite. Although ad-hoc monitoring by the FPLP team provides some mitigation, it is not a sustainable solution.

There is also inconsistency between development (GINI) and planned monitoring metrics (F1-score), raising concerns over lifecycle alignment. While no immediate business impact is observed—as noted in the MSII—and the model has shown reliable GINI performance in development and out-of-time samples, potential financial and customer impacts may arise if the model underperforms undetected.

The business impact is assessed as Medium, consistent with similar audit findings (A302140). No regulatory or reputational impact is expected. With an MSII raised and monitoring planned by July 2025, the issue is classified as High Risk.
