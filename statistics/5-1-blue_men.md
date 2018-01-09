[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python
import scipy.stats

#Population statistics given
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

#function to convert inches to cm
def cm(inches):
    return 2.54*inches

#find probability range for 5'10 (70in) to 6'1" (73in)
lower = cm(70)
higher = cm(73)
lower_prob = dist.cdf(lower)
upper_prob= dist.cdf(upper)

percent = upper_prob - lower_prob
print ("Amount of males that qualify:",percent)

```
