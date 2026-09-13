# Candy Sales Analysis

A Python-based exploratory data analysis project examining candy distribution and sales patterns over time using Pandas and Plotly.

## Project Overview

This project analyzes candy sales data recorded across multiple dates from December 2022 to January 2024.

The objective is to transform the raw dataset into an analysis-friendly format, compare candy performance by color, examine descriptive statistics, and visualize changes in total candy counts over time.

The project demonstrates a simple analytical workflow:

**Raw Data → Data Transformation → Aggregation → Analysis → Visualization → Insights**

---

## Objectives

The analysis focuses on answering the following questions:

- Which candy color has the highest total count?
- How is the overall candy distribution divided across colors?
- How do candy counts vary across recorded dates?
- Are there noticeable spikes or changes over time?
- How can a wide-format dataset be transformed for easier analysis and visualization?

---

## Dataset

The dataset contains the following columns:

| Column | Description |
|---|---|
| `date` | Date of the recorded observation |
| `red` | Number of red candies |
| `orange` | Number of orange candies |
| `yellow` | Number of yellow candies |
| `green` | Number of green candies |
| `blue` | Number of blue candies |
| `total` | Total number of candies recorded |

The dataset contains observations spanning from **December 2022 to January 2024**.

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Plotly Express
- Jupyter Notebook

---

## Data Preparation

The original dataset was stored in wide format, with each candy color represented as a separate column.

The date column was first converted into a proper datetime format:

```python
df['date'] = pd.to_datetime(df['date'])

The dataset was then transformed from wide format into long format using Pandas melt():

df = df.melt(
    id_vars='date',
    var_name='candy',
    value_name='count'
)

This structure makes it easier to:

compare candy categories
calculate aggregated values
generate grouped statistics
create visualizations
Exploratory Analysis
Candy Distribution

Candy counts were aggregated by color using Pandas groupby().

The total number of candies recorded was 1,279.

Candy Color	Total Count	Share
Red	441	34.5%
Orange	219	17.1%
Green	213	16.7%
Blue	207	16.2%
Yellow	199	15.6%
Key Observation

Red candy was clearly the most frequently recorded color, accounting for approximately 34.5% of all candies.

The remaining four colors were distributed relatively evenly, each contributing approximately 15–17% of the total.

Descriptive Statistics

The analysis also examined descriptive statistics for each candy color, including:

mean
standard deviation
minimum
maximum
quartiles
total count

For example, red candy had:

Metric	Value
Total	441
Mean	7.35
Minimum	2
Median	7
Maximum	12

This indicates that red candy consistently appeared in larger quantities than the other individual colors.

Visualizations
1. Candy Distribution by Color

This visualization compares the total count of each candy color.

<!-- Add the exported chart to: assets/candy-distribution.png Then remove this comment and uncomment the line below. ![Candy Distribution](assets/candy-distribution.png) -->
2. Candy Counts Over Time

A time-series visualization was created to examine how total candy counts changed across the recorded dates.

<!-- Add the exported chart to: assets/candy-over-time.png Then remove this comment and uncomment the line below. ![Candy Counts Over Time](assets/candy-over-time.png) -->
Key Findings

The analysis produced several clear observations:

Red candy dominated the dataset

Red recorded a total count of 441, approximately twice the total of any other individual color.

The remaining colors were relatively balanced

Orange, green, blue, and yellow each contributed between approximately 15% and 17% of the total candy count.

Candy totals were generally stable across many observations

Most recorded totals remained within a relatively narrow range, although several dates showed noticeable spikes.

Data reshaping simplified the analysis

Converting the original wide dataset into long format made aggregation and visualization significantly easier.

Analytical Workflow
Raw CSV Data
      ↓
Load with Pandas
      ↓
Convert Date Column
      ↓
Reshape with melt()
      ↓
Aggregate with groupby()
      ↓
Descriptive Statistics
      ↓
Time-Series Analysis
      ↓
Plotly Visualizations
      ↓
Insights
Skills Demonstrated

This project demonstrates practical use of:

Exploratory Data Analysis
Data Cleaning
Data Transformation
Data Reshaping
Pandas melt()
Pandas groupby()
Aggregation
Descriptive Statistics
Time-Series Analysis
Data Visualization
Plotly Express
Jupyter Notebook

Future Improvements

This project can be expanded by:

aggregating results by month
calculating percentage contribution over time
comparing month-to-month changes
identifying unusual spikes or outliers
improving chart titles and annotations
creating an interactive dashboard
adding automated data validation
separating data preparation and analysis into clearer notebook sections
Project Limitations

This project focuses primarily on exploratory analysis of candy counts.

The dataset does not contain additional business variables such as:

product prices
revenue
cost
customers
geographic information
inventory

Therefore, the analysis should not be interpreted as profitability or customer behavior analysis.

Author

Tsani Fauzan Alhakim

Aspiring Data Analyst focused on Python, SQL, Power BI, Excel, data visualization, and business analytics.

Portfolio: tsanialhkm.github.io
GitHub: github.com/TsaniAlhkm
