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
  
## Dataset
The dataset consists of event-level e-commerce data, including:
- `user_id` – unique identifier for each user
- `event_type` – user action (page_view, add_to_cart, checkout_start, payment_info, purchase)
- `event_date` – timestamp of the event
- `product_id` – product interacted with
- `amount` – transaction value (for purchases)
- `traffic_source` – acquisition channel (email, organic, paid, social)

<img width="662" height="30" alt="image" src="https://github.com/user-attachments/assets/29038c34-d706-4bc7-8189-c3992751c417" />

<img width="1153" height="460" alt="Sample dataset" src="https://github.com/user-attachments/assets/e1651527-2076-4652-8d5b-9a9124ca25c4" />


##  Key Analyses

### 1. Funnel Analysis
Tracked how users move through the funnel:
- Page View → Add to Cart → Checkout → Payment → Purchase

<img width="847" height="266" alt="image" src="https://github.com/user-attachments/assets/d6824240-3674-4820-80e2-430e24ed8aae" />

<img width="792" height="85" alt="funnel stages" src="https://github.com/user-attachments/assets/9312810d-95b1-4a70-9621-656eac552d55" />

**Key Insight:**  
- A large drop-off occurs between page view (5000 users) and add-to-cart (1553 users), indicating that only about 31% of users show purchase intent.
  
**Business Implication:**  
- This suggests potential issues with product appeal, pricing, or user experience on product pages.

### 2. Conversion Rates
- Calculated conversion rates between each stage to identify drop-offs.

<img width="924" height="537" alt="image" src="https://github.com/user-attachments/assets/d1b9320d-d637-47b9-90a2-b2c7fc9b3a14" />

<img width="1337" height="100" alt="funnel stages conversion rates" src="https://github.com/user-attachments/assets/df9059e5-1bf0-42e9-9329-0be5d7cdbcc5" />

**Key Insights:**  
- View → Cart conversion is relatively low (~31%), representing the largest drop-off in the funnel  
- Cart → Checkout (~71%) and Checkout → Payment (~82%) show strong progression  
- Payment → Purchase (~92%) indicates minimal friction in the final step
  
**Business Implication:**  
- The checkout process is highly optimized, and improvement efforts should focus on earlier funnel stages where the majority of users are lost.

### 3. Traffic Source Analysis
Compared user behavior and conversion performance across different acquisition channels.

<img width="1034" height="206" alt="funnel by source" src="https://github.com/user-attachments/assets/bbf00bcd-08d9-45a7-87e0-740aa9bc8e7c" />

**Key Insights:**  
- Social media drives a high volume of traffic but has the lowest conversion rate  
- Email shows the highest conversion efficiency despite lower traffic volume  
- Organic and paid channels fall in between in terms of performance
  
**Business Implication:**  
Marketing efforts should prioritize high-converting channels like email and shift social media strategy toward retargeting and lead generation rather than awareness alone.

### 4. Time-to-Conversion
- Measured the time it takes users to move from initial interaction to purchase.
  
<img width="792" height="86" alt="image" src="https://github.com/user-attachments/assets/0b40a77e-8188-4ff8-827a-7a6332092e3f" />

**Key Insight:**  
- On average, users complete their journey from initial interaction to purchase in approximately 24 minutes.

**Business Implication:**  
- The relatively short conversion window suggests that users who intend to purchase do so quickly, making real-time engagement strategies (e.g., discounts, reminders) highly effective.

### 5. Revenue Analysis
Calculated:
- Total revenue
- Number of orders
- Average order value

<img width="779" height="110" alt="funnel revenue" src="https://github.com/user-attachments/assets/625e2cdc-4f8c-4f4d-9e0b-7b7bd20926ba" />

**Key Insights:**  
- Total revenue is driven by a relatively small subset of users who complete purchases  
- Average order value (AOV) is approximately $115
  
**Business Implication:**  
- Improving conversion rates earlier in the funnel could significantly increase total revenue without increasing traffic.

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

