MRI #03: Documentation inconsistency and unclear model design explanation. Severity: HIGH (New)

Description
The document describes a test-control methodology for the model, but the explanation is unclear and lacks sufficient detail. Specifically, the section states:

"For the test-control of the model we will take some random clients (1% of each decile) and we renamed the Label to a New Label. The idea is to seed clients in the deciles 1-5. First, we convert the clients that are L to be clients H and M. Then we convert the clients that are M to be clients H, and finally the clients that are H we convert to be clients M. With this we can mitigate that the model becomes dependent on the campaigns and when it needs to be remodeled we can do it without the campaign effect."

However, the logic behind these label conversions is not well explained, making it difficult to understand how the test-control process works and why these specific transformations are applied. It is unclear how this seeding strategy mitigates model dependence on campaigns or ensures unbiased retraining. Additionally, the methodology for selecting and modifying labels is not fully documented, raising concerns about consistency and reproducibility.

Business Risk / Consequence and Justification of Severity and Classification
Unclear documentation on model design can lead to misinterpretations, inconsistencies in implementation, and challenges in validating model performance. If stakeholders do not understand how the test-control process is structured, they may struggle to assess its effectiveness or make necessary adjustments. Furthermore, lack of transparency can hinder governance, compliance, and future model retraining efforts.

Given the potential impact on model reliability and decision-making, this issue is classified as HIGH severity. Clear, well-documented methodologies are essential to ensuring the integrity and effectiveness of the model.

