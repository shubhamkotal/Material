
Got it. Here's the revised version of the MRI issue without any mention of overfitting, while still focusing on the complexity, interpretability, and lack of clarity in the variable selection process:


---

mri #03: insufficiently parsimonious model and unclear variable selection process leading to unnecessary model complexity and reduced model transparency

Severity: MEDIUM (New)

Description
The current model is designed to classify real-time credit and debit card transactions into fraudulent and non-fraudulent categories and assign an appropriate risk score. It has been developed using a machine learning approach, with LightGBM chosen as the final model. As part of best practices in machine learning development, it is important to perform robust variable selection to ensure that only the most relevant and informative features are used in the model.

In this case, FLoD has used 85 features in the final model. As noted in Section 5 of the MDT, feature selection was embedded within the LightGBM modeling process rather than conducted as a separate, upfront step. This raises concerns regarding model parsimony—i.e., using the fewest number of variables necessary to meet predictive goals—as well as transparency and traceability of the modeling process.

Additionally, it remains unclear how variables were selected or eliminated during benchmarking with other models such as Random Forest and XGBoost. Since variable selection was not independently documented before model training, there is limited visibility into which features were retained across models, or whether important features were appropriately evaluated. The lack of a structured variable selection process weakens the overall interpretability and governance of the model.

The use of a high number of features (85) increases model complexity and may obscure the understanding of key drivers influencing model output. This also introduces challenges in maintaining the model in the future, as more variables require more effort to monitor, explain, and validate.

Business risk / Consequence and justification of severity and classification
A clear and structured variable selection process, along with model parsimony, is critical to ensure that models are interpretable, transparent, and maintainable. When the rationale behind variable inclusion is not clearly documented, it becomes difficult for business and validation teams to fully understand the model's logic and ensure its alignment with business expectations and regulatory standards.

That said, the current model has shown better performance compared to its previous version, with improved Value Detection Rate (VDR) and high recall observed in both development (71%) and out-of-time tests (82%). These results indicate strong detection capability and consistency.

However, despite this improved performance, the elevated number of features and absence of a dedicated variable selection phase introduce avoidable complexity and limit explainability. These gaps could affect long-term maintainability and model governance. Accordingly, IMR raises this as a medium severity MRI.

Tag(s)

No Tags applicable


Theme

Model Design and Assumptions



---

Let me know if you'd like this formatted into a Word or PDF document.

