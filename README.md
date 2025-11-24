# MSCS_634_Lab_6
**Author:** Komalben Suthar  
**Course:** MSCS 634 – Advanced Programming Languages  
**Dataset:** Online Retail (UCI)

---

## Purpose
The purpose of this lab is to explore association rule mining techniques using the Apriori and FP-Growth algorithms on the Online Retail transactional dataset. The lab demonstrates how to preprocess transactional data, identify frequent itemsets, generate meaningful association rules, and visualize patterns for better interpretation. This exercise also compares the performance and outputs of both algorithms.

---

## Key Insights
- Both Apriori and FP-Growth identified similar frequent itemsets when using the same support threshold.
- FP-Growth was faster than Apriori, demonstrating its efficiency on larger, sparse datasets.
- High lift and high-confidence rules highlight product combinations that often occur together, which can be used for cross-selling or promotional strategies.
- Visualizations such as barplots of frequent itemsets and scatterplots of confidence vs. lift helped identify strong association rules clearly.

---

## Challenges and Decisions
- **Data Cleaning:** Removed cancelled transactions, negative quantities, and missing CustomerIDs to ensure clean transaction records.
- **One-Hot Encoding:** Creating a one-hot transaction matrix required careful memory management; limited the dataset to relevant items for efficiency.
- **Support and Confidence Thresholds:** Required trial-and-error to balance the number of frequent itemsets and rules. Started with a min_support of 0.02 and min_confidence of 0.3.
- **Performance:** Apriori can be slow on large datasets; FP-Growth was used to improve efficiency.

---
