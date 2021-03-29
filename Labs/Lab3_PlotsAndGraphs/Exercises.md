# Lab 3 - Plots and Graphs

## Instructions
- Use the material covered in LAB 3(Plots and Graphs) Notes to answer the questions in this lab.
- Complete each of the problems in the required problems section.
- Choose only one of the listed projects and answer each of the associated questions
- Upload your answers to your questions.
- If your document is a notebook that contains code (for instance like an ipynb file), then upload a single file. here
- If you have a separate document that contains code then upload the code you used to answer the questions to LAB 3(Plots and Graphs) CODE 

## Required Problems

Complete each of the problems below.

1. Use the mpg data set and ggplot and to create a single figure that compares histograms of the city mileages of Ford and Toyota vehicles.
2. Use the mpg data set and ggplot to create a single figure with boxplots of city mileage for all cylinder types.
3. Create random a vector of data with 1000 observations associated to log-normal distribution, use this data to create a data frame, and then make a normality plot for the resulting data.
4. Using the random data from the previous problem, create a quantile plot comparing the data to the log-normal distribution.

## Projects

Choose one of the projects below and answer all associated questions.

### Project 1

In this project we will be using the datasets available in the Lahman package. You should already have this package installed on your version of R, if not you will need to install it. Be sure to load this package before attempting these problems


1. How many players on the Seattle Mariners have been at bat, but did not get a hit?
2. Create a histogram of the hits for players that have been at bat as least once in 2019.
3. Create a scatterplot for the number of hits for Hank Aaron for each season of his career.
4. The top 5 players with the  most career home runs (as of 2019) are Barry Bonds, Hank Aaron, Babe Ruth, Alex Rodriguez, and Willie Mays. Create a single scatter plot of the number of home runs in each season for all of these players.
5. Albert Pujois passed Willie Mays in career home runs during the 2020 season. What is the chance that Pujois will get a hit in a game if he is at bat at 3 times? [Hint: use the binomial distribution]
6. Use the data to construct a plot of your choosing.




### Project 2

New York city has numerous data sets available via https://opendata.cityofnewyork.us/data/. We will be studying vehicle collisions

1. Use the link https://data.cityofnewyork.us/api/views/h9gi-nx95/rows.csv?accessType=DOWNLOAD to upload a csv of the data directly into your R workspace.
2. Clean the data by creating two new data frames; one with valid BOROUGH and one with NA in BOROUGH column.
3. Construct a bar chart to compare the number of collisions for each BOROUGH.
4. Create a histogram of the number of accidents for every hour in NYC.
5. Astoria is the a neighborhood in Queens associated with the zip codes 11101, 11102, 11103, 11105, and 11106. What is the probability that there will be at least 4 accidents in Astoria in a day? [Hint: Use Poisson distribution]
6. Use the data to construct a plot of your choosing.

### Project 3

The CDC has multiple data sets available to study the spread and impacts of Covid-19. The COVID-19 case surveillance system database includes individual-level data reported to U.S. states and autonomous reporting entities, including New York City and the District of Columbia (D.C.), as well as U.S. territories and states. You can find more information about this here, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data/vbim-akqf


1. Upload the CDC COVID-19 Case Surveillance Public Use Data into your R workspace.
2. Clean the data set to only contain valid entries in the age group column
3. Create a single bar chart that compares the deaths and recovered for each age group.
4. Create a histogram for the number of cases reported to the cdc per day.
5. On of January 26, 2021 there were  151,616 new cases of Covid-19. Estimate the number of these new cases that will lead to death.
6. Use the data to construct a plot of your choosing.

### Project 4

A yield curve is a line that plots yields (interest rates) of bonds having equal credit quality but differing maturity dates. The slope of the yield curve gives an idea of future interest rate changes and economic activity. Treasury securities are often viewed as the safest securities available and thus offer a baseline for yield rates of other bonds. You can find information about treasury yield curve rates here, https://www.treasury.gov/resource-center/data-chart-center/interest-rates/pages/TextView.aspx?data=yield


1. Upload the csv, daily_treasury_yield_curve_rates.csv   into your R workspace.
2. Create a scatterplot of the 1 month rates throughout 2020. Can you explain the behavior? What do you think is happening?
3. Create a single plot with boxplots comparing 10 , 20, and 30 year yield rates.
4. Find the summary of the 1 month yield rates and then clear the dataset of any outliers. Create a qq plot of the 1 month yield rates with no outliers. 
5. Find the mean and standard deviation of the 1 month yield rates with no outliers. What yield rate is greater than 95% of the other? Compare this value to the yield rates for January 2021 found on https://www.treasury.gov/resource-center/data-chart-center/interest-rates/pages/TextView.aspx?data=yield
6. Use the data to construct a plot of your choosing.
