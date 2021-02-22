# Introduction to R

## The R programming language

R is a programming language for data analysis and statistics. It is free, and very widely used by professional statisticians. It is also very popular in certain application areas, including bioinformatics. R is a dynamically typed interpreted language (similar to Python), and is typically used interactively (similar to Mathematica). It has many built-in functions and libraries, and is extensible, allowing users to define their own functions and procedures using R, C or Fortran. It also has a simple object system.

## Jupyter Notebooks (and other ways to interact with R)

The Jupyter Notebook (https://jupyter.org/) is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization, machine learning, and much more. 

Jupyter notebooks can support a wide variety of programming languages. In this class we will mostly be using Python as well as R. Python automatically comes as part of Jupyter. In the case of R, the R package IRkernel can be downloaded which will connect your version of R to Jupyter notebooks. 

Most of the labs in this class will come as both html files and ipynb files. Using Jupyter notebook, ipynb files will enable you to see and manipulate the code I give you.

A Jupyter notebook is made up of cells. The cells that I am currently writing this is set to `markdown`. Markdown is a lightweight markup language for creating formatted text using a plain-text editor. I use Markdown when creating all of the documents for this class. It allows for an easy creation of html files which is the format I choose for all my documents. 

By default, cells are set to `code`. The code cells will be set to evaluate in whatever kernel you have chosen to access. In this case, I have chosen an R kernel. So when I write some command in a cell and hit **shift+return** Jupyter runs the code (note that you also need to hit shift+return to compile any markdown). 


```R
summary(cars)
```


         speed           dist       
     Min.   : 4.0   Min.   :  2.00  
     1st Qu.:12.0   1st Qu.: 26.00  
     Median :15.0   Median : 36.00  
     Mean   :15.4   Mean   : 42.98  
     3rd Qu.:19.0   3rd Qu.: 56.00  
     Max.   :25.0   Max.   :120.00  


In the cell above, I called the `summary()` function on the data set `cars`. R (and its packages) often come with preloaded data sets. The `cars` data set is one that is loaded with the base stucture of R.

You can also embed plots in Jupyter notebook, for example:


```R
plot(pressure)
```


![png](output_4_0.png)


We will see lots of different uses of the Jupyter notebook as we continue in the class. 

Although I am recommending that we use Jupyter for the class, I want to make sure that you know that there are other options available. The nice thing about Jupyter notebooks is that it is interactive and the notebook files can be exported as a variety of different formats. 

The most basic way to access R is through a terminal. This will allow you to run small snippets of code but isn't the most robust way to develop in R. In this very basic non GUI based way of coding, you would use a plain text editor (emac, vi, nano) to write .R scripts and then run them from the terminal. There is a time and place for this type of coding, but probably not this class.

If you would prefer to not use Jupyter then I suggest one of the following editors.

- Bare bones editors
    - emacs, https://www.gnu.org/software/emacs/ 
        - I use emacs for some field specific programming languages, specifically Macaulay2
    - vi/vim, https://www.vim.org/ 
        - When accessing a Unix/Linux machine use of vi is most likely unavoidable
- Open source
    - atom, https://atom.io/ 
        - I use atom as a general text editor. I like the easy interaction with GitHub
    - notepad++, https://notepad-plus-plus.org/downloads/ 
- Bells and whistles
    - sublime text, https://www.sublimetext.com/ 
    - pycharm, https://www.jetbrains.com/pycharm/ 
- Windows
    - visual studio code, https://code.visualstudio.com/
        - Even outside of windows, VS code is a great editor.

## Basics

First thing we need to do is cover some of the very basic operations in R.

### Vectors

Vectors are a fundamental concept in R, as many functions operate on and return vectors, so it is best to master these as soon as possible. For the technically inclined, in R, a (numeric) vector is an object consisting of a one-dimensional array of scalars.


```R
rep(1, 10)
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li></ol>



You can assign any object (including vectors) using the assignment operator <-,


```R
ten_ones <- rep(1, 10)
one_through_ten <- 1:10
```

and combine vectors and scalars with the c function.


```R
c(ten_ones, one_through_ten)
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>1</li><li>2</li><li>3</li><li>4</li><li>5</li><li>6</li><li>7</li><li>8</li><li>9</li><li>10</li></ol>



The c function concatenates vectors. If you want to add vectors,


```R
ten_ones+one_through_ten
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>2</li><li>3</li><li>4</li><li>5</li><li>6</li><li>7</li><li>8</li><li>9</li><li>10</li><li>11</li></ol>



Or do any operations


```R
ten_ones+2*one_through_ten
ten_ones/one_through_ten
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>3</li><li>5</li><li>7</li><li>9</li><li>11</li><li>13</li><li>15</li><li>17</li><li>19</li><li>21</li></ol>




<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>1</li><li>0.5</li><li>0.333333333333333</li><li>0.25</li><li>0.2</li><li>0.166666666666667</li><li>0.142857142857143</li><li>0.125</li><li>0.111111111111111</li><li>0.1</li></ol>



You can also use the c function to create a vector.


```R
c(1,2,3)
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>1</li><li>2</li><li>3</li></ol>



Note that arithmetic operations act element-wise on vectors. To look at any object (function or data), just type its name.


```R
one_through_ten
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>1</li><li>2</li><li>3</li><li>4</li><li>5</li><li>6</li><li>7</li><li>8</li><li>9</li><li>10</li></ol>



Vectors can be sorted and randomly sampled. The following command generates a random set of 6 numbers between 1 and 49 and then sorts them.


```R
sort(sample(1:49,6))
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>6</li><li>30</li><li>32</li><li>35</li><li>39</li><li>49</li></ol>



If you ever have any questions about a function, package, or class you can always use the help call. The code below will pull up a help document about the function `sample.`


```R
help("sample")
```

One thing that will continue to cause chaos when using R is that vectors and list start at 1 rather than 0. So for instance if I would like to pull the second entry from our vector `b` above, I would use 


```R
one_through_ten[2]
```


2


Notice that if I try to use `one_through_ten[0]`, R returns nothing.


```R
one_through_ten[0]
```





### Statistics
R is also good at simulating vectors of quantities from standard probability distributions. The command `rnorm(5,1,2)` generates 5 Normal random variates with mean 1 and standard deviation (not variance) 2. There are lots of functions that act on vectors.


```R
rnorm(5,1,2)
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>3.61058844123621</li><li>-4.76351255091901</li><li>1.08545011677539</li><li>1.8111820528913</li><li>3.35883907549254</li></ol>



The first argument is the number of values, the second is the mean, and the third is the standard deviation. Thus if we want 50 random values sampled from the normal distribution with mean equal to 2 and standard deviation of 3 we would use `rnorm(50,2,3)`,


```R
normal_example <- rnorm(50,2,3)
```

Since I assigned the output to a variable, R does not output anything to the display. Let's see what we got


```R
normal_example
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>2.79301377726843</li><li>5.22817847323335</li><li>3.42388495173185</li><li>7.84890485020424</li><li>-0.177335881598359</li><li>2.1641992747977</li><li>0.13340576872794</li><li>8.58377786735015</li><li>-0.335023663881238</li><li>4.64286285908433</li><li>6.13424886857296</li><li>6.49212183176748</li><li>1.75616309510524</li><li>3.07537198615853</li><li>3.18602853695739</li><li>1.04842211305371</li><li>0.746256667892026</li><li>3.92543890107908</li><li>-1.15821800070683</li><li>7.58980943256275</li><li>-5.102851137495</li><li>7.54426691813742</li><li>1.48338394206792</li><li>6.26155885041426</li><li>1.60765508798814</li><li>4.9785342892855</li><li>4.87233521091517</li><li>1.01476304475854</li><li>7.99349958730029</li><li>-5.25769450408727</li><li>-0.378408711647899</li><li>6.86698771103302</li><li>1.41579431204005</li><li>0.811563136236684</li><li>6.69466415799763</li><li>2.81736141111695</li><li>6.41830092118494</li><li>0.52044096352006</li><li>3.2264553587348</li><li>2.56346023505944</li><li>4.34603066088619</li><li>-2.31359661834501</li><li>1.99096445875014</li><li>0.487812367572442</li><li>2.57191575421423</li><li>2.28812075677725</li><li>8.28922936197011</li><li>3.87759312664094</li><li>4.23710350141754</li><li>7.77010507353656</li></ol>



We can now perform a number of statistical operations on x. Let’s check that the mean is approximately 2


```R
mean(normal_example)
```


3.13997721874683


and that the length is equal to 50.


```R
length(normal_example)
```


50


Since the standard deviation of our distribution is 3, the variance of the values in our vector should be approximately 9,


```R
var(normal_example)
```


10.7271034785239


Some functions in R create outputs with much more information than just a single value. If we want the five number summary we use the ‘summary’ function.


```R
summary(normal_example)
```


       Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
     -5.258   1.023   2.946   3.140   5.908   8.584 


There is a multitude of functions in R. The hope is that through these labs you will be exposed to these functions and see how you can use them on sets of real-world data.

## Packages in R

### Tidyverse

There are two basic philsophies when programming in R; Base R and Tidyverse. For the purposes of this class we will be using Tidyverse, which is an R package. We will be making use of R packages on occasion in this class.

An R package is a collection of functions, data, and documentation that extends the capabilities of base R. Using packages is key to the successful use of R. The packages in the tidyverse share a common philosophy of data and R programming, and are designed to work together naturally.

You can install the complete tidyverse with a single line of code: `install.packages("tidyverse")`

On your own computer, type that line of code in the console, and then press enter to run it. R will download the packages from CRAN and install them on to your computer. 

You will not be able to use the functions, objects, and help files in a package until you load it with library(). Once you have installed a package, you can load it with the `library()` function.


```R
library(tidyverse)
```

    ── [1mAttaching packages[22m ─────────────────────────────────────── tidyverse 1.3.0 ──
    
    [32m✔[39m [34mggplot2[39m 3.3.3     [32m✔[39m [34mpurrr  [39m 0.3.4
    [32m✔[39m [34mtibble [39m 3.0.4     [32m✔[39m [34mdplyr  [39m 1.0.2
    [32m✔[39m [34mtidyr  [39m 1.1.2     [32m✔[39m [34mstringr[39m 1.4.0
    [32m✔[39m [34mreadr  [39m 1.4.0     [32m✔[39m [34mforcats[39m 0.5.0
    
    ── [1mConflicts[22m ────────────────────────────────────────── tidyverse_conflicts() ──
    [31m✖[39m [34mdplyr[39m::[32mfilter()[39m masks [34mstats[39m::filter()
    [31m✖[39m [34mdplyr[39m::[32mlag()[39m    masks [34mstats[39m::lag()
    


This tells you that tidyverse is loading the ggplot2, tibble, tidyr, readr, purrr, and dplyr packages. These are considered to be the core of the tidyverse because you’ll use them in almost every analysis.

Packages in the tidyverse change fairly frequently. You can see if updates are available, and optionally install them, by running tidyverse_update().

###  Other packages

There are many other excellent packages that are not part of the tidyverse, because they solve problems in a different domain, or are designed with a different set of underlying principles. This doesn’t make them better or worse, just different. In other words, the complement to the tidyverse is not the messyverse, but many other universes of interrelated packages. As you tackle more data science projects with R, you’ll learn new packages and new ways of thinking about data.

Using packages is key to the successful use of R. It is good to get familiar with some of the most important ones. You can search for packages with specific functions and uses in the CRAN repository, https://cran.r-project.org/.

Here are some of the packages we’ll use that are from outside the tidyverse:

`install.packages(c("nycflights13", "gapminder", "Lahman", "mosaic"))`

These packages provide data on airline flights, world development, baseball, and some additional tools that will make coding in R easier.

## Working with Data

### Tidy Data and Data Frames

Data comes in all different forms. For instance, the image below is data. 

<img src=Lab0Meme.jpg width=50%>

It is 1000x758 pixels and each pixel has a defined color. This color can defined in a variety of ways; gray scale, RGB, CYMK, etc. In this case, this is a color JPEG image so it most likelt uses an RGB color scheme which means that each pixel contains 3 bytes (one for each color). This would give us a 6 dimensional array of data, (x position, y position, red,green,blue). 

However, this type of image data isn't "tidy" and by "tidy" I mean something very specific. Hadley Wickham defined "Tidy Data" as data sets that are arranged such that each variable is a column and each observation (or case) is a row. Notice that our image above does not follow this structure.

Tidy data is a standard way of mapping the meaning of a dataset to its structure. A dataset is messy or tidy depending on how rows, columns and tables are matched up with observations, variables and types. In tidy data:

- Each variable forms a column.
- Each observation forms a row.
- Each type of observational unit forms a table.

In R, tidy data is normally represented by either data frames or tibbles. We will be using both a good amount in R. A data frame is more general than a matrix or vector, in that different columns can have entries of different types (numeric, character, factor, etc.) A tibble can be thought of as a data frame with some additional functionality.

We can upload tabular data as a data frame by using the data() function. I am going to load the women data set. This is a preloaded data set in R. You can look at the codebook for this data set by typing help(women) in the console. There is not a lot of information about this data set, but the code book does say the following

    The data set appears to have been taken from the American Society of Actuaries Build and Blood >Pressure Study for some (unknown to us) earlier year.

    The World Almanac notes: “The figures represent weights in ordinary indoor clothing and shoes, and heights with shoes”.


```R
data(women)
```

There are lots of functions that operate on data frames. The first is the structure function, `str()`.


```R
str(women)
```

    'data.frame':	15 obs. of  2 variables:
     $ height: num  58 59 60 61 62 63 64 65 66 67 ...
     $ weight: num  115 117 120 123 126 129 132 135 139 142 ...


This gives the structure of the data frame. There is a list of the columns along with the number of observations and some examples of the observations. We can see there are 2 columns, height and weight, and 15 observations.

If we want to pull a column from a data frame as a vector in order to perform numerical operations on it, then we use `data$column`.


```R
women_height<-women$height
```

Here we have created a vector called height from the column labelled height in our data frame. Let’s look at the values in our vector.


```R
women_height
```


<style>
.list-inline {list-style: none; margin:0; padding: 0}
.list-inline>li {display: inline-block}
.list-inline>li:not(:last-child)::after {content: "\00b7"; padding: 0 .5ex}
</style>
<ol class=list-inline><li>58</li><li>59</li><li>60</li><li>61</li><li>62</li><li>63</li><li>64</li><li>65</li><li>66</li><li>67</li><li>68</li><li>69</li><li>70</li><li>71</li><li>72</li></ol>



### The Filter Function

Suppose that we want to be able to create a new data frame that restricts our observations to some specific condition on one of our columns. Maybe we want a data frame where the value of height in our observations is greater than 5’6". To do this we use the filter() function.

The filter funtion, filter (DATA, PROPERTIES), has two inputs, DATA and PROPERTIES.

    -DATA, the data frame of interest
    -PROPERTIES, a logical statement related to the data frame.

So in our example we want height>66 (5’6" is 66 inches).


```R
Tall_women_height<-filter(women,height>66)
Tall_women_height
```


<table>
<caption>A data.frame: 6 × 2</caption>
<thead>
	<tr><th scope=col>height</th><th scope=col>weight</th></tr>
	<tr><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>67</td><td>142</td></tr>
	<tr><td>68</td><td>146</td></tr>
	<tr><td>69</td><td>150</td></tr>
	<tr><td>70</td><td>154</td></tr>
	<tr><td>71</td><td>159</td></tr>
	<tr><td>72</td><td>164</td></tr>
</tbody>
</table>



This saves a new data frame, Tall, that only includes observations in which the height is over 66 inches. The filter function is part of the dplyr library which is in the tidyverse. So it is important that the tidyverse is loaded in order for it to work properly.

### read_csv

Thus far we have only used existing data sets that come preloaded in R. Most data sets in the real world are not preloaded into R. Thus we need to be able to load our own data sets into R. One way to do this is to read in a csv (csv stands for comma separated values) file that contains the tabular data that you want to study. You can do this via the `read_csv()` function.

All you need to do is upload the data set then use command, `read_csv("FILE PATH")` where “FILE_PATH” is the path to the csv you want to upload. If the file is in the same directory as you current working directory then the file path is just the name of the file. You can check your working directory by using the `getwd()` command.

Be sure to save the output of the `read_csv()` command as some variable. The `read_csv()` will create what is called a tibble of the data. A tibble is similar to a data frame, but for now we want to keep using data frames. In order to change a tibble to a data frame use `data.frame()` function.

I am going to use `read_csv` to upload data about State of Washington Employee salaries. You can find this data here, http://fiscal.wa.gov/salaries.aspx


```R
washington_annual_employee_salary<-read_csv("AnnualEmployeeSalary.csv")
```

    
    [36m──[39m [1m[1mColumn specification[1m[22m [36m────────────────────────────────────────────────────────[39m
    cols(
      Agy = [31mcol_character()[39m,
      AgyTitle = [31mcol_character()[39m,
      Name = [31mcol_character()[39m,
      JobTitle = [31mcol_character()[39m,
      Sal2015 = [32mcol_number()[39m,
      Sal2016 = [32mcol_number()[39m,
      Sal2017 = [32mcol_number()[39m,
      Sal2018 = [32mcol_number()[39m,
      Sal2019 = [32mcol_number()[39m
    )
    
    


### UW Employee Salary

Now that we have uploaded the data we can looks at the structure of University of Washginton Employees.


```R
uw_annual_employee_salary<-filter(washington_annual_employee_salary,AgyTitle=="University of Washington")
str(uw_annual_employee_salary)
```

    tibble [141,974 × 9] (S3: spec_tbl_df/tbl_df/tbl/data.frame)
     $ Agy     : chr [1:141974] "360" "360" "360" "360" ...
     $ AgyTitle: chr [1:141974] "University of Washington" "University of Washington" "University of Washington" "University of Washington" ...
     $ Name    : chr [1:141974] "PETERSEN, CHRISTOPHER" "HOPKINS, MICHAEL" "FERGUSON, KEITH" "COHEN, JENNIFER" ...
     $ JobTitle: chr [1:141974] "HEAD COACH-FOOTBALL" "HEAD COACH-MENS BASKETBALL" "PROFESSIONAL STAFF - CONTRACT P3 (E S X)" "DIRECTOR OF ATHLETICS PS CONTRACT (E S)" ...
     $ Sal2015 : num [1:141974] 0 0 0 0 645200 ...
     $ Sal2016 : num [1:141974] 0 0 0 0 675400 ...
     $ Sal2017 : num [1:141974] 0 1379900 0 0 715400 ...
     $ Sal2018 : num [1:141974] 3473300 1925000 1200600 670000 760300 ...
     $ Sal2019 : num [1:141974] 3949600 2485000 1002300 892500 795000 ...
     - attr(*, "spec")=
      .. cols(
      ..   Agy = [31mcol_character()[39m,
      ..   AgyTitle = [31mcol_character()[39m,
      ..   Name = [31mcol_character()[39m,
      ..   JobTitle = [31mcol_character()[39m,
      ..   Sal2015 = [32mcol_number()[39m,
      ..   Sal2016 = [32mcol_number()[39m,
      ..   Sal2017 = [32mcol_number()[39m,
      ..   Sal2018 = [32mcol_number()[39m,
      ..   Sal2019 = [32mcol_number()[39m
      .. )


We can see that there are 141,974 rows in this tibble. Each of these rows corresponds to a UW employee. Let's look at the first few employees.


```R
head(uw_annual_employee_salary)
```


<table>
<caption>A tibble: 6 × 9</caption>
<thead>
	<tr><th scope=col>Agy</th><th scope=col>AgyTitle</th><th scope=col>Name</th><th scope=col>JobTitle</th><th scope=col>Sal2015</th><th scope=col>Sal2016</th><th scope=col>Sal2017</th><th scope=col>Sal2018</th><th scope=col>Sal2019</th></tr>
	<tr><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>360</td><td>University of Washington</td><td>PETERSEN, CHRISTOPHER</td><td>HEAD COACH-FOOTBALL                     </td><td>     0</td><td>     0</td><td>      0</td><td>3473300</td><td>3949600</td></tr>
	<tr><td>360</td><td>University of Washington</td><td>HOPKINS, MICHAEL     </td><td>HEAD COACH-MENS BASKETBALL              </td><td>     0</td><td>     0</td><td>1379900</td><td>1925000</td><td>2485000</td></tr>
	<tr><td>360</td><td>University of Washington</td><td>FERGUSON, KEITH      </td><td>PROFESSIONAL STAFF - CONTRACT P3 (E S X)</td><td>     0</td><td>     0</td><td>      0</td><td>1200600</td><td>1002300</td></tr>
	<tr><td>360</td><td>University of Washington</td><td>COHEN, JENNIFER      </td><td>DIRECTOR OF ATHLETICS PS CONTRACT (E S) </td><td>     0</td><td>     0</td><td>      0</td><td> 670000</td><td> 892500</td></tr>
	<tr><td>360</td><td>University of Washington</td><td>MURRAY, CHRISTOPHER  </td><td>PROFESSOR                               </td><td>645200</td><td>675400</td><td> 715400</td><td> 760300</td><td> 795000</td></tr>
	<tr><td>360</td><td>University of Washington</td><td>CAUCE, ANA           </td><td>PRESIDENT                               </td><td>125600</td><td>714300</td><td> 734000</td><td> 749000</td><td> 764600</td></tr>
</tbody>
</table>



If I wanted to just consider the 2019 salary, I could use the `select()` function.


```R
uw_2019_employee_salary<-select(uw_annual_employee_salary,c(AgyTitle,Name,JobTitle,Sal2019))
head(uw_2019_employee_salary)
```


<table>
<caption>A tibble: 6 × 4</caption>
<thead>
	<tr><th scope=col>AgyTitle</th><th scope=col>Name</th><th scope=col>JobTitle</th><th scope=col>Sal2019</th></tr>
	<tr><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>University of Washington</td><td>PETERSEN, CHRISTOPHER</td><td>HEAD COACH-FOOTBALL                     </td><td>3949600</td></tr>
	<tr><td>University of Washington</td><td>HOPKINS, MICHAEL     </td><td>HEAD COACH-MENS BASKETBALL              </td><td>2485000</td></tr>
	<tr><td>University of Washington</td><td>FERGUSON, KEITH      </td><td>PROFESSIONAL STAFF - CONTRACT P3 (E S X)</td><td>1002300</td></tr>
	<tr><td>University of Washington</td><td>COHEN, JENNIFER      </td><td>DIRECTOR OF ATHLETICS PS CONTRACT (E S) </td><td> 892500</td></tr>
	<tr><td>University of Washington</td><td>MURRAY, CHRISTOPHER  </td><td>PROFESSOR                               </td><td> 795000</td></tr>
	<tr><td>University of Washington</td><td>CAUCE, ANA           </td><td>PRESIDENT                               </td><td> 764600</td></tr>
</tbody>
</table>



Let's look at the 5-number summary to get an idea of the spread of this data


```R
summary(uw_2019_employee_salary$Sal2019)
```


       Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
          0       0       0   20777   24400 3949600 


Over half of the salaries here are 0. Let's see what some of those positions that get paid 0 salary are.


```R
sample_n(filter(uw_2019_employee_salary,Sal2019==0),10)
```


<table>
<caption>A tibble: 10 × 4</caption>
<thead>
	<tr><th scope=col>AgyTitle</th><th scope=col>Name</th><th scope=col>JobTitle</th><th scope=col>Sal2019</th></tr>
	<tr><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><td>University of Washington</td><td>PARK, STEPHANIE    </td><td>BUDGET/FISCAL ANALYST LEAD (E S SEIU 925 NON SUPV)</td><td>0</td></tr>
	<tr><td>University of Washington</td><td>NICKLASON, HELAINA </td><td>FDA SEIU - PROJECT                                </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>FISCHLE, THOMAS    </td><td>VISITING SCIENTIST                                </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>LARA, PEDRO        </td><td>CUSTODIAN (NE S WFSE CAMPUSWIDE)                  </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>GARVEY, SEAN       </td><td>REGISTERED NURSE 2                                </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>KASUKURTHI, RAHUL  </td><td>FELLOW ACGME                                      </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>PECKHAM, TREVOR    </td><td>LIMITED TERM APPOINTMENT - PROF STAFF             </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>GENSHEIMER, MICHAEL</td><td>CHIEF RESIDENT                                    </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>DHAMI, GURLEEN     </td><td>RESIDENT                                          </td><td>0</td></tr>
	<tr><td>University of Washington</td><td>SILVA, CATHLENE    </td><td>ADMINISTRATIVE ASSISTANT A                        </td><td>0</td></tr>
</tbody>
</table>



Some of these positions look as though they are hourly positions. This would mean that their listed salaries would be 0. However, in order to be sure we would have to look at the documentation for the data set. In either case, I would like to only consider employees with a positive salary.


```R
uw_2019_employee_salary_pos<-filter(uw_2019_employee_salary,Sal2019>0)
summary(uw_2019_employee_salary_pos$Sal2019)
```


       Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
        300   13200   42100   54381   76600 3949600 


The interquartile range of a numerical data set is the difference between the 1st (Q1) and 3rd quartile (Q3). In this case the the interquartile range(IQ) is 63400. The inner fence of the data is defined to be [Q1-1.5IQ,Q3+1.5IQ] whereas the outer fence is defined to be [Q1-3IQ,Q3+3IQ].

Any value beyond the inner fence is traditionally called a *mild outlier* and any value beyond the outer fence is called an *extreme outlier*. Let's see how many mild and extreme outliers there are in this data set


```R
lower_inner_fence<-13200-1.5*63400
upper_inner_fence<-76600+1.5*63400
lower_outer_fence<-13200-3*63400
upper_outer_fence<-76600+3*63400
```


```R
uw_2019_salaries_mild_outliers<-filter(uw_2019_employee_salary_pos,Sal2019<lower_inner_fence | Sal2019>upper_inner_fence)
uw_2019_salaries_extreme_outliers<-filter(uw_2019_employee_salary_pos,Sal2019<lower_outer_fence | Sal2019>upper_outer_fence)
```


```R
str(uw_2019_salaries_extreme_outliers)
```

    tibble [450 × 4] (S3: tbl_df/tbl/data.frame)
     $ AgyTitle: chr [1:450] "University of Washington" "University of Washington" "University of Washington" "University of Washington" ...
     $ Name    : chr [1:450] "PETERSEN, CHRISTOPHER" "HOPKINS, MICHAEL" "FERGUSON, KEITH" "COHEN, JENNIFER" ...
     $ JobTitle: chr [1:450] "HEAD COACH-FOOTBALL" "HEAD COACH-MENS BASKETBALL" "PROFESSIONAL STAFF - CONTRACT P3 (E S X)" "DIRECTOR OF ATHLETICS PS CONTRACT (E S)" ...
     $ Sal2019 : num [1:450] 3949600 2485000 1002300 892500 795000 ...


As we can see there are 450 employees that are extreme outliers. This would make up $450/141974\approx 0.0032$ or 0.32% of all employees that have positive salary positions, i.e. not hourly.

## Looking Ahead

I hope this small introduction gives you an idea of how we can use R to perform statistical analysis. In the coming weeks we will learn more about the functionality of R. If you have any questions or concerns please let me know. If you are interested in learning more there are free online books and resources available.

- List of R tutorials https://www.r-bloggers.com/2015/12/how-to-learn-r-2/
- R for Data Science https://r4ds.had.co.nz/
- R markdown https://bookdown.org/yihui/rmarkdown/
