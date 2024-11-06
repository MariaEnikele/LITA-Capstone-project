# LITA-Capstone-project

### Project Title:Sales Peformance Analysis 
[Project Oveview](#project_overview)
[Data Sources](#data-sources)
[Tools Used](#tools-used)
[Data Cleaning and Preparations](#data-cleaning-and-preparations)
[Exploratory Data Analysis](#exploratory-data-analysis)
[Data Analysis](#data-analysis)
[Data Visualization](#Data-visualization)
### Project Oveview
---
This data is to explore sales data to uncover key insights such as top-selling products, regional performance, and monthly sales trends.

### Data Sources
---
The primary source of data used is LITA Capstone Dataset and this is a dataset downloaded from the Canvas LMS platform.

### Tools Used
---
- Microsoft Excel [download Here](https://www.microsoft.com).
  1. Data cleaning
  2. Data Analysis
  3. Visualization
- SQL-Structured Query Language for querying of data
- Power BI for data analysis and visualization
- Github for Porfolio Building

### Data Cleaning and Preparations
---
In the initial phase of the Data cleaning and preparation, I performed the following action;
1. Data loading and Inspection
2. Handling missing variables
3. Data cleaning and formatting

### Exploratory Data Analysis
---
EDA involved the exploring of the Data to answer some questions such as;
- Which is the Top selling product
- Regional Sales Performance
- Monthly Sales Trend
  
### Data Analysis
---
Enclosed are some of the line of codes/queries used in my analysis
```SQL
SELECT * FROM [dbo].Sales_data

 -----Totalsales---------
 SELECT 
    Product AS Product_Category,
    SUM(CAST(Quantity AS INT) * CAST(UnitPrice AS INT)) AS Total_Sales
FROM 
    [dbo].Sales_data
GROUP BY 
    Product;

-------Numberofsales in each Region------

	SELECT 
    Region,
    COUNT(OrderID) AS Number_of_Transactions
FROM 
    [dbo].Sales_data
GROUP BY 
    Region;

----------Highest selling product by totalsales value
	SELECT 
    TOP 1 Product AS Product_Category,
    SUM(CAST(Quantity AS INT) * CAST(UnitPrice AS INT)) AS Total_Sales
FROM 
    [dbo].Sales_data
GROUP BY 
    Product
ORDER BY 
    Total_Sales DESC;
-------Total revenue by product------
	SELECT 
    Product AS Product_Category,
    SUM(CAST(Quantity AS INT) * CAST(UnitPrice AS INT)) AS Total_Revenue
FROM 
    [dbo].Sales_data
GROUP BY 
    Product;

Excel Formulas used to calculate average per product and sales per region respectively
=AVERAGEIF(C2:C50001, "Shoes",H2:H50001)
=SUMIFSUMIF(C2:C75001,"North",H2:H75001)

```
### Data Visualization
---
## Total sales by Product
![total sales by product](https://github.com/user-attachments/assets/1654e60d-be03-4dd1-bca2-ed30d4acba3a)
## Total sales by Region
![Total sales by Region](https://github.com/user-attachments/assets/6bb490f0-3308-40a6-a815-b9c6352baa61)
## Total sales by Month
![Total sales by month](https://github.com/user-attachments/assets/1b3d2674-473b-48b0-94ce-5a1034a18ba1)
## Using Excel formulae to calculate Average total sales per product
![Average sales by product](https://github.com/user-attachments/assets/a8c1fad9-94ee-4c31-9538-a82087d27d64)
## Using Excel formulae to calculate total revenue per region
![using excel formulae to caculate total revenue by region](https://github.com/user-attachments/assets/641e54d5-d8cd-4597-912d-432fe7d083f5)

## Comparative sales analysis showing increase and decline in the sales revenue and quantity sold between year 2023 and 2024
![Comparative sales analysis](https://github.com/user-attachments/assets/cbfb7457-bb24-4bf5-902e-8e1fad8298f8)

### SQL
## Total sales for each product category
![SQL TOTAL SALES BY EACH PRODUCT](https://github.com/user-attachments/assets/fb2e0291-fc6a-4e38-ac4f-ad22f2e70dc0)
## Sales transactions in each Region
![sales transaction in each region](https://github.com/user-attachments/assets/e5c92e29-d1b9-4b95-a991-d6cfb70c72ad)
## Highest selling poduct by total sale
![highest selling product by total revenue](https://github.com/user-attachments/assets/04141d54-3315-44e9-8d19-b5c9d5a0dd5b)
## Total revenue per product
![total revenue by product](https://github.com/user-attachments/assets/347bfc12-2a16-478f-ab59-6517254097ff)
