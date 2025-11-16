# AI Project README

## Part 1: Short Answer Questions

### 1. Problem Definition

**Hypothetical AI Problem:** Predicting student dropout rates.

**Objectives:**

1. Identify students at high risk of dropping out.
2. Provide early intervention recommendations.
3. Improve overall retention rates.

**Stakeholders:**

* University administration
* Academic advisors

**KPI:**

* Area Under the ROC Curve (AUC) for dropout prediction.

### 2. Data Collection & Preprocessing

**Data Sources:**

1. Student academic history
2. Attendance and engagement logs

**Potential Bias:**

* Overrepresentation of certain socioeconomic groups may skew predictions.

**Preprocessing Steps:**

1. Handle missing values
2. Normalize numeric features
3. Encode categorical variables

### 3. Model Development

**Chosen Model:** Random Forest — chosen for interpretability, robustness, and strong baseline performance.

**Data Splitting:**

* 70% training, 15% validation, 15% test

**Hyperparameters to Tune:**

1. Number of trees — affects performance and stability
2. Maximum depth — controls overfitting

### 4. Evaluation & Deployment

**Evaluation Metrics:**

* Accuracy: measures overall correctness
* F1-Score: balances precision and recall for imbalanced data

**Concept Drift:**
Changes in underlying data patterns over time. Monitored by comparing model predictions to actual outcomes regularly.

**Technical Challenge:**

* Scalability when processing large datasets.

---

## Part 2: Case Study Application

### 1. Problem Scope

**Problem:** Predict patient readmission risk within 30 days.

**Objectives:**

* Reduce unplanned readmissions
* Support clinical decision-making

**Stakeholders:**

* Hospital administrators
* Physicians and nurses

### 2. Data Strategy

**Data Sources:**

* Electronic Health Records (EHRs)
* Patient demographics

**Ethical Concerns:**

1. Patient privacy
2. Potential bias in historical medical treatment patterns

**Preprocessing Pipeline:**

1. Remove or impute missing medical data
2. Standardize numeric clinical measurements
3. Feature engineering (e.g., count of prior admissions, comorbidity scores)

### 3. Model Development

**Chosen Model:** Gradient Boosting Machine for its strong performance on structured clinical data.

**Hypothetical Confusion Matrix:**

|                   | Predicted Readmit | Predicted No Readmit |
| ----------------- | ----------------- | -------------------- |
| Actual Readmit    | 40                | 10                   |
| Actual No Readmit | 20                | 130                  |

**Precision:** 40 / (40 + 20) = 0.67

**Recall:** 40 / (40 + 10) = 0.80

### 4. Deployment

**Integration Steps:**

1. Deploy model within hospital IT infrastructure
2. Connect to EHR system for real-time data
3. Provide risk scores in clinician dashboards

**Regulatory Compliance:**

* Encrypt all data
* Restrict access
* Conduct regular HIPAA compliance audits

### 5. Optimization

* Use dropout or regularization to reduce overfitting

---

## Part 3: Critical Thinking

### 1. Ethics & Bias

**Impact of Biased Data:**
Biased data may lead to misclassification of vulnerable patient groups, impacting care quality.

**Mitigation Strategy:**

* Fairness-aware sampling during training

### 2. Trade-offs

**Interpretability vs Accuracy:**
More complex models may be accurate but harder to explain to clinicians.

**Limited Resources:**

* Hospital may prefer lighter models like logistic regression.

---

## Part 4: Reflection & Workflow Diagram

### 1. Reflection

**Most Challenging Part:**

* Ensuring fairness throughout the pipeline due to the sensitivity of healthcare data.

**Improvements:**

* Collect more diverse datasets and perform deeper bias audits.

### 2. Workflow Diagram

```
Start --> Problem Definition --> Data Collection --> Preprocessing -->
Model Development --> Evaluation --> Deployment --> Monitoring --> End
```
