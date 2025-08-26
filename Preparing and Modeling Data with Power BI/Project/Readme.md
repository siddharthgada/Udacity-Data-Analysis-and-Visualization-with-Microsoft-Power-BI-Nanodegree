# Seven Sages Brewing Company - Power BI Sales & Profitability Analysis

## Project Overview
This project involves building a comprehensive **Power BI data model and report** for Seven Sages Brewing Company (SSBC). The goal is to provide the CFO with actionable insights on **beer sales performance, profitability, and seasonal trends**. By consolidating data from multiple sources, this project solves the challenge of data silos and creates a foundation for advanced reporting, DAX calculations, and scalable data models.

---

## Project Steps

### 1. Source Data & Data Model Planning
- Review all source files provided by SSBC.
- Sketch a data model including **fact tables** (Sales) and **dimension tables** (e.g., Products, Customers, Currency and Date).
- Identify keys for relationships between tables.
- Decide which tables to **merge or append** to optimize the model.

### 2. Load and Transform Data (Power Query)
- Use **Get Data** to load data into Power BI.
- Clean and format datasets for consistency.
- Appended monthly sales data to create one fact table  
- Ensure fields have **logical names** and proper data types.

### 3. Create a Dynamic Date Table
- Build a continuous date table in **Power Query** to support time intelligence.
- Include:
  - Calendar year, month and month number
  - Fiscal year, fiscal quarter, fiscal period
- Note: SSBC’s fiscal year runs **Oct 1 – Sept 30**.

### 4. Build Relationships
- Establish relationships from dimension tables to fact tables for accurate reporting.
- Link currency tables to Sales to handle multi-currency calculations.

### 5. Define DAX Measures
Create measures to satisfy CFO requirements:

1. **Sales in USD**  
2. **Cost of Sales in USD**  
3. **Gross Profit Margin (%)**  
4. **Sales in CAD**  
5. **Unit Sales by Product**  
6. **Gross Profit by Product**  

### 6. Build Reports

#### Report 1 – Sales and GPM
- Label tab: `Sales and GPM`
- Add **Card visuals**: `Sales USD` and `Sales CAD`
- Build a **Matrix**:
  - Rows: `Customer Type`, `Customer`
  - Columns: `FY Quarter`
  - Values: `Sales USD`, `GPM (US)`
- Executive Summary: While the highest sales by customer type are "Distributors", the highest gross profit margins are 60.82%. Among individual customers, the highest sales for the year are $52,676 by
customer "Barrel's Best" Distributor, while the highest gross profit margins are with "The Black Bear" Bar at 37.93% other than the SSBC Tasting Room, which has a gross profit margin of 60.82%.

#### Report 2 – Gross Profit and Unit Sales
- Label tab: `Gross Profit and Unit Sales`
- Build a **Matrix**:
  - Rows: `Product Name`
  - Columns: `Unit Sales %`, `Gross Profit Margin`
- Executive Summary: "Bamboo Grove Maibock" has the highest percentage of Units sold (29.41%) compared to other products. "Bamboo Grove Maibock" has the highest gross profit margin (31.67%) compared to other products. Although "Imperial Poet Porter" and "Henan Hops Wheat Beer" are not sold as much as other products, they still have a high gross profit margin (30.63% and 20.20% respectively). The sales team can review these products to market them better for increased sales and profits.

#### Report 3 – Product Type Profitability
- Label tab: `SO1 - Product Type`
- Add a **Calculated Column**: `Gross Profit` (`Sales - Cost`)
- Build a **Matrix**:
  - Rows: `Product Type`, `Product Name`
  - Values: `Quantity`, `Gross Profit`
- Expand hierarchy and sort by `Average Gross Profit per Serving`
- Executive Summary: Kegs are most profitable on average, and the most profitable keg in the product line is the "Henan Hops Wheat Beer" keg; each unit sold makes a gross profit of $113.8. Six-packs are the least profitable for all the products. The least profitable is the "Scholar's Saison" six-pack; each unit sold costs us $0.14 (Loss).

#### Report 4 – Seasonality
- Label tab: `SO2 - Seasonality`
- Build a **Matrix**:
  - Rows: `Product Name`
  - Columns: `Year`, `Month`
  - Values: `Unit Sales %`
- Executive Summary: Sales of units are high during Summer and Fall and low during winter, except for Imperial Poet Porte, which has the highest sales in January and the lowest in May & June.
Drill Down:
- Bamboo Grove Maibock: Highest number of units are sold in May (43.79%) and lowest in September (21.74%)•
- Han Dynasty Spiced Lager: Highest number of units are sold in May (12.42%) and lowest in January (8.28%)•
- Henan Hops Wheat Beer: The Highest number of units is sold in September (26.09%) and the lowest in August (13.64%)•
- Imperial Poet Porter: Highest number of units are sold in January (33.14%) and lowest in May & June (3.92%)•
- Liu Ling's IPA: The Highest number of units is sold in April (10.49%) and the lowest in January (7.10%)•
- Scholar's Saison: The Highest number of units are sold in June (30.07%) and the lowest in January (8.88%)

---

## Key Learnings
- Combining data from multiple sources into a **centralized model**  
- Cleaning and transforming data in Power Query  
- Creating a **dynamic date table** for fiscal year reporting  
- Building **relationships between fact and dimension tables**  
- Writing **DAX measures** for sales, costs, profitability and unit metrics  
- Developing **executive-friendly Power BI reports** with cards, matrices and summaries  
- Analyzing **product performance and seasonality trends**  

---

## Technologies Used
- **Power BI Desktop**  
- **Power Query**  
- **DAX (Data Analysis Expressions)**  

---

## Project Outcome
A robust, interactive Power BI dashboard that allows SSBC's CFO to make **data-driven decisions** regarding beer production, pricing, and marketing strategy. This project demonstrates **core BI principles** that are scalable for more advanced reporting and larger datasets.
