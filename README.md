Predictive Inventory & Customer Intelligence Engine

The Mission

In the world of e-commerce, data is noise unless it’s actionable. This project isn't just about looking at what we sold; it’s about predicting the future and understanding the human behavior behind the transactions.

I built this end-to-end analytics engine to bridge the gap between messy transactional data and high-level strategic decision-making. By combining Python (Prophet) for forecasting and Tableau for business intelligence, I’ve created a system that identifies high-value customers and predicts seasonal demand spikes before they happen.

The Tech Stack

Language: Python (Pandas, NumPy)

Predictive Modeling: Meta Prophet (Time-Series Forecasting)

Intelligence Layer: RFM (Recency, Frequency, Monetary) Segmentation

Visualization: Tableau Desktop

Environment: Google Colab

The Thought Process

Phase 1: Data Audit & Cleaning

Real-world data is filthy. I started with 1M+ rows of retail transactions.

Business Logic: I filtered out cancellations (invoices starting with 'C') and zero-priced items to ensure the revenue KPIs were 100% accurate.

Normalization: Engineered a TotalRevenue field and standardized timestamps into a Month_Year format to enable clean seasonality analysis.

Phase 2: Customer Behavioral Intelligence (RFM)

Not all customers are created equal. I implemented an RFM Model to score every customer from 1-5 on:

Recency: How recently they shopped (loyalty indicator).

Frequency: How often they buy (engagement indicator).

Monetary: Total lifetime value (revenue indicator).

Result: Created segments like "Champions" (555) and "At Risk" (111) to help marketing teams prioritize their budget.

Phase 3: Predictive Forecasting (Meta Prophet)

Instead of just looking at historical averages, I utilized Prophet to decompose the data into three critical components:

Growth Trend: Is the business actually expanding? (Spoiler: Yes, with a strong upward trajectory for 2012).

Weekly Seasonality: Identified Monday and Friday as peak transaction days, which is critical for warehouse labor planning.

Yearly Seasonality: Captured the "Holiday Surge," showing a massive demand spike starting in mid-November.

Business Insights & Conclusions

1. The Pareto Principle in Action

My RFM Treemap revealed that a small pocket of "Champions" (Segment 555) drives a disproportionate amount of total revenue.

Action: Recommended a VIP loyalty program to maximize retention for this specific group.

2. The Holiday Velocity

The Sales Velocity chart shows that Q4 isn't just a peak—it's a 2x surge.

Action: Calculated that safety stock levels must be increased by 40% starting in October to prevent stockouts identified by the predictive model.

3. The "Monday" Mystery

The weekly component plot showed that sales dip on Thursdays but surge on Mondays.

Action: Optimized supply chain "Reorder Points" to trigger on Thursdays, ensuring the warehouse is fully stocked for the Monday rush.

Link to the dataset: https://archive.ics.uci.edu/dataset/502/online+retail+ii (it was too big to upload, lol)
