[![English](https://img.shields.io/badge/English-Click_to_View-blue?style=for-the-badge)](README.md)
&nbsp;&nbsp;
[![繁体中文](https://img.shields.io/badge/繁体中文-点击查看-blue?style=for-the-badge)](README.zh-TW.md)

# 邓仲文（Ross Tang）

### BI & Operations｜Power BI、SQL 与报表分析｜贸易及物流背景

我建立实用的报表及数据分析方案，协助贸易、批发及中小企团队将销售、库存和营运数据，转化为更清晰的仪表板、可行的商业洞察和更有效的日常决策。

我的背景结合物流营运、销售及出货协调、库存管理、进出口文件及业务报表。我运用 Power BI、SQL、Excel 和 Python，支持销售、产品、客户、发票及库存分析。

**职涯方向：** BI & Operations Analyst · Operations Analyst · Sales Operations Analyst · Reporting Analyst · Inventory Analyst  

**作品集：** [Notion Portfolio](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link) · **LinkedIn：** [Chung Man Tang](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 技能与工具

**业务及营运分析**
- 销售报表、盈利能力及折扣分析
- 库存周转、缺货、呆滞库存、ABC 分类及补货规划
- 客户旅程、转换漏斗及客户终身价值分析
- 营销绩效分析：CTR、CVR、CPA、ROI 及 ROAS
- KPI 报表及流程改善

**程序及查询**
- SQL：MySQL、PostgreSQL、Google BigQuery
- Python：pandas、openpyxl

**商业智能及可视化**
- Power BI：DAX、数据模型、交互式仪表板
- Power Query 及 Excel 报表

**数据工程及数据模型**
- dbt：staging 及 marts 分层数据模型
- Star Schema 及 Snowflake Schema
- ETL／ELT pipeline 设计、分析用 Views 及数据验证

**业务及支持工具**
- Excel：PivotTables、进阶公式及 Power Query
- Git／GitHub
- NAS 及 UPS 设置与维护，支持小型团队的业务持续性

---

## 精选专案

### 1. 销售与盈利能力分析
**MySQL · Python · Power BI**

分析 Kaggle Superstore Sales Dataset：涵盖 2011 至 2014 年、七个全球市场及超过 51,000 笔纪录，以找出产品盈利能力的关键因素及折扣策略风险。

- 在 MySQL 建立 Snowflake Schema 数据仓储：staging → 维度表 → 事实表 → 分析用 views
- 执行双向 reconciliation，验证各数据管线层之间的数据完整性
- 建立三页交互式 Power BI 仪表板，涵盖管理层 KPI、产品表现及促销影响
- **主要成果：** 发现 Furniture Tables 子类别即使销售增长仍持续亏损，说明需要建立折扣管控及利润率监察机制

<div align="left">
  <a href="https://github.com/ross-bi/01_Superstore_Sales_Analysis/blob/master/README.zh-CN.md">
    <img src="https://img.shields.io/badge/View_Project-01_Superstore_Sales_Analysis-blue?style=for-the-badge&logo=github" alt="Superstore Sales Analysis">
  </a>
</div>

---

### 2. 电商客户旅程分析
**BigQuery · PostgreSQL · dbt · Python · Power BI**

使用 Google BigQuery Public Data 中的 GA4 Obfuscated Sample E-Commerce Dataset，针对 2020 年 11 月约 274,000 笔 GA4 event records 进行端到端客户旅程分析。

- 从 BigQuery 提取巢状 GA4 event data，并载入 PostgreSQL
- 建立 dbt 数据转换 pipeline：staging → marts，包含 incremental models、surrogate keys 及 26 个自动化数据质量测试（`PASS=26`）
- 建立转换漏斗事实表 `fact_sessions` 及客户终身价值维度表 `dim_customers`
- 分析不同 traffic source、装置及地区的转换表现
- **主要成果：** 找出客户在浏览产品前出现明显流失，并发现 referral traffic 的转换率最高，约为 2.2%–2.3%

<div align="left">
  <a href="https://github.com/ross-bi/02_Ecommerce_Customer_Journey/blob/main/README.zh-CN.md">
    <img src="https://img.shields.io/badge/View_Project-02_Ecommerce_Customer_Journey-blue?style=for-the-badge&logo=github" alt="E-Commerce Customer Journey Analytics">
  </a>
</div>

---

### 3. 流量来源及广告 ROI 分析
**Python · Google BigQuery · SQL · Power BI**

使用可重现的 2024 全年仿真数据，分析 Google Ads、Facebook Ads、Email、Organic 及 Direct 五个渠道的广告成效及 ROI。

- 使用 Python、pandas、NumPy 和 Faker，以 `seed=42` 生成可重现的仿真数据
- 在 BigQuery 执行 ETL pipeline，包括 NULL 检查、去重、标准化及衍生字段建立
- 建立 Star Schema 数据模型：`campaigns` → `ad_impressions` / `sessions` / `conversions`，并建立分析用 SQL views
- 建立三页交互式 Power BI 仪表板，涵盖渠道表现、CTR 与 CVR 关系，以及 campaign ROI ranking
- **主要成果：** Email Abandoned Cart 的 ROAS 为 45.12x、CPA 为 $2.27；Google Display Remarketing 则是唯一负 ROI 的 campaign，ROAS 为 0.70x、ROI 为 -30%

> **作品集注记：** 本项目使用可重现的仿真数据，仅供学习及作品集展示用途；当中的指标及建议属示范性质。

<div align="left">
  <a href="https://github.com/ross-bi/03_Traffic_Sources_Ad_ROI_Analysis/blob/main/README.zh-CN.md">
    <img src="https://img.shields.io/badge/View_Project-03_Traffic_Sources_Ad_ROI_Analysis-blue?style=for-the-badge&logo=github" alt="Traffic Sources and Ad ROI Analysis">
  </a>
</div>

---

### 4. 库存绩效分析
**PostgreSQL · Python · SQL · Power BI**

使用 PwC × Kaggle Inventory Analysis Case Study dataset，分析一间多门市酒类零售商于 2016 全年的库存表现；资料涵盖约 1,280 万笔销售交易及 80 间门市。

- 使用 `psycopg2` 和 `COPY` 建立 Python bulk loader，加载包含 1,280 万笔纪录的销售档案
- 执行三层 ELT pipeline：raw → staging → marts，包含 defensive casting 及七部分数据质量验证
- 设计 Star Schema，包括产品、门市、供货商和日期维度表，以及销售与库存快照事实表
- 在 PostgreSQL 使用 window functions 实作 static ABC classification，以避免 Power BI Import Mode 的计算逾时问题
- 计算 inventory turnover、DSI、stockout rate、dead-stock rate 及 reorder points
- 建立三页交互式 Power BI 仪表板，涵盖管理层总览、库存风险及补货优先次序
- **主要成果：** 发现库存价值按年上升 17.1%；Class C SKU 占产品目录 61.67%，但只带来 5% 营收，反映过量库存及营运资金风险

<div align="left">
  <a href="https://github.com/ross-bi/04_Inventory_Performance_Analysis/blob/master/README.zh-CN.md">
    <img src="https://img.shields.io/badge/View_Project-04_Inventory_Performance_Analysis-blue?style=for-the-badge&logo=github" alt="Inventory Performance Analysis">
  </a>
</div>

---

## 精选证书

| 证书 | 颁发机构 | 验证 |
|---|---|---|
| Microsoft Power BI Data Analyst Professional Certificate | Microsoft | [验证](https://coursera.org/verify/professional-cert/JZMXX254FKRO) |
| Google Business Intelligence Professional Certificate | Google | [验证](https://coursera.org/verify/professional-cert/P6RVCIH4QIRA) |
| IBM Generative AI for BI Analysts Specialization | IBM | [验证](https://coursera.org/verify/specialization/142IUDS1KXQV) |
| Google Data Analytics Professional Certificate | Google | [验证](https://coursera.org/verify/professional-cert/RB0NWMXRN2MQ) |
| IBM Data Analyst Professional Certificate | IBM | [验证](https://coursera.org/verify/professional-cert/2VW236K260MZ) |

---

## 联络方式

[![Notion](https://img.shields.io/badge/Notion-Portfolio-black?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/Chung-Man-Ross-Tang-2cc75a3c84e1807d8e6ec0bad9e0fa84?source=copy_link)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chung-man-tang-2a7616177)

---

## 授权条款

本 repository 采用 [MIT License](./LICENSE) 授权。
