# Market-Basket Analysis & Association Rules for Cross-Selling

**Week 4 — Specialist Advanced Data Science Project**

## 1. Project Overview

This project applies Market-Basket Analysis and Association Rule Mining to a regional ride-hailing startup scenario. The goal is to identify services or items that frequently occur together in transactions and translate these patterns into actionable cross-selling recommendations.

Using Python and the `mlxtend` library, the project applies the FP-Growth algorithm to discover frequent itemsets, generate association rules, and evaluate their usefulness through support, confidence, and lift.

## 2. Project Objectives

- Analyse a transaction dataset containing at least 6,500 baskets.
- Identify frequently occurring items and service combinations.
- Apply FP-Growth using three different minimum-support thresholds.
- Generate association rules and focus on rules with lift greater than 1.2.
- Compare rule stability across two different months.
- Develop five actionable cross-selling recommendations.
- Estimate potential revenue impact using clearly stated assumptions.
- Document data limitations, collection bias, testing, and validation.

## 3. Tools and Technologies

- **Python** — Data processing and analysis
- **Jupyter Notebook** — Interactive development and documentation
- **Pandas** — Data manipulation and preparation
- **NumPy** — Numerical operations
- **Matplotlib / Seaborn** — Data visualisation, where used
- **mlxtend** — FP-Growth and association rule mining
- **GitHub** — Version control and project delivery

## 4. Methodology

### Step 1: Data Loading and Preparation

Loaded the transaction dataset, inspected its structure, and checked data quality, including missing values and duplicate records. Prepared the transactions in a suitable format for frequent itemset mining.

### Step 2: Item Frequency Analysis

Calculated item frequencies and visualised frequently occurring items. Rare items were reviewed to determine whether they should be excluded from the analysis.

### Step 3: Frequent Itemset Mining

Applied the FP-Growth algorithm using three minimum-support thresholds to compare the number of frequent itemsets discovered under different settings.

### Step 4: Association Rule Generation

Generated association rules and evaluated them using:

- **Support:** Proportion of all transactions containing the relevant item combination.
- **Confidence:** Proportion of transactions containing the antecedent that also contain the consequent.
- **Lift:** Measures the observed association relative to the consequent's overall frequency.

Rules with lift greater than 1.2 were prioritised for further review. Obvious, trivial, or impractical rules were considered for removal.

### Step 5: Temporal Validation

Compared selected association rules across two different months to assess whether the identified patterns remained relevant in another time period.

### Step 6: Cross-Selling Strategy

Selected promising rules and translated them into five potential cross-selling actions. Estimated revenue impact using explicit assumptions about eligible transactions, expected uptake, and additional revenue per successful cross-sell.

## 5. Business Value

The analysis can help a ride-hailing business:

- Identify services that may be suitable for cross-promotion.
- Recommend relevant add-ons during the customer journey.
- Design targeted promotional offers.
- Prioritise potential cross-selling opportunities.
- Develop data-driven experiments to evaluate additional revenue opportunities.

Association rules reveal relationships in historical transactions; they do not establish causation or guarantee future revenue growth.

## 6. Bias and Limitations

The findings depend on the quality, coverage, and collection method of the transaction dataset.

If the dataset overrepresents particular locations, customers, service types, or months, the discovered patterns may not generalise to the entire customer population. If simulated data was used, the results should be treated as illustrative rather than evidence of actual customer behaviour.

Other limitations include changes in customer preferences over time, the possibility of unstable rules, and uncertainty in estimated revenue impact.

Future improvements could include testing recommendations through controlled A/B experiments, incorporating more months of data, and evaluating actual conversion and incremental revenue.

## 7. Validation and Testing

The project is intended to evaluate:

- Data quality and transaction preparation.
- Frequent itemset counts under three support thresholds.
- Association rule filtering using lift.
- Rule stability across two different months.
- The practicality of five cross-selling recommendations.
- Revenue estimates under explicitly stated assumptions.

Actual test results, discovered problems, and fixes should be documented using notebook outputs and supporting evidence.

## 8. Project Structure

A suggested repository structure is:

```text
market-basket-analysis/
│
├── Untitled2.ipynb
├── data/
│   └── README.md
├── outputs/
│   ├── association_rules.csv
│   ├── cross_sell_action_plan.csv
│   └── charts/
├── screenshots/
├── README.md
├── requirements.txt
└── CHANGELOG.md
```

Include only files and outputs that you have actually created. Keep large or confidential datasets out of the public repository. If the data cannot be shared, document how to obtain an authorised copy or prepare an appropriate sample.

## 9. Installation and Usage

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd market-basket-analysis
```

Create and activate a virtual environment if desired, then install the dependencies:

```bash
pip install pandas numpy matplotlib seaborn mlxtend jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `Untitled2.ipynb` and run the notebook cells in order. Ensure that the dataset is available at the path expected by the notebook.

## 10. Key Deliverables

- Jupyter Notebook containing the analysis.
- Frequent itemset and association rule results.
- Comparison of three minimum-support thresholds.
- Temporal validation evidence.
- Five cross-selling recommendations.
- Revenue impact estimates and assumptions.
- Screenshots and supporting outputs.
- Project walkthrough video.
- Documentation of testing, limitations, and improvements.

## 11. Conclusion

This project demonstrates the application of frequent pattern mining and association rule learning to a business-oriented ride-hailing scenario. By combining transaction analysis with validation and practical recommendations, it provides a structured approach to identifying potential cross-selling opportunities.

The business value of these recommendations must ultimately be confirmed through real-world testing.

---

**Project:** Week 4 — Specialist Advanced Data Science  
**Primary Library:** mlxtend  
**Algorithm:** FP-Growth  
**Author:** Huzaifa
