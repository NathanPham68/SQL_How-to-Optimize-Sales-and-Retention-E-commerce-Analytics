# [SQL] How to Optimize Sales and Retention? | E-commerce Analytics

<img width="1920" height="800" alt="image" src="https://github.com/user-attachments/assets/db704c9a-cf77-4ee9-a422-e2d4ca0f885e" />

## Table of Contents
I. [📌 Introduction](#I.-Introduction)

II. [📂 Dataset](#II.-Dataset)

III. [🧠 Main Process](#III.-Main-Process)

IV. [📊 Exploring the Dataset](#IV.-Exploring-the-Dataset)

V. [🔎 Final Conclusion](#V.-Conclusion)

## I. Introduction
🎉Overview:
This project aims to provide insights and visualizations into the AdventureWorks database, which is a sample database provided by Microsoft for learning and testing purposes.

The AdventureWorks database contains data related to a fictitious bicycle manufacturer, including information on products, sales, customers, and employees. In this project, we will use console.cloud.google to analyze the data in order to gain a better understanding of the business operations of AdventureWorks.

To get started with this project, we will need to have access to the AdventureWorks database and have Google Cloud Platform account.

🏹 Objective:
This project examines sales, customer retention, and inventory patterns in AdventureWorks to:

✔️ Assess sales performance and trends in category growth.

✔️ Pinpoint top-performing territories and evaluate the impact of seasonal discounts.

✔️ Evaluate inventory levels and stock-to-sales ratios for optimization.

✔️ Study customer retention trends to enhance loyalty programs.

👤 Who is this project for?

✔️ Sales & Marketing Teams

✔️ Supply Chain & Inventory Managers

✔️ Business Analysts & Decision-makers

## II. Dataset

📂 Dataset Access - [AdventureWorksDW2019.bak](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms)

The eCommerce dataset is stored in a public Google BigQuery dataset. To access the dataset, follow these steps:

* Sign in to your Google Cloud Platform account and create a new project.
* Navigate to the BigQuery dashboard and select your newly created project.
* In the navigation panel, select "Add Data" and then select "Search Projects".
* Enter the project ID "adventureworks2019" and click "Enter".
* Click on the table "adventureworks" to the dataset.

📂 Requirements
* Query Editing Tool - Microsoft SQL Server Management Studio (SSMS)

📂 Table Schema & Data Snapshot

<details>
  <summary><strong>Table: Session Data</strong></summary>

| Column Name |	Data Type |	Description |
| ---         | ---       | ---         |
|fullVisitorId|	STRING|	Unique visitor ID|
|date|	STRING|	Session date in YYYYMMDD format|
|totals|	RECORD|	Aggregated session metrics|
|totals.bounces|	INTEGER|	1 if session bounced, else NULL|
|totals.hits|	INTEGER|	Total number of hits in the session|
|totals.pageviews|	INTEGER|	Total number of pageviews|
|totals.visits|	INTEGER|	1 for interactive sessions, NULL otherwise|
|totals.transactions|	INTEGER|	Total number of e-commerce transactions|
|traffic.source|	STRING|	Traffic source (e.g., search engine, URL, referrer)|

</details>

<details>
  <summary><strong>Table: Hits Data</strong></summary>

| Column Name |	Data Type |	Description |
| ---         | ---       | ---         |
|hits|	RECORD|	Contains details of individual hits|
|hits.eCommerceAction|	RECORD|	All e-commerce actions during the session|
|hits.eCommerceAction.action_type|	STRING|	Action type (view, add-to-cart, checkout, purchase, etc.)|
|hits.product|	RECORD|	Nested product details for e-commerce transactions|
|hits.product.productQuantity|	INTEGER|	Quantity of product purchased|
|hits.product.productRevenue|	INTEGER|	Revenue from product purchase (scaled by 10^6)|
|hits.product.productSKU|	STRING|	Product SKU|
|hits.product.v2ProductName|	STRING|	Product Name|

</details>

## III. Main Process

1️⃣ Data Cleaning & Preprocessing
* Ensured session and transaction data integrity
* Filtered out incomplete or irrelevant records

2️⃣ Exploratory Data Analysis (EDA)
* Analyzed bounce rates, page views, and transactions
* Identified key e-commerce actions and trends

3️⃣ SQL Analysis
* Used window functions, joins, and aggregations to extract insights
* Created queries for session behavior and revenue analysis

## IV. Exploring the Dataset
### Query 01: Calculate Quantity of items, Sales value & Order quantity by each Subcategory in L12M
[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:305d0077c9174b34acfe97e3a71bbe19)
* SQL code

![image](https://github.com/user-attachments/assets/e7c56c28-8c07-4b1b-a681-39f408c4f620)

* Query results

![image](https://github.com/user-attachments/assets/f19ee6e3-b8af-4da8-a5a4-c7aba32072a1)

### Query 02: Calculate % YoY growth rate by SubCategory & release top 3 cat with highest grow rate
[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:f32cff4e377f4ee499fbaa51425bc001)
* SQL code

![image](https://github.com/user-attachments/assets/5ba93385-671c-4e13-95cc-f043691f45e4)

* Query results

![image](https://github.com/user-attachments/assets/0d4a18ae-8d24-4a31-a106-e153d54ab550)

### Query 03: Ranking Top 3 TeritoryID with biggest Order quantity of every year
If there's TerritoryID with same quantity in a year, do not skip the rank number

[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:e28c14941d7646ada0899fc259795ba4)
* SQL code

![image](https://github.com/user-attachments/assets/eb390f7a-246b-4007-9117-f46a93b20b10)

* Query results

![image](https://github.com/user-attachments/assets/12c18025-1ec7-48d7-867e-f11f2deb349d)

### Query 04: Calculate Total Discount Cost belongs to Seasonal Discount for each SubCategory
[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:16682e27bdaa4989914f4b454c308a00)
* SQL code

![image](https://github.com/user-attachments/assets/122bf524-b59f-4c00-9ae9-476272795061)

* Query results

![image](https://github.com/user-attachments/assets/4e5a2b0e-73ec-4cae-b40e-0fbf8f947abb)

### Query 05: Retention rate of Customer in 2014 with status of Successfully Shipped (Cohort Analysis)
[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:d616903810904471b83a9be70a5efcc0)
* SQL code

![image](https://github.com/user-attachments/assets/2decc231-86c5-4c6e-a369-7639abc31841)

* Query results

![image](https://github.com/user-attachments/assets/d37fa23d-480f-49f7-8d64-829464e91aae)

### Query 06: Trend of Stock level & MoM diff % by all product in 2011. If %gr rate is null then 0. Round to 1 decimal
[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:5dacf766edbc4fd5a0ad7c358066bf8d)
* SQL code

![image](https://github.com/user-attachments/assets/d21307de-80d8-40a5-940c-42aec3c84f6f)

* Query results

![image](https://github.com/user-attachments/assets/41bd95b5-3502-4895-ba9c-8821d6b41012)

### Query 07: Calculate Ratio of Stock / Sales in 2011 by product name, by month
Order results by month desc, ratio desc. Round Ratio to 1 decimal

[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:abe8741e20264f0ea115bebb3c08a3b2)
* SQL code

![image](https://github.com/user-attachments/assets/341472ea-be67-4828-8a87-ebb913e04c3b)

* Query results

![image](https://github.com/user-attachments/assets/f5dc0bf0-7cfb-490f-be33-191b2d6a38ba)

### Query 08: No of order and value at Pending status in 2014
[Link to code](https://console.cloud.google.com/bigquery?sq=322729696559:3d423d5a8aed4dbb8868d6de075f131f)
* SQL code

![image](https://github.com/user-attachments/assets/d7c9b0df-2146-4485-a6e1-7de8a650e929)

* Query results

![image](https://github.com/user-attachments/assets/cbcc398b-1813-48e4-af2b-40225f0827fd)

## V. Conclusion
✔️ Enhance the product page experience to lower bounce rates.

✔️ Deliver personalized offers to highly engaged users.

✔️ Streamline the checkout process to minimize cart abandonment.
