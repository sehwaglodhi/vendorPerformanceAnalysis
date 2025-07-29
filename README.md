# Sales Data Analytics Project with SQLite Integration

This project performs a full analytical workflow on retail sales data — including data cleaning, exploratory data analysis (EDA), visualizations, and storing grouped results into a SQLite database for BI reporting.

---

## Project Overview

This analysis uncovers key business patterns across sales transactions from multiple vendors. Using Python, the project explores product-wise, vendor-wise, contributions to sales revenue. Final results are stored in a `.db` file for seamless Power BI integration.

---

## Project Structure

| Notebook                   | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `EDA.ipynb`                | Cleans raw data, handles missing values, and performs datetime formatting  |
| `Analysis.ipynb`           | Analyzes cleaned data, builds visualizations, and generates business insights |
| `Database_file_saving.ipynb` | Saves input files into SQLite database  |

---

## Tools & Technologies

- Python 
- `pandas`, `matplotlib`, `seaborn`
- `sqlite3` (built-in database module)
- Jupyter Notebook

---

## Data Cleaning Highlights (EDA)

- Dropped rows with missing `Description`, `CustomerID`, and `InvoiceNo`.
- Converted `InvoiceDate` to datetime format.
- Created new column `Amount = Quantity × UnitPrice` for revenue tracking.

---

## Key Business Insights (from Analysis.ipynb)

### 1. **Vendor Contribution Analysis**
- Using the Pareto chart:
  - Top **10 vendors** contributed to approximately **~70% of total purchasing revenue**.
  - After 15 vendors, contribution flattened — showing a long tail of low-contributing vendors.

### 2. **Product-Level Insights**
- Only a few products generated **most of the revenue** (Pareto principle).
   
### 3. **Cumulative Contribution Patterns**
- Both vendor and product cumulative charts showed a **sharp initial increase**, then **flattened**, confirming that **a small % of items/vendors drive the majority of business**.
---

## Files in this Repo

- `analysis.py`: Python script for data cleaning & analysis
- `vendor_data.db`: SQLite database
- `README.md`: Project explanation
