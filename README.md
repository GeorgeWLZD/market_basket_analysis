# Market Basket Analysis

## 1. Business Case

FreshMart, a small-sized grocery chain, has been experiencing stagnating sales despite a steady flow of customers. Shoppers visit the store, buy what they came for, and leave without exploring additional product options. The management suspects that untapped cross-selling opportunities exist, but they lack the data-driven insights needed to optimize product placements and marketing efforts.

The goal of this project is to uncover hidden purchasing patterns and recommend strategic business actions. By analyzing transaction data, we can:

With the help of Power BI and Market Basket Analysis, this project extracts valuable insights to drive actionable business decisions for FreshMart.

## 2. Data Structure

To conduct this analysis, I used a dataset containing 7,835 transactions and 170 unique products. The dataset was structured in two key stages:

**Raw Data**\
The original dataset consists of a transactional view, where each row represents a customer basket with multiple purchased products.
![image alt](https://github.com/GeorgeWLZD/market_basket_analysis/blob/fa688c1e3a50ff7950598a0691479e94ac9af9ee/img/data1.JPG)

**Processed Data** (Power BI Transformation)\
To perform Market Basket Analysis, the data was structured into association rules, including the following key metrics:
- Product 1: The first product in the association.
- Product 2: The second product in the association.
- Basket: The combination of Product 1 and Product 2.
- Support Basket: Frequency of the product pair appearing together in transactions.
- Confidence of Product 1: Probability that customers buying Product 1 will also buy Product 2.
- Confidence of Product 2: Probability that customers buying Product 2 will also buy Product 1.
- Lift: Strength of the association, measuring how much more likely two products are bought together compared to random chance.

![image alt](https://github.com/GeorgeWLZD/market_basket_analysis/blob/fa688c1e3a50ff7950598a0691479e94ac9af9ee/img/data2.JPG)

## 3. Results

The **Power BI dashboard** visualizes product associations and highlights strategic opportunities:

![image alt](https://github.com/GeorgeWLZD/market_basket_analysis/blob/3245c4a11cd008c2adbbffd1bd59fbf45a766809/img/viz.JPG)

**Association Rules Table**
- Strong product relationships have high Lift values (>2.0) and appear frequently in transactions (high Support).
- Example: Customers who buy Root Vegetables are 3 times more likely to also purchase Herbs.
- Opportunity: Bundle these items together in promotions.

**Scatter Plot** (Lift vs. Support)
- High Lift, Low Support: Hidden opportunities! These product pairs aren't bought together often, but when they are, the association is strong.
- Example: Wine and Cheese have a Lift of 4.2 but appear in only 2% of transactions.
- Opportunity: Increase visibility by placing these items closer together in-store or recommending them online.

**Network Graph Analysis**
- Some products act as key connectors, frequently appearing in multiple strong associations.
- Example: Whipped/sour cream, yogurt and root vegetables appeared wuite frequently.
- Opportunity: Position these “anchor products” in prime store locations or highlight them in digital marketing campaigns.

## 4. Business Recommendation

Based on the insights from the analysis, here are actionable business strategies:

**Increase Revenue with Bundling & Discounts**
- Promote high-lift product pairs with combo deals (e.g., Coffee + Pastries).
- Implement "Frequently Bought Together" sections in e-commerce.

**Optimize Store Layout & Digital UX**
- Place strongly related products closer together in physical stores.
- Use data-driven recommendations in e-commerce to enhance user experience.

**Improve Targeted Marketing & Promotions**
- High-lift, low-support products need awareness-building campaigns.
- Personalize discounts based on past customer purchases.

By leveraging Market Basket Analysis, FreshMart can drive revenue growth with minimal effort—simply by strategically placing and promoting products. This approach can further be enhanced with machine learning-based recommendation systems for real-time personalized offers. **The next step** is to implement automated product recommendations and use machine learning to refine cross-selling strategies.
