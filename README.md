Here is the revised version with a more concise Business risk / Consequence section, aligned with the original image's length:


---

mri #01: lack of transparency in model score output cut-off to flag potentially fraudulent transactions and absence of acceptable false positive rate threshold

Severity: MEDIUM (Updated)

Description
The model generates risk scores ranging from 0 to 1000, where higher scores indicate higher fraud likelihood. However, there is no clearly defined score cut-off above which transactions are flagged for further investigation. This lack of transparency makes it difficult to assess whether the model effectively balances true positives (correctly flagged frauds) and false positives (legitimate transactions incorrectly flagged), leading to possible inefficiencies in investigation efforts.

Additionally, the acceptable false positive rate (FPR) threshold has not been specified. Without this, it remains unclear whether the chosen score cut-off aligns with business tolerance for false positives. This uncertainty may lead to misaligned risk handling and compromises model interpretability.

Business risk / Consequence and justification of severity and classification
Without a defined score threshold and FPR acceptance level, the model may inconsistently classify transactions, increasing either operational costs or fraud risk. This hinders efforts to ensure the model remains aligned with business goals. However, given the recent increase in Verified Detection Rate (VDR) and stable FPR, classification performance has improved, justifying a Medium severity classification due to reduced immediate impact but ongoing documentation gaps.

Tag(s)

Operational Error


Theme

Model Performance



---

Let me know if you want to apply this to any other MRIs or need a formatted version.

