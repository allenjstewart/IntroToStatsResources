# Lab 4 - Correlation and Regression

## Instructions
- Use the material covered in LAB 4(Correlation and Regression) Notes    to answer the questions in this lab.
- Complete each of the problems in the required problems section.
- Choose only one of the listed projects and answer each of the associated questions
- Upload your answers to your questions.
- If your document is a notebook that contains code (for instance like an ipynb file), then upload a single file. here
- If you have a separate document that contains code then upload the code you used to answer the questions to LAB 4(Correlation and Regression) CODE  

## Required Problems

Complete each of the problems below.

1. Use the mosaicData package to upload the Utilities data set and calculate the correlation between gas usage and temperature.
2. Create a plot with both the scatter plot and the least squares line where $x$ is the temperature and $y$ is the gas usage
3. Create two residual plots (one for $x$ and one for $\hat{y}$) for the linear model in the previous question.
4. Use the linear model to predict the gas usage when the temperature is 47 degrees Fahrenheit.

## Projects

Choose one of the projects below and answer all associated questions.

### Project 1

The data set that we looked at in the lab notes with SAT scores and teacher salary is contained in the mosiacData package and is called `SAT`. There is a more recent set of data called SAT_2010 in the mdsr package.

1. Install and load the mdsr package.
2. Let $x$ be average annual teacher salary and $y$ be the average total SAT score. Find the correlation, regression line, and coefficient of determination. Interpret what each of the calculations tells you about the relationship between teacher salary and SAT score.
3. Predict the SAT scores for a state that pays its teachers $35,000/year on average.
4. Stratify the data by fraction of students eligible for the SAT. Create a single scatter plot that displays the stratified data and the regression line for each stratification.
5. Investigate each stratification using regression line and correlation. What can you say about these relationships?
6. Are there any other variables that you think would affect state average of SAT scores? If they are in the data set, perform an analysis? If not, explain how you would collect the data.




### Project 2

The paper PanTHERIA: a species-level database of life history, ecology, and geography of extant and recently extinct mammals. Ecology 90:2648. by Jones et. al. (Source: http://esapubs.org/archive/ecol/E090/184/) details the `PanTHERIA` database which contains information about mammals. We will use this database to study some relationship between physiological characteristics of mammals.

1. Upload the csv, PanTHERIA_1-0_WR05_Aug2008.csv , into your R workspace.
2. Clean the data so that the columns, AdultBodyMass_g and BasalMetRate_mLO2hr contain only positive values.
3. Let $x$ be the  mass of the mammal and $y$ be the basal metabolic rate. Find the correlation, regression line, and coefficient of determination. Interpret what each of the calculations tells you about the relationship between the mass of a mammal and the metabolic rate.
4. Research suggests that the metabolic rate of mammals is equal to $\text{mass}^{2/3}$ (source: https://www.pnas.org/content/100/7/4046). Change your linear model to the model $x^{2/3}$. How has the coefficient of determination changed? What are the coefficients? Does your data support the research?
5. Supposing the average mass of person is 60 kg, what is your model's prediction of the average basal metabolic rate for humans? The average basal metabolic rate is 16 L of oxygen per hour (source: http://hyperphysics.phy-astr.gsu.edu/hbase/Biology/metab.html). How does your predication compare?
6. Trophic level measures the position of an animal in the ecological hierarchy. For this data set we have; herbivores-1,omnivores-2,carnivores-3. Stratify the data by Trophic level (be sure to clean out any -999 values). Create a single scatter plot that displays the stratified data and the regression models for each stratification. What might explain the differences in the models?

### Project 3

In this project we will look at some data about US colleges. This data has been pulled, cleaned, and abridged into a csv file from https://data.ed.gov/dataset/college-scorecard-all-data-files-through-6-2020/resources. The names of the columns are given below

UNITID, Unit ID for institution
OPEID, 8-digit OPE ID for institution
INSTNAM, Institution name
CITY, City
STABBR, State postcode
ZIP, ZIP code
CCBASIC, Carnegie Classification -- basic
ADM_RATE, Admission rate
PCIP14, Percentage of degrees awarded in Engineering.
COSTT4_A, Average cost of attendance (academic year institutions)
TUITFTE, Net tuition revenue per full-time equivalent student
INEXPFTE, Instructional expenditures per full-time equivalent student
AVGFACSAL, Average faculty salary
PCTFLOAN, Percent of all undergraduate students receiving a federal student loan
C150_4,Completion rate for first-time, full-time students at four-year institutions (150% of expected time to completion)

1. Upload the csv, colleges.csv , into your R workspace.
2. Let $x$ be average annual faculty salary and $y$ be the completion rate. Find the correlation, regression line, and coefficient of determination. Interpret what each of the calculations tells you about the relationship between teacher salary and completion rates.
3. Make a residual plot for the linear model. Do you think that a linear model captures the full relationship? Why or why not?
4. Predict the completion rate for an institution that has an average faculty salary of 9500 dollars. Compare this with the entry in the data for Seattle U.
5. Seattle U has a Carnegie Classification of 17. Create a scatterplot of admission rate vs. average cost for all the universities with Carnegie Classification 17 coloring the points according to percentage of degrees awarded in engineering.
6. Do you suspect that there is any relationship between admission rate and cost at universities given the data. If so, what function do you think would be an accurate model? If not, why?

### Project 4

For this project we will be looking at data collected from the World Bank and provided by Gapminder. To do this project you will need to install the gapminder package and then load it into you R workspace. The gapminder packages contains two data sets, gapminder and gapminder_unfiltered, we will be using the gapminder data set.

1. Create a scatterplot of life expectancy vs. GPD per capita.
2. Let $x$ be GPD per capita and $y$ be the average life expectancy. Find the correlation, regression line, and coefficient of determination. Interpret what each of the calculations tells you about the relationship between GPD and life expectancy.
3. The 2019 GPD per capita for the US is 65,297.52 dollars. What do you expect the average life expectancy in the US given your data? Look up the actual life expectancy and compare it with your prediction.
4. Create a residual plot for your  linear model. Do you think that the linear model accounts for all the variation between the variables? Why or why not?
5. Let $x$ be GPD per capita and $y$ be the average life expectancy. Use the model y~log(x) to find the correlation, regression line, and coefficient of determination. Interpret what each of the calculations tells you about the relationship between GPD and life expectancy.
6. Create a residual plot for your log model. How does this model compare to the linear model? Do you think that the log model accounts for all the variation between the variables?


### Project 5

For this project we will be looking at recent data regarding the stock prices of Gamestock(GME) and AMC (AMC) in the beginning of 2021.

1. Upload the csv, AMC_GME.csv, into your R workspace.
2. Let $x$ be Gamestop's opening price and $y$ be AMC's opening price. Find the correlation, regression line, and coefficient of determination. Interpret what each of the calculations tells you about the relationship between teacher salary and completion rates.
3. Make a residual plot for the linear model. Do you think that a linear model captures the full relationship? Why or why not?
4. Predict the opening rate for GME if the opening of AMC is 7 dollars.
5. Create two residual plots for a linear model of AMC vs GME open and AMC vs GME close. Do you think that the linear model captures the relationship? Why or why not?
6. Use the mutate function to create a new column in the data frame of categorical variable labeling what quartile of the AMC_Volume the observation is in. Create a single scatter plot that displays the stratified data and the regression models for each stratification. What might explain the differences in the models?
