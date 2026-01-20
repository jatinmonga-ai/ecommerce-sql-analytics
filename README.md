# Capstone SQL & Analytics Project

**Description:**
This project demonstrates advanced SQL analytics using a sample e-commerce dataset. The workflow includes creating tables from an **online DB Fiddle**, importing them into a **local PostgreSQL database**, and performing analysis in **Jupyter Notebook**. The focus is on **window functions**, customer spend analysis, and deriving **business insights**.

---

## **Project Workflow**

### 1. Data Preparation
- The dataset was originally created and tested in [Online DB Fiddle](https://dbfiddle.uk/YEzOwka3).
- A local PostgreSQL database was created to store the tables: `customers`, `orders`, `order_items`, `products`, and `categories`.
- Tables were populated using the SQL scripts from DB Fiddle.
- The local database was then connected to **Jupyter Notebook** for analysis using `psycopg2` / `SQLAlchemy`.

---

### 2.  Analysis Using Jupyter Notebook
- **Window Functions Practice:**
  1. **LAG()** – Compare current order with previous orders to track trends and customer repeat behavior.
  2. **LEAD()** – Look at next order to analyze time gaps and potential churn.
  3. **ROW_NUMBER()** – Sequence customer orders to identify first and repeat purchases.
  4. **RANK() & DENSE_RANK()** – Rank customers by spend, with and without gaps.
  5. **Cumulative Spend (SUM() OVER)** – Running total of revenue per customer to identify top contributors.
  6. **Moving Average (AVG() OVER)** – Rolling average of order values to smooth short-term fluctuations.
  7. **NTILE() / 20% Quartiles** – Segment customers into 5 equal groups (top 20%, next 20%, etc.) for targeted analysis.

- **Visualizations:**
  - **Bar plots** for customer distribution by spend quartiles.
  - **Pie charts** to show percentage contribution of each quartile to total revenue.

---

### 3. Business Key Takeaways & Insights

| Insight | Description |
|---------|-------------|
| Top 20% Customers Contribution | Top 20% of customers generate a significant portion of total revenue. |
| Repeat Purchase Behavior | LAG() analysis shows which customers are repeat buyers; helpful for retention strategy. |
| Revenue Growth Tracking | Cumulative spend over time highlights revenue accumulation trends. |
| Customer Segmentation | 20% quartile ranking allows targeting high-value customers for marketing campaigns. |
| Rolling Average Trends | Moving average smooths spikes, highlighting true spending patterns. |

---

### **Technologies Used**
- **PostgreSQL** – Local database for structured data storage.
- **Jupyter Notebook** – SQL queries, Python integration, and visualization.
- **Pandas / Matplotlib / Seaborn** – Data extraction, manipulation, and plotting.
- **SQL Window Functions** – ROW_NUMBER, RANK, DENSE_RANK, LAG, LEAD, SUM, AVG, NTILE.

---

### **Project Highlights**
- Demonstrates **end-to-end SQL workflow**: DB creation → data import → window function analytics.
- Includes **real-world business insights** based on SQL outputs.
- Uses **Python and Jupyter Notebook** to visualize and interpret SQL results (bar plots and pie charts).
- Fully portfolio-ready for **data analyst or SQL-focused roles**.

---

### **How to Reproduce**
1. Clone the repository.
2. Create a local PostgreSQL database and import the tables using the SQL scripts.
3. Connect Jupyter Notebook to the database (update connection string).
4. Run the notebook cells to practice window functions and generate graphs.
5. Review the **Business Insights** section to understand the analytical outcomes.
