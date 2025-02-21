
MRI #03: Lack of Exploration of Alternative Modeling Techniques and Absence of Benchmark Testing. Severity: HIGH (New)

Description
The current fraud detection model relies solely on logistic regression, without exploring alternative machine learning techniques such as XGBoost or Random Forest. These ensemble methods often capture complex patterns in data more effectively than traditional regression models, potentially improving fraud detection accuracy. However, no benchmark testing was conducted to assess whether logistic regression is the most suitable approach.

The model owner cited limitations in SAS Enterprise Guide (EG) as the reason for not exploring other techniques. However, SAS Viya or Enterprise Miner could have been integrated to facilitate the use of advanced machine learning models. The failure to explore these options raises concerns about whether the best possible model was chosen.

Without benchmarking against other techniques, it is unclear whether logistic regression provides an optimal balance between precision and recall. A more sophisticated model might have reduced false positives (minimizing unnecessary investigations) or false negatives (reducing missed fraud cases). The absence of comparative testing limits confidence in the model’s predictive power and may result in suboptimal fraud detection.

Business Risk / Consequence and Justification of Severity and Classification
Relying on a single modeling approach without benchmarking poses significant business risks. If logistic regression is not the best-performing model, the organization may face financial losses due to undetected fraudulent transactions or increased operational costs due to excessive false positives.

Additionally, the lack of exploration limits the model’s adaptability to evolving fraud patterns. Over time, fraud tactics become more sophisticated, and more advanced models may be necessary to keep up. Without alternative techniques, the model may become outdated more quickly, reducing its long-term effectiveness.

This issue is classified with a Severity level of HIGH, as it directly impacts model performance, business efficiency, and fraud mitigation effectiveness. Transparent benchmarking and a broader exploration of machine learning techniques are critical for ensuring that the best possible model is in use.

MRI #04: Lack of Validation to Ensure Sample Representativeness. Severity: HIGH (New)

Description
No tests have been conducted to confirm that the sample used for model development accurately represents the overall population, specifically the in-scope bank portfolio distribution. Ensuring that the modeling sample aligns with the broader population is critical, as an unrepresentative sample can lead to biased predictions and reduced model reliability.

Without proper validation, the model may be overfitted to certain segments while underrepresenting others, leading to skewed risk assessments. This can result in an increased rate of false positives or false negatives, negatively impacting fraud detection effectiveness and operational efficiency.

Business Risk / Consequence and Justification of Severity and Classification
If the sample does not reflect the full distribution of bank portfolios, the model’s predictions may not generalize well, leading to poor performance in real-world scenarios. This could result in financial losses due to undetected fraud or unnecessary investigations on legitimate transactions.

Furthermore, the absence of sample validation raises concerns about model fairness and regulatory compliance, as certain customer segments may be disproportionately affected. Given these risks, the issue is classified with a Severity level of HIGH, as it directly impacts the model’s accuracy, fairness, and business credibility.

