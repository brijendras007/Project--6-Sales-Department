# Advanced Retail Sales Forecasting Model

## Objective

The goal of this project is to develop an advanced predictive model to forecast future daily sales for a retail chain using historical sales data from 1115 stores. By analyzing and leveraging various features such as store type, promotions, holidays, and competition, the project aims to provide accurate sales predictions to optimize operations and enhance profitability.

## Dataset

### Features

- **Transaction ID**: Unique identifier combining Store and Date.
- **Store**: Unique store ID.
- **Sales**: Sales per day (target variable).
- **Customers**: Number of customers on a given day.
- **Open**: Boolean indicating whether a store is open (0 = closed, 1 = open).
- **Promo**: Indicates if the store is running a promotion on that day.
- **StateHoliday**: Type of state holiday affecting the store (a = public holiday, b = Easter holiday, c = Christmas, 0 = None).
- **SchoolHoliday**: Indicates if public schools were closed on that day.
- **StoreType**: Type of store (a, b, c, d).
- **Assortment**: Type of product assortment (a = basic, b = extra, c = extended).
- **CompetitionDistance**: Distance to the closest competitor store (in meters).
- **CompetitionOpenSince**: Date when the closest competitor store opened.
- **Promo2**: Indicates if the store is participating in a consecutive promotion (0 = not participating, 1 = participating).
- **Promo2Since**: Date when the store started participating in Promo2.
- **PromoInterval**: Describes the consecutive intervals when Promo2 starts (e.g., "Feb,May,Aug,Nov").

## Steps

1. **Import Libraries and Datasets**  
   Load the necessary libraries and import the training and store datasets separately.

2. **Analyze Data**  
   Perform an initial analysis of the datasets using functions like `info()` and `describe()`.

3. **Explore Data**  
   - Create histograms to visualize data distribution.
   - Check for NULL records and handle them appropriately.
   - Analyze the maximum number of customers and the count of open vs. closed stores.

4. **Data Cleaning**  
   - Filter out closed stores and drop the `Open` column.
   - Address missing values in the store dataset:
     - Set values to zero if `promo2` is zero.
     - Fill missing `CompetitionDistance` values with the average distance.
     - Set missing values in `CompetitionOpenSince` to zero.

5. **Merge DataFrames**  
   Combine the sales and store dataframes using the `Store` column.

6. **Correlation Analysis**  
   - Calculate and analyze correlations between features and sales.
   - Create a heatmap to visualize these correlations.

7. **Feature Engineering**  
   - Extract Year, Month, and Day from the date and create separate columns for each.
   - Calculate and plot average sales per month using a line chart.

## Conclusion

This project involves comprehensive data analysis and cleaning, exploration of feature correlations, and engineering features to build a robust sales forecasting model. The insights and models developed are aimed at providing accurate sales predictions, which will help in strategic decision-making and optimizing retail operations.

## Next Steps

- Develop and validate the predictive models using the cleaned and processed dataset.
- Fine-tune model parameters and evaluate performance.
- Explore additional features and model enhancements based on initial findings.

## Acknowledgments

Thank you for reviewing this project. For any questions or feedback, please feel free to reach out.

