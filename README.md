# Algonive-Employee-Attrition-Prediction

## 📌 Project Overview
This project predicts whether an employee is likely to leave a company (attrition) using machine learning.

Employee attrition is a big problem for companies because losing employees increases cost and reduces productivity. So, the goal of this project is to identify employees who are at risk of leaving and understand the reasons behind it.

---

## 📊 Dataset
I used an HR analytics dataset that contains employee information such as:
- Age
- Salary (MonthlyIncome)
- Job Satisfaction
- Overtime
- Work-Life Balance
- Years at Company

The target column is:
- Attrition (0 = Stay, 1 = Leave)

---

## 🔍 Data Preprocessing
Before building models, I prepared the data:

- Converted categorical values (Yes/No → 1/0)
- Used One-Hot Encoding for columns like JobRole and Department
- Converted boolean values into numbers
- Removed unnecessary columns (like EmployeeNumber)
- Split data into training and testing sets
- Applied StandardScaler for Logistic Regression
- This step ensures the data is clean and usable for machine learning.

---

## 📈 Exploratory Data Analysis (EDA)

I analyzed the data using graphs to understand patterns:

- Attrition Distribution → Most employees stay (imbalanced data)
- Overtime vs Attrition → Employees with overtime leave more
- Salary vs Attrition → Lower salary employees leave more
- Job Satisfaction → Low satisfaction leads to higher attrition
- These insights helped understand the problem before modeling.

---

## 🤖 Models Used

### 1. Logistic Regression
- Simple baseline model
- Works well for classification problems
- Needs feature scaling

### 2. Random Forest
- More powerful model using multiple decision trees
- Handles complex patterns better
- Gives feature importance

### 3. Decision Tree
- Easy to understand model
- Works like decision rules
- But can overfit easily

---

## ⚙️ Model Improvement

The dataset is imbalanced (very few employees leave), so models were not detecting attrition properly.

To fix this:
- Used `class_weight='balanced'`

This helps the model focus more on employees who leave.

---

## 📊 Feature Importance

Using Random Forest and Decision Tree, I identified the most important features:

- Monthly Income
- Overtime
- Age
- Total Working Years
- Job Level

---

## 📉 Model Comparison

I compared all models based on accuracy and recall:

- Logistic Regression → Good baseline
- Improved Logistic Regression → Better recall
- Random Forest → High accuracy
- Improved Random Forest → Best overall model
- Decision Tree → Lower performance
- Improved Decision Tree → Slight improvement

---

## 🏆 Best Model

The best model is:

👉 **Improved Random Forest**

Reason:
- Good accuracy
- Better performance on attrition cases
- More reliable than other models

---

## 💡 Business Recommendations

Based on insights:

- Reduce overtime workload
- Increase employee salary where possible
- Improve job satisfaction
- Focus on work-life balance

These actions can reduce employee attrition.

---

## 🧠 Conclusion

This project shows how machine learning can help companies predict employee attrition and take action early.

Even though accuracy is good, recall for attrition is still a challenge, which means further improvement is needed for real-world use.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## 📂 Project Structure

- main.ipynb → Complete code
- dataset.csv → Dataset used
- README.md → Project explanation

---

## 🙌 Final Note

This project helped me understand:
- Data preprocessing
- Model building
- Evaluation
- Real-world problem solving
