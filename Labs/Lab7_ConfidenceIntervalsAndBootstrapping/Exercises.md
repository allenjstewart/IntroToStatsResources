
# Lab 7 - Confidence Intervals and Bootstrapping

## Instructions
- Use the material covered in LAB 7(Confidence Intervals and Bootstrapping) Notes    to answer the questions in this lab.
- Complete each of the problems in the required problems section.
- Choose only one of the listed projects and answer each of the associated questions
- Upload your answers to your questions.
- If your document is a notebook that contains code (for instance like an ipynb file), then upload a single file. here
- If you have a separate document that contains code then upload the code you used to answer the questions to LAB 7(Confidence Intervals and Bootstrapping) CODE 

## Required Problems 

Complete each of the problems below.

1. Create a random sample of size 10 from a normal distribution with $\mu=5$ and $\sigma=2$. Calculate the sample mean and then construct a 95% confidence interval. Is the population mean covered by your confidence interval?
2. Create 100 random samples of size 10 from an exponential distribution with $\lambda=2$ and check the number of these samples for which the 95% confidence interval covers the population mean? Does this number align with the 95% confidence? Why or why not.
3. Create a single sample of size 20 from an exponential distribution with $\lambda=2$ then construct a 95% confidence level using bootstrapping with 10000 iterations.

## Projects

Choose one of the projects below and answer all associated questions.

### Project 1

We will use the payroll data from NYC to investigate confidence intervals. 

1. Upload the NYC_Payroll2018.csv   data set. This data set has both hourly, daily, and yearly rates. We are only concerned with the yearly rates. Filter the data set to only include the "per Annum" observations.
2. Create a sample of 100 employees and then use a QQ chart to verify that the sample data is normally distributed.
3. Calculate the sample mean and create a 95% confidence interval for this estimation.
4. Is the population mean you calculated in part 3 within your confidence interval? If not, explain why this might be the case.
5. What size sample should you create in order to create a 95% confidence interval of total length 5000 dollars? Create such a sample and find the associated confidence interval.


### Project 2

We will use the payroll data from NYC to investigate confidence intervals as in project 1. However, in this case we will be using a smaller sample


1. Upload the NYC_Payroll2018.csv   data set. This data set has both hourly, daily, and yearly rates. We are only concerned with the yearly rates. Filter the data set to only include the "per Annum" observations.
2. Create a sample of 10 employees and then use a QQ chart to verify that the sample data is normally distributed.
3. Calculate the sample mean and create a 95% confidence interval for this estimation. (be sure to use the t-distribution)
4. Is the population mean you calculated in part 3 within your confidence interval? If not, explain why this might be the case.
5. What size sample should you create in order to create a 95% confidence interval of total length 5000 dollars? Create such a sample and find the associated confidence interval.


### Project 3

We will use the payroll data from NYC to investigate confidence intervals. However, in this case we will be using bootstapping


1. Upload the NYC_Payroll2018.csv   data set. This data set has both hourly, daily, and yearly rates. We are only concerned with the yearly rates. Filter the data set to only include the "per Annum" observations.
2. Create a sample of 15 employees and then use a QQ chart to verify that the sample data is normally distributed.
3. Calculate the sample mean and use bootstrapping with 10,000 iterations to create a 95% confidence interval for this estimation.
4. Is the population mean you calculated in part 3 within your confidence interval? If not, explain why this might be the case.
5. Create 20 different 15 employee samples and then bootstrap 95% confidence intervals using 10,000 iterations. How many of these 20 confidence intervals contain the population mean?



### Project 4

Use your own data set that contains at least 1000 observations of a numerical variable.

1. Create a sample of size 100.
2. Use a QQ chart to determine whether that the sample data is normally distributed. If it is not normally distributed, test some other distributions.
3. Calculate the sample mean and create a 95% confidence interval for this estimation.
4. Is the population mean you calculated in part 3 within your confidence interval? If not, explain why this might be the case.
5.  What size sample should you create in order to create a 95% confidence interval of total length of 5? Create such a sample and find the associated confidence interval.



