
# TOP SELLING PRODUCTS

### Dashboard Snap : ![Screenshot 2024-09-02 221148](https://github.com/user-attachments/assets/5ab933e3-6c59-4afd-97d9-b6748b0f8e60)


## Problem Statement

Project Description:  
This project addresses the need to analyze the performance of newly launched products to determine which products are truly excelling in terms of sales. The insights generated will be used to make informed decisions about inventory management, marketing strategies, and future product development.


### Dashboard Features:
#### Yearly Product Sales Overview:

The dashboard provides an overview of all products launched over the past years. This allows stakeholders to grasp the overall performance of each product over time.

#### Highlight Top Performers:  
The dashboard lists products that consistently top the sales charts, helping to identify and celebrate the most successful products.

#### Visual Representation of Product Sales:
A bar chart visually represents product sales, making it easy to understand the hierarchy of product performance.

#### Product Sales Trends Over Time:
The dashboard allows users to observe the sales trends of newly launched products over time, determining whether there is sustained interest or a decline in sales.

#### Correlation with Marketing Efforts:
By analyzing sales data alongside marketing campaigns and promotions, the dashboard helps evaluate the effectiveness of marketing pushes, highlighting any correlations between campaigns and sales spikes.

### Key Performance Indicators (KPIs):
#### Top Selling Products:
Identifies the products that generate the most sales over a specified period, helping the business understand market demands and customer preferences.
#### Applications:
#### Inventory Management:
Helps in aligning inventory with the demand for top-selling products.
#### Promotional Campaigns:
Aids in optimizing marketing efforts based on product performance.
#### Future Product Development:
Guides the development of new products by understanding customer preferences and market trends.

### Implementation Details:
#### 1. Date Table Creation:

A custom date table was created to provide meaningful time-based insights.

Date Table Code:

Date = 
VAR MinYear = YEAR(MIN('Top Selling Product'[Sale Date]))
VAR MaxYear = YEAR(MAX('Top Selling Product'[Sale Date]))
RETURN
ADDCOLUMNS(
    FILTER(
        CALENDARAUTO(),
        AND(YEAR([Date]) >= MinYear, YEAR([Date]) <= MaxYear)
    ),
    "Year", YEAR([Date]),
    "Month Name", FORMAT([Date], "mmmm"),
    "Month Name Short", FORMAT([Date], "mmm"),
    "Month Number", MONTH([Date]),
    "Quarter Name", "Q" & FORMAT([Date], "Q YYYY"),
    "Quarter Number", FORMAT([Date], "YYYYQ")
)


#### 2. Slicers Implementation:

Four slicers were created: Region, Marketing Campaign, Sales Team, and Month & Year to filter data and provide meaningful insights.

#### 3. Stacked Column Chart:

A stacked column chart was used to visualize top sales by product name, offering a clear comparison of product performance.
#### 4.Line Chart:

A line chart was implemented to track the sales of top-selling products by month name, highlighting trends and patterns.
#### 5.Matrix Table:

A matrix table was created to analyze sales based on campaign, month, and product name, allowing for detailed performance evaluation.




### How to Use:
#### Interactive Filters:
Use the slicers to filter the data by region, marketing campaign, sales team, or specific time periods to tailor the insights according to your needs.

#### Visual Analysis:
Leverage the visualizations (bar and line charts) to quickly understand which products are performing well and how their performance is trending over time.

#### Decision-Making:
Utilize the insights from the matrix table and correlation analysis to make informed decisions about inventory management, marketing efforts, and product development.

This project serves as a comprehensive tool for recognizing the top-selling products and aligning business strategies with market demands.
