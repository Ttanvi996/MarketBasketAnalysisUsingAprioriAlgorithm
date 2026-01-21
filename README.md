Market Basket Analysis in Python Using the Apriori Algorithm

This project performs Market Basket Analysis (MBA) using the Apriori algorithm to uncover association rules between items frequently purchased together.
It uses Python along with the apyori library to generate frequent itemsets and meaningful rules.

Project Overview

Market Basket Analysis helps businesses understand customer purchasing behavior by identifying patterns such as:

Items frequently bought together

Strong product associations

Insights for promotions, store layout, cross-selling, and bundling

In this project, we:

Load transaction data from Market.csv

Prepare data into list-of-lists format

Apply Apriori Algorithm using the apyori package

Extract association rules (support, confidence, lift)

Interpret results for actionable insights

Requirements

Install required dependencies:

pip install apyori pandas numpy

Dataset

Market.csv contains transaction records, where each row represents a customer transaction and each column represents an item purchased.

1. Import Libraries
import pandas as pd
import numpy as np
from apyori import apriori

2. Load Data
data = pd.read_csv('Market.csv', header=None)

3. Transform to Transactions
transactions = []
for i in range(0, data.shape[0]):
    transactions.append(data.iloc[i].dropna().tolist())

4. Apply Apriori Algorithm
rules = apriori(
    transactions,
    min_support=0.003,
    min_confidence=0.2,
    min_lift=3,
    min_length=2
)
results = list(rules)

5. Display Rules

Each rule gives:

Base itemset

Associated itemset

Support

Confidence

Lift

Example Output Interpretation

If a rule states:

{Milk} → {Bread}, confidence = 0.35, lift = 4.2

This means:

When customers buy Milk, they also buy Bread 35% of the time.

The lift of 4.2 indicates a strong positive association.

Use Cases

Grocery stores → product placement

E-commerce → personalized recommendations

Marketing → promotion bundling

Retail analytics → optimized inventory management

