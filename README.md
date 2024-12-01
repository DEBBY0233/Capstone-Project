# LITA_CLASS_DOCUMENTATIONS

### PROJECT TITLE: LITA_SALES_DATA

### PROJECT OVERVIEW
This Data Analysis Project aims to look into the sales performance of each Region, total sales of each product, sum of total sales by the Region in the year under review. To analyse the product in stock, Total Sales, Average Sales, and Sum of Total Revenue. Also , Pivot table was generated to reflect total sum of Revenue. By analysing the various parameters in the data receivedg, we seek to gather enough insight to make reasonable decision which then enable us to write compelling stories around our data from the insight gotten and to have the best outcome from our Data.

### DATA SOURCES
The primary source of Data used is sales data csv this is an open source data which was downloaded from canvas under LITA class assignment.

### TOOLS USED
- Microsoft Excel [download here](https://www.microsoft.com) for Data Cleaning, Analysis and Visualization.
- SQL - Structure Query Language for Querying of Data.
- Github - for Portfolio Building

### DATA CLEANING AND PREPARATION
In the initial cleaning of the Data and Preparation, we perform the following actions:
1. Data Loading and Inspection
2. Handling missing variables
3. Data cleaning and formatting

### EXPLORATORY
Exploratory Data Analysis involves the exploring of the Data to answer somr questions about the Data such as:
- What is the overall sales trend?
- Which product are top sellers?
- What product are peak sales?

### DATA ANALYSIS
This is where we include some basic lines of code and queries or even some of the Data Analysis Expression used during the Analysis.

#### DATA ANALYSIS ON EXCEL
After the data set was cleaned on Excel, the following analysis was performed

- Total Sales
```
=F2*G2
```
- Transaction Category
```
=IF(F2<=5,"low")
```
- Grand Total Sales
```
=SUM(H2:H9922)
```
- Total Sales per Product
```
=SUMIFS(H2:H9922,C2:C9922,C2)
```
### PIVOT TABLES AND CHARTS
![image](https://github.com/user-attachments/assets/ffa9f3fc-d092-4160-8b0f-bd8429ed31d0)
![image](https://github.com/user-attachments/assets/e6c7eb8c-59d0-47ea-bc1e-f6aaf219af34)
![image](https://github.com/user-attachments/assets/df1e85e9-8c02-4a48-bcdf-87b37d2b02ad)
![image](https://github.com/user-attachments/assets/8be1acf8-0b15-404c-9b55-9d14853471ec)

### ANALYSIS ON SQL
#### Below are the queries run on SQL
- To retrieve the total sales from each category
```
select product,sum(revenue) as Total_Revenue
from[dbo].[SALES_DATA_] Group by Product
```
- Number of Sales Transaction in each region
```
Select Region,sum(Revenue) as Total_Sales
from  [dbo].[SALES_DATA_] Group by Region
```
- Highest selling product by Total sales
```
Select Product, sum(Quantity) as Total_sales_or_Total_Quantity_Sold
from [dbo].[SALES_DATA_] Group by Product
Order by Total_sales_or_Total_Quantity_Sold Desc
```
- Total Revenue by Product
```
Select Product,sum(Revenue) as Total_Revenue_per_Product
from [dbo].[SALES_DATA_]
Group by Product
```
- Total Revenue by Region
```
Select Region,sum(Revenue) as Total_Revenue_per_Region
from [dbo].[SALES_DATA_]
Group by Region
```



### DATA VISUALIZATION
![image](https://github.com/user-attachments/assets/c7654384-f109-4f20-8d54-b2298a344fd9)


