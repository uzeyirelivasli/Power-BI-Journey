# Power BI Journey

My learning journey into Power BI, as part of my path to becoming a data scientist.

I am documenting everything I learn here: homework, practice files, and dashboards. The repo is updated at the end of every week.

**Started:** 13 October 2026

---

## About me

I graduated in marketing from Azerbaijan State University of Economics and I am moving into data science. I already work with Python Libraries(Pandas, NumPy) Excel , SQL , ML & NN models. Power BI is the next tool I am adding, so I can turn data into dashboards that people can understand and use.

## Goals

- Learn to load, clean, and model data in Power BI
- Build clear and interactive dashboards
- Learn basic DAX (formulas for calculations)
- Finish with a portfolio-ready dashboard project

## Learning plan (4 weeks)

| Week | Topic | Folder | Status |
| ---- | ----- | ------ | ------ |
| 1 | Power Query: data cleaning, append, merge, unpivot, relationships | [PBI-WEEK1_HW](PBI-WEEK1_HW) | Done |
| 2 | Data modeling, relationships, first dashboard: visuals, slicers, formatting | [PBI-WEEK2_HW](PBI-WEEK2_HW) | Done |
| 3 | Basic DAX, advanced visuals, interactivity | PBI-WEEK3_HW | Not started |
| 4 | Final dashboard project | PBI-WEEK4_HW | Not started |

> I update this table every week.

## Weekly log

### Week 1: Power Query and data modeling

Folder: [PBI-WEEK1_HW](PBI-WEEK1_HW)

- Imported an Excel file and fixed column data types
- Filtered rows and created a whole-number `Customer Codes` column
- Combined two sales tables with **Append**, and joined tables with **Merge**
- Used **Unpivot Other Columns** to turn product columns into rows
- Added a conditional column (`Sales Analysis`: high / low)
- Created a **many-to-many relationship** between two tables

### Week 2: Product analysis dashboard

Folder: [PBI-WEEK2_HW](PBI-WEEK2_HW)

![Week 2 dashboard](PBI-WEEK2_HW/dashboard.png)

- Loaded the supermarket data with **Transform data** and checked column types, especially `Time`
- Created a **relationship** between the category and sales tables (`MəhsulID` and `Məhsul kodu`)
- Built a **line chart** (custom color, bold and larger X axis) and a **bar chart** for categories
- Added **cards** for total sales and products sold, and a **map** for sales by city
- Added a **slicer** for product category to filter all visuals
- Built a **clustered column chart** for ratings by category
- Grouped product categories with **New group** and added a report **title**

### Week 3

*(coming soon)*

### Week 4

*(coming soon)*

## Repository structure

```
Power-BI-Journey/
├── README.md
├── PBI-WEEK1_HW/
│   ├── README.md
│   ├── questions.txt
│   └── PBI-W1-HomeWork.pbix
└── PBI-WEEK2_HW/
    ├── README.md
    ├── questions.txt
    ├── dashboard.png
    ├── PBI-W2_HomeWork.pbix
    └── SuperMarket_Data.xlsx
```

More folders will be added each week.

## Tools

- Power BI Desktop
- Power Query
- Excel / CSV datasets

## Contact

- LinkedIn: [*uzeyirelivasli*](https://www.linkedin.com/in/uzeyirelivasli/)
- GitHub: [uzeyirelivasli](https://github.com/uzeyirelivasli)
