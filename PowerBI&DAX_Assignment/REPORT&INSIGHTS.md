# Agricultural Data Analysis - DAX Logic Report

## One-Page Written Explanation of DAX Logic

This analysis leverages Data Analysis Expressions (DAX) to transform raw agricultural data into dynamic, actionable insights. By creating calculated measures and columns, we can evaluate crop performance, resource efficiency, and livestock profitability across different regions.

## Measures and Logic Derived

### Total Crop Yield
- **Function**: `SUM`
- **Purpose**: Calculate the total crop yield in Kilograms from the Crop production table
- **Benefit**: Helps calculate the total harvest weight

### Average Yield per Crop
- **Function**: `AVERAGE`
- **Purpose**: Calculate the mean yield across all records
- **Implementation**: Used dynamically in a matrix visual with the crop type field
- **Benefit**: Ensures we understand the typical output for any given crop

### Top Performing Crop
- **Functions**: `TOPN`, `CALCULATE`, `ALL`
- **Purpose**: Dynamic measure to identify the top-performing crop by revenue
- **Logic**: 
  - Uses `TOPN` function to return the top 1 crop type from the entire table
  - Ignores filters with `ALL` function
  - Ranked by the `[Total Revenue]` measure in descending order
  - `CALCULATE` extracts the name of that top crop
- **Benefit**: Allows the "top crop" to change based on other filters applied to the report (e.g., per region)

### Region with Highest Yield
- **Functions**: `CALCULATE`, `TOPN`, `ALL`
- **Purpose**: Identify the top-performing region by total harvest weight
- **Benefit**: Demonstrates the power of `CALCULATE` to modify filter context dynamically

### Percentage Contribution per Crop
- **Functions**: `DIVIDE`, `CALCULATE`, `ALL`
- **Purpose**: Calculate the percentage of total revenue that each crop contributes
- **Logic**:
  - **Numerator**: Revenue for a specific crop (in the current filter context)
  - **Denominator**: Uses `CALCULATE` with `ALL` to remove the filter on crop type, giving the grand total revenue across all crops
  - **Calculation**: `DIVIDE` function safely handles the division

## Benefits and Impact

The combination of these DAX formulas transforms static data into an interactive analytical tool and this logic empowers users to:

- Quickly identify key trends
- Optimize resource allocation
- Improve overall agricultural decision-making

## Key Insights

### Revenue Dependency Analysis
- The percentage distribution of each crop to total revenue clearly visualizes the business's dependency on certain crops

### Strategic Decision Support
- By analyzing the top-performing crop by revenue, management can make data-driven decisions on:
  - Where to invest more resources
  - Promoting certain crops in specific regions
  - Negotiating better prices

### Production Capacity Assessment
- The total harvest weight provides a clear picture of overall production capacity