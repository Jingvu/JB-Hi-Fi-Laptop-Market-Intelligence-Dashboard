# JB-Hi-Fi-Laptop-Market-Intelligence-Dashboard

<img width="1968" height="1125" alt="JB Hi-Fi" src="https://github.com/user-attachments/assets/baf684e2-6937-4068-926c-7d14e54b53ce" />


## Project Status: Active & Refreshed Daily

This project moves beyond simple data scraping to build a strategic market intelligence tool. It answers the core business question: "What does it take to succeed in the competitive Australian laptop market?"

By capturing and analyzing live product data from a major retailer like JB Hi-Fi, this project creates a comprehensive overview of the pricing, specifications, and brand dynamics that define the industry, culminating in an interactive Power BI dashboard for strategic decision-making.

## Key Features
### 1. Pricing Landscape
- Tracks the full SKU and median prices across laptop categories (Standard, Lightweight, Performance, Gaming).
- Identifies top/bottom priced products, brand price trends, and SKU concentration.
- Helps buyers and stakeholders benchmark pricing range and market spread.

### 2. Spec Dominance
- Highlights dominant hardware specs: RAM tiers, SSD sizes, GPU/Processor popularity.
- Plots how these specs influence both price and market presence.
- Shows if premium specs (e.g. Apple M3, 2TB SSD) truly command higher prices.

### 3. Rating Momentum
- Analyzes customer feedback across brands.
- Bubble quadrant compares median price vs. rating vs. brand presence.
- Tracks rating trends and model popularity shifts over time.

### 4. On-Sale Insights
- Focuses on discounts, with average/max % discount and product-specific deals.
- Visualizes which brands are most aggressive on markdowns.
- Includes price vs. rating bubble to reveal value-for-money deals.

## Key Strategic Insights
The dashboard doesn't just show data, it reveals actionable insights. A hiring manager or brand strategist could use this tool to identify market gaps and competitive opportunities.

- **The Market is Sharply Divided into Tiers:** There's a clear split between elite, high-performance brands (Alienware/MSI averaging over $4.5K) and budget-focused players (Lenovo dominating the sub-$1K space). This reveals that a "one-size-fits-all" strategy is unviable, success depends on targeting a specific price tier.

## Data Pipeline Summary
This project covered the entire data lifecycle, from web scraping and governance to cleaning and Power BI visualization.

### 1. Data Collection & Scraping
**- Scraped product listings:** Used Selenium to extract laptop listings, prices, ratings, tags, and inferred brand names.\
**- Fetched and merged technical specifications:** Pulled specs ìnormation from product pages, parsed JSON, and merged into the main dataset.\
**- Data Governance & Management:** Saved daily scrapes, merged with duplication checks, auto-backed up, and validated schema and row counts.

### 2. Preprocessing & Data Cleaning (Python)
**- Initial Exploration:** Analyzed structure, data types, and distributions to guide cleaning and transformation.\
**- Product Info Cleanup:** Standardized prices, cleaned text fields, flagged discontinued items, and dropped noise.\
**- Technical Spec Cleanup:** Cleaned and bucketed specs, created flags, and ensured consistent formats across columns.

### 3. BI Integration (Power BI)
**- Final outputs:**\
    📁 results_tagged.csv → pricing, tags, brand, and lifecycle flags.\
    📁 results_specs_cleaned_all.csv → full product specs.
- Loaded into Power BI using Power Query, with additional transformations, grouping and calculations for dashboarding.

## View the Dashboard
https://app.powerbi.com/view?r=eyJrIjoiOWM1YzhiOTYtYjUwMS00ZWY4LThjMTItMGViNjc2OTkxYzcwIiwidCI6Ijc4NGU5YWE4LWI4ZjQtNGFhOS1iMTgzLTE5ODExNjE5YjllZSJ9

## How to Use
Click the link to explore the dashboard. Use filters and drill-downs to interact with different segments and discover trends.
