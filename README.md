
mri #XX: sample distribution and data quality gaps
severity: medium (vendor)

description:
The current sample distribution deviates from the true population due to the use of random sampling. Specifically, the 19–30 age group is overrepresented, while the 46–60 age group is underrepresented. This imbalance results in a non-representative sample, which may bias the model’s learning process. Consequently, the model could underrepresent patterns associated with older customers and overemphasize those from younger groups. In addition, no detailed data quality checks have been documented—duplicate removal, outlier detection/correction, missing value treatment (potential systemic bias), and multi-collinearity assessment were not confirmed. These omissions reduce transparency and limit assurance on the robustness of the dataset used for modeling.

business risk / consequence and justification of severity and classification:
The imbalance in age-group representation introduces the risk of overlooking potential customers in the under-sampled segment and over-prioritizing the over-sampled segment. This may lead to ineffective marketing strategies, missed opportunities in high-value customer groups, and suboptimal allocation of resources. The absence of clear data quality checks further raises the risk of biased or unstable model outcomes. However, since the model’s current performance indicators (AUC, GINI, and KS) remain stable across train and test, the issue is classified as medium severity.
