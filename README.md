## Project Title

Market Basket Analysis in Python Using the Apriori Algorithm

---

## Description

This project uses Apriori algorithm to identify frequently purchased item combinations and generate association rules. The analysis helps understand customer buying behavior and supports business decisions such as product bundling, placement, and targeted marketing.

---

## Dataset

The dataset (`Market.csv`) contains multiple market transactions.

* Each row represents a single transaction.
* Each column represents an item purchased in that transaction.
* Blank values indicate no additional items in that particular transaction.
  The dataset is used in a raw format and then converted into a suitable structure for running Apriori.

---

## Requirements

Install the required Python packages before running the notebook: pip install apyori pandas numpy

---

## Workflow Summary

1. Load the dataset using pandas.
2. Clean and convert the data into a list of transaction lists.
3. Configure Apriori parameters such as minimum support, confidence, and lift.
4. Execute the Apriori algorithm to extract frequent itemsets.
5. Generate association rules from the extracted itemsets.
6. Display and interpret rule metrics for analysis.

---

## Apriori Parameters Used

* **min_support**: Defines how frequently an item must appear.
* **min_confidence**: Measures the reliability of a rule.
* **min_lift**: Evaluates rule strength relative to item independence.
* **min_length**: Ensures rules contain at least a set number of items.

These parameters help filter meaningful and strong associations.

---

## Key Code Components

* Reading data using `pd.read_csv()`
* Transaction list formation using loops
* Applying Apriori with `apriori()`
* Extracting support, confidence, and lift from rule results
* Iterating through rules and printing readable outputs

---

## Output

The analysis produces:

* Frequent itemsets showing which items appear together regularly
* Association rules showing relationships like A → B
* Metrics including support, confidence, lift, and rule strength
  These outputs help identify actionable insights for retail decision-making.

---

## Use Cases

* Product placement optimization
* Recommendation systems
* Cross-selling strategies
* Optimized promotions and discount bundles
* Inventory planning and forecasting


