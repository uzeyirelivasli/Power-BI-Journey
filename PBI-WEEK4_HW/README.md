# Week 4: Data Professional Survey Dashboard

For Week 4 I took a raw survey of data professionals (630 answers), cleaned it in Power Query, and built a one-page dashboard that shows who answered, what they earn, which programming language they prefer, and how happy they are at work.

## Files in this folder

| File | What it is |
| ---- | ---------- |
| `PowerBI-Week4.xlsx` | The raw survey data (1 sheet, 630 rows, 28 columns) |
| `PBI-Week4.pbix` | My Power BI file with the cleaning steps and the dashboard |
| `Week4_Dashboard.png` | Screenshot of the finished dashboard |

## Dashboard

![Week 4 dashboard](Week4_Dashboard.png)

## Step 1: Cleaning the data in Power Query

The raw data had many messy columns, so I cleaned it before building any visual:

- **Removed empty columns:** `Browser`, `OS`, `City`, `Country`, `Referrer` had no data.
- **Fixed data types:** dates as Date, times as Time, happiness scores and age as whole numbers, everything else as text.
- **Cleaned job titles:** split `Q1` at the `(` character and kept only the first part, so the extra text in brackets is gone.
- **Cleaned the programming language column:** split `Q5` at `:` so answers like "Other (Please Specify): Go" became just "Other".
- **Cleaned industry and country:** split `Q4` and `Q11` at `(` and kept the first part. Any country that was typed in by hand became "Other".
- **Created an `AverageSalary` column:** salaries came as text ranges like `41k-65k`, which cannot be averaged. I duplicated the column, split it into the lower and upper number, removed the `k` and `-` characters, and took the middle of the two numbers. For `225k+` I used 225.

## Step 2: Dashboard

| Visual | What it shows |
| ------ | ------------- |
| **Treemap** | Country of survey takers |
| **Bar chart** | Average salary by job title, sorted from high to low |
| **Stacked column chart** | Favorite programming language, split by job title |
| **Card** | Average age of survey takers |
| **Card** | Number of survey takers |
| **Gauge** | Happiness with salary (scale 0 to 10) |
| **Gauge** | Happiness with work-life balance (scale 0 to 10) |

I also added a title banner, and used one color theme across all visuals so the page looks clean.

## Key results

- **630** people answered the survey, with an average age of **29.87**.
- **Python is the clear favorite**: 420 of 630 people (67%) chose it, far ahead of R (101).
- **Data Scientists earn the most** on average (about $94K per year), compared with about $65K for Data Engineers and about $55K for Data Analysts. Salary values are in thousands of USD.
- **Salary is the weak spot:** people rate happiness with salary at only **4.27 out of 10**, lower than work-life balance (**5.74 out of 10**).
- The **United States** is the biggest single country (261 answers), followed by India (73), the United Kingdom (40) and Canada (32).

## Things to keep in mind

- Average salary is an estimate. It uses the middle of each salary range, not the real salary.
- Some job titles have very few answers (3 Data Architects, 5 Database Developers), so their averages are not reliable. Data Analysts are 381 of the 630 answers.
- "Other" countries add up to 224 answers (36%), because each country outside the top four was grouped into "Other".
- The happiness averages ignore blank answers (7 for salary, 10 for work-life balance).

## What I learned

- Cleaning data in Power Query (splitting columns, replacing values, changing types) takes more time than building the charts, and it decides how good the charts are.
- A text range like `41k-65k` can be turned into a number you can calculate with.
- Which visual to use depends on the question: treemap for parts of a whole, bar chart for ranking, gauge for a score out of 10, card for one key number.

## Tools

Power BI Desktop, Power Query, Excel
