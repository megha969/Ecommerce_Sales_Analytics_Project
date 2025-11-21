# Power BI Notes for E‑Commerce Sales Analytics Project

## 📘 Overview
This document explains how Power BI is used in the E‑Commerce Sales Analytics Project. It includes data loading, cleaning, DAX formulas, visualizations, and insights to help build a complete business intelligence dashboard.

---

## 🔹 1. Importing Data
1. Open **Power BI Desktop**
2. Click **Get Data → Text/CSV**
3. Select the `sales.csv` file
4. Load the dataset into Power BI

Dataset columns:
- Order ID
- Order Date
- Category
- Sub-category
- Customer Name
- State
- Quantity
- Sales
- Profit
- Discount

---

## 🔧 2. Data Cleaning (Power Query)
Open **Power Query Editor** using *Transform Data*.

### ✔ Remove Duplicates
- Remove duplicate rows based on `Order ID`

### ✔ Fix Data Types
- Order Date → Date
- Sales/Profit → Decimal Number
- Quantity → Whole Number

### ✔ Create Calculated Columns (DAX)

**Month Name**
```
Month = FORMAT('sales'[Order Date], "MMMM")
```

**Year**
```
Year = YEAR('sales'[Order Date])
```

**Profit Margin %**
```
Profit Margin = DIVIDE('sales'[Profit], 'sales'[Sales]) * 100
```

Apply changes → **Close & Apply**

---

## 📊 3. Build Visualizations
Below are the key visuals used in the dashboard.

### 1️⃣ Sales by Month (Line Chart)
- Axis → Month
- Values → Sales

### 2️⃣ Sales by Category (Bar Chart)
- Axis → Category
- Values → Sales

### 3️⃣ Top 10 Customers (Bar Chart)
- Axis → Customer Name
- Values → Sales
- Top N → 10

### 4️⃣ Sales by State (Map)
- Location → State
- Values → Sales

### 5️⃣ Profit vs Sales (Scatter Plot)
- X-axis → Sales
- Y-axis → Profit
- Category → Details

### 6️⃣ KPI Cards
Create these DAX measures:
```
Total Sales = SUM(sales[Sales])
Total Profit = SUM(sales[Profit])
Total Quantity = SUM(sales[Quantity])
```

Add KPI visuals:
- Total Sales
- Total Profit
- Total Orders

---

## 🧩 4. Dashboard Layout
Suggested layout for the final dashboard:

### **Top Row: KPI Cards**
- Total Sales
- Total Profit
- Total Orders

### **Middle Row: Trend & Category Analysis**
- Line chart → Sales by Month
- Bar chart → Sales by Category
- Bar chart → Profit by Category

### **Bottom Row: Geography & Customers**
- Map → Sales by State
- Bar chart → Top 10 Customers

### **Slicers**
- Year
- Category
- State

---

## 📢 5. Insights & Interpretation
### ✔ Category-wise Performance
- Electronics generates the highest revenue
- Furniture has high sales but low profit margin

### ✔ Monthly Trends
- Sales peak in **November and December** (holiday season)

### ✔ Regional Analysis
- Maharashtra, Karnataka, and Delhi contribute the highest sales
- Low-performing states indicate potential markets for growth

### ✔ Discount Impact
- High discounts reduce profit margins
- Suggests revisiting discount strategy

### ✔ Customer Insights
- Top 10 customers contribute ~40% of total sales

---

## 🧠 6. Why Power BI is Important for This Project
- Shows ability to clean and analyze business data
- Highlights your visualization and storytelling skills
- Demonstrates understanding of KPIs and business metrics
- Strong value for Data Analyst, BI Analyst & Business Analyst roles

---

## 📦 7. Files Connected to Power BI
- `sales.csv` → Main dataset
- `powerbi.pbix` → Final dashboard (optional)
- `powerbi_notes.md` → Explanation for GitHub

---

## ✅ Final Deliverable
This document can be uploaded directly to **GitHub** under the `powerbi/` folder as `powerbi_notes.md`. It explains exactly how the dashboard is built and what business insights it delivers.

