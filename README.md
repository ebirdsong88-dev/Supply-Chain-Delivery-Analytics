* [README](https://github.com/ebirdsong88-dev/Supply-Chain-Delivery-Analytics#)

# Supply Chain Delivery Analytics

## Business Problem
Operations and supply chain teams rely on delivery and order volume metrics to make staffing, inventory, and process decisions. But a metric built directly from transactional data can be misleading if the underlying data structure changes over time — a trend that looks like a business decline may actually be an artifact of how the data itself was recorded, not a real drop in activity. This project demonstrates an end-to-end workflow for analyzing delivery performance, validating a suspicious trend in the data before drawing conclusions from it, and building a predictive model to flag high-risk orders in advance.

## Objective
Analyze ~180,000 orders from the DataCo Smart Supply Chain dataset to identify what drives late deliveries, verify — rather than assume — the cause behind an apparent drop in order volume, and predict late delivery risk before an order ships.

## Approach
* Imported and cleaned ~180,000 order-level records in Python
* Reviewed record counts, missing values, and column structures
* Removed PII and constant/mostly-missing columns prior to analysis
* Engineered features (shipping delay, profit margin, order timing)
* Analyzed late delivery rate by shipping mode and region
* Analyzed profitability by product category
* Investigated an apparent ~60% drop in order volume rather than taking it at face value
* Diagnosed a change in row granularity (line-items vs. one row per order) as the true cause
* Rebuilt the order volume metric on a corrected, order-level basis
* Verified the corrected trend wasn't itself a data completeness artifact
* Built a Random Forest classifier to predict late delivery risk from order-time features
* Extracted and visualized feature importance to explain model drivers

## Tools Used
* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Scikit-learn
* Jupyter Notebook

## Analytical Techniques Demonstrated
* Record count and data granularity validation
* Row-to-entity ratio diagnostics (rows-per-order)
* Metric correction and re-validation
* Data completeness / truncation testing
* Late delivery rate segmentation by category
* Profitability analysis by product category
* Classification modeling (Random Forest)
* Feature importance interpretation

## Skills Demonstrated
* Data Validation
* Data Quality Investigation
* Exploratory Data Analysis
* Python
* Pandas / NumPy
* Predictive Modeling (Scikit-learn)
* Data Visualization
* Technical Documentation

## Business Impact
This workflow demonstrates how to avoid a common and costly analytical mistake: acting on a metric before confirming what it's actually measuring. Had the naive order volume chart been taken at face value, it would have suggested a sharp decline in business activity — when the real, verified trend was an increase of roughly 20% in the final months of the dataset. The predictive model further supports proactive operations by flagging high risk-of-delay orders before they ship, using only information known at order time — helping teams intervene earlier rather than reacting after a delivery is already late.
