# Market Basket Analysis

## 1. Business Case

FreshMart, a small-sized grocery chain, has been experiencing stagnating sales despite a steady flow of customers. Shoppers visit the store, buy what they came for, and leave without exploring additional product options. The management suspects that untapped cross-selling opportunities exist, but they lack the data-driven insights needed to optimize product placements and marketing efforts.

The goal of this project is to uncover hidden purchasing patterns and recommend strategic business actions. By analyzing transaction data, we can:

With the help of Power BI and Market Basket Analysis, this project extracts valuable insights to drive actionable business decisions for FreshMart.

## 2. Data Structure

An A/B experiment will be conducted on the Zapoos website, where different versions of **promotional copies** will be tested. Three variations of copys with different approaches will be defined and shown randomly to different user groups, **these are the versions**:

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/9ba9ef66524f9c86b41e07d4c0d3b23097d1764c/img/copys.JPG)

The metric that will define which copys is better is **sales**. Considering the statistical power ($\beta$ = 0.8), a **stratified sampling** was carried out according to the 3 purchasing times, obtaining a total sample of **738 users** who purchased at least one product in the website, in the table below we can see the distribution of **time and treatment** in the sample:

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/88add6c7d2c8e55d0d28b974642ba878266e4b12/img/sampling.JPG)

## 3. Statistical Results

Once the data was collected, an **analysis of variance (ANOVA)** was executed in order to determine if there is any statistical difference between the performance of the copys. The **F test** indicates that there are statistical significance (p < 0.05), as we see in the table below highlighted in yellow:

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/c47b2096d52b8c8c97db24c76e92a324e07a406c/img/anova.JPG)

In order to identify which copy was the best, I executed multiple comparisons using the **Tukey and Bonferroni post hoc tests**, in all the cases all the differences were statistical significant (p < 0.05), in the table below we can see the results highlighted in yellow:

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/c47b2096d52b8c8c97db24c76e92a324e07a406c/img/posthoc.JPG)

Finally, I checked the **assumptions** of the ANOVA technique, this is important to get valid statistical inferences. First, **normality assumption** was checked using the **Kolmogorov-Smirnov** and S**hapiro-Wilk** tests, in both cases the results indicate that the assumption was accomplished.

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/c47b2096d52b8c8c97db24c76e92a324e07a406c/img/normal.JPG)

The **homoscedasticity assumption** was checked using the **Levene's test**, in this case the results indicate that the variances are the same in all groups.

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/c47b2096d52b8c8c97db24c76e92a324e07a406c/img/variance.JPG)

All the results indicate that we can trust the statistical inferences and determine with confidence **the right copy** in order to increase the sales.

## 4. Business Recommendation

The A/B test results showed that **Copy B generated the highest sales revenue**, reaching $247, compared to Copy A with $178 and Copy C with $157. Given this outcome, Copies A and C will be discarded in favor of Copy B. We se the results in the following plot:

![image alt](https://github.com/GeorgeWLZD/ab_testing_project/blob/e42e7ca58f09e5f91136335ef20767f213bb8be5/img/results.JPG)

Based on this result, the **recommendations** are:
- **Implement copy B permanently**: Given its superior performance, Copy B should be set as the default promotional message across all relevant pages.
- **Monitor performance continuously**: Even though Copy B outperformed the other versions, ongoing monitoring and analysis should be conducted to ensure its effectiveness over time.
- **Optimize other website elements**: Since promotional copy impacts sales, additional A/B tests should be conducted on other website components, such as call-to-action buttons, images, and layout.
- **Personalize copy for different audiences**: Further segmentation and testing should be explored to tailor promotional messages to different customer segments and preferences.
