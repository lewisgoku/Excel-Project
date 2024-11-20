# Excel Project: Coffee Shop Sales

## Table of Contents
- [Project Overview](#project-overview)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)


### Project Overview
---
This data analysis project aims to provide insights into an e-commerce company's sales performance over the past year. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.
![image](https://github.com/user-attachments/assets/aa187afd-a182-4db0-9a0c-bd9d094706c0)
![Screenshot_OrderTable](https://github.com/user-attachments/assets/ddace4b4-6b6f-49cc-bbf0-acb984da1e73)

### Data and Analysis Sources
Sales Data: The primary dataset used for this analysis is the "coffeeOrdersData.xlsx" file, which contains detailed information about customers and products for the fictional Coffee Shop. The Orders worksheet is derived as follow;

  
  

### Tools
- Microsoft Excel - Data Cleaning, Analysis and Visualization
  - [Download here](https://www.microsoft.com/en-ca/microsoft-365/excel)

### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis
EDA involved exploring the sales data to answer critical questions, such as:
- What is the overall sales trend?
- Which products are top sellers?
- What are the peak sales periods?

### Data Analysis
Include some exciting code/features worked with
```SQL
Select * from table
wHERE ID = 3,

```Microsoft Excel
Customer Name =XLOOKUP(C2,customers!$A$1:$A$1001,customers!$B$1:$B$1001,,0)
```

```Microsoft Excel
-  Customer Name = XLOOKUP(C2,customers!$A$1:$A$1001,customers!$B$1:$B$1001,,0)
-  Email = IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C1:$C1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C1:$C1001,,0))
Country = XLOOKUP(C2,customers!$A$1:$A$1001,customers!$G$1:$G$1001,,0)
Coffee Type = INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!J$1,products!$A$1:$G$1,0))
Roast Type =
Size = 
Unit price = 
Sales = E2*L2
Coffee Type Name = IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica",""))))
Roast Type Name = IF(J2="M","Medium",IF(J2="L","Light",IF(J2="D","Dark","")))
Loyalty Card = XLOOKUP([@[Customer ID]],customers!$A$1:$A$1001,customers!$I$1:$I$1001,,0)
```

### Results and Findings
The analysis results are summarized as follows:
1. The company's sales have been steadily increasing over the past year, with a noticeable peak during the holiday season.
2. Product Category A is the best-performing category in terms of sales and revenue.
3. Customer segments with high lifetime value (LTV) should be targeted for marketing efforts.

### Recommendations
Based on the analysis, we recommend the following actions:
- Invest in marketing and promotions during peak sales seasons to maximize revenue.
- Focus on expanding and promoting products in Category A.
- Implement a customer segmentation strategy to target high-LTV customers effectively.

### Limitations
I had to remove all zero values from budget and revenue columns because they would have affected the accuracy of my conclusions from the analysis. There are still a few outliers even after the omissions but even then we can still see that there is a positive correlation between both budget and number of votes with revenue.

### References
Dataset  by Mo Chen: *mochen862*

😄

🖥️

|Heading1 |Heading2|
|---------|--------|
|Content|Content|
|Python|SQL|

`column_1`

**bold**

*Italic*





















