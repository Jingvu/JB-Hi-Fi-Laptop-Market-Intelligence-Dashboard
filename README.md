# JB-Hi-Fi-Laptop-Market-Intelligence-Dashboard
<img width="2434" height="1374" alt="JB Hi-Fi" src="https://github.com/user-attachments/assets/3ad24b6d-bfcf-4a5b-9c3a-838476b7ee11" />


## Project Status: Active & Refreshed Daily

This project moves beyond simple data scraping to build a strategic market intelligence tool. It answers the core business question: "What does it take to succeed in the competitive Australian laptop market?"

By capturing and analyzing live product data from a major retailer like JB Hi-Fi, this project creates a comprehensive overview of the pricing, specifications, and brand dynamics that define the industry, culminating in an interactive Power BI dashboard for strategic decision-making.

## Key Strategic Insights
The dashboard doesn't just show data, it reveals actionable insights. A hiring manager or brand strategist could use this tool to identify market gaps and competitive opportunities.

- **The Market is Sharply Divided into Tiers:** There's a clear split between elite, high-performance brands (Alienware/MSI averaging over $4.5K) and budget-focused players (Lenovo dominating the sub-$1K space). This reveals that a "one-size-fits-all" strategy is unviable, success depends on targeting a specific price tier.

- **Apple is Justified by Customer Loyalty:** Apple successfully commands high prices by delivering the highest customer satisfaction (4.4/5 rating). This demonstrates a powerful brand moat built on user experience, proving that specs alone don't win the premium market. Any competitor in this space must compete on brand and satisfaction, not just price.

- **A "Sea of Sameness" Creates a Mid-Market Opportunity:** The analysis shows a crowded mid-range market saturated with similar specs (Windows 11, Intel processors). This signals a significant opportunity for a brand to differentiate itself not on core specs, but on design, unique features (e.g., battery life, build quality), or a superior customer service experience.

- **Ratings Volatility Indicates Market Fluctuation:** The dashboard tracks day-over-day rating changes, revealing market sentiment in near real-time. This metric could serve as an early warning system for brand reputation issues or the positive reception of a new product launch.

## Technical Workflow
To build this intelligence tool, I managed the full data lifecycle, from acquisition to visualization.

- **Live Data Acquisition:** I used a Python script using Selenium to perform a real-world web scraping task on JB Hi-Fi's dynamic. The script was designed to be robust, navigating product categories and handling "load more" events to capture a comprehensive dataset.

- **Data Transformation and Modeling:** I implemented a two-stage data wrangling strategy to handle the messy raw data. Initial cleaning and structuring were performed using Python and its Pandas library. The refined data was then ingested into Power BI, where I leveraged Power Query to merge it with the detailed specifications dataset and finalize the unified, reliable data model for analysis.

-** Interactive Dashboard Development:** Using Power BI, I developed three distinct dashboard views—Pricing Landscape, Spec Dominance, and Rating Momentum. The design focuses on intuitive navigation and clear, high-impact KPIs, allowing a non-technical user to immediately grasp key market insights and drill down for more detail.

## View the Dashboard
https://app.powerbi.com/view?r=eyJrIjoiOWM1YzhiOTYtYjUwMS00ZWY4LThjMTItMGViNjc2OTkxYzcwIiwidCI6Ijc4NGU5YWE4LWI4ZjQtNGFhOS1iMTgzLTE5ODExNjE5YjllZSJ9

## How to Use
Click the link to explore the dashboard. Use filters and drill-downs to interact with different segments and discover trends.
