MRI #XX: misalignment between development and monitoring performance windows
Severity: MEDIUM (New)

Description:
The model was developed using a six-month observation period and a two-month performance period to measure customer response and derive model lift, aligned with the stated objective of identifying target customers based on short-term response behaviour. However, during ongoing monitoring, performance is assessed using a three-month performance window, which is inconsistent with the development framework.
The longer monitoring performance window increases the likelihood of capturing additional responses, which may artificially inflate observed lift—particularly in the top deciles. As a result, monitored performance metrics (currently showing lift of ~13) are not directly comparable to development benchmarks, reducing confidence that reported performance reflects true model effectiveness rather than extended response capture.

Business risk / consequence and justification of severity:
This misalignment may lead to overstated model performance, delayed identification of genuine deterioration, and sub-optimal business decisions related to targeting and campaign effectiveness. While no immediate performance concerns have been observed, the inconsistency undermines governance discipline and the reliability of monitoring outcomes; therefore, the residual risk is assessed as Medium.

MRI #XX: absence of data representativeness validation and post-treatment assessment
Severity: MEDIUM (New)

Description:
The model documentation indicates that a sample of 12,700 eligible customers was used for training and development based on acceptable performance outcomes agreed with the business. However, no documented rationale or sampling methodology has been provided to demonstrate how this sample was selected or to confirm that it is representative of the overall eligible population.
In addition, following sample selection and data treatment, no evidence has been shared to confirm that representativeness was retained. No diagnostic checks, distributional comparisons, or assessments of potential bias or distortion in variable relationships have been provided to demonstrate that data preprocessing steps did not materially impact the underlying data structure.

Business risk / consequence and justification of severity:
The absence of representativeness validation and post-treatment diagnostics introduces a risk that the model may be exposed to hidden bias or instability when applied to the full population. However, given that the model demonstrated satisfactory performance during development and continues to show stable monitoring results (including a model lift of ~13), there is no immediate evidence of material adverse impact. The issue primarily represents a governance and assurance gap rather than an observed performance failure; therefore, the residual risk is assessed as Medium.
