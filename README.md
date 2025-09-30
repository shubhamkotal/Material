
mri #09: (a) missing framework for handling differences between development and monitoring metrics; (b) lack of clarity on sensitivity testing approach
severity: MEDIUM (New)

description
The monitoring framework does not contain a defined section on how to manage situations where monitoring metrics differ from those applied during development, nor does it provide justification for such differences. This creates ambiguity in ensuring that performance evaluation remains consistent with original benchmarks. In addition, there is a lack of clarity on how sensitivity testing will be conducted, particularly regarding the role of PSI/CA in assessing model robustness under data shifts.

business risk / consequence and justification of severity and classification
The absence of a framework for handling differences in metrics reduces transparency and risks undermining comparability of model performance over time. Similarly, the lack of a clear sensitivity testing methodology introduces uncertainty in evaluating the model’s resilience to variations in input data. These gaps weaken the overall monitoring framework and may delay detection of emerging issues, though existing stability and strength checks provide partial mitigation. Therefore, the issue is classified as medium severity.
