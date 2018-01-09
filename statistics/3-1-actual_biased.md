[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
import nsfg
import thinkstats2
import thinkplot

#function to bias pmf based on distribution
def bias_pmf(pmf,label):
    new_pmf = pmf.Copy(label=label)
    
    for x,p in pmf.Items():
        new_pmf.Mult(x,x)
    
    new_pmf.Normalize()
    return new_pmf

#read data into pmf
resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh,label="actual")

#apply bias for observed distribution
biased_pmf = bias_pmf(pmf,"observed")

#Calculate means
print("Actual Mean:",pmf.Mean())
print("Observed Mean:",biased_pmf.Mean())

#plot actual & observed pmf
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf,biased_pmf])
thinkplot.Show(xlabel='Kids per family', ylabel='Probability')

```
