# Lab 2 - Distributions 

## Instructions
- Use the material covered in LAB 2(Distributions) Notes  to answer the questions in this lab.
- Complete each of the problems in the required problems section.
- Choose only one of the listed projects and answer each of the associated questions
- Upload your answers to your questions.
- If your document is a notebook that contains code (for instance like an ipynb file), then upload a single file. here
- If you have a separate document that contains code then upload the code you used to answer the questions to LAB 2(Distributions) CODE

## Required Problems

Complete each of the problems below.

1. Create a histogram of 1000 random values from a lognormal distribution with mean 10 and standard deviation 2
2. If $x$ is a random variable whose distribution is normal with mean 100 and standard deviation 23, for what value of $c$ is there a 65% that $x\le c$?
3. Given that a product has a 98% chance of success, what is the probability that there is at most 3 faulty products in a group of 100?
4. If $x$ is a discrete random variable whose distribution is Poisson with $\lambda=6.7$, what is the likelihood that $x>8$?

## Projects

Choose one of the projects below and answer all associated questions.

### Project 1

We have investigated a sample of the data collected by Albert Michelson in 1879 during an experiment to measure the speed of light on a previous worksheet. The full set of data is saved in R under the morley data frame.

1. How many observations are in the morley data frame?
2. What are the columns of the data frame?
3. Create a histogram of the speeds measured. Be sure to include labels.
4. Notice that the this data is roughly normal. Find the mean and standard deviation.
5. Use the normal distribution associated to the data to create an interval of values for which you are 95% certain that the speed of light lies between.
6. Are there any measurements are outside this 95% range? Which ones?




### Project 2

The City of Seattle has public data available at https://data.seattle.gov. We will be studying the SPD Crime Data. These incidents are based on initial police reports taken by officers when responding to incidents around the city and then edited as the report makes its way through the legal system. The information enters the City of Seattle's Records Management System (RMS) and is then transmitted out to data.seattle.gov. The information is published within 6 to 12 hours after the report is filed into the system.

1. Use the link https://data.seattle.gov/api/views/tazs-3rd5/rows.csv?accessType=DOWNLOAD to upload a csv of the data directly into your R workspace.
2. What are the columns of the data frame?
3. The data begins on 1/1/2008 and has entries all the way through to 1/18/2021. Find the average number of police reports incidents per day.
4. What is the chance that more than 10 police reports will happen in a day in Seattle?
5. What is the chance of exactly 10 police reports will happen in a day in Seattle?
6. What is the maximum number of police reports that would have to happen in a day in order for that day to be 95% "safer'' than other days? (Note that this data is purely police reports and is not necessarily an accurate depiction of crime in an area. Hence, the quotation marks. Lots of crimes go unreported and lots of reports are not connected to any crime.) 

### Project 3

The website, https://www.the-numbers.com/, has lots of data regarding the success of movies. I have included two csvs that include data about the top 100 grossing movies of all time, TopMovies_thenumbers.csv. Note that these numbers have not been adjusted for inflation.

1. Upload the TopMovies_thenumbers.csv into your R workspace.
2. What are the columns of the data frame?
3. Create a new data frame that only includes the Domestic Box Office.
4. What percentage of top 100 grossing movies (domestic) were produced by Walt Disney?
5. If you randomly selected 10 of the top grossing movies of all time (domestic), what is the chance that at least 50% of them were produced by Walt Disney?
6. Rotten Tomatoes has released a list of the 89 most anticipated movies of 2021 (https://editorial.rottentomatoes.com/article/most-anticipated-movies-of-2021/). With 95% confidence, at least how many of the 89 top movies of 2021 do you predict will be produced by Walt Disney?
