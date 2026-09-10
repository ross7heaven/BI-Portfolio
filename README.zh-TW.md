[![English](https://img.shields.io/badge/English-Click_to_View-blue?style=for-the-badge)](README.md)
&nbsp;&nbsp;
[![简体中文](https://img.shields.io/badge/简体中文-点击查看-blue?style=for-the-badge)](README.zh-CN.md)

# 鄧仲文（Ross Tang）

### BI & Operations｜Power BI、SQL 與報表分析｜貿易及物流背景

我建立實用的報表及數據分析方案，協助貿易、批發及中小企團隊將銷售、庫存和營運數據，轉化為更清晰的儀表板、可行的商業洞察和更有效的日常決策。

我的背景結合物流營運、銷售及出貨協調、庫存管理、進出口文件及業務報表。我運用 Power BI、SQL、Excel 和 Python，支援銷售、產品、客戶、發票及庫存分析。

**職涯方向：** BI & Operations Analyst · Operations Analyst · Sales Operations Analyst · Reporting Analyst · Inventory Analyst  

**作品集：** [Notion Portfolio](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link) · **LinkedIn：** [Chung Man Tang](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 技能與工具

**業務及營運分析**
- 銷售報表、盈利能力及折扣分析
- 庫存週轉、缺貨、呆滯庫存、ABC 分類及補貨規劃
- 客戶旅程、轉換漏斗及客戶終身價值分析
- 營銷績效分析：CTR、CVR、CPA、ROI 及 ROAS
- KPI 報表及流程改善

**程式及查詢**
- SQL：MySQL、PostgreSQL、Google BigQuery
- Python：pandas、openpyxl

**商業智能及視覺化**
- Power BI：DAX、資料模型、互動式儀表板
- Power Query 及 Excel 報表

**數據工程及資料模型**
- dbt：staging 及 marts 分層資料模型
- Star Schema 及 Snowflake Schema
- ETL／ELT pipeline 設計、分析用 Views 及資料驗證

**業務及支援工具**
- Excel：PivotTables、進階公式及 Power Query
- Git／GitHub
- NAS 及 UPS 設置與維護，支援小型團隊的業務持續性

---

## 精選專案

### 1. 銷售與盈利能力分析
**MySQL · Python · Power BI**

分析 Kaggle Superstore Sales Dataset：涵蓋 2011 至 2014 年、七個全球市場及超過 51,000 筆紀錄，以找出產品盈利能力的關鍵因素及折扣策略風險。

- 在 MySQL 建立 Snowflake Schema 資料倉儲：staging → 維度表 → 事實表 → 分析用 views
- 執行雙向 reconciliation，驗證各資料管線層之間的資料完整性
- 建立三頁互動式 Power BI 儀表板，涵蓋管理層 KPI、產品表現及促銷影響
- **主要成果：** 發現 Furniture Tables 子類別即使銷售增長仍持續虧損，說明需要建立折扣管控及利潤率監察機制

<div align="left">
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis/blob/master/README.zh-TW.md">
    <img src="https://img.shields.io/badge/View_Project-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. 電商客戶旅程分析
**BigQuery · PostgreSQL · dbt · Python · Power BI**

使用 Google BigQuery Public Data 中的 GA4 Obfuscated Sample E-Commerce Dataset，針對 2020 年 11 月約 274,000 筆 GA4 event records 進行端到端客戶旅程分析。

- 從 BigQuery 提取巢狀 GA4 event data，並載入 PostgreSQL
- 建立 dbt 資料轉換 pipeline：staging → marts，包含 incremental models、surrogate keys 及 26 個自動化資料品質測試（`PASS=26`）
- 建立轉換漏斗事實表 `fact_sessions` 及客戶終身價值維度表 `dim_customers`
- 分析不同 traffic source、裝置及地區的轉換表現
- **主要成果：** 找出客戶在瀏覽產品前出現明顯流失，並發現 referral traffic 的轉換率最高，約為 2.2%–2.3%

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey/blob/main/README.zh-TW.md">
    <img src="https://img.shields.io/badge/View_Project-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="E-Commerce Customer Journey Analytics">
  </a>
</div>

---

### 3. 流量來源及廣告 ROI 分析
**Python · Google BigQuery · SQL · Power BI**

使用可重現的 2024 全年模擬數據，分析 Google Ads、Facebook Ads、Email、Organic 及 Direct 五個渠道的廣告成效及 ROI。

- 使用 Python、pandas、NumPy 和 Faker，以 `seed=42` 生成可重現的模擬數據
- 在 BigQuery 執行 ETL pipeline，包括 NULL 檢查、去重、標準化及衍生欄位建立
- 建立 Star Schema 資料模型：`campaigns` → `ad_impressions` / `sessions` / `conversions`，並建立分析用 SQL views
- 建立三頁互動式 Power BI 儀表板，涵蓋渠道表現、CTR 與 CVR 關係，以及 campaign ROI ranking
- **主要成果：** Email Abandoned Cart 的 ROAS 為 45.12x、CPA 為 $2.27；Google Display Remarketing 則是唯一負 ROI 的 campaign，ROAS 為 0.70x、ROI 為 -30%

> **作品集註記：** 本專案使用可重現的模擬資料，僅供學習及作品集展示用途；當中的指標及建議屬示範性質。

<div align="left">
  <a href="https://github.com/ross-bi/03_Traffic_Sources_Ad_ROI_Analysis/blob/main/README.zh-TW.md">
    <img src="https://img.shields.io/badge/View_Project-03_Traffic_Sources_Ad_ROI_Analysis-blue?style=for-the-badge&logo=github" alt="Traffic Sources and Ad ROI Analysis">
  </a>
</div>

---

### 4. 庫存績效分析
**PostgreSQL · Python · SQL · Power BI**

使用 PwC × Kaggle Inventory Analysis Case Study dataset，分析一間多門市酒類零售商於 2016 全年的庫存表現；資料涵蓋約 1,280 萬筆銷售交易及 80 間門市。

- 使用 `psycopg2` 和 `COPY` 建立 Python bulk loader，載入包含 1,280 萬筆紀錄的銷售檔案
- 執行三層 ELT pipeline：raw → staging → marts，包含 defensive casting 及七部分資料品質驗證
- 設計 Star Schema，包括產品、門市、供應商和日期維度表，以及銷售與庫存快照事實表
- 在 PostgreSQL 使用 window functions 實作 static ABC classification，以避免 Power BI Import Mode 的計算逾時問題
- 計算 inventory turnover、DSI、stockout rate、dead-stock rate 及 reorder points
- 建立三頁互動式 Power BI 儀表板，涵蓋管理層總覽、庫存風險及補貨優先次序
- **主要成果：** 發現庫存價值按年上升 17.1%；Class C SKU 佔產品目錄 61.67%，但只帶來 5% 營收，反映過量庫存及營運資金風險

<div align="left">
  <a href="https://github.com/ross-bi/04_Inventory_Performance_Analysis/blob/master/README.zh-TW.md">
    <img src="https://img.shields.io/badge/View_Project-04_Inventory_Performance_Analysis-blue?style=for-the-badge&logo=github" alt="Inventory Performance Analysis">
  </a>
</div>

---

## 精選證書

| 證書 | 頒發機構 | 驗證 |
|---|---|---|
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | [驗證](https://coursera.org/verify/professional-cert/JZMXX254FKRO) |
| Google Business Intelligence Professional Certificate | Google | [驗證](https://coursera.org/verify/professional-cert/P6RVCIH4QIRA) |
| IBM Generative AI for BI Analysts Specialization | IBM | [驗證](https://coursera.org/verify/specialization/142IUDS1KXQV) |
| Google Data Analytics Professional Certificate | Google | [驗證](https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ) |
| IBM Data Analyst Professional Certificate | IBM | [驗證](https://coursera.org/verify/professional-cert/2VW236K260MZ) |

---

## 聯絡方式

[![Notion](https://img.shields.io/badge/Notion-Portfolio-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 授權條款

本 repository 採用 [MIT License](./LICENSE) 授權。
