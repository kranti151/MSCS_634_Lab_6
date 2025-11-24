# MSCS_634_Lab_6
## Association Rule Mining using Apriori and FP-Growth
**Author:** Komalben Suthar  
**Course:** MSCS 634 – Advanced Programming Languages  
**Dataset:** Online Retail (UCI)

---

## Purpose
The goal of this lab is to explore association rule mining techniques using the Apriori and FP-Growth algorithms on the Online Retail transactional dataset. The lab demonstrates:  
- How to preprocess and clean transactional data for mining  
- Identification of frequent itemsets using Apriori and FP-Growth  
- Generation and interpretation of association rules with support, confidence, and lift metrics  
- Visualization of frequent itemsets and association rules for better insights  
- Comparison of algorithm efficiency and output quality  

---

## Key Insights
- **Frequent Itemsets:** Both Apriori and FP-Growth generated similar frequent itemsets when using the same support threshold (0.02). The most commonly purchased items were easily identified.  
- **Association Rules:** High-confidence and high-lift rules highlighted product combinations that frequently occur together. For example, customers buying Item A are likely to also buy Item B.  
- **Algorithm Efficiency:** FP-Growth was significantly faster than Apriori on this dataset due to its ability to avoid repeated candidate generation, demonstrating its suitability for larger, sparse datasets.  
- **Visual Analysis:** Barplots for top frequent itemsets and scatterplots of confidence vs. lift provided clear visual insights into the strongest associations.  

---

## Comparative Summary

| Algorithm   | Frequent Itemsets | Top Rules | Runtime Efficiency |
|------------|-----------------|-----------|-----------------|
| Apriori    | 120             | 50        | Moderate         |
| FP-Growth  | 120             | 50        | Fast             |

**Observation:** FP-Growth is preferable for larger datasets or when runtime is critical, while Apriori is more intuitive for learning purposes.

---

## Challenges and Decisions
1. **Data Cleaning:**  
   - Removed cancelled transactions, negative quantities, and rows with missing CustomerIDs.  
   - Converted transactional data into one-hot encoded format for compatibility with the algorithms.  

2. **Threshold Selection:**  
   - Chose `min_support = 0.02` and `min_confidence = 0.3` after trial-and-error to balance rule discovery and computational feasibility.  

3. **Performance Issues:**  
   - Apriori was slower on the full dataset, so FP-Growth was used for faster processing.  
   - Limited visualizations to top N frequent itemsets and rules to ensure readability.  

4. **Interpretation:**  
   - Evaluated both algorithms based on support, confidence, and lift to identify meaningful business insights.  

---

## Files in Repository
- `Lab_6_Association_Rule_Mining.ipynb` : Complete Jupyter Notebook with code, outputs, and visualizations  
- `frequent_itemsets_apriori.csv` : Apriori frequent itemsets  
- `frequent_itemsets_fpgrowth.csv` : FP-Growth frequent itemsets  
- `association_rules_apriori.csv` : Apriori association rules  
- `association_rules_fpgrowth.csv` : FP-Growth association rules  

---

