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
- **Highest Percentage of Coupons Accepted**: Carry out & Take away with 73.6%
- **Lowest Percentage of Coupons Accepted**: Bar with 41.12%

![TotalCouponAcceptance](https://github.com/user-attachments/assets/1c1c5e3a-beee-4630-b583-14dabf8915ea)

![TotalandAcceptedCoupons](https://github.com/user-attachments/assets/3b93d2eb-c98c-47a0-b3e3-cc180876c33f)

![PercAcceptCoupon](https://github.com/user-attachments/assets/1d653c84-0b9b-4391-a2c8-e9a2f0ce34cf)

