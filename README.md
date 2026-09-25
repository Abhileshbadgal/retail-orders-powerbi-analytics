# Retail Orders & Sales Performance Analytics (Power BI)

## 📌 Business Overview
This project delivers an executive-level interactive Power BI dashboard analyzing **$12.28M in total order revenue** across **2,500 transaction records**, **2,500 customer profiles**, and **92 Sales POCs**. The objective is to evaluate global sales channel efficiency, track regional performance against targets, and optimize sales team productivity.

* **Tools Used:** Power BI, DAX, Power Query, Microsoft Excel
* **Scale of Data:** 2,500 Orders | $12.28M Revenue | 14 Countries | 92 Sales POCs

---

## 🎯 Key Business Questions Addressed
1. **Revenue Benchmarking:** What is the overall gross revenue, total order count, and Average Order Value (AOV)?
2. **Regional & Channel Splits:** Which geographic markets and order channels (App, Website, WhatsApp) drive the highest volume and value?
3. **Target Attainment:** How are sales teams and individual Sales POCs performing against their 2023 sales targets?

---

## 💡 Key Findings & Data Insights

* **Overall Revenue Performance:** Total revenue reached **$12,275,890** across 2,500 orders with an Average Order Value (**AOV**) of **$4,910.36**.
* **Geographic Top Drivers:** 
  * **USA** generated the highest volume with **$4.27M** (888 orders).
  * **France** (**$1.64M**, 324 orders) and **Spain** (**$1.38M**, 269 orders) represent the top European markets.
* **Order Source Balance:** Revenue is evenly distributed across channels:
  * **Website:** 639 orders ($3.14M)
  * **WhatsApp:** 635 orders ($3.12M)
  * **App:** 626 orders ($3.07M)
  * **Other:** 592 orders ($2.95M)
* **Team Performance vs. Target:**
  * **Team Alpha** exceeded target expectations, generating **$3.86M** (**104.7% target achievement** vs. $3.69M target).
  * Top performing POC: **Diego Freyre** achieved **$1.09M** in sales (**108.9% of $1.00M target**).

---

## 📐 Custom DAX Measures Engineered

```dax
// Total Revenue
Total Revenue = SUM(Orders[Order Value])

// Total Orders Count
Total Orders = COUNTROWS(Orders)

// Average Order Value (AOV)
Average Order Value = DIVIDE([Total Revenue], [Total Orders], 0)

// Target Achievement %
Target Achievement % = DIVIDE([Total Revenue], SUM('Sales Targets'[2023 Sales Target]), 0)
