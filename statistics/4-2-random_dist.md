[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
import numpy as np
import thinkstats2
import thinkplot

#generate random values
nums = np.random.random(1000)

#create pmf and plot
#One problem is there are gaps in the data (i.e. numbers that didn't get picked). 
#No values got picked more than once, but it is hard to tell if the gaps are uniformly distributed.
pmf = thinkstats2.Pmf(nums,label="nums")
thinkplot.Pmf(pmf)
thinkplot.Show(xlabel = "nums", ylabel="probability")

#create cdf and plot
#From the CDF we can see that it is basically uniform (approx slope of ~1)
cdf = thinkstats2.Cdf(nums,label="nums")
thinkplot.Cdf(cdf)
thinkplot.Show(xlabel = "nums", ylabel="cumulative probability")
