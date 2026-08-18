# 🛍️ Customer Shopping Behavior Analysis

> **End-to-End Data Analytics Pipeline: Python ETL → SQL Database → SQL Analysis → Power BI Dashboard**

## 🎯 Business Question

How can customer shopping behavior, product performance, revenue patterns, discounts, subscriptions, and customer segments be analyzed to improve retention, marketing, product strategy, and revenue?

## 📊 Dataset

- **Source:** Customer Shopping Behavior dataset
- **Size:** 3,900 customer purchase records × 18 columns
- **Description:** The dataset contains customer demographics, purchase details, product information, ratings, subscription status, shipping preferences, discounts, previous purchases, payment methods, and purchasing behavior.
- **Data Preparation:** 37 missing review ratings were imputed using the median rating of the respective product category.

## 🛠️ Tools Used

- **Python (pandas)** — Data extraction, cleaning, missing-value handling, standardization, and feature engineering
- **SQL / MySQL** — Data storage, EDA, aggregation, and business analysis
- **SQLAlchemy** — Database connectivity and loading cleaned data
- **Power BI** — Interactive dashboard, KPI cards, DAX measures, and slicers
- **GitHub** — Project documentation and version control

## 🔄 Project Workflow

```text
Raw CSV Data
     ↓
Python ETL
     ↓
Cleaned & Feature-Engineered Data
     ↓
SQL Database
     ↓
SQL Analysis & Business Questions
     ↓
Power BI Dashboard
     ↓
Business Insights & Recommendations
```

## 🔍 Methodology

The project follows a reproducible end-to-end analytics workflow. The raw CSV data was first loaded into Python using pandas. Data quality checks were performed using structural information and descriptive statistics. Missing review ratings were handled using category-level median imputation, column names were standardized to `snake_case`, and additional features such as `age_group` and `purchase_frequency_days` were created. A redundant promotional-code field was removed after checking its relationship with the discount field.

The cleaned dataset was then loaded into a SQL database using SQLAlchemy, creating a centralized source for analysis. SQL was used to perform exploratory analysis and answer 10 business questions covering revenue by gender, discount-dependent products, product ratings, shipping behavior, subscriptions, customer segmentation, product performance, repeat buyers, and revenue by age group.

Finally, Power BI was connected to the database using a SQL connector. KPI cards, DAX measures, charts, and interactive slicers were created to communicate the findings. The dashboard provides a business-friendly view of customer behavior, revenue, subscriptions, product performance, and other important dimensions.

## 📈 Key Findings

1. 💰 **Male customers generated more than 2× the revenue of female customers** — **$157,890 vs. $75,191**.
2. 👥 **Non-subscribers generated the majority of revenue** — **$170,436 vs. $62,645** from subscribers.
3. 🛒 **Average spending was almost identical** for subscribers and non-subscribers — **$59.49 vs. $59.87**, suggesting the current subscription program is not clearly driving higher spending.
4. ⭐ **Top-rated products** included **Gloves (3.86)**, **Sandals (3.84)**, and **Boots (3.82)**.
5. 🚚 Customers using **Express shipping spent slightly more on average** — **$60.48 vs. $58.46** for Standard shipping.
6. ❤️ **Loyal customers dominate the customer base** — **3,116 Loyal**, **701 Returning**, and **83 New** customers.
7. 🏷️ **Hat, Sneakers, and Coat** showed high discount dependency, with discount rates around **49–50%**, creating a potential margin risk.
8. 📦 Top-selling products included **Jewelry, Blouse, Sandals, and Jacket** across their respective categories.
9. 👤 Revenue was relatively balanced across age groups, indicating that **age alone is not a strong revenue differentiator**.

## 💡 Business Recommendations

- 🎯 **Prioritize customer retention:** With 3,116 customers classified as Loyal, focus marketing and loyalty investments on retaining existing high-value customers.
- 🏷️ **Review discount strategy:** Test price sensitivity and demand elasticity for discount-dependent products such as Hat, Sneakers, and Coat before reducing promotions.
- ⭐ **Promote high-performing products:** Feature highly rated products such as Gloves, Sandals, and Boots in marketing campaigns.
- 📦 **Strengthen product campaigns:** Highlight top-selling products such as Jewelry, Blouse, Sandals, and Jacket.
- 👨 **Use targeted marketing:** Male customers generated substantially higher revenue in this dataset, making them an important segment for targeted campaigns.
- 🚚 **Evaluate express shipping:** Express-shipping customers show slightly higher average spending, so premium shipping options could be explored as part of the customer experience strategy.
- 🔄 **Re-evaluate the subscription program:** Since average spending is almost the same for subscribers and non-subscribers, analyze subscription benefits and conversion drivers before increasing promotional investment.

## 📁 Project Files

- `data_cleaning.py` — Python ETL and data-cleaning workflow
- `analysis.sql` — SQL queries used for EDA and business questions
- `analysis.ipynb` — Jupyter notebook for Python-based analysis
- `powerbi_dashboard.pbix` — Power BI dashboard file
- `Project_Report.pdf` — Detailed project documentation and findings
- `README.md` — Project overview and documentation
- `dashboard_link` — 🔗 Power BI / dashboard link

> **Note:** Update the file names and `dashboard_link` above to match the actual files included in your GitHub repository.

## 📌 Business Questions Answered

1. What is the total revenue generated by each gender?
2. Which customers used discounts but still spent above the average purchase amount?
3. Which products have the highest average ratings?
4. How does average spending differ between Standard and Express shipping?
5. Do subscribers spend more than non-subscribers?
6. Which products are most dependent on discounts?
7. How are customers distributed across New, Returning, and Loyal segments?
8. What are the top products within each category?
9. Are customers with more than five purchases more likely to subscribe?
10. Which age groups contribute the most revenue?

## 📊 Dashboard Highlights

The Power BI dashboard includes:

- 💵 Total Revenue
- 👥 Total Customers
- ⭐ Average Review Rating
- 🛒 Average Purchase Amount
- 📈 Revenue analysis
- 👤 Customer segmentation
- 🏷️ Discount analysis
- 📦 Product performance
- 📋 Subscription analysis
- 🎚️ Interactive slicers for Subscription Status, Gender, Category, and Shipping Type

## ⚠️ Assumptions & Limitations

- The analysis is based on **3,900 purchase records** and represents the available dataset rather than the complete behavior of a real customer base.
- Missing review ratings were imputed using the median rating of the corresponding product category.
- Customer segments were defined using purchase-history information available in the dataset.
- Revenue and behavioral patterns describe the observed dataset and should be validated against larger historical datasets before making major business decisions.
- Correlation between customer characteristics and revenue should not automatically be interpreted as causation.

## 🚀 Conclusion

This project demonstrates a complete data analytics workflow from **raw transactional data to business-ready insights**. Python was used for ETL and data quality, SQL was used for centralized analysis and business queries, and Power BI was used to transform the results into an interactive dashboard.

The project highlights how an analyst can combine **Python + SQL + Power BI** to solve real-world business problems and turn raw customer data into actionable recommendations.

---

### 👩‍💻 Project Focus

**Customer Analytics | Retail Analytics | ETL | SQL | Python | Power BI | Business Intelligence**
