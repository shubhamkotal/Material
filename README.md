mri #XX: missing implementation report from fiserv platform limits confidence in model readiness before go-live

Severity: HIGH (Proposed)

Description
The Zelle model, which is used to detect fraud, is hosted on the Fiserv network. All HSBC transactions for this payment type will be processed through the Fiserv network, and the model’s monitoring will also be done from that platform. Since the model will not run within HSBC’s internal systems, it is important for HSBC to receive an implementation report directly from the Fiserv platform.

This report is needed to confirm that the model has been properly set up in the live network, that it is running as expected, and that it produces correct and stable outputs when processing HSBC transactions. Without this report, HSBC has no visibility into whether the model is behaving as designed once deployed on the Fiserv side.

Even though some performance results may have been shared earlier, those do not replace the need for a proper implementation report from the actual environment where the model will operate in real-time.

Business risk / Consequence and justification of severity and classification
If the implementation report is not provided, HSBC will not be able to confirm whether the Zelle model is working correctly within the Fiserv platform. This creates a serious risk, as any technical issues, misfiring logic, or incorrect outputs may only be detected after go-live. For a fraud model, this could lead to missed fraud cases, false alerts, financial losses, or operational delays.

Since HSBC has no direct control or visibility into the Fiserv system, the implementation report becomes the only way to confirm model readiness before deployment. For this reason, IMR is raising a high severity MRI to highlight the importance of receiving this report before the model is approved for production use.
