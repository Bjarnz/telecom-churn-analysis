# Telecom Customer Churn Analysis  
**Machine Learning | Exploratory Data Analysis | Random Forest Modeling**

## 📌 Project Overview
Customer churn is a critical business problem in the telecommunications industry, where retaining existing customers is often more cost-effective than acquiring new ones.  
This project analyzes telecom customer behavior to **identify key drivers of churn** and **build predictive models** that can support proactive retention strategies.

The goal is not only high predictive performance, but **interpretable insights** that align with real-world business decisions.

---

## 🧠 Objectives
- Explore customer usage, plan characteristics, and service interactions
- Identify behavioral patterns associated with churn
- Build and evaluate a **baseline Random Forest model**
- Improve churn detection through **model tuning and validation**
- Emphasize recall and business-relevant performance metrics

---

## 📊 Dataset
- Public telecom churn dataset (commonly used for benchmarking churn models)
- Binary target variable: `Churn`
- Mixture of:
  - Usage metrics (minutes, calls)
  - Service interactions (customer service calls)
  - Plan features (international plan, voicemail usage)

> The dataset is split into:
> - **churn-80**: training data  
> - **churn-20**: held-out test data  

---

## 🧹 Data Preprocessing
Key preprocessing steps include:
- Converting categorical yes/no variables into binary indicators
- Encoding churn as a binary target variable
- Ensuring consistency between training and test sets
- Retaining correlated features where appropriate (tree-based models are robust to multicollinearity)

All preprocessing is handled **explicitly and transparently** in the notebook.

---

## 🔍 Exploratory Data Analysis (EDA)
EDA focuses on understanding how customer behavior differs between churners and non-churners.

### Key Insights
- Customers who churn tend to:
  - Make more **customer service calls**
  - Have higher **daytime and international usage**
- International plan customers exhibit a higher churn rate
- Strong linear relationships exist between minutes and charges (expected billing behavior)

Visualizations include:
- Boxplots comparing behavioral features vs churn
- Correlation heatmap highlighting key relationships

---

## 🌲 Baseline Model: Random Forest
A baseline Random Forest classifier was trained to establish a reliable benchmark.

### Validation Strategy
- **5-fold cross-validation** used to assess model stability
- Cross-validation ensures results are not dependent on a single train-test split

### Baseline Performance Highlights
- High overall accuracy
- Strong precision for churn predictions
- Moderate recall for churn, indicating missed churners

This reflects a common real-world tradeoff: models often favor majority classes unless explicitly tuned.

---

## ⚙️ Model Tuning & Improvement
To address the baseline model’s limitations, hyperparameter tuning was applied to:
- Control tree depth
- Reduce overfitting
- Improve recall and F1-score for churn detection

The tuned model trades some overall accuracy for **significantly better churn recall**, which is more valuable from a business perspective.

---

## 📈 Evaluation Metrics
Models are evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices
- Cross-validation statistics

Emphasis is placed on **recall for churners**, as false negatives represent lost retention opportunities.

---

## 🧩 Technologies Used
- Python
- pandas, NumPy
- scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

---

## 🚀 Key Takeaways
- Customer service interactions are one of the strongest churn indicators
- Usage intensity alone does not explain churn — **service friction matters**
- Model evaluation should align with business costs, not just accuracy
- Tree-based models provide strong performance with interpretable insights

---

## 📂 Repository Structure

