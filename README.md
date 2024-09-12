# **Heart Disease Prediction Model **

## **Project Overview:**
This project leverages the **Framingham Heart Study** dataset to predict the 10-year risk of coronary heart disease (CHD) using a logistic regression model. The model analyzes various demographic, behavioral, and medical factors to forecast CHD risk and provides critical insights into heart disease prevention.

### **Motivation:**
Coronary heart disease is the leading cause of death in the U.S., with over **18.2 million adults** affected. Early prediction of heart disease risk can aid in guiding lifestyle changes and medical interventions, reducing mortality rates and enhancing quality of life.

---

## **Objectives:**
- To identify and quantify key risk factors contributing to heart disease.
- To build a logistic regression model capable of predicting the likelihood of developing CHD.
- To use model insights for preventive healthcare strategies and risk assessment.

---

## **Data Source:**
- **Framingham Heart Study** dataset (initiated in 1948).
- Comprising over **4000 individual records** with 15 attributes, the dataset provides a comprehensive view of factors influencing heart disease, including:
  - **Demographic factors**: Age, Sex.
  - **Behavioral factors**: Smoking habits.
  - **Medical history**: Hypertension, Diabetes, Stroke, Blood Pressure, Cholesterol levels, BMI, and more.

---

## **Methodology:**

### **1. Data Preprocessing:**
- The dataset was cleaned by removing unnecessary columns (e.g., `education`).
- Renamed columns for clarity (e.g., `male` → `Sex_male`, `currentSmoker` → `IsCurrentSmoker`).
- Missing values were removed using **listwise deletion**, given their small proportion of the overall dataset.

### **2. Logistic Regression:**
- **Logistic Regression** was chosen due to its suitability for binary classification (CHD vs. No CHD).
- The model was built using the `glm()` function in R with **backward elimination** to remove non-significant variables based on p-values greater than 0.05.

### **3. Model Evaluation Metrics:**
- The model was evaluated using:
  - **Accuracy**: Achieved 88% accuracy in predicting 10-year CHD risk.
  - **Sensitivity**: 99.2%, indicating a strong ability to identify individuals at risk.
  - **Specificity**: 7.02%, suggesting the model tends to over-predict heart disease.
  - **AUC (Area Under Curve)**: 0.725, reflecting a moderately accurate model.

### **4. Key Findings:**
- **Gender Impact**: Males are **78.8%** more likely to develop heart disease compared to females.
- **Age Effect**: Each additional year increases the risk by **7%**.
- **Smoking Habits**: Every additional cigarette smoked per day raises the risk by **2%**.
- **Blood Pressure**: A **1.7%** increase in risk is associated with each unit increase in systolic blood pressure.
- **Cholesterol & Glucose**: Surprisingly, no significant association was found between total cholesterol or glucose levels and heart disease risk, potentially due to the balancing effect of **HDL ("good cholesterol")**.

---

## **Model Insights & Interpretation:**

### **1. High Sensitivity, Low Specificity**:
- **Sensitivity**: The model is excellent at identifying those at risk (99.2%), making it suitable for **early screening**.
- **Specificity**: The low specificity (7.02%) suggests over-prediction of heart disease, which could lead to false positives.

### **2. Predictive Power**:
- **Odds Ratios**: Provide a clear understanding of how each factor influences the probability of developing heart disease.
- **Positive Predictive Value (PPV)**: The PPV of 7.02% shows that while the model isn’t highly reliable in confirming heart disease when it predicts it, it is very effective in ruling out heart disease (high **Negative Predictive Value** of 99.2%).

### **3. Model Refinement**:
- **Backward elimination** removed insignificant predictors such as cholesterol and glucose levels, improving model specificity by **12%**.

---

## **Business Insights:**

### **Healthcare and Insurance Applications**:
- **Risk Identification**: The model can help healthcare providers and insurance companies identify high-risk individuals for more intensive follow-ups or preventive measures.
- **Insurance Underwriting**: Insurance companies can use the model to adjust premiums based on the likelihood of heart disease, helping manage risk more effectively.

### **Marketing Insights**:
1. **Gender-Specific Campaigns**: Men are more susceptible to heart disease, and campaigns can be tailored to promote regular check-ups and cardiovascular health products.
2. **Older Demographics**: As age increases the risk of heart disease, marketing efforts should focus on older adults, offering health insurance plans and educational resources.
3. **Smoking Cessation Programs**: The model confirms smoking’s strong association with heart disease, making anti-smoking campaigns and products (e.g., nicotine patches) highly relevant.

---

## **Conclusion:**

- **Model Accuracy**: The logistic regression model predicted CHD risk with **88% accuracy**.
- **AUC**: The **AUC of 0.725** shows that the model is reasonably effective in distinguishing between individuals who will and will not develop heart disease.
- **Key Risk Factors**: Age, gender, smoking, and systolic blood pressure are significant predictors of heart disease, while cholesterol and glucose levels were found to be less impactful.
- **Practical Use**: This model is beneficial for **early screening**, where missing a case (false negative) could have severe consequences, making it especially useful in healthcare settings.

---

## **Key Outcomes:**
- **Model Accuracy**: 88%
- **Sensitivity**: 99.2%
- **Specificity**: 7.02%
- **AUC**: 0.725
- **Business Impact**: Early screening for high-risk individuals, healthcare prevention strategies, and insurance premium adjustments.
