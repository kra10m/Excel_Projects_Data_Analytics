# Raw Data Directory

To adhere to data storage best practices and prevent repository bloat, the raw transaction dataset is not version-controlled in this repository.

---

## Source Dataset Information
* **Dataset Name:** Sample Superstore Dataset
* **Source:** [Kaggle - Vivek468 / Superstore Dataset Final](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
* **Format:** Comma-Separated Values (`.csv`)
* **Volume:** ~9,994 transactional records across multi-regional e-commerce retail operations.

---

## Schema Overview
The primary transactional file expected by the Power Query ETL pipeline contains the following fields:

| Field Name | Data Type | Description |
| :--- | :--- | :--- |
| `Row ID` | Integer | Unique identifier per row |
| `Order ID` | Text | Transaction order code |
| `Order Date` | Date | Date when the purchase was placed |
| `Ship Date` | Date | Date when the order was dispatched |
| `Ship Mode` | Text | Delivery level (Standard, Second Class, First Class, Same Day) |
| `Customer ID` | Text | Unique identifier for individual client |
| `Customer Name`| Text | Full customer identity |
| `Segment` | Text | Business market segment (Consumer, Corporate, Home Office) |
| `Country` | Text | Destination country |
| `City` | Text | Destination city |
| `State` | Text | Destination administrative state |
| `Postal Code` | Text | Regional delivery postal code |
| `Region` | Text | Broad geographic market (West, East, Central, South) |
| `Product ID` | Text | Unique SKU identifier |
| `Category` | Text | Macro-level product department |
| `Sub-Category` | Text | Micro-level product classification |
| `Product Name` | Text | Full item title |
| `Sales` | Decimal | Gross transactional revenue |
| `Quantity` | Integer | Units purchased |
| `Discount` | Decimal | Percentage discount applied |
| `Profit` | Decimal | Net margin gained or lost |

---

## Local Pipeline Setup
To refresh or replicate this analytical pipeline locally:
1. Download `Sample - Superstore.csv` directly from the Kaggle link above.
2. Place the file inside this directory:
   ```text
   Project_3-ecommerce-operations-analytics-engine/01_Raw_Data/Sample - Superstore.csv
