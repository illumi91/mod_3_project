# Hypothesis testing project on Northwind Database by Luigi Fiori

## Files 

- Northwind_small.sqlite: Raw Data
- Project_Northwind_db.ipynb: Notebook for Analysis
- Presentation.pdf

## Introduction

We need to perform soem hypothesis tests on the Northwind Database.
This is a Microsoft open sorce/free database.

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_category/Northwind_ERD.png](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_category/Northwind_ERD.png)

Our goal is to formulate hypothesis tests such that we can get some valuable insights for a potential company.

My approach for this project has been:

1. Formulate interesting questions-->In order to get some useful insights
2. EDA--> In order to get an understanding of our data summarizing their main characteristics mainly through visualization 
3. Defining Null and Alternative Hypotheses-->Answer to the research question and guide data collection and interpretation
4. Set Alpha level--> I used a alpha level of 0.05 for all my Hypotheses
5. Test our Data Set--> Use different tests to understand the p-value
6. Check Effect Size--> d cohen's formula
7. Obtain valuable Insights--> Give some raccomandations


### Formulate our Questions

1. Does discount amount have a statistically significant effect on the quantity of a product in an order? If so, at what level(s) of discount?

2. Is it December, considering the Christmas time period in it, the month with the highest revenue?

3. Does discount amount have a statistically significant effect on the revenue of a product in an order? If so, at what level(s) of discount?

4. There is a statistically significant difference on shipping time between different shipper companies?

5. There is a statistically significant difference in terms of Revenue for different countries?

6. There is statistically significant difference in terms of Revenue between different categories?


Let's go through each question!


# 1. Does discount amount have a statistically significant effect on the quantity of a product in an order? If so, at what level(s) of discount?


### Defining Null and Alternative Hipothesis

Considering that we wanna observe if the quantity sold discounted is greater than the quantity sold not discounted we'll perform a **_One Tail Test_**.

**H_null** = qt. discounted sold <= qt. not discounted sold
**H_alt** =  qt. discounted sold > qt. not discounted sold

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/1.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/1.PNG)


### Welch's Test

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/welch_disc_qt.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/welch_disc_qt.PNG)

### Effect Size

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/cohen_disc_qt.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/cohen_disc_qt.PNG)

### With or Without Discount Applied

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/p_val_disc_nodisc_qt.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/p_val_disc_nodisc_qt.PNG)

### Conclusions

Results are all statistically significant except for the level 0.1.

This means that a discount of 10% on average doesn't have any impact on the quantity sold compared to not applying the discount.

We advice so, to use a 5% discount instead, d Cohen's for 5% discount results being the one with the highest effect size, moreover smaller leave us more profit but still does have an  higher impact on quantity sold compared to the 10%, or to apply an higher discount level to try to increase the quantity sold.

### Different Levels of Discounts

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/p_val_disc_differ_qt.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pictures_qt_disc/p_val_disc_differ_qt.PNG)

### Conclusions

Results, as we can see from the p-value, are all not statistically significant.

This means that we failed to reject the null hypothesis.

We advice the management build their strategies taking in consideration the presence or not of the discount instead of a comparison between different levels of discount.


# 2. Is it December, considering the Christmas time period in it, the month with the highest revenue?

### Defining Null and Alternative Hipotheses

**H_null** = Revenue for December <= Revenue other month

**H_alt** =  Revenue for December > Revenue other month


![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_december/Capture.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_december/Capture.PNG)

As we thought during December we've got an high Revenue peak due to the Christmas, but as we can see May results having the highest peak followed by August.

### Welch's Test

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_december/p-value_diff_months.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_december/p-value_diff_months.PNG)

### Conclusions

As we can see we failed to reject our hyphotheses for April, May, June, August and November.

This means that our Revenue is actually higher on these months compared to December.

Our advice is to focus our product strategies during these months, May furthermore gives us the highest effect size.

In fact could probably be more difficult trying to increase the overall Revenue during December, being the potential competition much higher and obstinate.



# 3. Does discount amount have a statistically significant effect on the revenue of a product in an order? If so, at what level(s) of discount?

### Defining Null and Alternative Hipotheses

**H_null** = Revenue with discount <= Revenue without discount

**H_alt** =  Revenue with discount > Revenue without discount

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/rev_disc_nodisc.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/rev_disc_nodisc.PNG)

### Welch's Test

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/welch_rev.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/welch_rev.PNG)

### Effect Size

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_december/cohen_rev.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_december/cohen_rev.PNG)

### With or Without Discount Applied

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/p_val_disc_nodisc.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/p_val_disc_nodisc.PNG)

### Conclusions

Results are not statistically significant for the levels 0.1, 0.15 and 0.2.

This means that a discount of 10%, 15% and 20% on average doesn't have any impact on the Revenue for the product sold compared to not applying the discount.

We advice so, to use a 5% discount instead, that being smaller leave us more profit but still does have an  higher impact on Revenue, considering also the highest effect  size, compared to the 10%, 15% an 20% or to apply a 25% discount level to try to increase the total Revenue.

###  Different Levels of Discounts

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/p_val_differ_discs.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_revenue_disc/p_val_differ_discs.PNG)

### Conclusions

We reject our null hypothesis for 5% and 20% discounts and 20% and 25% discounts.

This means that there's statistical significant difference in terms of Revenue taking in consideration these 2 different levels of discount.

Our advice is to focus our attention on 5% and 20% , the d Cohen's effect size is significantly higher and the possibly strategies leave us with a higher profit being on comparison 25% discount higher than these 2.


# 4. There is a statistically significant difference on shipping time between different shipper companies?

### Defining Null and Alternative Hipotheses

**H_null** = there is no statistically difference beetwen different companies in terms of shipping time

**H_alt** =  there is statistically difference beetwen different companies in terms of shipping time

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_shippers/Capture.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_shippers/Capture.PNG)

### Tukey Test

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_shippers/tukey_ship.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_shippers/tukey_ship.PNG)

### Conclusions

The test shows clearly that Federal Shipping is more efficient .

We advice the management to understand why the others companies are taking longer and in case to ask for a discount or to switch all the orders to the Federal shipper.

# 5. There is a statistically significant difference in terms of Revenue for different countries?

### Defining Null and Alternative Hipotheses


**H_null** = there is no statistically  significant difference beetwen Europe and North-America in terms of Revenue

**H_alt** =  there is statistically significant difference beetwen Europe and North-America in terms of Revenue

![https://github.com/illumi91/mod_3_project/blob/master/pics_countries/ei.PNG](https://github.com/illumi91/mod_3_project/blob/master/pics_countries/ei.PNG)


### Conclusions

We reject the Null Hypothesis for all Groups compared, in terms of Revenue.

The Profit is the same in proportion no matter which Group we take in consideration.



# 6. There is statistically significant difference in terms of Revenue between different categories?


### Defining Null and Alternative Hipotheses

**H_null** = there is no statistically difference beetwen different categories in terms of Revenue

**H_alt** =  there is statistically difference beetwen different categories in terms of Revenue


![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_category/pic_categ.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_category/pic_categ.PNG)


### Tukey Test

![https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_category/Capture.PNG](https://raw.githubusercontent.com/illumi91/dsc-mod-3-project-online-ds-pt-051319/master/pics_category/Capture.PNG)

### Conclusions

From our test results that there's a significant difference between categories.

Comes out that the categories with the highest Revenue are Seafood, Produce and Meat/Poultry.

In particular we raccomand to focus our production on Produce.

Being the description of this category "Dried fruit and bean curd" we know that are easy to conserve and ship compared to Seafood and Meat/Poultry.