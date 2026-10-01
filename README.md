# Sales Analysis – Power BI

An end-to-end data analysis project: cleaning raw sales data with **Power Query**, building a **data model**, and presenting the results in an interactive **Power BI** report.

> This is a practice project built to sharpen my data analysis skills.

## Report Preview

![Report preview](images/report-preview.png)

## Project Goals

- Clean and prepare messy sales data
- Build a proper relational data model
- Create measures and visuals that answer real business questions
- Present the results in a clear, interactive dashboard

## Data

The project uses the following tables (Arabic column names):

| Table | Description |
|-------|-------------|
| المبيعات (Sales) | Main fact table: orders, quantities, unit prices, discounts, totals |
| الموظفين (Employees) | Employee details, including hire dates |
| المنتجات (Products) | Product details and unit prices |
| العملاء (Customers) | Customer details |
| الفئات (Categories) | Product categories |

## Data Cleaning (Power Query)

- Filled missing employee numbers in the sales table by matching against the employees table
- Extracted clean numeric values from the unit price column (it mixed Arabic-Indic digits with currency text)
- Recalculated missing totals as `Quantity × Unit Price` after applying the discount
- Normalized the discount column (it mixed fractions like `0.1` and whole numbers like `10`)
- Treated negative quantities as returns, so their totals come out negative
- Handled missing values in hire dates and product prices
- Added a custom tax column

## Data Model

A star-schema style model with the sales table at the center, related to the employees, products, customers, and categories tables.

## Key Insights

<!-- Replace with your own findings -->
- Insight 1: ...
- Insight 2: ...
- Insight 3: ...

## Tools Used

- Power BI Desktop
- Power Query (M)
- DAX

## Files

- `sales-analysis.pbix`: the Power BI report
- `images/`: report screenshots
- `data/`: source data files (if included)

## How to Open

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
2. Download the `.pbix` file from this repository
3. Open it in Power BI Desktop

## Author

**Your Name**
[LinkedIn](https://linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)
