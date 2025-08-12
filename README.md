# 🌍 Global SuperStore Sales and Market Analysis Using Power BI


**Author:** Hà Minh Khuê

**Date:** 05/08/2025

**Tools Used:** Power BI

## Table of Contents
1. [📌 Background & Overview](#background--overview)
2. [📂 Dataset Description & Data Structure](#dataset-description--data-structure)
3. [🧠 Design Thinking Process](#design-thinking-process)
4. [📊 Key Insights & Visualizations](#key-insights--visualizations)
5. [🔎 Final Conclusion & Recommendation](#final-conclusion--recommendation)

---

## 📌 Background & Overview

**Objective:**

**📖 What is this project about?**

This project aims to build a **Power BI dashboard** using the *Global Superstore Sales* dataset, which includes data on 3 tables: (**Orders**), (**People**) and (**Returns**).
The goal is to provide senior managers and stakeholders with **data-driven insights** to:

- **Understand current business performance**
 
- ** market expansion strategies**

- **Identify strategic products for growth**

- **Support better decision-making to drive revenue and ROI**


**👤 Who is this project for?**

✔️ Data analysts & business analysts seeking actionable insights.

✔️ Marketing and sales teams focusing on product performance and market growth.

✔️ Route to Product team aiming to improve product quality via return product.


**❓Business Questions:**

✔️ What is the current performance of Superstore?

✔️ Which markets should Superstore expand into to increase revenue and ROI?

✔️ Which products should be prioritized for strategic growth and should we improve the quality of most returned product?


**🎯Project Outcome:**

- Revenue increased significantly, but profit margin remained flat, indicating rising costs and limited operational efficiency gains.  
- Canada emerged as a high-margin market (28%) despite low revenue, while Africa and EMEA showed the fastest YoY growth, revealing expansion potential.  
- Oceania and Africa attracted the most new customers, whereas most revenue still came from loyal, returning buyers.  
- Technology led revenue growth and profitability, but return rates in some tech SKUs (e.g., Cisco, Motorola) impacted margins.  
- Products like Copiers delivered the highest profit per unit, while low-performing items (e.g., Suppliers, Furnishings) diluted overall profitability.

By aligning regional and product strategies, senior managers can **scale in high-margin markets**, **invest in scalable profitable categories**, and **optimize acquisition and return management**, driving **sustainable long-term growth**.

## 📂 Dataset Description & Data Structure

### **📌 Data Source** 

- **Source**: Kaggle  
- **Size**: The **Orders** table contains **51,290** records.  
- **Format**: CSV  

### 📊 **Data Structure & Relationships**  

#### 1️⃣ **Tables Used:**  
The dataset consists of **three tables**:  

- 🛒 **Orders** – Contains detailed transaction and customer information (**51,290 records**).

<details>
<summary> <strong>Table 1: Orders</strong></summary>

| Column Name       | Data Type   | Description                              |
|------------------|------------|------------------------------------------|
| `Order ID`      | `VARCHAR`   | Unique identifier for each order.       |
| `Order Date`    | `DATE`      | Date when the order was placed.         |
| `Ship Date`     | `DATE`      | Date when the order was shipped.        |
| `Ship Mode`     | `VARCHAR`   | Shipping method used for delivery.      |
| `Customer ID`   | `VARCHAR`   | Unique identifier for each customer.    |
| `Customer Name` | `VARCHAR`   | Full name of the customer.              |
| `Segment`       | `VARCHAR`   | Customer segment (e.g., Consumer, Corporate). |
| `City`         | `VARCHAR`   | City where the order was placed.        |
| `State`        | `VARCHAR`   | State where the order was placed.       |
| `Country`      | `VARCHAR`   | Country where the order was placed.     |
| `Postal Code`  | `VARCHAR`   | Postal code of the shipping address.    |
| `Market`       | `VARCHAR`   | Market region (e.g., APAC, EMEA).       |
| `Region`       | `VARCHAR`   | Geographical region of the order.       |
| `Product ID`   | `VARCHAR`   | Unique identifier for each product.     |
| `Category`     | `VARCHAR`   | Product category (e.g., Furniture, Office Supplies). |
| `Sub-Category` | `VARCHAR`   | Sub-category of the product.            |
| `Product Name` | `VARCHAR`   | Name of the product ordered.            |
| `Sales`        | `DECIMAL`   | Revenue generated from the order.       |
| `Quantity`     | `INT`       | Number of items ordered.                |
| `Profit`       | `DECIMAL`   | Profit earned from the order.           |

</details>

- 🔄 **Returns** – Stores data on returned orders.

<details>
<summary> <strong>Table 2: Returns</strong></summary>

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>
  
- 👥 **People** – Holds information about sales representatives.

<details>
<summary> <strong>Table 3: People</strong></summary>

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `Person`    | `VARCHAR` | Name of the salesperson. |
| `Region`    | `VARCHAR` | Geographic region where the salesperson operates. |

</details>

#### 2️⃣ Data Relationships:



| **From Table** | **To Table** | **Join Key**   | **Relationship Type**                                  |
|------------|----------|------------|----------------------------------------------------|
| `Orders`   | `People` | `Region`   | Many-to-One (multiple orders belong to one region) |
| `Orders`   | `Returns`| `Order ID` | One-to-One or Left Join (not all orders are returned) |

## 🧠 Design Thinking Process

### 1️⃣ Empathize




### 2️⃣ Define point of view 



### 3️⃣ Ideate



### 4️⃣ Prototype and review

This part is in the dashboard

## 📊 Key Insights & Visualizations

### 🔍 Dashboard Preview

### I. Overview

<img width="1332" height="744" alt="image" src="https://github.com/user-attachments/assets/b910ee6d-1357-4e93-887d-204e8d628bc6" />

### 📌 Key Findings:

# Strategic Dashboard Analysis

## Summary of KPIs
- **Total Sales:** 9.48M  
- **Total Profit:** 1.09M  
- **Profit Margin %:** 0.12 (~12%)  
- **Sales YoY Growth %:** 0.51 (~51%)  
- **Return Rate %:** 0.05 (~5%)  

> Note: YoY Growth appears higher than the yearly growth shown in the chart (2014 vs 2013 ≈ +23%). This may be due to calculation method (e.g., max year vs min year) or filters applied.

---

## Yearly Trend (Business Performance: 2011–2014)
- **Sales growth:** 1.7M → 2.0M → 2.6M → 3.2M  
- **Profit growth:** 0.2M → 0.2M → 0.3M → 0.4M  
- **Profit Margin % trend:** Peaked in 2013 (12.0%), dropped slightly in 2014 (~11.5%).  
- Insight: Growth in 2014 was driven more by volume than by margin.

---

## By Market & Category
- **EU:** High sales and highest profit margin. Large share of Technology products (good margins).  
- **APAC:** Second highest sales, mid-to-high margin; room to optimize margins, especially in Furniture and Office Supplies.  
- **LATAM:** Medium sales, margins are stable but not outstanding.  
- **US:** Lower-than-expected sales; worth checking filters or data.  
- **EMEA:** Lowest sales and margin (~5%); possible pricing, cost, or discounting issues.

---

## Order Count by Country
- Large clusters in **North America**, **Europe**, **Australia**.  
- Scattered orders in **Africa** and **Indian Ocean** regions.  
- Order count does not equal revenue; some regions may have many small-value orders.

---


### II. Category and Market Analysis

<img width="1329" height="743" alt="image" src="https://github.com/user-attachments/assets/fe67d5cf-4574-4289-a793-9e886b2b21f3" />

### 📌 Key Findings:

# Strategic Dashboard Analysis

## Top Highest Sub-Category (by Total Sales)
1. **Phones:** 1.4M  
2. **Copiers:** 1.2M  
3. **Chairs:** 1.2M   

**Insight:** Phones dominate in sales volume, followed by high-value office and furniture items. Top 4 sub-categories contribute a significant portion of total sales.

---

## Total Profit by Person and Category
- **Top performer:** Anna Andrews — strong profit, especially in Furniture and Technology.
- Jack Lebron and Shirley Daniels follow as key contributors.
- Remaining sales reps have noticeably lower profit generation.
- Technology and Furniture appear in top contributors’ portfolios, suggesting high-margin opportunities.

---

## Yearly Sales & Profit Performance
**Trends:**
- Steady growth in sales and profit from 2011 to 2014.
- Highest jump in both sales and profit between 2012 and 2013.
- Return count increases over time, possibly linked to higher sales volume.

---

## Yearly Trends (Chart: Total Sales, Total Profit, Sales YoY Growth %)
- **Strong growth** in 2013 (~30% YoY), followed by slightly slower growth in 2014.
- Total profit tracks closely with sales growth.
- Momentum maintained, but YoY growth rate peaked in 2013 and declined in 2014.

---

## Key Insights
1. **Phones, Copiers, and Chairs** are key sales drivers; optimizing inventory, pricing, and promotion in these areas could yield significant gains.
2. **Top sales reps** (especially Anna Andrews) contribute a disproportionate share of profits — their sales approach could be analyzed and replicated.
3. **Return counts** increase alongside sales; worth investigating if high-return sub-categories overlap with top-selling items.
4. **2013 peak YoY growth** indicates a strong year; identifying the market or campaign drivers from that year could inform future strategies.
5. Maintaining growth in 2014 required higher sales volume but achieved with a lower growth rate compared to 2013.

---

     
### III. Returned Product Analysis

<img width="1332" height="741" alt="image" src="https://github.com/user-attachments/assets/443f14d9-0296-4dae-8757-b101843683c8" />

### 📌 Key Findings:

# Return Product Analysis Dashboard 


## Most Returned Products (by Return Value)
1. **Samsung Smart …** — 17K  
2. **HP Wireless Fax …** — 6K  
3. **Safco Classic Bookcase …** — 5K  

**Insight:** Samsung Smart product line is a major outlier with return value far exceeding other items. Electronics dominate the top return list, suggesting potential product quality, compatibility, or customer expectation issues.

---

## Return Count and Return Rate % by Year
- **2011 → 2012:** Increase in both return count and rate.  
- **2012:** Peak return rate (~5.2%).  
- **2013 → 2014:** Return rate decreases slightly, even though return counts remain high.  
- Indicates possible improvement in return management processes while sales volumes grew.

---

## Order Count and Return Count by Market
- **Highest orders:** EU and LATAM.  
- **Return counts** are also highest in EU and LATAM.  
- **Lowest orders:** APAC, but still records returns, indicating that returns are not solely volume-driven.

---

## Key Insights
1. **High-return products** are largely electronics, especially Samsung Smart devices. Root causes should be investigated (e.g., defect rates, customer dissatisfaction, misleading product descriptions).  
2. **EU and LATAM** have both the highest orders and returns — focus on targeted return reduction strategies in these markets.  
3. **Return rate improvements** after 2012 suggest positive changes in quality control, supplier selection, or product information clarity.  
4. Tracking **return value impact** is essential: reducing top product returns could significantly increase net profit.


## 🔎 Final Conclusion & Recommendation 

## Conclusion
The business shows **consistent growth** in sales and profit from 2011 to 2014, driven primarily by **high-performing markets (EU, APAC)** and **top sub-categories (Phones, Copiers, Chairs, Bookcases)**.  
While profit margins have remained healthy, the slight drop in 2014 indicates that recent growth has been **volume-driven** rather than margin-led.  
**Returns remain a notable challenge**, particularly in high-value electronics, with EU and LATAM contributing the most to total returns.  
Top-performing sales representatives have significantly influenced profitability, but performance disparity across the team suggests potential untapped revenue opportunities.

---

## Recommendations

### 1. Revenue and Margin Growth
- **Prioritize high-margin products** (Technology and select Furniture) in EU and APAC.
- **Reassess low-margin regions** (EMEA) and optimize product mix, pricing, and logistics.
- Introduce **bundling and upsell strategies** in top sub-categories to lift Average Order Value (AOV).

### 2. Return Reduction
- Focus on **high-return electronics** (e.g., Samsung Smart, HP Wireless Fax) — investigate defect rates, compatibility issues, and customer expectations.
- Enhance **product descriptions, quality checks, and packaging** to minimize dissatisfaction.
- Target **EU and LATAM** with return prevention campaigns and post-sale support.

### 3. Sales Team Performance
- **Analyze top sales reps’ strategies** (e.g., Anna Andrews) and replicate best practices across the team.
- Provide targeted training for lower-performing reps to close the performance gap.

### 4. Operational Monitoring
- Track **Profit per Order, Return Value %, and COGS% by Category** in the dashboard for deeper operational control.
- Implement **drill-through views** for country-level and product-level return analysis.
- Monitor **YoY Growth measure accuracy** to ensure KPIs reflect true business performance.

### 5. Strategic Planning
- Use insights from **2013’s peak YoY growth** to identify effective campaigns or market moves for replication.
- Balance **volume growth with margin stability** to protect long-term profitability.
