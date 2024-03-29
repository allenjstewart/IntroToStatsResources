# Lab 1 - Histograms
## Instructions
- Use the material covered in LAB 0(Introduction to R) Notes and LAB 1(Histograms) Notes to answer the questions in this lab.
- Complete each of the problems in the required problems section.
- Choose only one of the listed projects and answer each of the associated questions
- Upload your answers to your questions.
- If your document is a notebook that contains code (for instance like an ipynb file), then upload a single file. here
- If you have a separate document that contains code then upload the code you used to answer the questions to LAB 1(Histograms) CODE 

## Required Problems

Complete each of the problems below.

1. As we discussed in LAB 0(Introduction to R) Notes , R can create vectors of random data. Create a vector of 10 random values using rnorm and then create a histogram using this data. Label the histogram "Random Normal Data", label the x axis "Values", and use green as the color for the bars.
2. Using the same design parameters as in number 1, i.e. label, x-axis, bar color, create a histogram of 500 random values using rnorm. Then do it again using 50,000 values.
3. For each of the the three histograms, what was width of the classes that R used by default? Adjust each of these histograms so that the height of the bars is density rather than frequency and there are 50 classes in each histogram.
4. What is happening as you increase the size of the data as well as the number of bins? Does the shape being created look familiar? Describe what you think would happen to the histogram as the size of the data goes to infinity and the class width goes to 0?

## Projects

Choose one of the projects below and answer all associated questions.

### Project 1

Puromycin is a data set in R on the velocity of an enzymatic reaction obtained by Treloar (Treloar, M. A. (1974), **Effects of Puromycin on Galactosyltransferase in Golgi Membranes**, M.Sc. Thesis, U. of Toronto.). The number of counts per minute of radioactive product from the reaction was measured as a function of substrate concentration in parts per million (ppm) and from these counts the initial rate (or velocity) of the reaction was calculated (counts/min/min). The experiment was conducted once with the enzyme treated with Puromycin, and once with the enzyme untreated.

1. Construct a histogram for the instantaneous reaction rates. Is the shape of the data unimodal, bimodal, or multimodal? Looking at all columns of the data set, justify your answer.
2. Construct a histogram for the enzymatic reaction rate for only the treated cells. And construct another for the enzymatic reaction rate for only the untreated cells. Using these two histograms, what might you conjecture about the affect of Puromycin on reaction rate? [This is only a conjecture. The histograms alone are not substantial statistical evidence.]
3. By default, most statistical software (including R) will decide for you what widths of intervals to use for a histogram. But you can also change the interval widths. Construct two new histograms for the treated cells- one with wider intervals than the default and one with narrower intervals than the default. Compare both of these to the histogram of treated cells from part 2. Of these three histograms, which one do you feel gives you the most useful summary of the data? why?

### Project 2

1. What is the description of the nycflights13 library?

2. Use the flights data frame in the nycflights13 library to create a two histograms; one for air time of all flights and one for the distance of all flights. Are these histograms unimodal, bimodal, or multimodal? Approximate the the value associated to each mode by looking at the histogram. What are some possible destinations for which these modes be associated?

3. Create another histogram that graphically displays information about whether flights arrive early, late, or on time. Using the histogram, approximate the proportion of flights that are over 30 minutes late.
