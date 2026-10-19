# Week 2: Product Analysis Dashboard

Second week of my [Power BI Journey](../README.md). This week I built a one-page **Product Analysis** dashboard on supermarket sales data (Jan to Mar 2019, three cities in Myanmar).

![Product Analysis dashboard](PBI-WEEK2_HW/dashboard.png)

## Files

| File | Description |
| ---- | ----------- |
| `questions.txt` | The 10 tasks for this week (in Azerbaijani) |
| `PBI-W2_HomeWork.pbix` | Power BI report file |
| `SuperMarket_Data.xlsx` | Source data (`Satış` and `Kateqoriya` sheets) |
| `dashboard.png` | Screenshot of the finished dashboard |

## Data

- **Satış** (sales): 1,000 rows. Product code, branch, city, customer type, gender, product category, unit price, quantity, total sales, date, time, payment method, profit, rating.
- **Kateqoriya** (category): 667 rows. Product ID, product category, date.

## What I did

1. Loaded the data with **Transform data** and checked column types, especially the `Time` column.
2. Created a **relationship** between `Kateqoriya[MəhsulID]` and `Satış[Məhsul kodu]`.
3. Built a **line chart** with a custom color and a larger, bold X axis (Segoe UI Bold).
4. Built a **bar chart** to compare product categories, with readable category names.
5. Added two **cards**: total sales amount and number of products sold.
6. Added a **map** that shows the sales by city.
7. Added a **slicer** for product category so every other visual can be filtered.
8. Built a **clustered column chart** for customer ratings by category.
9. Grouped product categories with **New group**.
10. Added a **title** to the report.

## Dashboard at a glance

| Visual | What it shows |
| ------ | ------------- |
| Cards | Total sales: **323K**, products sold: **5,510** |
| Bar chart | Profit by product category |
| Column chart | Rating by product category |
| Map | Sales by city (Yangon, Naypyitaw, Mandalay) |
| Line chart | Profit over time (Jan to Mar 2019) |
| Slicer | Filter by product category |

## What I learned

- Why the data type of a column (especially date and time) matters before building visuals.
- How a relationship lets visuals use fields from two tables together.
- How to format visuals so they are easy to read: colors, fonts, axis size, titles.
- How slicers make a dashboard interactive.

## Things I want to improve

- The `(Blank)` category in the charts comes from sales rows that have no match in the `Kateqoriya` table (it has 667 rows, `Satış` has 1,000). I will fix the relationship or use the category column from `Satış`.
- Show customer activity **by hour** with the `Time` column.
- Add a card for the **number of orders** next to the quantity card.
