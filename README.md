# Sales Budget & Forecast Analysis - Power BI Project

## Overview
An interactive Power BI dashboard that analyzes historical sales data and compares it with budget and forecast values. The project helps identify sales trends, variances, and future projections to support data-driven business decisions.

## Dataset
- **Budgets and Forecasts.xlsx**: Contains historical sales data along with budgeted and forecasted values across different time periods and categories.
- **budget and forecast on sales data.pbix**: The main Power BI report file with dashboards, measures, and visualizations.

## Key Features
- **Sales Performance Analysis**: Compare actual sales vs budgeted vs forecasted values.
- **Variance Tracking**: Identify positive and negative variances between actual and budget/forecast.
- **Trend Visualization**: Line and bar charts showing sales trends over time.
- **Interactive Filters**: Filter data by date, product category, region, or sales channel.
- **Forecasting**: Built-in Power BI forecasting to predict future sales based on historical patterns.

## Tools & Technologies
- **Power BI Desktop** - For data modeling and visualization
- **Excel** - For source data storage and initial cleaning
- **DAX** - For creating calculated measures and KPIs

## Project Structure
/data
  Budgets and Forecasts.xlsx - Raw sales and budget data
budget and forecast on sales data.pbix - Power BI dashboard file
README.md - Project documentation

## Dashboard Insights
1. **KPI Cards**: Total Sales, Total Budget, Total Forecast, Overall Variance %
2. **Variance Analysis**: Bar chart showing variance by month/category
3. **Trend Line**: Actual vs Budget vs Forecast over time
4. **Category Breakdown**: Sales distribution by product or region

## How to Use
1. **Open the Report**:
   - Install Power BI Desktop from Microsoft
   - Open `budget and forecast on sales data.pbix`
2. **Refresh Data**:
   - Click `Refresh` in Power BI to load the latest data from `Budgets and Forecasts.xlsx`
   - Ensure the Excel file path remains unchanged or update the data source in Power BI
3. **Interact with Dashboard**:
   - Use slicers to filter by date range, category, or region
   - Hover over charts for detailed tooltips

## Key DAX Measures Used
```dax
Total Sales = SUM('Sales'[ActualAmount])
Total Budget = SUM('Sales'[BudgetAmount]) 
Total Forecast = SUM('Sales'[ForecastAmount])
Variance = [Total Sales] - [Total Budget]
Variance % = DIVIDE([Variance], [Total Budget])
