Market Basket Analysis in Python Using the Apriori Algorithm

This project performs Market Basket Analysis using the Apriori algorithm to identify item associations within transaction data. The goal is to uncover frequently purchased item combinations and generate association rules that can support business decisions such as product placement, bundling, and cross-selling.

Objectives

Load and preprocess transaction data.

Apply the Apriori algorithm to identify frequent itemsets.

Generate association rules with support, confidence, and lift.

Interpret discovered patterns for actionable insights.

Dataset

The project uses a CSV file (Market.csv) containing market transactions. Each row represents a single transaction, with each column containing one item purchased in that transaction. Missing values represent no additional items.

Requirements

Install the necessary Python libraries:

pip install apyori pandas numpy

Methodology

Import required libraries.

Load the dataset using pandas.

Convert the transactional data into a list-of-lists format.

Run the Apriori algorithm with specified thresholds for support, confidence, and lift.

Extract and display association rules.

Key Code Components

Data loading: pd.read_csv('Market.csv', header=None)

Data transformation: converting rows into transaction lists.

Apriori execution: apriori(transactions, min_support, min_confidence, min_lift)

Rule interpretation: converting results into readable form.

Output

The output includes:

Frequent itemsets

Association rules

Metrics such as support, confidence, and lift

These outputs help identify which products tend to be purchased together and how strong those relationships are.

Applications

Retail product placement

Recommendation systems

Promotion and bundling strategies

Inventory planning
