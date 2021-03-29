
<h2>Probability I</h2>
<hr style="height: 3px; background-color: #AA0000;" />
<h3> Answer each of the following questions regarding probability. For the purposes of this worksheet assume the following

- A coin always lands on either heads or tails
- A deck of cards has 52 cards
  - There are four suits (clubs, hearts, diamonds, and spades) each with 13 cards
  - There are two colors (black and red) each with 26 cards
<hr style="height: 2px; background-color: #003282;" />

<h4> Problems: </h4>

1. If I flip a fair coin, what is the chance of the coin coming up heads?

> Solution:
> The sample space for a coin flip is $\{H,T\}$, which has a size of 2. The size of the event of coming up heads is equal to the size of the set $\{H\}$, which is just 1. Thus the probability of coming up heads is $1/2=.50$ or 50\%


2. If I draw a playing card from a shuffled deck, what is the chance of the card being red?

> Solution:
> The sample space for choosing a card is given by the elements
\[
\begin{array}{ccccccccccccc}
AS & 2S & 3S & 4S & 5S & 6S & 7S & 8S & 9S & 10S & JS &QS & KS \\
AC & 2C & 3C & 4C & 5C & 6C & 7C & 8C & 9C & 10C & JC &QC & KC \\
AD & 2D & 3D & 4D & 5D & 6D & 7D & 8D & 9D & 10D & JD &QD & KD \\
AH & 2H & 3H & 4H & 5H & 6H & 7H & 8H & 9H & 10H & JH &QH & KH \\
\end{array}
 \]
 > which has a size of 52. The red cards in the deck are hearts and diamonds. This means that the size of the event of choosing a red cars is $13+13=26$. Thus the probability of choosing a red card is $26/53=.50$ or 50\%

3. If I flip two fair coins at the same time, what is the chance of the coins both comping up heads?
> Solution:
> The sample space for flipping two coins is $\{HH,TH,HT,TT\}$, which has a size of 4. The size of the event of both coins coming up heads is equal to the size of the set $\{HH\}$, which is just 1. Thus the probability of coming up heads is $1/4=.25$ or 25\%

4. If I draw two playing cards at the same time from a shuffled deck, what is the chance of both cards being red?
> Solution:
> The sample space for choosing two cards at the same time is given by the array below

<img src="WS8.png" width=50%>

> The diagonal is blacked out because we cannot choose the same card simultaneously. Since the diagonal is blacked out, the size of the sample space is $52\cdot 52-52=52\cdot 51=2652$.  The size of the event of both cards coming up red is given by lower right hand square. The number of squares that aren't blacked out is $26*26-26=26*25=650$.  Thus the probability of choosing a red card is $650/2652\approx .245$ or 24.5\%


5. Why are the answers to problems 1 and 2 the same but the answers to problems 3 and 4 different?
> Solution:
> When flipping two coins the probability of one coin flip does not affect the probability of the other coin flip. However, for drawing two cards the probability of drawing one card can possible affect the probability of choosing another, i.e. you can't choose two of the same card. We say that the coin flips are independent and the card draw is conditional.
> >
>Specifically in this case, we can think about choosing the card one at a time or maybe labeling them after we chose them. If we label the cards 1 and 2, then we can see how the probability of the first card being red affects the probability of the second card being red. If card 1 is not red then card 2 has 26/51 chance of being red. If card 1 is red, then card 2 has a 25/51 chance of being red. Since these are different, the probability of card one affect card two unlike the two coins.
