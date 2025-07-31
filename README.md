mri #03: inconsistent performance metrics and lack of statistical evaluation in monitoring
severity: MEDIUM (New)
description
The monitoring approach lacks alignment and methodological rigor in two key areas:
a) Inconsistent performance metric usage: The model performance was primarily evaluated during the development phase using Recall and Precision. However, the Monitoring Test Execution & Reporting document states that model performance will be identified based on model accuracy evaluated by the feedback from the Quality Analyst from CCB. In the absence of comparable testing results between development and monitoring time frames, one cannot comment on how well the model is functioning when compared to development as a baseline.
b) Use of manual approach over statistical method: Monitoring evaluation relies on manual judgment by Quality Analysts rather than applying statistical metrics to assess performance. This introduces subjectivity and inconsistency, as model drift, stability, or degradation cannot be tracked in a quantifiable and repeatable manner. Without statistical rigor, early warning signals for performance deterioration or population shift may go unnoticed, increasing model risk exposure over time.
business risk / justification of severity and classification
Although the latest monitoring results have been found to be satisfactory and Recall performance has consistently exceeded 90% across products, the inconsistencies in metric selection and absence of statistical evaluation introduce interpretability and governance challenges. These issues reduce transparency in performance assessment and hinder the ability to validate ongoing model reliability under changing conditions. Given that the current model output is performing as expected, but these omissions weaken long-term monitoring robustness, the issue is classified as medium severity.


mri #03: missing impact assessment for feeder model used as input

severity: MEDIUM (New)
description

The Inscope model uses a feeder model (Google speech-to-text) to convert audio sales calls into transcripts, which are then used as input features. However, no assessment has been found regarding the feeder model's limitations, accuracy, or stability.

As per GMR Policy v5.0 section xx, “where feeder models are used, key limitations of feeder model and their impact on model output must be assessed.” The absence of such analysis limits visibility into how transcription errors may affect the Inscope model’s inputs and performance.

business risk / justification of severity and classification
Although the model currently shows Recall above 90% across all products and monitoring results are satisfactory, the lack of transparency around the feeder model’s quality introduces governance and input reliability concerns. Given this, the issue is classified as medium severity.
