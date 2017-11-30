### ***Project 1 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** Good work on this! You presented a thorough analysis/research plan, and you're clearly familiar with some modeling techniques. We will get into this in a few lessons, but for now take the time to familiarize yourself with the tools (Jupyter, Pandas, Seaborn, etc.) and how we structure our analysis in the Data Science framework (asking the right questions, issues we may run into with missing values and outliers, re-formatting data, assumptions we need to test, assumptions we need to make, etc.).

**Some Notes**

You can write [text](https://jupyter.brynmawr.edu/services/public/dblank/Jupyter%20Notebook%20Users%20Manual.ipynb#4.-Using-Markdown-Cells-for-Writing) and [math expressions](http://data-blog.udacity.com/posts/2016/10/latex-primer/) in your Jupyter Notebooks for some handy displaying.

* ***Plotting:*** When plotting, try using [Seaborn](https://elitedatascience.com/python-seaborn-tutorial). It's a good bit easier to use than matplotlib, and it has some very handy built-in methods for plotting! For example:

```python
import seaborn as sns

#Box plots:
sns.boxplot( x=admit_data["prestige"], y=admit_dat["gpa"] )
plt.show()
```

```python
#Nice variable-by-variable plotting!
sns.pairplot(admit_data, hue='admit')
plt.show()
```

* *Q.3a* Outliers will skew the mean, but what outliers will also impact the models that we build. We will discuss this in class, but we usually have to find some way to handle them intelligently.
* *Q.4a/b* We can definitely test/observe co-linearity via a regression, but  usually co-linearity will impact your regression and you want to investigate it before hand via a correlation matrix or some statistical test. Also, it's good to note that this is a linear relationship (a concept we will discuss further in class).

**Something to think about**

We touch on this a bit in class, but think about how you can apply statistical tests to your data. There are many handy tests to determine difference of means (very useful), tests to determine assumptions of an underlying distribution, etc. For example, there are specific tests which will estimate how close a given distribution is to a normal distribution.

Also, check out this KDNuggets post for [outlier analysis](https://www.kdnuggets.com/2017/02/removing-outliers-standard-deviation-python.html) in Python!
