<h2> Quantiles </h2>
<hr style="height: 3px; background-color: #AA0000;" />

### Part of developing different computational tools is doing an analysis of the computational time of algorithms. This can be done a couple of different ways in R. You can either use `system.time()` or a package called `microbenchmark`. Let's look at the computational time of the `sort()` algorithm, in particular the `quicksort` method. The quicksort algorithm was developed by Tony Hoarse in 1959. It is a particularly fast sorting algorithm that has an average computation time of $n\log(n)$ for a list of size $n$.

### First we create a random vector of size 1000000 by `x<-rnorm(1000000)`

### Implementing the code,
```
system.time(sort(x,method="quick"))
```
### 10 times we have the following table of computational times for the quick sort algorithm

<h3>

| Measurement | Elapsed time (secs)|
| -           | -           |
| 1    |  0.088  |
| 2    |  0.109  |
| 3    |  0.093  |
| 4    |  0.083  |
| 5    |  0.086  |
| 6    |  0.088  |
| 7    |  0.088  |
| 8    |  0.110  |
| 9    |  0.085  |
| 10   |  0.104 |

</h3>
<hr style="height: 2px; background-color: #003282;" />

<h4> Problems: </h4>

1. What is the population of the study? What is the sample?
2. Give the five number summary of the data.
3. The `microbenchmark` library automatically runs a code snippet multiple times. Use the code `summary(microbenchmark(sort(x,method="quick"),times=10,unit="s"))` to find the 5 number summary of computational times using `microbenchmark`.
4. Draw boxplots of both the `system.time()` and `microbenchmark` summaries on a single axis.

### Suppose a random variable $X$ follows an exponential distribution with $\lambda=5$.
<hr style="height: 2px; background-color: #003282;" />
<h4>Problems: </h4>

1. What is the lower quartile for $X$?
2. What is the 80th percentile for $X$?
3. What is the median for $X$?
4. How does the median for $X$ compare with the mean for $X$? Discuss how this makes sense in terms of the shape of the distribution.
