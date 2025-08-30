# Sales-Profit-Dashboard

This project is an **interactive Power BI dashboard** that provides insights into sales, profit, and customer behavior.  
It is designed to help understand **which products, customers, and demographics drive profitability**.

## 🛠 Data Modeling & Transformations

To enable time-based analysis in the dashboard, I created a Calendar table that included all dates within the dataset range. This allowed:

- Month, Quarter, and Year-level aggregation
- Easy filtering and slicing by time
- Accurate trend analysis for revenue and profit
- The table was linked to the retail dataset via the Date column to allow dynamic calculations across all time periods.

Defined key measures to calculate important metrics dynamically by creating another table:

- Total Sales = SUM(dataset[Total Amount])
- Total Quantity = SUM(dataset[Quantity])
- Total Profit = SUM([Total Amount])
- Total Cost = SUM([Quantity]) * 'Cost per Unit'[Cost per Unit Value]
- Profit = [Total Sales] - [Total Cost]
- Profit Margin % = DIVIDE([Profit], [Total Sales], 0)
- Sales per Unit = DIVIDE([Total Sales], [Total Quantity], 0)

Scenario Analysis – created a dynamic measure to adjust profit based on changes in cost per unit. This measure uses an extra parameter I added, 
which was not present in any table, allowing “What-If” analysis for cost variations.

These measures allowed the dashboard to respond instantly to slicers and filters, giving meaningful insights such as:
- Top-performing products and categories
- Profit contribution by demographics
- Impact of cost changes on overall margins

---

## 🚀 Features
- **KPIs**: Total Sales, Total Profit, Profit Margin, Total Cost
- **What-if Analysis**: Interactive slicer to adjust *Cost per Unit*  
- **Customer Insights**: Profit by Age Group & Gender, Sales & Profit by CustomerID  
- **Product Insights**: Profit by Product Category, Sales per Unit by Category  
- **Time Trends**: Total Sales & Profit by Month  
- **Demographic Breakdown**: Treemap (Total Sales by Age Group & Gender), Matrix (Profit Margin by Age & Gender)  

---

## 📌 Dashboard Highlights
```
Top-Performing Categories: Electronics contributed the highest total sales & profit, while Beauty showed the lowest performance.

Profit Margins by Demographics: Customers aged 36–50 generated the highest profit margins overall. Within this group,
female customers contributed slightly more (50%) than males (49%),
and customers aged less than 25 contributed less.

Monthly Trends: Sales and profit peaked in May, with a noticeable dip in March and September.

Customer-Level Insights: A small group of loyal customers drove a major share of revenue, while many customers contributed minimal profit.

What-if Analysis: Profit margins are highly sensitive to unit costs. Reducing the cost per unit from ₹60 to ₹10 increases total profit
from ₹305.16K to ₹430.86K, demonstrating the substantial effect of cost optimization on overall profitability.
```
---

## 🛠️ Tools Used
- **Power BI** (Data Modeling & Visualization)  
- **CSV** (Data Source)  

---

## 📷 Screenshots

<img width="1157" height="622" alt="image" src="https://github.com/user-attachments/assets/04c43c2a-ae98-4ccf-83cf-73710be7ef86" />

<img width="1153" height="645" alt="image" src="https://github.com/user-attachments/assets/de1f04e1-9b99-4589-86d4-d4be31508cae" />

## About Me  
👋 Hi, I'm Liza Deka — a data enthusiast.  
   I enjoy building projects, analyzing real-world data, and sharing insights through GitHub and LinkedIn. 
   
  📬 Let’s Connect: <a href="https://www.linkedin.com/in/liza-deka-869473369/">LinkedIn</a>
