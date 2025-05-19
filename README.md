
mri # 03 : no fpr acceptance level defined and no strategic upsampling explored to optimize value detection rate (vdr)

severity : medium (new)
description:
The current modeling approach lacks a defined False Positive Rate (FPR) acceptance threshold, and no structured upsampling of event observations has been explored. Despite downsampling non-events, the dataset remains imbalanced, with events continuing to represent a small fraction of the total population.

business risk / consequence and justification of severity and classification:
Without a defined FPR boundary, model threshold tuning lacks alignment with business risk tolerance, potentially limiting recall improvements. Additionally, the absence of event upsampling exploration may result in under-detection of valuable cases, leading to missed opportunities or inefficient targeting. This conservative setup restricts the model's ability to balance precision and recall based on business priorities.

Despite these limitations, the current model shows stable performance across in-sample, out-sample, and out-of-time validations with no significant misclassifications. Therefore, the issue poses no immediate operational risk but introduces potential long-term inefficiencies. The severity is classified as medium, reflecting the need for strategic consideration while acknowledging the model's present adequacy.
