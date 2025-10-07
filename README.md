# 🧩 Full Data Extraction from a Realistic Sales Dataset  

This project demonstrates **data extraction techniques** using Python to generate and process realistic sales data. It showcases both **Full** and **Incremental Data Extraction** — two key concepts in data engineering and warehousing.

## 🔍 Overview

The script simulates **60 days of sales transactions** across multiple major retailers, then applies two data extraction approaches:

* **Full Extraction** → Loads the entire dataset from the source
* **Incremental Extraction** → Retrieves only new or updated records after a specified date

This setup mimics real-world ETL workflows, where efficiency and freshness of data are essential.

## ⚙️ Features

* Generates realistic, timestamped sales data
* Simulates multiple customer transactions across various retailers
* Demonstrates **Full vs Incremental Extraction** patterns
* Exports the dataset to CSV format for persistence
* Leverages **Pandas** for data manipulation and filtering

## 🧾 Data Structure

Each generated record contains the following columns:

| Column         | Description                                                     |
| -------------- | --------------------------------------------------------------- |
| `id`           | Unique transaction identifier                                   |
| `customers`    | Retailer name (Amazon, Walmart, Target, Best Buy, Costco, eBay) |
| `date`         | Transaction date                                                |
| `amount`       | Sales amount (range: 100–2000)                                  |
| `last_updated` | Timestamp of the latest record update                           |

## 🧩 Installation Requirements

Install dependencies before running the script:

```bash
pip install pandas numpy matplotlib seaborn
```

## 🚀 Usage

1. Run the script:

   ```bash
   python sales_data_extraction.py
   ```

2. The program will:

   * Generate **60 days** of synthetic sales data starting from **April 1, 2025**
   * Create **3–6 transactions** per day
   * Save the dataset to **sales data.csv**
   * Display both **Full Extraction** and **Incremental Extraction (after April 15, 2025)** samples

## 🧠 Code Components

### 🔸 Data Generation

* Simulates daily transactions for 60 consecutive days
* Randomizes timestamps within each day
* Generates realistic sales amounts and IDs

### 🔸 Data Extraction Methods

* **Full Extraction** → Loads the entire dataset from CSV
* **Incremental Extraction** → Filters records where `last_updated` > `last_extraction_date`

## 📊 Output

* **Generated File:** `sales data.csv`
* **Console Output:** Displays sample rows from both extraction methods for quick verification.

## 🛠️ Customization

You can tweak these parameters for different scenarios:

| Variable                    | Description                       |
| --------------------------- | --------------------------------- |
| `customers`                 | List of retailer names            |
| `start_date`                | Starting date for data generation |
| `range(60)`                 | Number of days to simulate        |
| `random.randint(3, 6)`      | Range of transactions per day     |
| `random.randint(100, 2000)` | Range of sales amounts            |

## 💡 Use Cases

This project is ideal for:

* Practicing **data extraction** and **ETL** concepts
* Testing **incremental data loading** strategies
* Creating **synthetic datasets** for analysis or demo pipelines
* Building foundational knowledge for **Data Warehousing & Mining**

## ⚠️ Note

This project is purely **educational**.
All generated data is **synthetic** and uses **future dates** for demonstration purposes only.
