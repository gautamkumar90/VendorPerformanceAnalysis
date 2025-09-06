# 📊 Retail Vendor Performance Analysis  

## 🔎 Project Overview  
This project analyzes retail vendor performance using real-world inspired inventory and sales data. The goal is to uncover **patterns in purchasing, pricing efficiency, profitability, and inventory lock-ups** through **Exploratory Data Analysis (EDA)** and **statistical testing**.  

The analysis provides actionable insights into vendor contributions, bulk order benefits, pricing strategies, and inventory management.  

---

## 🎯 Objectives  
- Identify top vs. low-performing vendors.  
- Measure the impact of bulk purchasing on unit costs.  
- Detect locked capital in unsold inventory.  
- Compare profit margins between vendor groups using **confidence intervals** and **t-tests**.  
- Provide data-driven recommendations for pricing and promotional strategies.  

---

## 🛠 Tech Stack  
- **Programming:** Python  
- **Libraries:** Pandas, NumPy, Seaborn, Matplotlib, SciPy  
- **Database:** SQLite (for vendor and sales records)  
- **Environment:** Jupyter Notebook  

---

## 📊 Workflow
1. **Data Loading**
   - Connected to SQLite database and extracted vendor sales summary tables.
   - Verified available tables using SQL queries.

2. **Feature Engineering**
   - Added calculated columns:
     - `GrossProfit = TotalSalesDollars - TotalPurchaseDollars`
     - `ProfitMargin = (GrossProfit / TotalSalesDollars) * 100`
     - `StockTurnover = TotalSalesQuantity / TotalPurchaseQuantity`
     - `SalesToPurchaseRatio = TotalSalesDollars / TotalPurchaseDollars`

3. **Exploratory Data Analysis (EDA)**
   - Distribution plots (histograms + KDE) for numerical columns.
   - Boxplots for outlier detection.
   - Count plots for categorical columns (`VendorName`, `Description`).

4. **Data Cleaning**
   - Removed negative and zero values in profit, margin, and sales.
   - Filtered inconsistent records using SQL queries.

5. **Correlation Analysis**
   - Heatmap of numerical variables to study relationships between sales, purchases, and profitability.

6. **Vendor & Brand Performance**
   - Scatter plot of Sales vs. Profit Margin with thresholds for high margin and low sales.
   - Bar plots for **Top 10 Vendors** and **Top 10 Brands** by sales.
   - Pareto analysis & donut charts to assess vendor contribution to total market.

7. **Statistical Testing**
   - Computed **95% confidence intervals** for profit margins and sales.
   - Performed **t-tests** to check differences between vendor groups.

---

## 📈 Key Insights
- Some vendors/products were selling at a **loss** (negative gross profit).
- **Profit margin outliers** indicate potential premium products or pricing inefficiencies.
- **Freight cost variation** suggests logistics challenges.
- Pareto analysis showed that **~20% of vendors contribute ~80% of total sales**.
- T-tests confirmed **statistically significant differences** between certain vendor groups.

---

## 📊 Visualizations  
Some key visualizations generated during analysis:  

- ✅ **Pareto Chart** – Vendor contribution vs. cumulative %  
- ✅ **Donut Chart** – Purchase distribution among vendors  
- ✅ **Boxplot** – Impact of order size on unit price  
- ✅ **Confidence Interval Plots** – Top vs. low-performing vendors  
- ✅ **Scatter Plot** – Sales vs. Profit margin thresholds  

*(Screenshots included in `plots/` folder in repo)*  
