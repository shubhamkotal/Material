

mri #04: absence of defined fraud volume threshold and undefined baseline selection criteria in monitoring
severity: MEDIUM (New)

description
The monitoring approach has notable documentation and methodological gaps in two areas:

a) No defined fraud volume threshold for monitoring: During the Q2 2024 monitoring for the Europe use case, model strength was concluded as acceptable despite no fraud cases being observed, meaning statistical strength tests (e.g., GINI) could not be conducted. However, the Model Technical Document (MTD) does not specify the minimum number of fraud cases required for statistical monitoring to be considered reliable, nor does it outline when expert judgment should be used instead. This lack of threshold definition can lead to inconsistent decisions, reduced comparability over time, and ambiguity in interpreting monitoring outcomes.

b) Undefined baseline selection criteria for monitoring metric comparison: The Model Technical Document (MTD) shows monitoring results compared between Q1 2024 and Q2 2024, using the prior monitoring period as the baseline for calculating percentage changes. However, there is no documented rationale for why the most recent monitoring period was chosen instead of the development phase metrics, which typically provide the original performance benchmark. The absence of this explanation weakens transparency, may misrepresent performance trends, and limits the ability to detect longer-term degradation relative to the model’s intended baseline.

business risk / justification of severity and classification
Without a defined fraud volume threshold, there is a risk of drawing misleading conclusions from incomplete or statistically unreliable monitoring results. Similarly, without clear baseline selection criteria, performance comparisons may lack consistency and could obscure early signs of performance deterioration. However, during development, the model showed strong and consistent performance with GINI scores of 81% (out-of-sample), 84% (out-of-time pre-COVID), and 77% (out-of-time COVID), along with an ~18% uplift over the previous model. In the latest monitoring, the UK use case recorded a PSI of 0.03% and GINI of 67%, while the Europe use case had a PSI of 1.70% but no GINI due to zero fraud volume, which also indicates lower fraud risk. Given the stable monitoring results, strong historical performance, and low current fraud rates, the issue is classified as medium severity with no immediate business impact.

