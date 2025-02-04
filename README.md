MRI #03: Limited Assurance on Dataset Used for Model Development and Overfitting Concerns
Severity: HIGH (New)

Description

The dataset used for model development consists of 0.5 million genuine sessions and only the last six months of fraud cases. However, the data collection process itself is imperfect, leading to a small and imbalanced dataset of fraud versus genuine sessions. Additionally, there is no documented sampling methodology to address this imbalance—no oversampling of fraud cases or undersampling of genuine cases—raising concerns about the model's ability to generalize effectively.

Another key issue is the lack of validation on data similarity between the vendor's dataset and HSBC’s dataset. Without this comparison, it is unclear whether the vendor’s model will perform well on HSBC’s actual data. Additionally, the data used for model training has not been verified to ensure it represents the real-world distribution of transactions, which can significantly impact the model's effectiveness in production.

During cross-validation, five different test datasets were used, and the model's true positive rate varied widely from 47% to 86%. This suggests that the XGBoost model is overfitting—it has learned patterns specific to the training data but fails to generalize across different test datasets. The limited dataset used for modeling may not capture the full spectrum of fraud scenarios, leading to poor performance when deployed in real-world settings.

Business Risk / Consequence and Justification of Severity and Classification

The absence of proper sampling methods and validation checks introduces significant risks:

Model unreliability: The trained model may fail to detect fraud effectively due to an incomplete representation of real-world fraud cases, increasing false negatives and financial losses.

Operational inefficiencies: Without a balanced dataset, the model may produce high false positives, leading to unnecessary investigations, increased operational costs, and customer dissatisfaction.

Regulatory and governance risks: Lack of data validation and justification for data representativeness raises concerns over model fairness, bias, and compliance with governance standards.

Overfitting issues: The high variability in performance across different test datasets (47% to 86%) indicates that the model does not generalize well, making its predictions unreliable in production.


Given these factors, the issue is classified as HIGH severity, as it directly affects the model’s performance, decision-making reliability, and governance compliance. Addressing these gaps is critical to ensuring the model remains effective, fair, and aligned with business objectives.

