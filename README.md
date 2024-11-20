# Excel Project: Coffee Shop Sales

### Project Overview
---
This data analysis project aims to provide insights into the sales performance of a fictional coffee shop over a four-year period. By examining various aspects of the sales data, we intend to identify trends, make data-driven recommendations, and gain a deeper understanding of the coffee shop's overall performance.
![image](https://github.com/user-attachments/assets/aa187afd-a182-4db0-9a0c-bd9d094706c0)
![Screenshot_OrderTable](https://github.com/user-attachments/assets/ddace4b4-6b6f-49cc-bbf0-acb984da1e73)

### Tools
- Microsoft Excel - Data Cleaning, Analysis and Visualization
  - [Download here](https://www.microsoft.com/en-ca/microsoft-365/excel)

### Data Sources and Analysis
The main dataset for this analysis is the "coffeeOrdersData.xlsx" file, which includes detailed information about customers and products for the fictional Coffee Shop. The Orders worksheet is derived as follows:
```Excel
Customer Name = XLOOKUP(C2,customers!$A$1:$A$1001,customers!$B$1:$B$1001,,0)
```
```Excel
Email = IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C1:$C1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C1:$C1001,,0))
```
```Excel
Country = XLOOKUP(C2,customers!$A$1:$A$1001,customers!$G$1:$G$1001,,0)
```
```Excel
Coffee Type,Roast Type,Size,Unit price = INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!J$1,products!$A$1:$G$1,0))
```
```Excel
Sales = E2*L2
```
```Excel
Coffee Type Name = IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica",""))))
```
```Excel
Roast Type Name = IF(J2="M","Medium",IF(J2="L","Light",IF(J2="D","Dark","")))
```
```Excel
Loyalty Card = XLOOKUP([@[Customer ID]],customers!$A$1:$A$1001,customers!$I$1:$I$1001,,0)
```
### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks:
- Data loading and inspection.
- Handling missing values.
- Data cleaning and formatting.
  - Removed duplicates
  - Order Data: *Update custom format to dd-mmm-yyy*
  - Update Size: *Update custom format to 0.0"kg"*
  - Unit price/Sales: *Currency format $0.00*
  - Convert range to table

### Exploratory Data Analysis
EDA involves examining the sales data to address key questions, including:
- What is the overall sales trend by Coffee Type over the specified date range?
- What are the total sales figures across different countries?
- Which product sizes and roast types are the top sellers?
- How do sales compare between customers with loyalty cards and those without?

### Results and Findings
The analysis results can be summarized as follows:
1. Coffee shop sales fluctuated throughout the four years, with a significant peak during the holiday season.
2. The Light roast category is the top performer in terms of total sales.
3. Customer segments with loyalty cards exhibit higher turnover compared to those without.

### Recommendations
Based on the analysis, I recommend the following actions:
- Invest in marketing and promotions during peak sales seasons to maximize revenue.  
- Focus on expanding and promoting products within the light roast category.  
- Implement a customer segmentation strategy to effectively target loyal customers.  

### References
Dataset by [Mo Chen: mochen862](https://github.com/mochen862/excel-project-coffee-sales)

