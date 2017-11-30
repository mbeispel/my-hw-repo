*Project 1 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** Good work on this first assignment! You wrote a very clear, concise analysis plan. You also have a clear grasp on some key statistics fundamentals. Moving forward, I would focus on your skills with Python and Pandas so you can dig in and execute on this plan.

**Some Notes**

* *Q.3a/b* You are right, effective handling of outliers is key to statistical analysis and subsequent modeling. But the question is *how*? Outliers will skew estimators and force models to pick up on potential noise in the data, that may not be key for the model to focus on. Thus, we should deal with them if we do not believe they are representative. One way could be to drop them if they are more than 3 std. dev. away from the mean, but this is a pretty light punishment. A more standard route is a bit softer at 2-2.5 std. deviations. As a consequence of the central limit theorem, 2-2.5 std. devs. would imply that the data point is very unlikely given the distribution.
* *Q.4a/b* We can definitely test/observe co-linearity via a regression, especially when you see flags like an artificially high R^2 value (**great point**)! Usually you want to investigate co-linearity and inter-correlations before hand, or after you see some red-flags, via a correlation matrix or some statistical test. Also, it's good to note that this is a linear relationship. Alternatively, if you try out one model and then try out a different one, different results should raise some further questions.

**Something to think about**

Regarding covariance and generalized linear models (linear regressions/logistic regressions in this case), these are all linear metrics and estimators. Thus, these models will work will if the data is actually linear in structure. If there are some non-linearities, then the models will not work well and may lead to some false conclusions. Non-linear models is an area where the world of Machine Learning has far exceeded traditional statistics methods of estimation. If you are curious, I would be happy to share/discuss more in class!

***Note: Given you already have some solid exposure to statistical analysis, so if you ever feel a topic is too elementary or you want more, please ask for some suggestions for more advanced readings! I can send things your way, especially once we get into modeling!***
