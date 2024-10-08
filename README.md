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

![MissingValuesPercent_2](https://github.com/user-attachments/assets/3642c56a-e71e-47d2-997c-a90bcd3a48ab)


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

![PercAcceptCoupon](https://github.com/user-attachments/assets/7ab54f06-5b27-408b-b314-b7525d154704)


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

![gender_education](https://github.com/user-attachments/assets/8541c413-b773-4d0c-a11a-05cd359fe79c)

  
### Problem Statement#2: Why does Carry away and takeout coupon category have the maximum acceptance rate

- **Regardless of how often drivers took takeaways previously, they all accepted the coupon with a similar rate.**
  - Interestingly, people who did not get takeaways during a month had the highest acceptance rate of 0.78.
- **Even with kids as passengers, the acceptance rate was 0.695. Some of these storemight s have drive-through options, which might help with the decision.**
- **Income did not factor into the decision. Acceptance rate for Carry Away and Take out with, income below 50K and above 50K was 0.75 and 0.72 respectively.**
- **Widowed people had a higher acceptance rate compared to other marital statuses. People with other marital statuses also had high acceptance rates.**
- **In rainy weather, the coupon acceptance rate was lowest, followed by snowy days and warm days.**
  - Even for rainy weather, the coupon acceptance rate was 0.61
- **When destination is Home: the acceptance is highest at 0.79 compared to acceptance of 0.65 when destination is work**
- **Having children or not doesnt affect the acceptance rate**
- **Probably the convenience of Carry Away and Take Out is the reason the acceptance rate is high.**
  - We may have also developed the habit of takeaways during the Covid pandemic. It will be interesting to see what the data was before and after the pandemic.ndemic.
- **This is also an essential meal and might be the reason that driver sought out for this more**
- **Restaurat USD(<$20) and Carry out & Take away**
  - Had high acceptance rates among all attributes including expiration, weather, temperature, passenger, gender, time, destination, age, income, marital status, and having children.
  - One hypothesis to support this is that for everyone food is essential and are ready to consider cost-effective options like Restarant (<$20) and Carry out & Take away.
- **Coffee House**, **Bar**, and **RestUSDurant ($20-50)**
  - Had lower acceptance rates among all attributes including expiration, weather, temperature, passenger, gender, time, destination, age, income, marital status, and having children.
  - People may not have time to go to a high-end restaurant on short notice of 1 day. It will cost them a lot more money even with the coupon.
  - Bars had higher acceptance among single men in their 20s without kids and friends as passengers. This narrows down the acceptance rate and the bars might not cost them as much to go by themselves anyway.
  - Both men and women had a similar acceptance rate for Coffee House; they would go only when they had nothing urgent to attend to. Like the Bar coupon, the coffee coupon might not give them significant monetary advantage.
- General Remark: The coupon with a longer expiration duration of 1 day has a higher acceptance rate than the coupon with a shorter expiration rate of 2 hours.
- 
### Problem Statement #3: What inference can be drawn from the Corelation Matrix

- Temperatue has very low positive corelation with coupon acceptance (0.055): 
- Having children has very low negative corelation with coupon acceptance (-0.048)
- toCoupon_GEQ5min: No corelation
- toCoupon_GEQ15min: low negative corelation (-0.083)
- toCoupon_GEQ25min: Moderate negative corelation (-0.1)
- direction_same: low positive corelation (0.0147)
- direction_opposite: low negative corelation (-0.0147); same magnitude as direction_same but opposite correlation.
- If the direction is opposite to the drive direcion, the driver will not accept coupon

### Conclusion and next steps

- Restaurant (<20 USD) and Carry Away Coupons had higher acceptance rate than coffee house, bar and restaurant(20To50USD)
- One information that is missing in the data set is what is the nature of the coupon. How much percentage off do users get?
- If we want to improve the traction for Coffee House, Bar and restaurant(20To50USD) we need to understand this metric. Perhaps offering a first free drink or coffee might persuade drivers to accept these coupons more.
