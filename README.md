# Project Overview
![](https://github.com/Pham-Hung-tns/Toy-Business-Model-Analysis/blob/409700572180cd1ea78f3feb0e75aad1f091c922/Images/General.png)
# Data Model
## 1. Purpose
```From 2003 to the second quarter of 2005, the toy business with seven global locations recorded trends in revenue, profit, and unit sales—all three moving in the same direction. As the number of units sold increased, revenue and profit increased, and vice versa. However, the data also revealed bottlenecks in inventory turnover, customer channels, and seasonal variations. This analysis explores each of these issues and suggests solutions.```

## 2. Project Structure
```The dataset provides information about a toy model wholesaler with 7 branches worldwide: North America (3 branches), Europe (2 branches), Japan, Australia. This company sells 7 different product lines: Classic Car, Vintage Car, Truck, Plane, Motorcycles, Ships, Trains. By the second quarter of 2005, they had reached and had 98 customers using their services```.

## 3. List of questions that can help analyze the data
* Overview and Time Trend Questions (To find insights into revenue growth and seasonality):
   - How have revenue, profit, and orders changed over time?
   - Are there seasonal variations? For example, in which quarter/month is revenue highest?
   - Is the revenue growth rate consistent, and are there any outliers that affect it?
   - Are time factors (e.g., holidays) correlated with the number of products sold?
* Geographic and Branch Questions (To find insights into revenue variance and distribution paradox):
   - How is revenue distributed across branches and geographic areas?
   - What is the average number of customers and revenue per branch/area?
   - Are there performance differences between branches, e.g. where is revenue lowest?
* Product and Sales Performance Questions (To gain insights into key products and inventory turnover):
   - Which product lines contribute the most to revenue and profit?
   - How does the average selling price compare to MSRP and import price, and what percentage of profit is accounted for?
   - What is the sell-through to inventory ratio, and are there any outliers?
* Customer and Segmentation Questions (To find insights into small and distinct customer segments):
   - How are customers segmented based on creditLimit, and what are the characteristics of each group?
   - What is the total number of customers and their distribution by region?
   - How do AOV (Average Order Value) and average orders differ by segment?

## 4. Important KPIs
**MSRP**: Manufacturer's Suggested Retail Price (MSRP) is the retail price recommended by the manufacturer. This is a reference price to evaluate whether the product is being sold at a discount or a deep discount.
   - A price lower than MSRP: This may indicate a strategy of discounting, promotion, or using discounts to stimulate sales. However, if the difference is too large, it can reduce profit margins and create a negative impression of the product's value.
   - A price close to or above MSRP: This indicates that the product may be positioned as a premium or competitive product, while helping to protect profit margins. However, if the price is too high compared to the market, it can reduce purchasing power.

## 5. Summary of findings
### The revenue growth trend is clear but slowing down and seasonal:
   - Revenue increased from 3.3 million USD in 2003 to 4.3 million USD in 2004 (up ~25%), but only reached 1.49 million USD in the first 2 quarters of 2005 (up ~10.4% compared to the same period in 2004).     Estimated for the whole year of 2005 is about 4.8 million USD, showing signs of slowing down.
   - Revenue explodes in the 4th quarter of each year, especially in November (peak, for example, 1 million USD in 2004), while December declines despite the festival. Other months are stable but not extraordinary (for example, June 2004 was only 150K USD).

### Branch and geographic performance is uneven:
   - Paris (Europe) leads with $2.96 million in revenue, followed by London (also Europe). Total Europe (2 branches) reaches $4.28 million, surpassing North America (3 branches: $2.21 million).
   - Other branches range from $0.46 to $1.37 million, with Tokyo (Japan) the lowest ($0.46 million) and Boston (North America) the lowest in the region ($0.84 million).
   - Customers are concentrated in Europe (45/98 customers) but only 2 branches, while Asia has only 1 branch (Tokyo).

### Key Products and Sales Performance:
   - Classic Cars and Vintage Cars accounted for 62/100 products, contributing the most to revenue. Average selling price was $89.95 (below MSRP), ~50% profit due to low import price ($54.26/product).
   - However, only 16.7% of imported products (out of 608,965 products) were sold, leading to low inventory turnover and inventory pressure.

### Small retail customer segment, focusing on high-end groups but not yet fully exploited potential:
   - Total 98 customers (only creditLimit > 0), mainly Europe (45) and North America (38). Segment: Low (25 customers, ≤62,850 USD), Average (55 customers, ≤108,899 USD), High (16 customers, ≤177,975 USD), VIP (2 customers, >177,975 USD).
   - VIP and High bring in large revenue (VIP: average 20 orders/order 369 products), but Average/Low are not well approached due to high selling prices (for example, Low Group only buys a maximum of ~679 products/order based on creditLimit).

### Pricing and Channel Issues:
   - Prices below MSRP indicate a discounting strategy, but are still high relative to Low/Average Group’s affordability, limiting access to new customers.
   - Small customer base (98) despite 7 global locations, indicating that wholesale channels have not expanded effectively, may need additional online/retail channels.

## 6. Key Issues and Improvements
### For slowing and seasonal revenue growth trends:
   - Build a stimulus program beyond Q4: Design seasonal promotional campaigns from Q2 (e.g., 20-30% off Classic Cars in May-July, based on low stability data in these months). Work with distribution partners (such as collector stores) to boost sales in Q1-3, targeting a 15% increase in Q2-3 revenue compared to current.
   - Diversify seasonal products: Introduce gift bundles (e.g., Vintage Cars combined with festival accessories) for Q4, but develop new (non-seasonal) product lines for other quarters to reduce dependence, aiming to increase the proportion of non-seasonal revenue to 40%.

### For uneven branch and geographic performance:
   - Expand infrastructure in Europe and Asia: Prioritize opening 1-2 new branches in Europe (e.g. Berlin or Madrid) to serve 45 existing customers, reducing transportation costs by 10-15% (based on customer address data). In Asia, open branches in China or Russia to compensate for low Tokyo (0.46 million USD), aiming to increase Asia revenue by 20% in 1 year.
   - Optimize branch resource allocation: Transfer 10-20% of inventory from Boston/Tokyo to Paris/London through branch data analysis in PowerBI. KPI tracking: Quarterly revenue/branch, aiming to balance North America to Europe (up from 2.21 million USD).
   - Localization Campaign: Customize marketing by region (e.g. promote Historic Vintage Cars for Europe, Modern Classic Cars for North America), use local customer data to personalize, target to increase current low Asian customers to 20 new customers.

### For the retail customer segment, focusing on the high-end group but not fully exploited:
   - Customer segmentation strategy: Design a separate price package for the Average/Low Group (e.g., a 25% discount combo for orders under 500 products, based on a creditLimit ≤108,899 USD), while prioritizing VIP services (fast delivery, personalized consultation) for 2 VIP customers. The goal is to increase the number of orders from Average/Low to 2-3 orders/customer/year.
   - Expand the customer file: Use segmentation data (Vip/High/Average/Low) to run an email campaign/targeted ads targeting 50 new potential customers in Europe/North America, based on city address. Track KPIs: Number of new customers (from 98 to 120) and AOV (Average Order Value) for the Low Group (increased from currently low).
