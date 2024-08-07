# Sales Forecasting using Time Series Analysis

This project focuses on forecasting sales for the Rossmann chain of stores with a prediction horizon of 3 weeks into the future. The project involves performing necessary preprocessing, extracting valuable business insights from past historical data, and applying various time series modeling techniques to achieve accurate sales forecasts.

## Table of Contents

1. [Rossmann Stores](#rossmann-stores)
2. [Data](#data)
3. [Data Fields](#data-fields)
4. [Data Preprocessing](#data-preprocessing)
5. [Exploratory Data Analysis](#exploratory-data-analysis)
6. [Time Series Property Analysis](#time-series-property-analysis)
7. [Error Metrics for Modeling](#error-metrics-for-modeling)
8. [Time Series Modeling](#time-series-modeling)
   - [Univariate Forecasting](#univariate-forecasting)
   - [Multivariate Forecasting](#multivariate-forecasting)
   - [Best Fit Model](#best-fit-model)
9. [Contributing](#contributing)
10. [License](#license)
11. [Contact Information](#contact-information)

# Rossmann Stores

Rossmann operates over 3,000 drug stores in 7 European countries. Rossmann stores are a significant player in the European retail market, with a vast network of drug stores. Several factors influence store sales, including promotions, competition, school and state holidays, seasonality, and locality.

## Data

The dataset for this project can be obtained from the following link: [Rossmann Store Sales Data](https://www.kaggle.com/c/rossmann-store-sales/data)

## Data Fields

Most of the fields are self-explanatory. The following are descriptions for those that aren't.

- **Id**: An Id that represents a (Store, Date) duple within the test set.
- **Store**: A unique Id for each store.
- **Sales**: The turnover for any given day (this is what you are predicting).
- **Customers**: The number of customers on a given day.
- **Open**: An indicator for whether the store was open: 0 = closed, 1 = open.
- **StateHoliday**: Indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends.
  - a = public holiday
  - b = Easter holiday
  - c = Christmas
  - 0 = None
- **SchoolHoliday**: Indicates if the (Store, Date) was affected by the closure of public schools.
- **StoreType**: Differentiates between 4 different store models:
  - a
  - b
  - c
  - d
- **Assortment**: Describes an assortment level:
  - a = basic
  - b = extra
  - c = extended
- **CompetitionDistance**: Distance in meters to the nearest competitor store.
- **CompetitionOpenSince[Month/Year]**: Gives the approximate year and month of the time the nearest competitor was opened.
- **Promo**: Indicates whether a store is running a promo on that day.
- **Promo2**: Promo2 is a continuing and consecutive promotion for some stores:
  - 0 = store is not participating
  - 1 = store is participating
- **Promo2Since[Year/Week]**: Describes the year and calendar week when the store started participating in Promo2.
- **PromoInterval**: Describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store.

## Data Preprocessing

- Performed outlier detection and treatment to ensure data quality.
- Handled missing values and other inconsistencies.

## Exploratory Data Analysis

- Analyzed the combined sales of all stores on a yearly, monthly, daily, and day-of-the-week basis.
- Provided statistical details of sales across different store types.
- Examined the distribution of sales and customers by store type.
- Analyzed variations in sales, customers, and sales per customer for every store type and promotion status.
- Checked store operationality for each day of the week by month and store type.
- Examined promotion periods and competition exposure for each store type.
- Analyzed correlations between different variables affecting sales.

## Time Series Property Analysis

- Identified seasonal patterns for each store type.
- Analyzed sales trends for each store type.
- Generated Autocorrelation and Partial Autocorrelation plots for each store type.

## Error Metrics for Modeling

1. **Evaluation Metrics**:
   - Used a combination of MAPE and a custom error metric to measure the overall percentage of points outside the prediction interval.
   - Evaluated models using other metrics like MAE, RMSE, and MSE as well.
2. **Time Series Cross-Validation**:
   - Applied cross-validation techniques for robust model evaluation.

## Time Series Modeling

### Univariate Forecasting

1. **Base Models Forecasting**:
   - Implemented Average, Naive, Seasonal Naive, Drift, SES, HLT, HWM, and Theta models.
2. **AUTO-ARIMA**:
   - Performed forecasting, cross-validation, evaluation, and residual diagnostics.
   - Checked for stationarity using the Augmented Dickey-Fuller Test.
3. **SARIMA**:
   - Conducted forecasting, cross-validation, and evaluation.

### Multivariate Forecasting

1. **SARIMAX**:
   - Implemented forecasting, cross-validation, and evaluation.
2. **Vector Autoregression**:
   - Performed forecasting, cross-validation, evaluation, and residual diagnostics.
   - Conducted Granger Causality Test and ADF stationarity test.

### Best Fit Model

**Prophet Model**:

- Handled holidays and analyzed changepoints.
- Performed cross-validation for model accuracy.

## Contributing

Contributions are always welcome!

Please see `contributing.md` for ways to get started.

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact Information

- **Kizhakkeppattu Rahul Govindkumar**
- **Email**: krahulgovind@gmail.com
- **Github**: [rahulorihiki](https://github.com/rahulorihiki)
