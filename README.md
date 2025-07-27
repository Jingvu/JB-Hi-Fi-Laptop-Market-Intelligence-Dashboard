# JB-Hi-Fi-Laptop-Market-Intelligence-Dashboard
<img width="2434" height="1374" alt="JB Hi-Fi" src="https://github.com/user-attachments/assets/3ad24b6d-bfcf-4a5b-9c3a-838476b7ee11" />


## Project Status: Active & Refreshed Daily

This project moves beyond simple data scraping to build a strategic market intelligence tool. It answers the core business question: "What does it take to succeed in the competitive Australian laptop market?"

By capturing and analyzing live product data from a major retailer like JB Hi-Fi, this project creates a comprehensive overview of the pricing, specifications, and brand dynamics that define the industry, culminating in an interactive Power BI dashboard for strategic decision-making.

## Key Strategic Insights
The dashboard doesn't just show data, it reveals actionable insights. A hiring manager or brand strategist could use this tool to identify market gaps and competitive opportunities.

- **The Market is Sharply Divided into Tiers:** There's a clear split between elite, high-performance brands (Alienware/MSI averaging over $4.5K) and budget-focused players (Lenovo dominating the sub-$1K space). This reveals that a "one-size-fits-all" strategy is unviable, success depends on targeting a specific price tier.

## Data Pipeline Summary
This project covered the entire data lifecycle, from web scraping and governance to cleaning and Power BI visualization.\

### 1. Data Collection & Scraping
#### **a. Scraped product listings:**
  - Used Selenium (headless Chrome) to load all laptops from JB Hi-Fi by auto-clicking the “Load More” button.
  - Extracted product title, price, image URL, ratings, number of reviews, and promotional tags.
  - Inferred brand names from titles using a custom list.
#### **b. Fetched and merged technical specifications:**
  - Sent HTTP requests to each product page to extract hidden specs from window.themeConfig blocks.
  - Parsed and flattened the JSON into key-value pairs.
  - Merged spec data with the product list.
#### **c. Data Governance & Management:**
  - Automatically created a new file each day and saved that day’s scrape result as a CSV in jb_daily_data/ folder.
  - Ensured data integrity by padding tags and writing clean headers.
  - Each new file was merged into a master file after duplication checks (Used ['DateCollected', 'Title'] as unique keys for duplication check).
  - Created timestamped backups in jb_backup_data/ before every merge.
  - Added early exits and assert conditions to ensure files aren’t empty, schema matches, and row counts align post-merge.
  - Print statements notify about all steps and mismatches.\


### 2. Preprocessing & Data Cleaning (Python)
#### **a. Initial Exploration:**
  - Explored shape, useable columns, data types and descriptive summary for categorical and numerical columns.
  - Identified and removed duplicate product titles and irrelevant columns.
#### **b. Product Info Cleanup:**
  - Converted price fields to numeric, standardized boolean and text fields.
  - Removed irrelevant or sparse columns.
  - Ensured consistent brand formatting and product naming.
  - Compared the latest scrape date with each product’s final appearance.
  - Added Final appear day and a Discontinued flag to mark dropped SKUs.
#### **c. Technical Spec Cleanup:**
  - Dropped unused or noisy spec columns.
  - Bucketed and standardized spec fields, created new flags.
  - Ensured all columns are in the right data format.\


### 3. BI Integration (Power BI)
  - Final outputs:\
      📁 results_tagged.csv → pricing, tags, brand, and lifecycle flags.\
      📁 results_specs_cleaned_all.csv → full, enriched product specs.
  - Loaded into Power BI using Power Query, with additional transformations, grouping and calculations for dashboarding.

## View the Dashboard
https://app.powerbi.com/view?r=eyJrIjoiOWM1YzhiOTYtYjUwMS00ZWY4LThjMTItMGViNjc2OTkxYzcwIiwidCI6Ijc4NGU5YWE4LWI4ZjQtNGFhOS1iMTgzLTE5ODExNjE5YjllZSJ9

## How to Use
Click the link to explore the dashboard. Use filters and drill-downs to interact with different segments and discover trends.
