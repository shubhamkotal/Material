


mri #05: stress testing and limited data representativeness in model development. severity: medium (new)

description
The model has not been stress-tested to evaluate performance under critical situations, such as a sudden increase in fraud rates similar to what was observed during the COVID-19 period. Without this testing, it remains uncertain whether the model can maintain stability and accuracy when exposed to sharp changes in fraud patterns.

Additionally, only six months of data has been used for model development. This limited sample may not fully capture average fraud trends and could reflect either below-average or atypical event rates. Such a restricted window increases the risk of biased learning, potentially leading to reduced adaptability when fraud behavior deviates from the training period.

business risk / consequence and justification of severity and classification
If the model is not stress-tested and is trained on a potentially non-representative sample, its reliability under sudden fraud surges may be compromised. This could result in delayed detection, higher false negatives, and an inability to promptly adapt to changing fraud tactics—ultimately exposing the business to increased financial losses and reputational risks during critical periods.

However, the model currently shows improved validation performance, with higher VDR compared to the older model and an AUC of 96%, indicating strong classification capability under normal conditions. For this reason, the severity is classified as medium, acknowledging the model’s solid baseline performance but also highlighting the need for stress testing and broader data representativeness to ensure resilience in future critical scenarios.


