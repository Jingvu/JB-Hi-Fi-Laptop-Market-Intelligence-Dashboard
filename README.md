# JB-Hi-Fi-Laptop-Market-Intelligence-Dashboard

## Project Status: Active & Refreshed Daily
View the Dashboard: https://app.powerbi.com/view?r=eyJrIjoiOWM1YzhiOTYtYjUwMS00ZWY4LThjMTItMGViNjc2OTkxYzcwIiwidCI6Ijc4NGU5YWE4LWI4ZjQtNGFhOS1iMTgzLTE5ODExNjE5YjllZSJ9

This project moves beyond simple data scraping to build a strategic market intelligence tool. It answers the core business question: "What does it take to succeed in the competitive Australian laptop market?"

## Key Features
### 1. Pricing Landscape
<img width="1957" height="1125" alt="JB Hifi_Pricing" src="https://github.com/user-attachments/assets/e6d410ff-32c5-4825-b334-78dfe276e52f" />

- Tracks the full SKU and median prices across laptop categories (Standard, Lightweight, Performance, Gaming).
- Identifies top/bottom priced products, brand price trends, and SKU concentration.
- Helps buyers and stakeholders benchmark pricing range and market spread.

### 2. Spec Dominance
<img width="1979" height="1125" alt="JB Hifi_Specs" src="https://github.com/user-attachments/assets/0dc8f460-d0e6-4b66-880e-de7b54c11b8a" />

- Highlights dominant hardware specs: RAM tiers, SSD sizes, GPU/Processor popularity.
- Plots how these specs influence both price and market presence.
- Shows if premium specs (e.g. Apple M3, 2TB SSD) truly command higher prices.

### 3. Rating Momentum
<img width="1958" height="1125" alt="JB Hifi_Rating" src="https://github.com/user-attachments/assets/d25912d6-e1c7-4994-a44d-0bab71e628d0" />

- Analyzes customer feedback across brands.
- Bubble quadrant compares median price vs. rating vs. brand presence.
- Tracks rating trends and model popularity shifts over time.

### 4. On-Sale Insights
<img width="1206" height="684" alt="image" src="https://github.com/user-attachments/assets/afa3df29-a627-4bab-8855-9b272836c671" />


- Focuses on discounts, with average/max % discount and product-specific deals.
- Visualizes which brands are most aggressive on markdowns.
- Includes price vs. rating bubble to reveal value-for-money deals.

## Key Strategic Insights
### Which brands dominate different price tiers?
- The overall median price is $2.1K, with Gaming laptops commanding the highest median at $3.5K, while Standard models start from $2K.
- MSI dominates the gaming segment with wide price coverage ($1.1K–$11.8K) and holds 20% of all SKUs, 35.4% of gaming.
- ASUS, HP, and Lenovo heavily cover the budget segment (sub-$1K), offering options for price-sensitive customers.

### What specs are most common and drive up prices?
- Intel dominates both GPU and CPU share, followed by NVIDIA.
- The most common spec profile is 16GB RAM, 14” displays, and 1TB SSD—reflecting demand for compact yet capable devices.
- High-end configurations like NVIDIA RTX GPUs, Intel Ultra 9, and >1TB SSD are key drivers pushing prices beyond $5K.
- Despite Apple’s strong SKU presence, Windows 11 Home is the most common OS across listings.

### Are customers paying for quality or just branding?
- Apple earns top ratings (~5.0) with premium prices.
- MSI offers biggest discounts but lower ratings, potential quality concern.
- HP, Lenovo, and Dell hit the value sweet spot: strong ratings + lower prices.

### Which brands perform best under discount?
- ~48% of SKUs are discounted; 20–30% is the most common band.
- Apple and Dell retain high ratings post-discount.
- ASUS and HP show less rating improvement when discounted, suggesting limited impact on perceived value.
- MSI offers the highest number of discounted products, but Dell and ASUS feature the steepest markdowns.

## Data Pipeline Summary
This project covered the entire data lifecycle, from web scraping and governance to cleaning and Power BI visualization.

### 1. Data Collection & Scraping
- **Scraped product listings:** Used Selenium to extract laptop listings, prices, ratings, tags, and inferred brand names.
- **Fetched and merged technical specifications:** Pulled specs ìnormation from product pages, parsed JSON, and merged into the main dataset.
- **Data Governance & Management:** Saved daily scrapes, merged with duplication checks, auto-backed up, and validated schema and row counts.

### 2. Preprocessing & Data Cleaning (Python)
- **Initial Exploration:** Analyzed structure, data types, and distributions to guide cleaning and transformation.
- **Product Info Cleanup:** Standardized prices, cleaned text fields, flagged discontinued items, and dropped noise.
- **Technical Spec Cleanup:** Cleaned and bucketed specs, created flags, and ensured consistent formats across columns.

### 3. BI Integration (Power BI)
- **Final outputs:**\
    📁 results_tagged.csv → pricing, tags, brand, and lifecycle flags.\
    📁 results_specs_cleaned_all.csv → full product specs.
- Loaded into Power BI using Power Query, with additional transformations, grouping and calculations for dashboarding.

## How to Use
Click the link to explore the dashboard. Use filters and drill-downs to interact with different segments and discover trends.
