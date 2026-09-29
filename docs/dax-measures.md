# DAX Measures

To copy a formula: click the measure in the Data pane and copy it from the formula bar. Paste each one below with a one-line explanation.

## Confirmed

```DAX
Gross Profit Margin % =
DIVIDE ( [Gross Profit], [Total Revenue] )
```
Gross profit as a share of revenue. Formatted as a percentage.

> Check: Gross Profit is measured on completed orders but the denominator is Total Revenue (all orders). Dividing by Completed Revenue instead gives a slightly higher margin. State which you intend.

```DAX
Month Short = FORMAT ( Dim_Date[Date], "mmm yy" )
```
Calculated column on Dim_Date. Sorted by MonthSortKey so months appear in date order.

## To add (paste formulas)

| Measure | Formula | What it shows |
|---|---|---|
| Completed Revenue | | Revenue from completed orders |
| Gross Profit | | Profit on completed orders |
| Completed Orders | | Count of completed orders |
| Units Sold (Completed) | | Units on completed orders |
| Total Revenue | | Revenue across all orders |
| Total Orders | | All orders |
| % of Total Orders | | Share of orders by category |
| % of Total Revenue | | Share of revenue by category |
| Logistics Cost % of Revenue | | Logistics cost divided by revenue |
| Avg Logistics Cost | | Average logistics cost per order |
| Avg Delivery Lag | | Average delivery lag in days |
| Avg Order Value | | Average revenue per order |
| Avg Discount % | | Average discount |
| Customer Lifetime Revenue | | Revenue per customer |
| Return Count / Cancelled Count | | Returned and cancelled orders |