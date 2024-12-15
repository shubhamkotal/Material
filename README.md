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
