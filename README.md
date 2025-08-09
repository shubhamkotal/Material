


The in-scope UK X-Brand First Party Fraud Unsecured NTB Application model (XXX) has been developed using a logistic regression methodology with a segmentation-based approach. In this design, the application data was first segmented into two categories — thin bureau file and thick bureau file — based on the depth of bureau information available. Separate models were then developed for each segment to better capture the unique characteristics of their respective populations.

During model development, the outputs from both segment-specific models were aggregated to evaluate overall portfolio-level performance across HSBC, FD, and MNS portfolios. In production (monitoring phase), when a new application is received, the system determines the bureau data type (thin or thick) and routes the application to the corresponding segment model. The model output for that segment is then generated, and all outputs across segments are combined to assess the overall model performance at the portfolio level.

This segmentation is therefore part of a single, integrated modelling framework, with the final combined output representing the performance of the overall model.

