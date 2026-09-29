# Data Dictionary

Tables and columns in the Power BI model.

## Facts table (one row per order)

| Column | Description |
|---|---|
| Order ID | Unique order reference. Prefixes vary (LC, LCL-, ORD, CAR) and are kept as recorded |
| OrderDateKey | Key to Dim_Date for the order date |
| DeliveryDateKey | Key to Dim_Date for the delivery date |
| BranchKey | Key to Dim_Branch |
| CustomerKey | Key to Dim_Customer |
| VehicleKey | Key to Dim_Vehicle |
| GeographyKey | Key to Dim_Geography |
| LeadSourceKey | Key to Dim_LeadSource |
| SalesRepKey | Key to Dim_SalesRep |
| Units Sold | Number of vehicles on the order |
| Unit Cost | Cost per vehicle |
| Unit Selling Price | Selling price per vehicle |
| Total Cost | Total cost of the order |
| Total Revenue | Total revenue of the order |
| Discount | Discount applied to the order |
| Discount Bracket | Discount grouped into bands (0%, 0-5%, 5-10%, 10-15%, 15%+) |
| Payment Method | M-Pesa, Cash, Cheque, Bank Transfer, Asset Finance or RTGS |
| Payment Status | Paid, Partially Paid, Pending, Cancelled or Refunded |
| Delivery Status | In Transit, Delivered, Delayed, Cancelled, At Yard or Not Recorded |
| Delivery Lag | Delivery lag in days. Negative values are kept and shown on the Order Investigation page |
| Delivery Fee | Fee charged for delivery |
| Logistics Cost | Cost of delivering the vehicle |
| Price to Cost Ratio | Selling price divided by cost. Extreme values are surfaced on the Order Investigation page |
| Customer Rating / Rating Bracket | Customer rating and its grouped band (for example 4-5, 3-4, 2-3, Not rated) |
| Review Count | Number of reviews |
| Returned / Return Count | Whether the order was returned, and the number of returns |
| Flag for Investigation | Set to "Investigate" for orders selected for review |

## Dim_Branch

| Column | Description |
|---|---|
| BranchKey | Primary key |
| Branch | Nairobi HQ, Mombasa Port Yard, Athi River Yard, Kakamega Yard, Thika Yard, Eldoret Yard, Kisumu Yard or Nakuru Yard |

## Dim_Customer

| Column | Description |
|---|---|
| CustomerKey | Primary key. Customers are identified by this key, not by name |
| Customer Name | Customer name |
| Customer Type | Dealer, Government, NGO, Corporate or Individual |
| Customer Age | Age of the customer relationship or customer, as recorded in the source |

## Dim_Date

| Column | Description |
|---|---|
| DateKey | Primary key |
| Date | Calendar date |
| Year, Quarter, Month, MonthName, MonthNum, Weekday | Calendar attributes |
| MonthSortKey | Year and month number, used to sort months in date order |
| Month Short | Calculated column in the form "Jan 25", sorted by MonthSortKey |

## Dim_Geography

| Column | Description |
|---|---|
| GeographyKey | Primary key |
| City, County | Location |
| Region | Central, Coast, Eastern, Nairobi, Nyanza, Rift Valley or Western |

## Dim_LeadSource
Lead source (sales channel) attributes, keyed by LeadSourceKey.

## Dim_SalesRep
Sales representative attributes, keyed by SalesRepKey.

## Dim_Vehicle

| Column | Description |
|---|---|
| VehicleKey | Primary key |
| Car Make, Car Model | Manufacturer and model |
| Vehicle Type | SUV, Sedan, Pickup, Hatchback, Crossover, Wagon, Truck or Van |
| Vehicle Year | Model year of the vehicle (not the order year) |
| Fuel Type, Transmission, Color | Vehicle attributes |

## Delivery Breakdown (field parameter)
A helper table that lets one matrix switch between Region, Branch and Vehicle Type.
