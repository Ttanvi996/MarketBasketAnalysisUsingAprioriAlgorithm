

## Project Title

Market Basket Analysis in Python Using the Apriori Algorithm

---

## Overview

The goal of this project  is to identify frequent item combinations and generate association rules that reveal purchasing patterns within transactional data. The work demonstrates a practical application of association rule mining, commonly used in retail analytics and recommendation systems.

---

## Dataset Information

The project uses a transactional dataset (`Market.csv`).

* Each row represents a single transaction.
* Each column contains one item purchased during that transaction.
* Empty cells indicate no additional items.
  The dataset is pre-processed and transformed into a list-of-lists format required for Apriori.

---

## Requirements

Install all necessary Python libraries:

```
pip install apyori pandas numpy
```

You will also need:

* Python 3.8+
* Jupyter Notebook or any Python IDE (VS Code, PyCharm, etc.)

---

## How to Implement and Execute

Follow these steps to run the project successfully:

### 1. Clone or download the project files

Ensure the notebook and dataset are in the same directory.

### 2. Open the Jupyter Notebook

Run:

```
jupyter notebook
```

Open:
`Market_Basket_Analysis_in_Python_using_Apriori_Algorithm.ipynb`

### 3. Import libraries

The first cell installs and imports necessary libraries, including `apyori`.

### 4. Load the dataset

The file is loaded using:

```python
data = pd.read_csv('Market.csv', header=None)
```

### 5. Convert data into transaction format

Each row is converted into a list of purchased items. This format is required by the Apriori algorithm.

### 6. Apply the Apriori algorithm

The algorithm is executed with parameters such as:

* Minimum support
* Minimum confidence
* Minimum lift
* Minimum rule length

Example:

```python
rules = apriori(transactions, min_support=0.003, min_confidence=0.2, min_lift=3, min_length=2)
```

### 7. Extract and interpret rules

After executing Apriori, the rules are converted into a readable format to view support, confidence, and lift values.

---

## Apriori Parameter Summary

* **Support:** Frequency of item appearance in the dataset.
* **Confidence:** Strength of the implication in an association rule.
* **Lift:** Measure of rule strength compared to random chance.
* **Minimum length:** Ensures rules contain at least 2 items.
  These parameters help filter strong and meaningful rules.

---

## Output Description

The project generates:

* Frequent itemsets
* Association rules (A → B)
* Evaluation metrics such as support, confidence, and lift

These outputs are used to understand purchasing patterns and relationships between items.

---

## Applications

This analysis can be applied to:

* Designing product bundles
* Store layout planning
* Cross-selling strategies
* Recommendation system development
* Promotion targeting and marketing decisions

