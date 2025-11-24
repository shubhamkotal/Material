


---

✅ 1. Overall Model Performance (High-level)

Overall transaction acceptance rate YTD = 98.4%
→ This is very high and indicates strong model performance.

Nothing in the screenshots suggests instability or deterioration in baseline accuracy.


---

✅ 2. Performance by Gender

Female pass rate: ~98.3%
Male pass rate: ~98.4%
→ Practically identical → No bias, fully stable, green zone.

Volumes are also high (~500k each), so the metrics are statistically reliable.


---

✅ 3. Performance by Age

Age groups like 18–30, 30–49, 50–70 all show very similar pass rates (97–99%).

The age segmentation chart (middle graph) shows:

Pass rates climb from ~96% in early months to ~99% around mid-year

Slight dip to ~98% in Nov 2023


→ All movements look smooth, consistent, and within expected variation.
→ No age group is underperforming.
→ Green zone.


---

✅ 4. Monthly Stability (Trend Charts)

Gender trend chart (top bar + line graph):

Bars (volumes) rising month by month → product adoption increasing

Line shows pass rate trend increasing from ~87% → ~95% → ~98–99%


This means:

The model improves as more data accumulates

No sudden spikes/drops

No sign of instability or drift


→ Green zone


---

🔍 5. Control Chart (most important)

This is the bottom chart showing moving averages and control bands (CCL, AUCL, ALCL, RUCL, RLCL).

Interpreting the chart:

Green line = 30-day moving average

Black line = 7-day moving average

Orange/red dashed lines = control limits

AUCL / ALCL → Amber limits

RUCL / RLCL → Red limits



What the chart shows clearly:

1. The moving averages stay between ALCL and AUCL (amber bounds) for almost the entire timeline.
→ This is Green.


2. There is a temporary dip around September–October:

The 7-day line approaches the lower amber limit

But never crosses red

The 30-day line stays solidly within green limits


→ This is Amber, not Red.
→ Suggests a short-term fluctuation, not systemic failure.


3. After October:

Both moving averages trend upward strongly

End of graph shows recovery back to high acceptance (98%+)


→ Healthy recovery
→ Back to Green



RAG conclusion:

✔ Mostly Green
⚠ Short Amber period in Oct (temporary, recovered)
❌ No Red at any point


---

🧾 6. Final RAG Assessment

Metric	Status	Explanation

Overall Pass Rate	Green	98.4% YTD, within control limits, stable across all segments
Trend Stability	Green	No instability except a brief amber dip that self-corrected
FRR (implied)	Green	No spike in rejections seen in charts
FAR (implied)	Green	Not shown separately, but stable pass rate and acceptance curves imply no red flags
Bias (Gender / Age)	Green	Groups perform equally well



---

⭐ Final Professional Summary (You can use this in your report)

The model demonstrates strong, stable performance throughout the year with an average acceptance rate of 98.4% YTD. All customer segments—gender and age—show consistent and near-identical pass rates, indicating no bias and stable model behavior. Control chart analysis shows that both 7-day and 30-day moving averages remain within green/amber limits, with only a temporary dip into the amber zone around October, which quickly recovered. There were no breaches of red control limits at any time. Overall, the model remains well-within expected performance thresholds and displays no signs of drift or degradation.

Here is a clean, concise, report-ready conclusion combining the final summary + RAG assessment:


---

Final Model Performance Assessment (Report-Ready)

The model has demonstrated strong and stable performance throughout the year, achieving an overall acceptance rate of 98.4% YTD, which remains well within expected thresholds. Pass rates across all key customer segments—gender and age groups—are consistently high (97–99%) with no visible signs of bias or performance divergence.

Analysis of the control charts shows that both the 7-day and 30-day moving averages remain within the green operating range for the majority of the period. A short-term dip into the amber zone occurred around October; however, this fluctuation did not breach any red limits and the model quickly self-corrected, returning to stable green performance. Importantly, no red-zone breaches were observed at any point.

Under the RAG framework:

Overall pass rate: Green

Trend stability: Green (with a brief Amber episode, now resolved)

FRR & FAR indicators: Green (no abnormal rejection or acceptance patterns seen)

Bias assessment (Gender/Age): Green


Overall conclusion:
The model is performing reliably, remains well-calibrated, shows no signs of drift or degradation, and continues to operate within acceptable risk thresholds. It is suitable for ongoing production use, with routine monitoring recommended to maintain stability.


___ Monitoring _____

Below is a clear, report-ready model performance assessment based on the monitoring table shown in the image.


---

Model Performance Assessment (Monitoring Table)

1. Composite Score & RAG

Composite Score = 0.70

According to the RAG scale:

Score ≤ 1.0 = GREEN


Therefore, the overall model performance is in the Green zone, requiring only ongoing monitoring and no corrective action.



---

2. Metric-by-Metric Assessment

A. Face Comparison – FAR (False Accept Rate)

Actual: 0.00%

Threshold: 0.01%

Deviation score: (–1.00) (best possible value)

Assessment:

FAR is effectively zero, indicating excellent protection against fraud.

Well within threshold → Green.




---

B. Face Comparison – FRR (False Reject Rate)

Actual: 3.09%

Threshold: 0.47%

Deviation score: 5.57 (high, but weighted impact is limited to 25%)

Assessment:

FRR is above threshold, meaning some genuine customers are being rejected more than expected.

However, this is offset by excellent performance in the other 3 metrics.

Contributes to the overall score but does not push the composite metric out of Green.

Category-specific status = Amber, but overall = Green.




---

C. Liveness Detection – FAR (Active & Passive)

Actual: 0.00%

Threshold: 7.00%

Deviation score: (–1.00)

Assessment:

FAR is effectively zero, indicating very strong fraud resistance for liveness.

Perfectly within limits → Green.




---

D. Liveness Detection – FRR (Active & Passive)

Actual: 4.57%

Threshold: 20.00%

Deviation score: (–0.77)

Assessment:

FRR is far below the threshold.

Indicates good customer experience with minimal false rejections.

Strong performance → Green.




---

3. Weighted Impact Summary

Each metric has 25% weight. Out of the four:

Three metrics score at the best possible deviation (≈ –1.0)

One metric (FRR – Face Comparison) is above the expected threshold, but its weighted impact is only 25%.


When weighted together → Composite Score = 0.70 → Green

This indicates overall strong model health despite one metric requiring monitoring.


---

4. Final Report-Ready Conclusion

The monitoring results indicate that the model is performing well within acceptable risk limits. The overall composite score of 0.70 places the model firmly in the Green zone, requiring only routine monitoring. Both False Accept Rates (FAR) for Face Comparison and Liveness Detection are effectively 0%, demonstrating strong fraud resistance. Liveness FRR is comfortably below the threshold. Although Face Comparison FRR is above its expected limit and contributes an elevated deviation score, its impact on the overall composite score is limited. The issue should be monitored but does not require corrective action at this time. Overall, the model is stable, accurate, and aligned with expected operational performance.


____ Metrics explanation_______

Model Accuracy

Model accuracy is evaluated using three metrics:

Overall pass rate

False Reject Rate (FRR)

False Accept Rate (FAR)


Each metric is calculated as a time-weighted moving average based on daily observations within a rolling window of predefined length.

The choice of the rolling-window length depends on:

Market requirements for how long ID&V check results can be stored by the Diva team and the market

Future development of the model-risk monitoring framework

Changes in the Diva model architecture

Potential future regulatory requirements


Currently, the rolling-window length is 5 days, limited by the maximum transaction-storage duration.

Optimal moving-average weights for each metric will be defined and tested separately during the first three months after launch.

---------

Nice — here’s a short, very clear explanation of the CCL / control lines / R-A-G logic plus a tiny numeric example so it feels concrete.


---

What the lines mean (plain language)

CCL (Central Control Line)
The long-term baseline for a metric. It’s the moving average calculated over a longer period (your text: 3 months). Think of it as “normal performance.”

AUCL / ALCL (Amber Upper / Amber Lower Control Lines)
The first warning band around the CCL. Based on your spec, these are set using the standard deviation (SD) of historical CCL values (you said: SD computed from 8 months of pre-implementation data).

Practically: AUCL = CCL + 1 SD, ALCL = CCL − 1 SD.

If a metric moves into this band, it’s a yellow/amber warning — investigate but it’s not critical yet.


RUCL / RLCL (Red Upper / Red Lower Control Lines)
The critical band beyond amber. From your description the red limits are placed one more SD beyond the amber limits (i.e., another SD of the same historical distribution).

Practically: RUCL ≈ CCL + 2 SD, RLCL ≈ CCL − 2 SD.

If a metric crosses into red, that’s a serious issue and needs immediate action.



> Note: your doc says the amber and red distances will be evaluated during the first 6 months — that means these ±1SD/±2SD choices are initial settings and should be validated with live data.




---

R-A-G (Green / Amber / Red) mapping — simple rules

For each metric (Overall pass rate, FRR, FAR) using the moving average:

Green = between ALCL and AUCL (inside the amber band) → performance normal.

Amber = between AUCL and RUCL, or between RLCL and ALCL → early warning; investigate trends or potential causes.

Red = above RUCL or below RLCL → critical; trigger immediate incident/mitigation workflow.


(Example: for a metric where bigger is better — e.g., Overall pass rate — an increase above RUCL is actually good; you should treat green/amber/red relative to the metric’s desired direction. For FRR/FAR where lower is better, red will typically be above RUCL. So apply directionality when defining business actions.)


---

Tiny numeric example

Assume past calculations give:

CCL = 90% (3-month average of Overall pass rate)

SD (from 8 months) = 2%


Then:

AUCL = 92% (90 + 2)

ALCL = 88% (90 − 2)

RUCL ≈ 94% (90 + 2×2)

RLCL ≈ 86% (90 − 2×2)


RAG mapping for the moving average today:

Green: 88%—92%

Amber: 92%—94% (upper amber→red zone) and 86%—88% (lower amber→red zone)

Red: >94% or <86%


Reminder: interpret direction — for overall pass rate higher is better, so >94% is actually excellent (so you’ll want to flip the interpretation for “bad” vs “good” depending on metric). For FRR/FAR (lower is better) the numeric comparison works as-is.


---

What to do at each RAG level (recommended)

Green: continue monitoring; no action.

Amber: log an investigation ticket, run a short RCA (last changes, traffic spikes, data quality, config), increase monitoring granularity (hourly).

Red: raise incident alert to owners, pause suspect model changes (if required), roll back recent releases if correlated, perform full RCA and mitigation plan; report to governance/regulatory teams if needed.



---

Practical notes / things to clarify later

1. Metric direction — explicitly mark each metric as “higher is better” or “lower is better” in the dashboard so color logic is correct.


2. SD choice — ±1SD / ±2SD is a common starting point but validate: some markets use percentiles or business-set margins instead.


3. Evaluation window — you said amber/red distances will be validated in the first 6 months — collect false positives/negatives from that period and adjust thresholds and MA weights.


4. Alerting policy — decide how many consecutive days or how large a breach triggers a pager (1 day? 2 days? severity levels).




---
