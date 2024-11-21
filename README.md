# Business-Insights-360

## Problem Statement

AtliQ is a rapidly expanding technology firm that offers a wide range of products to consumers across numerous nations via different distribution methods, such as retail outlets, direct sales, and networks of distributors, both on the internet and in physical stores. To fuel its expansion and make informed choices based on data, AtliQ requires a team dedicated to data analytics. This initiative aims to address the concerns of stakeholders by covering all relevant areas, including finance, sales, marketing, and supply chain management.

## Tech Stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)

## Industry Related Terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - Cost of Goods Sold
- FY- Fiscal Year
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer
- Manufacturing costs, Freight costs
- Gross Margin, Gross Margin Percentage
- Net profit, Net Profit Percentage
- Sales quantity, Forecast Quantity
- Net Error, Absolute Error, Forecast Accuracy

## Acquired Techniques from Power BI

Before starting the project, what questions should be asked?
- How to create calculated columns
- How to create measures using DAX language
- What is involved in data modeling
- How to use Bookmarks to switch between two visuals
- How to perform page navigation with buttons
- How to use the divide function to prevent zero division errors
- What is the process for creating a date table using m language
- How to create dynamic titles based on applied filters
- How to effectively use KPI indicators
- How to apply conditional formatting to visualize values using icons or background color
- What are the best data validation techniques
- How PowerBi services work
- How to publish reports to PowerBi services
- What are the steps to set up a personal gateway for data auto refresh

### Dataset **Understanding**

It's important to have a good grasp of the available data before starting the analysis. Make sure to understand what data is accessible before delving into the analysis.

Dimension table : The static data will include information about customers and products.

Fact table : The static data will contain details regarding customers and products.

- gdb041:
    - Dim_Customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three Channels
            - Retailer
            - Direct
            - Distributors
    - Dim_Market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - Dim_Product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - Fact_Forecast_Monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - Fact_Sales_Monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - Freight_Cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - Gross_Price
        - Has the details of gross prices with product code
    - Manufacturing_Cost
        - Has the details of manufacturing cost with product code with year
    - Pre_Invoice_Deductions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_Invoice_Deductions
        - Post invoice deductions and other Deductions Details

## Importing data into PowerBi

In this project, since we are using MySQL as the database, we will have to transfer the datasets from the MySQL database to PowerBI by entering the access credentials for the database.

## Data Model

- The foundation of a report is built upon data modeling and it plays a crucial role in the process.
- All the visuals in the report will be created based on the data model.
- The overall performance of the report is impacted by inadequate data modeling.
- For this project, we adopted the Snowflakes data modeling approach.

<img src="https://github.com/yokesh-1894/Business-Insights-360/blob/main/Data%20Modeling.png" class="center">

## Final Outcome
         
  The report can be utilized to make decisions using the data. Additionally, it can aid in addressing numerous "why" questions relating to specific situations.

-	Finance View: Prepared a Profit and Loss statement to analyze the financial performance in different markets, products, and customer segments.
-	Sales View: Generated a list of both customers and products performance, along with their key metrics.
-	Marketing View: Developed Products and Market performance along with key metrics.
-	Supply chain View: Established Key Performance Indicators(KPI) such as Forecast accuracy, Net error, and Absolute error in order to evaluate the performance of the supply chain.
-	Executive View: A comprehensive perspective of important findings for corporate leaders.
  
## Interactive Dashboard

https://app.powerbi.com/view?r=eyJrIjoiZmRmMzk5YTYtNmQ1Ny00YTExLTgxYTctODUzMjA0YmRmZjc5IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=ReportSectione1bc1cbf18e18d33dbed


    
    
