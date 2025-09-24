
mri #XX: sample distribution not aligned with population
severity: medium (vendor)
description:
The current sample distribution deviates from the true population due to the use of random sampling. Specifically, the 19–30 age group is overrepresented, while the 46–60 age group is underrepresented. This imbalance results in a non-representative sample, which may bias the model’s learning process. Consequently, the model could underrepresent patterns associated with older customers and overemphasize those from younger groups. Such skewness limits the ability to ensure fair and balanced customer targeting for life insurance marketing.
business risk / consequence and justification of severity and classification:
The imbalance in age-group representation introduces the risk of overlooking potential customers in the under-sampled segment and over-prioritizing the over-sampled segment. This may lead to ineffective marketing strategies, missed opportunities in high-value customer groups, and suboptimal allocation of resources. However, since the model’s current performance indicators (AUC, GINI, and KS) remain stable across train and test, the issue is classified as medium severity.

--

mri #XX: model design and variable selection assumptions may impact stability
severity: medium (vendor)

description:
During model development, variable selection was embedded within the LightGBM (boosting) modeling process to reduce the variable set from 474 to 30. The final model, however, was built using Random Forest (bagging). Boosting and bagging handle bias–variance trade-offs differently: LightGBM tends to aggressively reduce bias while Random Forest reduces variance through averaging. As a result, the variables selected via LightGBM may not optimally capture the patterns required for Random Forest.

This design assumption contributed to observed overfitting: with 30, 20, or 15 variables, training Gini remained high while test Gini showed limited improvement. Reducing the set further to 12 variables lowered training Gini while test Gini remained similar, suggesting that the apparent mitigation of overfitting was achieved by trimming predictive power rather than selecting the most suitable features for Random Forest. Out-of-time testing showed a 10% KS drop compared to test-phase results, indicating potential instability in real-world deployment.

Because feature selection was embedded within the GBM process rather than performed as a separate, model-agnostic step, there is limited assurance that the model design accounts for Random Forest’s variance handling characteristics. A more robust approach would involve independent, non-embedded variable selection techniques to ensure the model uses truly informative features while maintaining stable performance across algorithms and deployment scenarios.

business risk / consequence and justification of severity and classification:
The methodological mismatch in model design increases the risk of excluding variables that are genuinely important for Random Forest, potentially leading to unstable performance in out-of-time or live data. Such instability may affect accurate targeting of customers for life insurance marketing campaigns. The 10% KS decline in out-of-time testing underscores this risk. Nevertheless, since core metrics (AUC, GINI, KS) remain acceptable during development testing, this issue is classified as medium severity.

----

mri #XX: recent monitoring results not provided
severity: medium (vendor)

description:
The model went live and monitoring results are available for September 2024, October 2024, and December 2024. While the model has shown satisfactory performance during these periods, with only a minor KS breach observed in October 2024 that was corrected by December 2024, recent monitoring results beyond December 2024 have not been provided. This gap makes it difficult to evaluate the current status of the model and to identify any potential consecutive breaches or performance drifts.

Although the model is monitored quarterly—exceeding the minimum framework requirement of annual monitoring—without the latest results, it is unclear how the model is performing at present. Robust and timely monitoring is critical to ensure ongoing model effectiveness and to promptly identify any operational issues.

business risk / consequence and justification of severity and classification:
The absence of current monitoring results introduces uncertainty regarding the model’s present performance and the detection of potential breaches. While past results indicate that the model is performing satisfactorily, the lack of recent data limits the ability to assess real-time stability and operational readiness. Since the model exceeds the minimum monitoring frequency required by the framework (quarterly vs. annual) and available results show stable performance, this observation is classified as medium severity.
