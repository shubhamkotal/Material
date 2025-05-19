
Understood. Here's the expanded version of the description, adding more detail while keeping the tone and structure aligned with your previous MRIs:


---

mri # 03 : no fpr acceptance level defined and no strategic upsampling explored to optimize value detection rate (vdr)

severity : medium (new)
description:
The current modeling approach does not include a defined False Positive Rate (FPR) acceptance threshold, nor has FPR been evaluated during the model performance review. The assessment has been primarily focused on precision, without a holistic view of how the model behaves in terms of incorrectly flagged non-events. This limited metric perspective restricts the understanding of the model’s trade-off between correctly identifying events (recall) and avoiding false positives (FPR).

In addition, although some balancing was attempted by downsampling non-event observations, the resulting dataset still remains imbalanced, with events constituting a small share (e.g., ~5%). No exploration has been conducted to understand how different levels of event representation could influence the model’s ability to detect more true events. The absence of any strategy to explore the impact of upsampling further constrains the model’s optimization potential and fails to examine if a better balance between recall and FPR could be achieved under different data conditions.

business risk / consequence and justification of severity and classification:
Without evaluating FPR or defining its acceptable threshold, the model cannot be tuned to meet business-aligned tolerance for false positives, potentially missing the opportunity to improve recall and VDR. Over-reliance on precision as the primary performance metric may lead to conservative models that underperform in detecting true events. Furthermore, by not exploring how changes in event representation might affect detection capability, the model design process omits a critical lever for performance enhancement.

That said, the current model demonstrates consistent and satisfactory results across in-sample, out-sample, and out-of-time validations, with no significant misclassifications observed. Hence, while the issue introduces strategic limitations and potential long-term inefficiencies, it does not pose an immediate risk. The severity is therefore classified as medium to reflect the need for broader evaluation and alignment with business detection goals.


---

Let me know if you'd like help drafting the action plan or recommendation next.

