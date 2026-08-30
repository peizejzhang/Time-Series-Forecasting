# A-Comparative-approach-to-Forecasting-Cocoa-Price-Using-SARIMA-and-GAM-Models
This repository contains final group project materials of STA457 Winter 2025 related to cocoa price modeling using ARIMA/SARIMA and GAM. Please open an issue in case of any difficulty running the R markdown files.

## Detail
- Programming Language: R

## Files
- Daily Prices_ICCO.csv: The times series data of cocoa future price between 1994 and 2025
- processed_monthly_prices_data.csv: Price data from Daily Prices_ICCO.csv that has been cleaned and converted into monthly average
- Ghana_data.csv: Historical data of precipitation and temperature in Ghana.
- API_PA.NUS.FCRF_DS2_en_csv_v2_13510.csv: Historical (annualized) exchange rate of currencies to USD between 1960 and 2023
- 457_clean_version_forcast2.Rmd.rmd: R-markdown file containing our R code for the GAM model.
- SARIMA.Rmd.rmd: R-markdown file containing our R code for the SARIMA model.
- STA457_Final_Project.pdf: Our final project report.

## Running the code
- install.packages(c(
  "dplyr", "lubridate", "forecast", "tseries",
  "astsa", "mgcv", "patchwork", "tidyr",
  "zoo", "purrr", "ggplot2", "knitr"
))
- For gam_analysis.rmd:
    - Change file_address_price to the location of Daily Prices_ICCO.csv.
    - Change file_address_weather to the location of Ghana_data.csv
    - Change file_address_exchange_rate to the location of API_PA.NUS.FCRF_DS2_en_csv_v2_13510.csv.
- For arima_analysis.rmd:
    - Change file_address_price to the location of Daily Prices_ICCO.csv.
    - Change file_address_weather to the location of Ghana_data.csv.
## Result
| Model | Test RMSE |
|---|---:|
| ARIMA(1,1,0) | 2059.942 |
| GAM with Time and Exchange Rate | **1430.807** |
## Acknowledgement
This team-based Kaggle project was led by Peize Zhang and completed in collaboration with Binhe Jia, Haoyuan Chen, and Jinting Liu. The original team repository is available at:
https://github.com/Binhe-Jia/Cocoa_Price_Forecasting.
