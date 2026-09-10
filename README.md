[![繁體中文](https://img.shields.io/badge/繁體中文-點擊查看-blue?style=for-the-badge)](README.zh-TW.md)
&nbsp;&nbsp;
[![简体中文](https://img.shields.io/badge/简体中文-点击查看-blue?style=for-the-badge)](README.zh-CN.md)

# Chung Man (Ross) Tang

### BI & Operations | Power BI, SQL & Reporting | Trading and Logistics Background

I build practical reporting and analytics solutions that help trading, wholesale and SME teams turn sales, inventory and operational data into clearer dashboards, actionable insights and better day-to-day decisions.

My background combines logistics operations, sales and shipping coordination, inventory control, import/export documentation and business reporting. I use Power BI, SQL, Excel and Python to support sales, product, customer, invoice and inventory analysis.

**Career focus:** BI & Operations Analyst · Operations Analyst · Sales Operations Analyst · Reporting Analyst · Inventory Analyst  
**Portfolio:** [Notion Portfolio](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link) · **LinkedIn:** [Chung Man Tang](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## Skills & Tools

**Business & Operations Analytics**
- Sales reporting, profitability and discount analysis
- Inventory turnover, stockout, dead stock, ABC classification and replenishment planning
- Customer journey, conversion funnel and lifetime value analysis
- Marketing performance analysis: CTR, CVR, CPA, ROI and ROAS
- KPI reporting and process improvement

**Programming & Querying**
- SQL: MySQL, PostgreSQL, Google BigQuery
- Python: pandas, openpyxl

**Business Intelligence & Visualisation**
- Power BI: DAX, data modelling, interactive dashboards
- Power Query and Excel reporting

**Data Engineering & Modelling**
- dbt: staging and marts layered modelling
- Star Schema and Snowflake Schema
- ETL / ELT pipeline design, analytical views and data validation

**Business & Supporting Tools**
- Excel: PivotTables, advanced formulas and Power Query
- Git / GitHub
- NAS and UPS setup and maintenance for small-team business continuity

---

## Featured Projects

### 1. Sales & Profitability Analysis
**MySQL · Python · Power BI**

Analysed the Kaggle Superstore Sales Dataset: 51,000+ rows across 2011–2014 and seven global markets, to identify product profitability drivers and discount strategy risks.

- Built a Snowflake-schema data warehouse in MySQL: staging → dimensions → fact table → analytical views
- Performed bidirectional reconciliation to validate data integrity across pipeline layers
- Delivered a 3-page interactive Power BI dashboard covering executive KPIs, product performance and promotion impact
- **Key outcome:** Identified loss-making Furniture Tables despite sales growth, demonstrating the need for discount governance and profit-margin monitoring

<div align="left">
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis">
    <img src="https://img.shields.io/badge/View_Project-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. E-Commerce Customer Journey Analytics
**BigQuery · PostgreSQL · dbt · Python · Power BI**

End-to-end customer journey analysis using approximately 274,000 GA4 event records from the GA4 Obfuscated Sample E-Commerce dataset in Google BigQuery public data for November 2020.

- Extracted nested GA4 event data from BigQuery and loaded it into PostgreSQL
- Built a dbt transformation pipeline: staging → marts, with incremental models, surrogate keys and 26 automated data-quality tests (`PASS=26`)
- Modelled a funnel fact table (`fact_sessions`) and customer lifetime-value dimension (`dim_customers`)
- Analysed conversion performance by traffic source, device and geography
- **Key outcome:** Identified major drop-off before product view and found referral traffic produced the strongest conversion rate of approximately 2.2%–2.3%

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey">
    <img src="https://img.shields.io/badge/View_Project-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="E-Commerce Customer Journey Analytics">
  </a>
</div>

---

### 3. Traffic Sources & Ad ROI Analysis
**Python · Google BigQuery · SQL · Power BI**

Analysed advertising effectiveness and ROI across Google Ads, Facebook Ads, Email, Organic and Direct channels using reproducible simulated full-year 2024 data.

- Generated reproducible simulated data using Python: pandas, NumPy and Faker with `seed=42`
- Executed a BigQuery ETL pipeline including NULL checks, deduplication, standardisation and derived fields
- Built a star-schema data model: `campaigns` → `ad_impressions` / `sessions` / `conversions`, with analytical SQL views
- Delivered a 3-page interactive Power BI dashboard covering channel performance, CTR vs CVR and campaign ROI ranking
- **Key outcome:** Email Abandoned Cart achieved ROAS of 45.12x at CPA of $2.27, while Google Display Remarketing was the only negative-ROI campaign with ROAS of 0.70x and ROI of -30%

> **Portfolio note:** This project uses reproducible simulated data for educational and portfolio purposes. Metrics and recommendations are illustrative.

<div align="left">
  <a href="https://github.com/ross-bi/03_Traffic_Sources_Ad_ROI_Analysis">
    <img src="https://img.shields.io/badge/View_Project-03_Traffic_Sources_Ad_ROI_Analysis-blue?style=for-the-badge&logo=github" alt="Traffic Sources and Ad ROI Analysis">
  </a>
</div>

---

### 4. Inventory Performance Analysis
**PostgreSQL · Python · SQL · Power BI**

Analysed full-year 2016 inventory performance for a multi-store liquor retailer using the PwC × Kaggle Inventory Analysis Case Study dataset: approximately 12.8 million sales transactions across 80 stores.

- Built a Python bulk loader using `psycopg2` and `COPY` to load the 12.8M-row sales file
- Executed a three-layer ELT pipeline: raw → staging → marts, with defensive casting and seven-section data-quality validation
- Designed a star schema with product, store, vendor and date dimensions plus sales and inventory-snapshot fact tables
- Implemented static ABC classification in PostgreSQL using window functions to avoid Power BI Import Mode calculation timeouts
- Calculated inventory turnover, DSI, stockout rate, dead-stock rate and reorder points
- Delivered a 3-page interactive Power BI dashboard covering executive overview, inventory risk and replenishment priorities
- **Key outcome:** Identified a 17.1% year-over-year inventory-value increase; Class C SKUs accounted for 61.67% of the catalogue but only 5% of revenue, highlighting overstock and working-capital risk

<div align="left">
  <a href="https://github.com/ross-bi/04_Inventory_Performance_Analysis">
    <img src="https://img.shields.io/badge/View_Project-04_Inventory_Performance_Analysis-blue?style=for-the-badge&logo=github" alt="Inventory Performance Analysis">
  </a>
</div>

---

## Selected Certifications

| Certificate | Institution | Verification |
|---|---|---|
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | [Verify](https://coursera.org/verify/professional-cert/JZMXX254FKRO) |
| Google Business Intelligence Professional Certificate | Google | [Verify](https://coursera.org/verify/professional-cert/P6RVCIH4QIRA) |
| IBM Generative AI for BI Analysts Specialization | IBM | [Verify](https://coursera.org/verify/specialization/142IUDS1KXQV) |
| Google Data Analytics Professional Certificate | Google | [Verify](https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ) |
| IBM Data Analyst Professional Certificate | IBM | [Verify](https://coursera.org/verify/professional-cert/2VW236K260MZ) |

---

## Contact

[![Notion](https://img.shields.io/badge/Notion-Portfolio-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## License

This repository is licensed under the [MIT License](./LICENSE).
