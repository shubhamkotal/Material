MRI #02: Lack of transparency in model score output cut-off definition and probability-to-score conversion process. Severity: HIGH (New)

Description
The model produces risk scores ranging from 0 to 1000, where a higher score indicates a higher likelihood of fraudulent activity. However, the specific score threshold used to classify transactions as fraudulent or non-fraudulent has not been defined or documented. Additionally, the methodology employed to convert predicted probabilities into these risk scores is not disclosed.

The lack of a defined score cut-off is critical as it directly influences classification decisions—whether a transaction is flagged for further investigation or deemed non-risky. Without a transparent threshold, stakeholders cannot ascertain if the model optimally balances the trade-offs between false positives (incorrectly flagging legitimate transactions) and false negatives (missing actual fraudulent activities). This uncertainty can lead to inconsistent decision-making and may compromise the effectiveness of the model.

Moreover, without a documented probability-to-score conversion process, it is challenging to ensure that the score accurately reflects the underlying probability of fraud. This opacity can hinder the interpretability and reliability of the model, raising concerns over its consistency across different datasets or time periods.

The absence of these critical components makes it difficult to monitor and benchmark model performance effectively. It also undermines confidence in the model's predictive power and hinders its governance, making it difficult to explain or justify decisions made based on the model's output to stakeholders.

Business Risk / Consequence and Justification of Severity and Classification
Not providing a well-defined score cut-off and the conversion methodology introduces significant operational and financial risks. Without these elements, the model may either excessively flag legitimate transactions (increasing operational costs and customer dissatisfaction) or fail to identify actual fraud cases (leading to financial losses and reputational damage).

Furthermore, this lack of transparency can impede the ability to perform effective model governance, audit, and compliance activities. It complicates efforts to ensure that the model remains fair, unbiased, and aligned with business objectives over time.

Given these factors, the issue is classified with a Severity level of HIGH, as it has a substantial impact on the model's reliability, decision-making efficacy, and overall business performance.

