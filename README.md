# Sales Data Analysis Project

This project is a **complete data analysis pipeline** built using Python and Google Colab. It analyzes daily electronic product sales over multiple months, focusing on product and regional performance, as well as overall revenue trends.

## Project Overview

- Dataset: Daily sales transactions for multiple products (Phone, Laptop, Tablet, Headphones, Monitor) with quantity, price, region, and total sales.  
- Goal: Understand which products and regions generate the most revenue, and how total sales change over time.  
- Tools: Python, pandas, matplotlib, Google Colab.

## Dataset Description

The dataset contains one row per sales transaction with the following columns:

- `Date`: Date of the transaction (YYYY-MM-DD).  
- `Product`: Product type sold (e.g., Phone, Laptop, Tablet, etc.).  
- `Quantity`: Number of units sold in the transaction.  
- `Price`: Price per unit.  
- `Customer_ID`: Unique identifier for the customer.  
- `Region`: Geographical region of the sale (e.g., North, South, East, West).  
- `Total_Sales`: Total revenue for the transaction (Quantity × Price).

## Analysis Pipeline

1. **Data Loading**  
   - Load the CSV file into a pandas DataFrame.  
   - Verify that all required columns are present.

2. **Data Cleaning**  
   - Convert the `Date` column to datetime.  
   - Convert `Quantity`, `Price`, and `Total_Sales` to numeric types.  
   - Drop rows with missing or invalid critical values.  
   - Recalculate `Total_Sales` as `Quantity * Price` for consistency.  
   - Create a derived `Month` column from the `Date`.

3. **Exploratory Analysis**  
   - Compute total sales by product.  
   - Compute total sales by region.  
   - Compute total sales by month.  
   - Inspect basic statistics and sample rows to understand the distribution of values.

4. **Visualizations**  
   The project includes at least two different chart types:

   - Bar chart: Total sales by product.  
   - Line chart: Total monthly sales.  
   - Optional pie chart: Sales share by region.

5. **Insights and Conclusions**  
   The notebook/report summarizes key findings, such as:

   - Which product categories generate the highest revenue.  
   - Which regions contribute most to overall sales.  
   - How total sales evolve across different months.

## Files and Structure

Suggested project structure:

```text
.
├── README.md
├── analysis.ipynb        # Google Colab notebook (exported)
├── data
│   └── sales_data.csv    # Input dataset
├── visualizations
│   ├── sales_by_product.png
│   ├── monthly_sales.png
│   └── sales_by_region_pie.png (optional)
└── report
    └── final_report.md or final_report.pdf
```

## How to Run (Google Colab)

1. Open Google Colab and upload `analysis.ipynb`.  
2. Upload `sales_data.csv` to the Colab environment (or mount Google Drive and place it in a `data/` folder).  
3. Run all cells from top to bottom:  
   - Data loading and cleaning.  
   - Analysis and aggregations.  
   - Visualizations and insight cells.  
4. Review the printed tables and generated charts.  
5. Export the notebook or report as PDF/HTML if required for submission.

## Technical Requirements Checklist

- [x] Data loading and validation.  
- [x] Data cleaning (types, missing values, recalculated totals).  
- [x] Basic analysis (grouped metrics by product, region, and time).  
- [x] At least two chart types (bar, line, optional pie).  
- [x] Written insights summarizing the findings.  
- [x] Clear project structure and documentation.

## Future Improvements

- Add interactive visualizations (e.g., Plotly).  
- Build a simple dashboard for non-technical users.  
- Extend analysis with profit margins, discounts, or customer segmentation if more columns are available.
