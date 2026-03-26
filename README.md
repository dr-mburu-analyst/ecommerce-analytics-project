# E-commerce Funnel Analysis (SQL | BigQuery)

## Overview
This project analyzes customer behavior across an e-commerce platform using event-level data. The goal is to understand how users move through the purchase funnel, identify drop-off points, and uncover opportunities to improve conversion rates and revenue.

The analysis was performed using SQL in Google BigQuery.

---
## Objectives
- Analyze user behavior across key funnel stages
- Measure conversion rates between stages
- Identify where users drop off before purchase
- Evaluate performance by traffic source
- Calculate time-to-conversion
- Assess revenue and average order value

---
## Tools & Technologies
- SQL
- Google BigQuery
- Data aggregation and transformation using CTEs
  
- -
## Dataset
The dataset consists of event-level e-commerce data, including:
- `user_id` – unique identifier for each user
- `event_type` – user action (page_view, add_to_cart, checkout_start, payment_info, purchase)
- `event_date` – timestamp of the event
- `product_id` – product interacted with
- `amount` – transaction value (for purchases)
- `traffic_source` – acquisition channel (email, organic, paid, social)

![Funnel Query](images/)
##  Key Analyses

### 1. Funnel Analysis
Tracked how users move through the funnel:
- Page View → Add to Cart → Checkout → Payment → Purchase

### 2. Conversion Rates
Calculated conversion rates between each stage to identify drop-offs.

### 3. Traffic Source Analysis
Compared user behavior and conversion performance across different acquisition channels.

### 4. Time-to-Conversion
Measured the time it takes users to move from initial interaction to purchase.

### 5. Revenue Analysis
Calculated:
- Total revenue
- Number of orders
- Average order value

## 💡 Key Insights
- Significant drop-off observed between product view and add-to-cart stage (~30% conversion)
- High conversion rates in later stages, with over 90% of users completing purchase after entering payment
- Traffic sources show varying performance in both engagement and conversion
- On average, users complete their journey in approximately 24 minutes

## 🚀 Business Impact
This analysis helps identify friction points in the customer journey and provides insights that can be used to:
- Improve product engagement
- Optimize checkout experience
- Increase conversion rates
- Drive higher revenue

## 📈 Recommendations

### 1. UX & Website Optimization
The analysis shows a high conversion rate in the final stages of the funnel (80%+ from payment to purchase), indicating a smooth and frictionless checkout experience.

**Recommendation:**
Focus optimization efforts on earlier stages of the funnel rather than redesigning checkout. Improving product pages and user engagement before checkout is likely to yield higher returns.

---

### 2. Marketing Strategy Optimization
While social media drives a significant portion of traffic, it demonstrates lower conversion rates compared to other channels such as email.

**Key Insight:**
- Social media: High traffic, low conversion  
- Email: Lower traffic, higher conversion (~13%)

**Recommendations:**
- Shift social strategy from awareness campaigns to retargeting campaigns  
- Implement email capture strategies (e.g., pop-ups, discounts) to convert visitors into leads  
- Increase investment in high-performing channels like email marketing  

---

### 3. Revenue & Cost Efficiency
The average order value (AOV) is approximately $115, which provides a benchmark for evaluating marketing spend efficiency.

**Key Insight:**
Low conversion rates from certain channels (e.g., social) combined with high acquisition costs can reduce profitability.

**Recommendations:**
- Establish customer acquisition cost (CAC) thresholds aligned with AOV  
- Audit marketing spend across channels to ensure positive return on investment  
- Reallocate budget toward higher-converting channels  

---

### 4. Funnel Optimization Opportunities
A significant drop-off occurs between the product view and add-to-cart stage (~30% conversion).

**Recommendations:**
- Improve product page design, pricing strategy, and product descriptions  
- Introduce incentives such as discounts or free shipping  
- Conduct A/B testing to identify factors impacting user engagement  

