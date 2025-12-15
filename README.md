

MRI #XX: insufficient component-level performance evidence for diva-ocrlabs
severity: MEDIUM (New)

description:
The in-scope DIVA-OCRLabs model is a component of the overall DIVA solution; however, the performance evidence provided reflects only the aggregated performance of the main DIVA model. Standalone or component-level performance metrics for DIVA-OCRLabs have not been presented, limiting the ability to independently assess its effectiveness.

The available performance results are largely focused on selfie and facial verification outcomes, with limited visibility into OCR and textual verification use cases that are central to the DIVA-OCRLabs model. Specifically, evaluation of customer-provided textual attributes (e.g., first name, last name, date of birth) against extracted document data, document authenticity checks, and screening against lost and stolen document databases have not been clearly evidenced.

business risk / consequence and justification of severity and classification:
The absence of component-level performance evidence may obscure potential weaknesses in document text extraction, data matching, or document authenticity validation, increasing the risk of undetected identity fraud. However, as the overall DIVA model performance has been assessed as satisfactory and no material end-to-end performance issues have been identified, this issue represents a governance and transparency gap rather than a confirmed control failure. Accordingly, IMR has classified this MRI as Medium severity, emphasizing the need for improved component-level performance visibility to support effective model risk oversight.


--


MRI #XX: absence of post-implementation monitoring results and breach of monitoring frequency
severity: HIGH (New)

description:
No post-implementation monitoring results have been provided for the in-scope model use case (MUC-00114912 – Hong Kong operation site), despite the model being live since August 2024. This represents a breach of the required semi-annual monitoring frequency, as the first monitoring cycle was due and reportable by March 2025. The absence of any documented monitoring outcomes prevents confirmation of ongoing model performance, stability, and risk behavior in production.

business risk / consequence and justification of severity and classification:
Failure to perform and report timely monitoring materially weakens model risk management and may allow performance degradation, control failures, or emerging fraud risks to remain undetected in a live environment. Given the extended period of live usage without monitoring evidence and the explicit breach of governance requirements, IMR has classified this issue as High severity, requiring immediate remediation to restore compliance, oversight, and operational risk control.


---
