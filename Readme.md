# Time Series Analysis For Total Goals Of Premier League

![prem](https://user-images.githubusercontent.com/79353291/153533536-5db5166e-06aa-471c-97a8-3302d47a6629.gif)

# Analysis Objectives
.The goal of this project is to determine and predict the total number of goals in the next two years in the premier league (England's league).
.Performing time series analysis by using Arima model

# Datasetes that will be utilized
.The data which I have collected comes from a library in R called worldfootballR, this library is immensely useful for people who want to perform soccer analysis for data science
. I needed to get twenty years of data from the 1999/2000-2020/2021 seasons

# Potenitial packages
.library(worldfootballR)
.library(tidyverse)
.library(data.table)
.library(ggpubr)
.library(tidyr)
.library(cowplot)
.library(forecast)
.library(tseries)
.library(lubridate)
.library(data.table)
.library(dplyr)
.library(TSstudio)

# Methods used for collecting the data
. Scraping Transfermarket.com by using worldfootballr library

# Methods used for data cleaning and feature engineering
.The columns that I wanted to keep and work on were only two columns and they were the date and goals columns and I dropped the rest
.convert the Date column into a Date object and GF column into a numeric object
.floor the Date of every month meaning
.fill the missing dates with 0
.group by the data by Date and sum up the goals

# Time Series
. Checking if data is stationary
![1_Xiwfm6zSBbFrU0mmLV6xAA](https://user-images.githubusercontent.com/79353291/153534841-75d3da0d-9664-436a-a562-c7b8c606438e.jpeg)

. Seasonal plotting
![1_a4mYZrdm26TapIGkRL4-Aw](https://user-images.githubusercontent.com/79353291/153534940-b94dcf18-7078-4a9c-85a3-df32c84370f7.png)

## Decomposition of the data
. Decomposing the data will give us a visual representation to see the trend, seasonality, and remainder of the data
. Using multiplicative decomposition

## Model making using Arima
. Choosing auto arima to have the best p,d,q values
![1_pzVe9yyGG2DfzbHs_F5AUw](https://user-images.githubusercontent.com/79353291/153535329-50195931-e212-4098-9888-aa70375577bb.png)

## Forecast

![1_a4mYZrdm26TapIGkRL4-Aw](https://user-images.githubusercontent.com/79353291/153535359-f5a16387-0a87-4fb2-861f-038e5c8d4c19.png)
