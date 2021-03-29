
<h2>Probability II<h2>
<hr style="height: 3px; background-color: #AA0000;" />
<h3>For our class, fill in the following table

| | On campus | Not on campus | Total |
| - | - | - | - |
| Lives with a pet| 1 | 17 | 18|
| Does not live with a pet | 9 | 26 | 35 |
| Total| 10 | 43 | 53 |

<hr style="height: 2px; background-color: #003282;" />

<h4> Problems: </h4>

> I have combined the data from both of my sections in the table above. Note that your answers will be a bit different depending on which section you are in.

1. What is the chance that a randomly selected student from our class is on campus?

> Solution:
> The total number of SU students in the classes on campus is $10$ and the total number of students is $53$. Thus the proportion of students from the classes that lives on campus is
\[
\frac{10}{53}\approx 0.1887
\]
> So the chance that a student chosen lives on campus is 18.87%

2. What is the chance that a randomly selected student from out class has a pet?

> Solution:
> The total number of students that has a pet in the classes is $18$ and the total number of students is $53$. Thus the proportion of students from the classes that have pets is
\[
\frac{18}{53}\approx 0.3396
\]
> So the chance that student chosen has a pet is 33.96%

3. What is the chance that a randomly selected student from our class both lives on campus and has a pet?

> Solution:
> The total number of students that are both on campus and lives with a pet is $1$ and the total number of students is $53$. Thus the proportion of students that both live on campus and have pets is
\[
\frac{1}{53}\approx 0.0189
\]
> So the chance that student chosen has a pet is 33.96%

4. If we add the total number of on campus students and the total number of students that live with pets, does that give us the total number of students who are either on campus or live with pets?

> Solution:
> No. Since there is one student that both lives on campus and has a pet we need to be careful how we count. If we add the total number of students that live with pets and the total number of students on campus we get, $10+18=28$. This number is too high, we have double counted the $1$ student who is both on campus and has a pet. The correct value would be $10+18-1=27$.

5. What is the chance that a randomly selected student from our class is either on campus or lives with a pet?

> Solution:
> At the end of the previous problem we found that the amount of students who either have pets or live on campus is $27$. The total number of students is $53$. Thus the proportion of students that are either from Washington or in their first year is
\[
\frac{27}{53}\approx 0.5094
\]
> So the chance a randomly selected student from our class is either on campus or lives with a pet is 50.94%

6. If I randomly select one student out of only the students that do not live on campus, what is the chance they live with a pet?

> Solution:
> The number of students that do not live on campus is $43$ and the number of students that do not live on campus and have pets is $17$. Thus the proportion of students who do live live on campus that have a pet is
\[
\frac{17}{43}\approx 0.3953
\]
> Thus the chance of a student that does not live on campus having a pet is 39.53%.

<h3> Out of all undergraduates at Seattle University, 43.6% are from Washington and 18.7% are in their first year. Out of all first-year students, 43.1% are from Washington. </h3>

<hr style="height: 2px; background-color: #003282;" />

>It's going to be helpful to form a contingency table for these problems. In order to form the contingency table we will need to know the probabilities across all four categories. First, since 43.6\% are from Washington, 56.4\% are from out of state. Second, since 18.7\% are in their first year, 81.3\% are second year and above. Finally, we know that out of all first-years, 43.1\% are from Washington. Thus, with regards to the total population, 43.1\% of the 18.7\% first-years are from Washington and in their first year. Considered as a proportion of the total population, this is equal to $.431\cdot .187\approx 0.0806$ or 8.06\%. This gives us the following table
\[
\begin{array}{|c|c|c||c|}
\hline
& \text{First-Year} & \text{Not a First-Year} & \text{Total} \\
\hline
\text{From Washington} & 0.0806 &  & 0.436\\
\hline
\text{Out of State} &  &  & 0.564\\
\hline
\hline
\text{Total}& 0.187 & 0.813 & 1 \\
\hline
\end{array}
\]
In order to fill in the rest, we use the totals along the side and bottom.
\[
\begin{array}{rl}\text{Not a First-year and from Washington}:& 0.436-0.0806=0.3554\\
\text{First-year and out of state}:&0.187-0.0806=0.1064 \\
\text{Not a First-year and out of state}:& 0.813-0.3554=0.4576\\
\end{array}
\]
This gives us the completed table.
\[
\begin{array}{|c|c|c||c|}
\hline
& \text{First-Year} & \text{Not a First-Year} & \text{Total} \\
\hline
\text{From Washington} & 0.0806 & 0.3554 & 0.436\\
\hline
\text{Out of State} & 0.1064 & 0.4576 & 0.564\\
\hline
\hline
\text{Total}& 0.187 & 0.813 & 1 \\
\hline
\end{array}
\]

<h4> Problems: </h4>

1. What is the chance that a randomly selected undergraduate from Seattle University is both from Washington and in their first-year?

> Solution
> The value is the upper left spot in the table, 8.06\%

2. What is the chance that a randomly selected undergraduate from Seattle University is both from out of state and in their first year?

> Solution:
> The is the lower left spot in the table, 10.64\%

3. What is the chance that a randomly selected undergraduate from Seattle University is both from Washington and **not** in their first year?

> Solution:
> This is the upper right spot in the table, 35.54\%

4. What is the chance that a randomly selected undergraduate from Seattle University is both from out of state and **not** in their first year?

> Solution:
> This is the lower right spot in the table, 45.76\%

5. What is the chance that a randomly selected undergraduate from Seattle University is either from Washington or in their first year?

> Solution:
> In order to calculate this we use the technique from the first page. The probability of an undergraduate being from Washington is 43.6\%, the probability of them being in their first-year is 18.7\%, and the probability of them being both is 8.06\%. So the probability of a randomly selected student being either from Washington or in their first-year is
\[
43.6\%+18.7\%-8.06\%=54.24\%
\]

6. If we randomly select one student out of only the students from Washington, what is the probability they are in their first year?

> Solution:
> This is a conditional probability. So we will need to use the formula
\[
\begin{array}{rl}
P\left(\text{first year | From Washington}\right)&=\frac{P\left(\text{From Washington and in First-year}\right)}{P\left(\text{From Washington}\right)}\\
&=\frac{0.0806}{0.436}\\
&\approx 0.1849
\end{array}
\]
So the probability is 18.49\%
