
MRI #03: Lack of Exploration of Alternative Modeling Techniques and Absence of Benchmark Testing. Severity: HIGH (New)

Description
The current fraud detection model relies solely on logistic regression, without exploring alternative machine learning techniques such as XGBoost or Random Forest. These ensemble methods often capture complex patterns in data more effectively than traditional regression models, potentially improving fraud detection accuracy. However, no benchmark testing was conducted to assess whether logistic regression is the most suitable approach.

The model owner cited limitations in SAS Enterprise Guide (EG) as the reason for not exploring other techniques. However, SAS Viya or Enterprise Miner could have been integrated to facilitate the use of advanced machine learning models. The failure to explore these options raises concerns about whether the best possible model was chosen.

Without benchmarking against other techniques, it is unclear whether logistic regression provides an optimal balance between precision and recall. A more sophisticated model might have reduced false positives (minimizing unnecessary investigations) or false negatives (reducing missed fraud cases). The absence of comparative testing limits confidence in the model’s predictive power and may result in suboptimal fraud detection.

Business Risk / Consequence and Justification of Severity and Classification
Relying on a single modeling approach without benchmarking poses significant business risks. If logistic regression is not the best-performing model, the organization may face financial losses due to undetected fraudulent transactions or increased operational costs due to excessive false positives.

Additionally, the lack of exploration limits the model’s adaptability to evolving fraud patterns. Over time, fraud tactics become more sophisticated, and more advanced models may be necessary to keep up. Without alternative techniques, the model may become outdated more quickly, reducing its long-term effectiveness.

This issue is classified with a Severity level of HIGH, as it directly impacts model performance, business efficiency, and fraud mitigation effectiveness. Transparent benchmarking and a broader exploration of machine learning techniques are critical for ensuring that the best possible model is in use.

MRI #04: Lack of Sample Representativeness and Event Rate Adjustment in Model Development. Severity: HIGH (New)

Description
No validation has been performed to ensure that the sample used for modeling accurately represents the overall population, particularly the in-scope bank portfolio distribution. Without this verification, the model’s predictions may not generalize well, leading to biased outcomes and reduced reliability in event detection.

Additionally, the event rate in the sample is less than 1%, meaning event occurrences are highly underrepresented. Despite this, no resampling techniques such as oversampling events or undersampling non-events were explored. An imbalanced dataset can cause the model to be skewed toward the majority class, increasing the likelihood of missing actual events and reducing overall model effectiveness.

Business Risk / Consequence and Justification of Severity and Classification
A non-representative sample and unadjusted event rate can significantly impact model performance. If the training data does not reflect the true population distribution, the model may struggle to detect relevant events accurately, leading to missed opportunities or incorrect classifications. This, in turn, can reduce confidence in model-driven decisions and hinder operational efficiency.

Given these risks, the issue is classified with a Severity level of HIGH, as it directly affects the model’s predictive accuracy, consistency, and ability to deliver meaningful insights. Ensuring a representative dataset and addressing class imbalance are critical for building a reliable and actionable model.

