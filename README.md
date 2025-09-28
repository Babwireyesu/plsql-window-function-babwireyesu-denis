# plsql-window-function-babwireyesu-denis
PL/SQL window functions assignment for PL
# PL/SQL Window Functions Assignment – Babwireyesu Denis

## Problem Definition

**Business Context**  
Denis Tech Business Group Ltd – Retail Analytics Department – Consumer Goods Industry

**Data Challenge**  
The company wants to analyze regional sales performance and customer behavior across its product catalog. With growing competition, it’s important to identify top-performing products, track monthly sales trends, and segment customers for targeted marketing.

**Expected Outcome**  
Gain insights into product popularity by region and quarter, monitor monthly growth, and classify customers into quartiles to guide promotional strategies.

---

## Success Criteria

To solve the business problem, I focused on five measurable goals using PL/SQL window functions:

1. **Top 5 products per region and quarter** – using `RANK()`
2. **Running monthly sales totals** – using `SUM() OVER()`
3. **Month-over-month growth** – using `LAG()` and `LEAD()`
4. **Customer quartiles** – using `NTILE(4)`
5. **3-month moving averages** – using `AVG() OVER()`

---

## Database Schema

### Tables

- **customers**: Stores customer information  
- **products**: Stores product catalog  
- **transactions**: Records sales data

### ER Diagram

![ER Diagram](er_diagram/er_diagram.png)

---

## Window Functions Implementation

Each query includes comments, screenshots, and a short interpretation.

### 1. Ranking – `RANK()`, `ROW_NUMBER()`, `DENSE_RANK()`, `PERCENT_RANK()`
**Use Case**: Identify top customers by revenue  
**Screenshot**: `screenshots/rank-results.png`  
**Interpretation**: The top 5 customers in Kigali contributed over 60% of total revenue.

### 2. Aggregate – `SUM()`, `AVG()`, `MIN()`, `MAX()` with frame comparisons  
**Use Case**: Running totals and trend analysis  
**Screenshot**: `screenshots/sum-over-results.png`  
**Interpretation**: Monthly sales peaked in Q2, with consistent growth in beverages.

### 3. Navigation – `LAG()`, `LEAD()`  
**Use Case**: Month-over-month growth  
**Screenshot**: `screenshots/lag-lead-results.png`  
**Interpretation**: Sales dropped in March due to seasonal factors, then recovered in April.

### 4. Distribution – `NTILE(4)`, `CUME_DIST()`  
**Use Case**: Customer segmentation  
**Screenshot**: `screenshots/ntile-results.png`  
**Interpretation**: Top quartile customers spent 4x more than the lowest quartile.

---

## Results Analysis

### 1. Descriptive – What happened?  
Sales were highest in Kigali and Huye during Q2. Beverages and packaged foods led across all regions.

### 2. Diagnostic – Why?  
Promotional campaigns and regional preferences influenced product performance. Kigali customers preferred premium items, while Huye leaned toward essentials.

### 3. Prescriptive – What next?  
Focus marketing efforts on top quartile customers in Kigali. Introduce bundled offers in Huye to increase average transaction value.

---

## References

1. Oracle PL/SQL Documentation  
2. TutorialsPoint – PL/SQL Window Functions  
3. GeeksforGeeks – SQL Analytics  
4. AUCA Course Materials  
5. Oracle Live SQL Examples  
6. W3Schools SQL Reference  
7. Stack Overflow – PL/SQL Best Practices  
8. dbdiagram.io – ER Diagram Tool  
9. draw.io – Schema Visualization  
10. Academic Paper: “Window Functions in Business Intelligence”

> “All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.”

---

