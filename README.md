# 📊 E-Commerce Sales Dashboard | Power BI

An interactive Power BI dashboard that analyses sales, profit and payment behaviour of an e-commerce store
(500 orders, 1,500 line items, Jan-Dec 2018), built with Power Query, a two-table data model and DAX measures.

![Dashboard](dashboard.png)

### Interactive demo
![Demo](demo.gif)

## Dataset
Source: <add the name or link of where you downloaded the dataset>
- `Orders.csv` (500 rows): Order ID, Order Date, CustomerName, State, City
- `Details.csv` (1,500 rows): Order ID, Amount, Profit, Quantity, Category, Sub-Category, PaymentMode

## Data preparation (Power Query)
- Loaded both CSVs and set data types (Order ID as text, Order Date as date)
- Validated the data: no nulls, duplicates or orphan Order IDs
- Trimmed text fields (State, City, CustomerName); one state had trailing spaces

## Data model
`Details` to `Orders`, many-to-one on Order ID.

## DAX measures
Total Revenue, Total Profit, Units Sold, Total Orders, AOV (Revenue / Orders),
Profit Margin % (Profit / Revenue), Loss Line % (share of line items with negative profit).

## Dashboard features
- 5 KPI cards, Quarter and State slicers, cross-filtering across all visuals
- Top 5 states by profit; Top 5 and Bottom 5 sub-categories by profit
- Monthly profit trend; units sold by category and by payment mode

## Key insights
- Revenue 437,771 | Profit 36,963 | 5,615 units | AOV 875.54 | Profit margin 8.4%
- 35.3% of line items are loss-making, which keeps the overall margin low
- Madhya Pradesh leads on profit (7,382) while Maharashtra leads on revenue, so sales rank alone does not show profit rank
- Rajasthan and Andhra Pradesh are loss-making states
- 5 of 17 sub-categories lose money (total -2,296); Furnishings is the largest (-806), Printers earns the most (8,606)
- Profit is negative in May, Jul, Sep and Dec; November peaks at 10.3K
- Clothing is 63% of units sold; Cash on Delivery is 44% of units, UPI 21%

## How to run
Keep `Orders.csv` and `Details.csv` in one folder, open the `.pbix` in Power BI Desktop,
update the Source path of both queries in Power Query to that folder, and click Refresh.

## Author
Nidhi Gupta | [LinkedIn](https://www.linkedin.com/in/nidhigupta1997) | [GitHub](https://github.com/nidhigupta868714-ai)
