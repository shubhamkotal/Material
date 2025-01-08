This text explains how a survey was created to help managers evaluate their employees' performance and behavior, ensuring they align with HSBC's core values. Here's the simplified version:

1. **Purpose of the Survey**:  
   Managers were asked to rate their employees based on their performance and alignment with HSBC's values.

2. **Process to Create the Survey**:  
   - The team (HSBC and SHL) used existing traits and behaviors from an assessment tool (called OPQ scales) and matched them with HSBC’s values.  
   - Based on this, they developed specific survey questions that reflect those values.  

3. **Considerations**:  
   - The survey was designed to be practical (not too long but detailed enough for analysis).  
   - Efforts were made to ensure participants clearly understood the questions and rated employees consistently.

4. **Outcome**:  
   A final version of the survey was created and attached in the appendix for reference.

   Here’s a simplified explanation broken down step by step for clarity:

---

### **Purpose of the Study**
- The goal is to check if **OPQ (Occupational Personality Questionnaire) traits** and **manager ratings** are related.
- This helps validate whether OPQ is useful for assessing people's alignment with desired values (like HSBC's).

---

### **Step 1: Start with Pearson Correlations**
- First, we calculate the **Pearson correlation** to see how strongly **OPQ traits** and **manager ratings** are related.
- Pearson correlation gives two things:
  1. **Direction** (positive or negative relationship).
  2. **Strength** (how strong the relationship is).

---

### **Step 2: Correct Correlations for Issues**
Validation studies face **two challenges**:  
1. **Unreliable manager ratings**  
   - Manager ratings can be subjective or inconsistent.  
   - To correct this, we assume a reliability score (e.g., 0.6) for the manager ratings and adjust the correlations using a formula.  
   - This gives a better estimate of the "true" relationship.  

2. **Restricted range of OPQ scores**  
   - In real applications, OPQ scores are spread out, but in this study, the range is limited.  
   - To fix this, we assume a broader range (e.g., 0.8 standard deviation) and adjust the correlations accordingly.  
   - After these corrections, correlations typically become stronger.

---

### **Step 3: Run a Regression Analysis**
- Next, we use **linear regression** to predict the **manager rating composite score** (dependent variable) using OPQ scores (independent variables).  
- Process:
  1. Include all OPQ attributes that are statistically related to manager ratings.  
  2. Refine the regression model by testing combinations of OPQ traits to find the best predictor.  
  3. The final output is a new score called the **Entity Level Control (ELC) score**, which predicts manager ratings while aligning with the company’s values (e.g., HSBC).

---

### **Step 4: Test the ELC Score**
- To confirm the ELC score is valid:
  1. **Compare it with manager ratings:** Check the correlation between ELC and manager ratings to ensure they align.
  2. **Test by levels and regions:**  
     - Group employees into senior levels (1-3) and junior levels (7-8).  
     - Run the test separately for each group and region to check consistency.  
     - Exclude regions with too few samples (like the Middle East with only 50 cases).

---

### **Step 5: Cross-Validation**
- To ensure the model works on different samples:
  1. Split the data into two random groups (50% each).  
  2. Use the first group to build the regression model and create a weighted ELC score.  
  3. Test if the weighted ELC score works consistently on both groups (Sample 1 and Sample 2).  

---

### **Key Takeaways**
- **Correcting correlations:** Fixes data issues (unreliable ratings, restricted score range).  
- **Regression model:** Builds a new ELC score using OPQ traits to predict manager ratings.  
- **Validation tests:** Confirms the ELC score is reliable across different levels, regions, and samples.  

---

Let me know if you want me to simplify it further!


Let me simplify this for you in **short and easy steps** with an example.

---

## **1. What is Happening Here?**  
This process calculates a **fraud score** for transactions. It uses:  
- Fraud **probability** (likelihood of fraud)  
- **Expected fraud amount** (amount of money at risk)  

The **decision boundary** and **diagonal length** help determine how "fraudulent" a transaction is.

---

## **2. Key Concept – Decision Boundary**  
Imagine a graph:  
- X-axis: **Expected Fraud Amount**  
- Y-axis: **Fraud Probability**  

Each **boundary** (e.g., 99%, 75%, 50%) is like a line that separates "safe" transactions from "fraudulent" ones.  
- Transactions **above the line** are more likely to be fraud.  
- The **diagonal** is a line from the origin (0,0) to a point on the boundary.  

---

## **3. Simple Steps to Calculate Fraud Score**  

### **Step 1: Find the Fraud Probability and Amount**  
Example:  
- Fraud Probability = **0.8** (80%)  
- Expected Fraud Amount = **4000**

### **Step 2: Calculate the Diagonal Length**  
The diagonal length is the distance from (0,0) to the transaction point:  
\[
\text{Diagonal Length} = \sqrt{(Probability^2 + Amount^2)}
\]  
Here:  
\[
\text{Diagonal Length} = \sqrt{(0.8)^2 + (4000)^2} \approx 4000.8
\]

### **Step 3: Normalize the Diagonal Length**  
- Normalize it by dividing by the **99th percentile diagonal length** (say it’s 5000):  
\[
\text{Normalized Length} = \frac{\text{Diagonal Length}}{\text{Diagonal Length at 99th Percentile}}
\]  
Here:  
\[
\text{Normalized Length} = \frac{4000.8}{5000} = 0.8
\]

### **Step 4: Apply the Transformation Function**  
Use the formula to calculate the fraud score:  
\[
\text{Fraud Score} = 1000 \times \frac{\exp(\text{Norm Length}) - 1}{\exp(\text{Norm Length}) + 1}
\]  

Substitute **Normalized Length = 0.8**:  
\[
\text{Fraud Score} = 1000 \times \frac{\exp(0.8) - 1}{\exp(0.8) + 1} 
\]  

After calculation:  
- Fraud Score ≈ **468**  

---

## **4. What Does the Score Mean?**  
- The fraud score tells you how risky the transaction is.  
- **Higher scores** mean higher fraud risk.  

---

### **Summary**  

1. Find the fraud probability and expected fraud amount.  
2. Calculate the diagonal length.  
3. Normalize it using the 99% boundary diagonal.  
4. Use the formula to calculate the fraud score.  

**Example Result**: Fraud Score = **468** → Moderate Risk  

Let me know if you want me to break down any step further!
Here is a more detailed explanation for each section:


---

1. Business Requirement and Model Output & Usage

This section defines the purpose and objectives of the model based on business needs. It outlines the problems the model aims to solve, the intended audience, and how the model outputs will be used in decision-making or operations. It also highlights any constraints or assumptions considered during development.


---

2. Model Development Data

Describes the data used for building the model, including sources, data types, and formats. It explains the data preprocessing steps such as cleaning, transformation, and handling missing values. This section also discusses quality checks performed to ensure data integrity and relevance, along with any sampling techniques applied.


---

3. Model Methodology and Model Selection

Covers the approach taken to design the model, including the techniques, algorithms, and frameworks considered. It explains the rationale for choosing a specific methodology and details the evaluation criteria used during model selection. This section may also include preliminary tests, comparisons, and trade-offs made between different methods.


---

4. Model Specifications

Provides a technical overview of the final model, including its structure, features, mathematical formulas, and underlying assumptions. It specifies input variables, output formats, and any transformation rules applied during processing. This section also details parameter settings, configuration options, and code snippets if required for implementation.


---

5. Model Testing and Evaluation

Focuses on the validation and testing process to assess the model's performance. It describes evaluation metrics such as accuracy, precision, recall, and error rates. Testing scenarios, stress testing, and edge cases are documented to ensure robustness. Results are analyzed to confirm whether the model meets predefined success criteria and business goals.


---

6. Model Monitoring Framework

Outlines the strategy for tracking the model’s performance after deployment. It includes plans for monitoring accuracy, data drift, and changes in input data patterns. Regular reporting, alerts, and retraining schedules are specified to ensure long-term reliability. It also defines roles and responsibilities for maintenance and issue resolution.


---

Let me know if you'd like further refinements!

