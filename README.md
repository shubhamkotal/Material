
MRI #XX: missing training-time performance and cross-validation results from model development phase
Severity: MEDIUM (Vendor)

Description:
The model development documentation lacks essential transparency on two key aspects: training-time performance metrics and k-fold cross-validation results. Only test-phase metrics (e.g., AUROC, recall) have been shared, with no details on how the model performed during training or across multiple validation splits. This restricts the ability to assess the bias-variance trade-off—a fundamental step in evaluating whether the model is underfitting, overfitting, or generalizing appropriately. Additionally, without k-fold cross-validation metrics, it is not possible to determine model performance consistency across different data partitions. These omissions reduce confidence in the robustness and stability of the model.

Business Risk / Consequence and Justification of Severity and Classification:
While the current model demonstrates acceptable performance—particularly with MAL classification rates exceeding the 50% benchmark—the missing development-phase insights hinder a complete and defensible validation process. The absence of training-time results and cross-validation evidence introduces uncertainty in the model’s generalizability and audit readiness. Since core business performance metrics are currently met, the observation is classified as medium severity.

a) Missing rationale for chosen MAL (Manual Authorised Losses) threshold
The documentation does not clearly state the rationale or business logic behind the threshold used to classify transactions as MAL or Non-MAL. Without this explanation, it is unclear whether the threshold aligns with HSBC’s risk appetite or operational guidelines.

b) Missing documentation of Fraud team's manual inspection capacity
There is no documented evidence outlining the maximum number or volume of transactions the Fraud team can manually review. This creates ambiguity in evaluating whether the model’s output volume is operationally manageable or exceeds human review capacity.

c) Missing specification of FPR (False Positive Rate) thresholds
The expected or acceptable False Positive Rate (FPR) threshold has not been documented. Absence of this benchmark prevents proper assessment of model performance and its alignment with business tolerances for false alerts.
