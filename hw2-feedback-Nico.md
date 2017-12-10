### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** A fantastic job on this assignment! You wrote some very pythonic/panda-y code on this one. Keep it going! Also, great use of statistical tests here. Applying statistical tests just gives you quantitative insight and gives support to claims.


**Some Notes**

* *Q.3:* Note that a `Series` is different from a `time series`. GRE and GPA are `Series` or just singular columns/features of our data. They do not have a particular time component.
* How Python of you! `df_only_missing=df_raw[~df_raw.index.isin(df_no_missing.index)]` Good work!
* *Q.10:* When we say correction, we typically refer to some form of transform. That would be a log transform, inverse transform, condensing function, or anything! You wouldn't want to explicitly change the data by adding .5 to the top or subtracting .5 from the bottom because that would change the underlying distribution! Not to mention that would really just shift the gap higher. Also, in this case, does this make sense? We already know that GPAs and GRE scores can't go above 4.0 and 800 respectively. In this case, even though the data is not totally normal, partially due to skew and partially do to the capping at 4.0 and 800, you wouldn't necessarily need to change the distribution. However, if you use a model that relies heavily on assumptions of normality, you have some key-information to point to if your model doesn't work well!
* Regarding your analysis plan, you should probably include what models/modeling techniques you think you should use. Considering we haven't gotten into it yet, this is more than okay to not include. However, typically when you write out your analysis plan, you include data cleaning, data manipulation, some analysis, and then modeling techniques to find, in this case, the relationship between Admission and Prestige!

**Something to think about**  
Dropping missing values can be necessary at times. In cases where you you have a lot of missing values, you might have to just drop those rows *or* ignore that feature all together (forget that column, we can't use it). However, as we proceed, you will find that data is gold to these algorithms. Very often, the more data you have, the more information you are giving to your model so it can generalize even better. To ensure we retain as much data as we can, a common practice is to fill missing values with the mean or median or mode so that you can keep those instances, without disturbing your distribution too much. Check out these guides:
https://machinelearningmastery.com/handle-missing-data-python/
https://chrisalbon.com/python/pandas_missing_data.html
