An investigator would like to choose 2 treatments in a Phase II trial from 5 candidates for Phase III confirmatory study. Assume the primary outcome is dichotomous and odds of success for the truly second best treatment (i.e., the treatment associated with the second highest success probability) compared to the third best treatment is at least 3. In addition, due to ethical consideration, the investigator would like to remove the inferior treatment(s) from the competition as soon as we have enough evidence to do so. Please help this investigator to design a sequential selection procedure to identify two treatments such that the probability of correct selection (i.e., the two selected treatments are the truly best two treatments) is at least 80%.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### (a) Describe the procedure in details regarding the sampling rule, stopping rule, and the decision rule, as well as explaining how you choose the design parameters.

Here we set the lower bound *P*<sup>\*</sup> = 0.8 and *c* = 5, *b* = 2.
Ranking all the treatment success probability as
*p*<sub>1</sub> &gt; *p*<sub>2</sub> &gt; *p*<sub>3</sub> &gt; *p*<sub>4</sub> &gt; *p*<sub>5</sub>,
and $w\_{i} = \\frac{p\_{i}}{1-p\_{i}}$.

Then trying to calculate the least integer *r* that fits
$\\frac{3^r}{3^r + 5 - 2} \\geq 0.8$, we get *r* = 3.

Then toss coins vector-at-a-time.

Stop the first time the coin/coins with the 2<sup>*n**d*</sup> largest
tally has 3 more heads than the coin/coins with the 3<sup>*r**d*</sup>
largest tally

Select the 2 leading coins as best.

### (b) Suppose the investigator would like to select only ONE treatment (out of 5) and wants to guarantee the probability that the selected treatment is one of the two best treatments is at least 80%. Assume the primary outcome is the same as described above and, again, odds of success for the truly second best treatment (i.e., the treatment associated with the second highest success probability) compared to the third best treatment is at least 3. How would you design a sequential selection procedure to achieve the goal proposed by the investigator?

Same as above, we set the lower bound *P*<sup>\*</sup> = 0.8 and
*c* = 5, *b* = 2. Ranking all the success probability as
*p*<sub>1</sub> &gt; *p*<sub>2</sub> &gt; *p*<sub>3</sub> &gt; *p*<sub>4</sub> &gt; *p*<sub>5</sub>,
and $w\_{i} = \\frac{p\_{i}}{1-p\_{i}}$. Then get *r* = 3.

Then toss coins vector-at-a-time.

The first time coin/coins fall 3 success behind the coin/coins with the
2<sup>*n**d*</sup> largest tally, eliminate those trailing coins as
inferior.

The first time coin/coins pull 3 success ahead the coin/coins with the
3<sup>*r**d*</sup> largest tally, recruit those trailing coins as
superior

Continue tossing the other coins at their current tallies. Iterate until
2 coins have been recruited and/or 3 coins have been eliminated.

Randomly pick one from these two coins as the only one treatment.
