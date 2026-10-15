# PBI-WEEK1_HW: Data Cleaning and Data Modeling with Power Query

Week 1 homework of my Power BI course (Data Science Academy). In this project I loaded an Excel file into Power BI, cleaned the data with **Power Query**, combined tables in three different ways (append, merge, unpivot), and connected two tables with a **many-to-many relationship**.

## Files

| File | Description |
|------|-------------|
| `questions.txt` | The 9 homework questions |
| `PBI-W1-HomeWork.pbix` | My Power BI solution file |

## Tables in the data model

| Table | What it is |
|-------|------------|
| `Müştəri detalları` | Customer details (customer code, name, product, amount) |
| `Total Sales` | `Satış1` and `Satış2` appended into one table |
| `AllCustomerDetails` | Customer details merged with Total Sales |
| `UNPİVOT` | Product columns turned into rows |

## What I did

| # | Task | Power Query feature used |
|---|------|--------------------------|
| 1 | Imported the Excel file | Get data, Excel workbook |
| 2 | Checked and fixed column types (text, number) | Changed Type |
| 3 | Removed the unwanted product codes from the customer details table | Filtered Rows |
| 4 | Combined `Satış1` and `Satış2` into `Total Sales` | Append Queries as New |
| 5 | Turned customer codes into whole numbers in a new `Customer Codes` column | Column From Examples, Replace Values, Whole number type |
| 6 | Added a `Sales Analysis` column with the values `high` and `low` (threshold: 135) | Conditional Column |
| 7 | Joined customer details with total sales into `AllCustomerDetails` | Merge Queries as New (Left Outer join) |
| 8 | Turned the product columns into rows | Unpivot Other Columns |
| 9 | Closed and applied, then created a relationship between `Total Sales` and `Müştəri detalları` on `Customer Codes` | Many-to-Many relationship |

## What I learned

- Power Query is the place to clean data **before** building any chart.
- **Append** stacks tables on top of each other, **Merge** joins tables side by side (like a SQL JOIN), and **Unpivot** turns columns into rows.
- Many-to-many relationships are possible, but only make sense when the column used for the connection has repeated values on both sides.

## How to open

1. Install Power BI Desktop (Windows).
2. Open `PBI-W1-HomeWork.pbix`.
3. The data comes from a local Excel file that is not included in this repo. To refresh the data, go to **Transform data > Data source settings** and point it to your own copy of the file.

## Tools

Power BI Desktop, Power Query, Excel
