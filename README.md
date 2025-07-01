# [SQL] bicycle_manufacturer

## I. Introduction

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

