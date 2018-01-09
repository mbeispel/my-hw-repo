### ***Project 3 Feedback***

***Nico Van de Bovenkamp***

***

**Overall**  
Awesome work on this assignment! You effectively built the models, and interpreted all outputs. As we discussed earlier, what I recommend is that you take this analysis/model, and try your hand using sklearn! Maybe even try out some different types of models we have learned: KNN, Decision trees, random forest, boosted trees, naive bayes, or SVMs!

***A note on Odds Ratios***  
In this case, the odds ratios are calculated based on the conditional probability of P(admit=1 | prestige_1) and
P(admit=0 | prestige_1). In other words, you take good outcome, given exposed, over good outcome, given not exposed. And then you take this odds and take the ratio over bad outcome, given exposed, over bad outcome, given not exposed. Here, admission=1 is the good outcome and prestige is the thing we are testing for! If you are then given the matrix of outcomes of:  
```python
pd.crosstab(handCalc['admit'], handCalc['prestige_1.0'], rownames=['admit'])
```
#### Admission table:

| prestige_1        |  0            | 1     |
| -------------     |:-------------:| -----:|
| admit             |               |       |
| 0                 |   243         |  28   |
| 1                 |   93          |  33   |

Then the calculation is as follows:  
Odds(admitted | prestige_1) = 33/28 = 1.179  
Odds(admitted | not prestige_1) = 94/245 = 0.384      
OddsRatio = 1.179/0.384 = 3.07

Thus, the interpretation of this is that students that attended a prestige_1 school are 3 times as likely to be admitted to grad school! Note that this is _not_ a percentage, but an interpretation of relative likelihood **given** some probability, or percentage. Odds ratios are handy for some level of data exploration, and, of course, when it comes to interpreting log odds coefficients. A minor note, but instructive nonetheless. Logistic regression coefficients are not always super informative, and, for the most part, you are often much more concerned with the performance of a model!
