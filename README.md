# Market-Basket-Analysis
This project implements *Market Basket Analysis (MBA)* on a transactional dataset to discover frequent itemsets and derive association rules.  
The goal is to understand *which products are commonly purchased together*, providing strategic insights for:

- 🏬 *Store layout optimization*
- 🧺 *Product bundling*
- 🎯 *Targeted promotions*

---

## 🎯 Project Goals

The primary objectives of this analysis are:

1. *Identify Association Rules:*  
   Discover strong rules of the form {Item A} → {Item B}  
   (e.g., Customers who buy Bread also buy Butter).

2. *Product Placement Optimization:*  
   Suggest optimal product placement within a retail environment.

3. *Targeted Promotions:*  
   Inform effective product bundles and cross-selling campaigns.

---

## 🛠️ Technologies and Libraries

This analysis pipeline was built entirely in *Python* with the following libraries:

- *Python* → Core programming language  
- *Pandas* → Data loading, cleaning, and transformation into a transaction matrix  
- *mlxtend* (or equivalent) → Implementation of the *Apriori Algorithm* and association rule mining  
- *re (Regular Expressions)* → Cleaning and standardizing product descriptions  

---

## 🧹 Data Preparation and Cleaning Steps

A series of preprocessing steps ensured clean and accurate input data for rule generation.

### 1. Data Inspection and Initial Loading
- Loaded dataset (df.shape) → *(541,909 × 8)* records  
- Key columns: InvoiceNo, Description, Quantity, UnitPrice, CustomerID

### 2. Handling Missing Data
- Dropped missing product descriptions using:  
  ```python
  df.dropna(axis=0, subset=['Description'])
