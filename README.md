# 🍽️ Zomato Restaurant Analytics Dashboard — Power BI Project

A complete Business Intelligence and Data Analytics project that analyzes restaurant performance, customer behavior, delivery efficiency, and revenue trends using SQL, Excel, and Microsoft Power BI.

This project focuses on understanding restaurant revenue patterns, customer ordering behavior, cuisine performance, delivery analysis, and business growth opportunities through an interactive Power BI dashboard.

The analysis is performed on a Zomato restaurant dataset containing restaurant details, customer information, and order transactions to generate meaningful business insights and support data-driven decision-making.

---

# 🎯 Business Problem

Food delivery platforms like Zomato handle thousands of restaurants and customer orders every day. Businesses need clear insights into:

- Restaurant revenue performance
- Customer ordering patterns
- Popular cuisines
- City-wise restaurant growth
- Delivery efficiency
- Customer retention
- Order cancellation trends

The objective of this project is to answer:

## 📌 Key Business Questions

✔ Which restaurants generate the highest revenue?

✔ Which cuisines are most popular among customers?

✔ Which cities contribute maximum revenue?

✔ What is the average delivery performance?

✔ Which restaurants have the highest ratings?

✔ What factors influence customer retention and cancellations?

---

# 🗂️ Project Files

| File | Description |
|------|-------------|
| 📊 Zomato_Dataset.xlsx | Raw restaurant and order transaction dataset |
| 📈 Zomato_Analytics_Dashboard.pbix | Complete Power BI dashboard file |
| 📘 README.md | Project documentation |
| 🖼️ Dashboard Screenshots | Dashboard previews |

---

# 🛠️ Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| 🟦 Microsoft Power BI | Dashboard creation, visualization and insights |
| 🟨 SQL | Data extraction and analytical queries |
| 📊 Excel | Dataset preparation and exploration |
| 📐 DAX | Calculated measures and KPIs |
| 📊 Data Visualization | Interactive reporting |

---

# 📊 Dashboard Pages

The dashboard contains 3 interactive pages:

---

# 🏠 HOME PAGE — Zomato

### Objective:

Provides an introduction page with Zomato branding and dashboard navigation.

Features:

- Zomato themed design
- Dashboard navigation
- Business analytics overview

---

# 📌 PAGE 1 — Zomato Executive Overview

## Objective:

Provide an overall view of Zomato business performance.

## KPIs:

- Total Revenue
- Total Orders
- Total Restaurants
- Average Rating
- Average Delivery Time

## Visual Analysis:

### 📈 Revenue Trend

- Monthly revenue analysis
- Identify business growth patterns

### 🏆 Top 5 Restaurants

- Revenue-based restaurant ranking

### 🗺️ Orders by City

- Geographic order distribution

### 💳 Payment Analysis

- Customer payment preferences

---

# 📌 PAGE 2 — Restaurant Performance Dashboard

## Objective:

Analyze restaurant-level performance and identify business leaders.

## KPIs:

- Highest Rated Restaurant
- Average Restaurant Revenue
- Total Cuisine

## Visual Analysis:

### 🏆 Top Performing Restaurants

- Compare restaurant revenue contribution

### 🍴 Cuisine Performance

- Analyze cuisine popularity

### 🌆 City-wise Restaurant Performance

- Compare revenue across cities

### 📊 Restaurant Ranking

- Identify best-performing restaurants

---

# 📌 PAGE 3 — Customer & Delivery Analytics

## Objective:

Analyze customer behavior, delivery efficiency, and order patterns.

## KPIs:

- Total Customers
- Average Order Value
- Cancellation Rate
- Repeat Customers

## Visual Analysis:

### 👥 Customer Membership Analysis

- Premium, Regular and Gold customer comparison

### 🚻 Gender Analysis

- Customer distribution analysis

### 💳 Payment Mode Analysis

- Revenue contribution by payment methods

### 📅 Monthly Order Trend

- Customer ordering pattern analysis

### 🚴 Delivery Partner Performance

- Delivery efficiency comparison

---

# 📐 DAX Measures Created

## 💰 Total Revenue

```DAX
Total Revenue =
SUM(Fact_Orders[Food_Amount])
```

---

## 📦 Total Orders

```DAX
Total Orders =
COUNT(Fact_Orders[Order_ID])
```

---

## 🍴 Total Restaurants

```DAX
Total Restaurants =
DISTINCTCOUNT(
    Dim_Restaurant[Restaurant_ID]
)
```

---

## ⭐ Average Rating

```DAX
Average Rating =
AVERAGE(
    Dim_Restaurant[Rating]
)
```

---

## 🚴 Average Delivery Time

```DAX
Avg Delivery Time =
AVERAGE(
    Fact_Orders[Delivery_Time]
)
```

---

# 📊 Restaurant Performance KPIs

## ⭐ Highest Rated Restaurant

```DAX
Highest Rating =
MAX(
    Dim_Restaurant[Rating]
)
```

---

## 💰 Average Restaurant Revenue

```DAX
Avg Restaurant Revenue =
DIVIDE(
    [Total Revenue],
    [Total Restaurants]
)
```

---

## 🍽️ Total Cuisine

```DAX
Total Cuisine =
DISTINCTCOUNT(
    Dim_Restaurant[Cuisine]
)
```

---

# 👥 Customer Analytics KPIs

## 👤 Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(
    Dim_Customer[Customer_ID]
)
```

---

## 🛒 Average Order Value

```DAX
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders]
)
```

---

## ❌ Cancellation Rate

```DAX
Cancellation Rate =

DIVIDE(

CALCULATE(
    COUNT(Fact_Orders[Order_ID]),
    Fact_Orders[Order_Status]="Cancelled"
),

[Total Orders]

)
```

---

## 🔁 Repeat Customers

```DAX
Repeat Customers =

COUNTROWS(

FILTER(
    VALUES(Dim_Customer[Customer_ID]),

    [Total Orders] > 1

)

)
```

---

# 📈 Dashboard Insights

✔ Analyzed restaurant and customer transaction data

✔ Identified top-performing restaurants based on revenue

✔ Compared cuisine performance and customer preferences

✔ Evaluated city-wise restaurant contribution

✔ Analyzed delivery efficiency

✔ Studied customer retention patterns

✔ Identified cancellation trends

---

# 🔍 Key Business Findings

## Restaurant Performance

- Top restaurants contributed significantly to total revenue.
- Highly rated restaurants achieved better customer engagement.
- Popular cuisines generated higher order volumes.

## Customer Behavior

- Repeat customers contributed to consistent revenue.
- Different customer segments showed different ordering patterns.
- Payment preferences varied across users.

## Delivery Insights

- Delivery time analysis helped evaluate operational efficiency.
- Faster delivery improved customer experience.

## Growth Opportunities

- Promote high-performing cuisines.
- Improve delivery operations.
- Increase repeat customer engagement.
- Optimize restaurant partnerships.

---

# 🎯 Final Conclusion

The Zomato Restaurant Analytics Dashboard demonstrates how raw restaurant and transaction data can be transformed into meaningful business intelligence.

Using SQL, Power BI, and DAX, the project analyzed:

✅ Restaurant Performance  
✅ Revenue Trends  
✅ Customer Behavior  
✅ Cuisine Analysis  
✅ Delivery Efficiency  
✅ Cancellation Patterns  

The dashboard helps food delivery platforms:

✅ Improve restaurant performance  
✅ Enhance customer satisfaction  
✅ Optimize delivery operations  
✅ Increase revenue opportunities  
✅ Make data-driven decisions  

---

# 🚀 How To Run The Project

## Step 1:

Install:

- Microsoft Power BI Desktop
- SQL Database
- Microsoft Excel

## Step 2:

Load the dataset into SQL / Power BI.

## Step 3:

Open:

```
Zomato_Analytics_Dashboard.pbix
```

## Step 4:

Refresh the dataset and explore interactive dashboards.

---

# ✅ Project Checklist

✔ Dataset Preparation  
✔ SQL Analysis  
✔ Data Modeling  
✔ Star Schema Design  
✔ DAX Measures  
✔ KPI Development  
✔ Interactive Dashboard  
✔ Restaurant Analytics  
✔ Customer Analytics  
✔ Delivery Analysis  
✔ Business Insights  

---

# 👨‍💻 Author

**Shruti Bhawsar**

📍 Ahmedabad, Gujarat, India

---

⭐ If you found this project useful, consider sharing feedback.

---

# 📊 Data Analytics | Business Intelligence | Power BI | Data-Driven Decisions
