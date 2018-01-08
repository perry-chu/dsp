[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python
import nsfg
import math

#read input file
preg = nsfg.ReadFemPreg()

#total live births
live = preg[preg.outcome==1]

#split into first born and other births
first = live[live.birthord==1]
other = live[live.birthord!=1]

#calculate mean
first_mean = first.totalwgt_lb.mean()
other_mean = other.totalwgt_lb.mean()

print("First born mean:",first_mean)
print("Other born mean:",other_mean)

#calculate variance (pooled var = weighted average var of the 2 groups)
total_var = live.totalwgt_lb.var()
first_var = first.totalwgt_lb.var()
other_var = other.totalwgt_lb.var()

pooled_var = (first_var*len(first) + other_var*len(other))/(len(first)+len(other))
print("Pooled var:",pooled_var)

#cohen's d calc
cd = abs(first_mean-other_mean)/math.sqrt(pooled_var)

print("Cohen's D for totalwgt_lb:",cd,"standard deviations")
```
