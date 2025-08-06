


mri #06: model built on outdated data without incorporating recent fraud trends
severity: MEDIUM (New)

description
The current model was developed using data from March 2021 to September 2022 and validated on the period from October 2022 to January 2023. However, the model was implemented in 2025, and no data beyond January 2023 was used during development. This creates a potential risk that newer fraud patterns emerging post-2023 are not captured by the model.

The development data was limited due to business constraints around live data search costs. Only historical data from a single credit bureau was used, avoiding additional costs from pulling newer data.

While this rationale is operationally valid, no supporting analysis has been provided to show whether the development data is representative of the more recent population. A comparison of non-bureau features between development and recent data could have helped confirm whether the model remains effective in identifying current fraud patterns.

It is noted that out-of-turn testing was conducted on older periods, such as March 2019 to February 2020 (pre-COVID) and March 2020 to February 2021 (COVID phase), to ensure the model captures different fraud dynamics like first-party fraud and pandemic-related spikes. However, these back-dated validations do not substitute for assessing whether fraud typologies that emerged after 2023 have also been captured. There remains a risk that newer fraud trends may go undetected by the model in upcoming quarters.

business risk / consequence and justification of severity and classification
The exclusion of recent data limits the model’s adaptability to evolving fraud trends. However, the model demonstrates improved GINI scores over prior versions and maintains consistent performance across out-of-sample and out-of-time datasets. This consistency reduces the likelihood of immediate degradation, justifying a medium severity classification.

