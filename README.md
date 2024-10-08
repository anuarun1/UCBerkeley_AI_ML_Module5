# UCBerkeley_AI_ML_Module5
UC Berkeley AI ML Course: Module 5
### Data Entries
- **There are 26 columns and 12,684 entries.**
- **All the columns do not have the same number of entries, indicating some columns have missing data.**
- **All the columns do not have the same data type.**
### Data Pre-Processing Procedure
**Following steps were taken:**
1. **Identify the missing rows using `isnull`.**
2. **Determine the percentage of data that is missing.**
3. **Based on the percentage of missing data, necessary action was taken:**
    - **Column 'car' was removed from the analysis.**
    - **For columns 'Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20', 'Restaurant20To50', the entries with missing rows were removed from analysis.**
4. **Estimate the number of duplicate rows. Only 74 rows were duplicates in the dataset of over 12,000 entries. These duplicate rows were removed.**
![MissingValuesPercent](https://github.com/user-attachments/assets/ef28da3f-1b2e-4125-8b0f-1286234f9d13)



### Missing Data Summary
| Column              | Num of Missing Values | Percent of data missing | Action Taken                        | Reasoning                                                                 |
|---------------------|-----------------------|-------------------------|-------------------------------------|--------------------------------------------------------------------------|
| car                 | 108                   | 99.15%                  | Remove column from analysis         | Most of the data (99.15%) is missing. This data is not sufficient to make any inference.               |
| Bar                 | 12577                 | 0.84%                   | Removed the rows with missing values| 0.84% of data is missing; final inference won't be impacted.                 |
| CoffeeHouse         | 12467                 | 1.71%                   | Removed the rows with missing values| 1.71% of data is missing; final inference won't be impacted.                 |
| CarryAway           | 12533                 | 1.2%                    | Removed the rows with missing values| 1.2% of data is missing; final inference won't be impacted.                  |
| RestaurantLessThan20| 12554                 | 1.02%                   | Removed the rows with missing values| 1.02% of data is missing; final inference won't be impacted.                 |
| Restaurant20To50    | 12495                 | 1.5%                    | Removed the rows with missing values| 1.5% of data is missing; final inference won't be impacted.                 |
### Coupon Acceptance Statistics

- **Overall Acceptance Rate**: 56.84% of the total observations chose to accept the coupon.

![TotalCouponAcceptance](https://github.com/user-attachments/assets/1c1c5e3a-beee-4630-b583-14dabf8915ea)

### Coupon Acceptance Distribution
- **Highest Percentage of Coupons Accepted**: Carry out & Take away with 73.6%
- **Lowest Percentage of Coupons Accepted**: Bar with 41.12%

![TotalandAcceptedCoupons](https://github.com/user-attachments/assets/3b93d2eb-c98c-47a0-b3e3-cc180876c33f)

### The Seaborn bar plot function returns the aggregate mean as default. 

![PercAcceptCoupon](https://github.com/user-attachments/assets/1d653c84-0b9b-4391-a2c8-e9a2f0ce34cf)


### Reasoning as to why Restaurat USD(<$20) and Carry out & Take away might have higher acceptance compared to Coffee House, Bar and Restaurant  :
- The coupon with a longer expiration duration of 1 day has a higher acceptance rate than the coupon with a shorter expiration rate of 2 hours.
- **Restaurat USD(<$20) and Carry out & Take away**
  - Had high acceptance rates among all attributes including expiration, weather, temperature, passenger, gender, time, destination, age, income, marital status, and having children.
  - One hypothesis to support this is that everyone needs to eat at some point and are ready to consider cost-effective options like RestaranUSDt (<$20) and Carry out & Take away.
- **Coffee House**, **Bar**, and **RestUSDurant ($20-50)**
  - Had lower acceptance rates among all attributes including expiration, weather, temperature, passenger, gender, time, destination, age, income, marital status, and having children.
  - People may not have time to go to a high-end restaurant on short notice of 1 day. It will cost them a lot more money even with the coupon.
  - Bars had higher acceptance among single men in their 20s without kids and friends as passengers. This narrows down the acceptance rate and the bars might not cost them as much to go by themselves anyway.
  - Both men and women had a similar acceptance rate for Coffee House; they would go only when they had nothing urgent to attend to. Like the Bar coupon, the coffee coupon might not give them significant monetary advantage.

### Bar Coupon Observation Summary
- **41.0% of Bar Coupons were accepted**
- Acceptance rate of those who went to a bar 3 or fewer times a month: **0.37**
- Acceptance rate of those who went to a bar more than 3 times a month: **0.77**
- Acceptance rate of those who went to a bar more than once a month and are above the age of 25: **0.69**
- Acceptance rate of those who went to a bar more than once a month across all age groups: **0.69**
- Conclusion:** There is no difference between the two categories.
- Acceptance rate: Bar more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry: **0.71**
- Acceptance rate: Go to bars more than once a month, had passengers that were not a kid, and were not widowed: **0.71**
- Acceptance rate: Go to bars more than once a month and are under the age of 30: **0.72**
- Acceptance rate: Go to cheap restaurants more than 4 times a month and income is less than 50K: **0.46**
- Acceptance rate: Go to cheap restaurants more than 4 times a month and all incomes: **0.43**

### Bar Coupon Driver Hypothesis

- **Drivers who went to the bar more than 3 times a month are more likely to accept the Bar coupon**
- **Drivers under the age of 25 are less likely to accept the Bar coupon**
- **Drivers with kids are less likely to accept the Bar coupon**
- **Drivers under age 30 are more likely to accept the Bar coupon**
- **Drivers with passengers as friends are more likely to accept the Bar coupon**
- **Income level doesn't contribute much to Bar coupon acceptance rate:**
  - Income below 50K has an acceptance rate of 0.43 compared to the acceptance rate of 0.43 for all incomes

### Problem Statement#1: What are the differences between male and female drivers acceptance rate.
- Female and male acceptance rate: 0.55 and 0.59 respectively
- More Men accepted the coupon compared to Women by 4 %. Is it because the women have lower buying power. Lets see the difference between the womens and mens income, job and education. What percentage of the data is men and women?
- In the survery there are actually more women than male (6158) than female (5849)
-Data also shows Women do earn lesser in average compared to men. 
-There is no corelation between income and coupon acceptance rate for both men and women
      -Although both men and women in the category of "some high school" education had the highest acceptance rate
      -It was interesting to see that men and women with "some high school", their income level was below 25K, even though they were in age category ['26' '31' '46']. The ratio of men and women in this category was 50%. Their economic condition explains the higher coupon acceptance rate
- People with children had a lower acceptance rate of 0.54 compared to the group without children 0.59. 
  
