### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** Great work on this homework! You're definitely comfortable with data analysis, and you are getting more and more comfortable with Pandas/Python. As we proceed into the modeling section, try experimenting with taking advantage of Python. Maybe you develop your own methods for dealing with pre-processing, or maybe your own class! Also, let me know if you have any questions on modeling, as this is the next **big** section in our journey!


**Some Notes**

* Regarding co-linearity, we don't typically refer to features as being co-linear unless they have a fairly high correlation, like on the order of 0.6 or higher. A correlation of 0.38 would mean that there is still soem information encoded in GRE that we may not otherwise get from GPA.
* Regarding your analysis plan, you should probably include what models/modeling techniques you think you should use. Considering we haven't gotten into it yet, this is more than okay to not include. However, typically when you write out your analysis plan, you include data cleaning, data manipulation, some analysis, and then modeling techniques to find, in this case, the relationship between Admission and Prestige!

**Something to think about**  
Dropping missing values can be necessary at times. In cases where you you have a lot of missing values, you might have to just drop those rows *or* ignore that feature all together (forget that column, we can't use it). However, as we proceed, you will find that data is gold to these algorithms. Very often, the more data you have, the more information you are giving to your model so it can generalize even better. To ensure we retain as much data as we can, a common practice is to fill missing values with the mean or median or mode so that you can keep those instances, without disturbing your distribution too much. Nice work on using the forward fill method, as an example! What you could do is test this method, then test the method of just imputing the mean/median values. Using a forward fill will make the assumption that the nearest value follows a similar distribution. This is a solid method, and it is often the case. However, you are imputing a bit more bias into your model than if you had imputed the mean/median.

Check out these guides:
https://machinelearningmastery.com/handle-missing-data-python/
https://chrisalbon.com/python/pandas_missing_data.html
