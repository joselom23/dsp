
[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

### Exercise 3.1:  

Something like the class size paradox appears if you survey children and ask how many children are in their family. Families with many children are more likely to appear in your sample, and families with no children have no chance to be in the sample.

Use the **NSFG** respondent variable **numkdhh** to construct the actual distribution for the number of children under 18 in the respondents' households.

Now compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.

Plot the **actual** and **biased** distributions, and compute their **means**.  

#### Answer:

Importing libraries:
```
import numpy as np
import matplotlib
import nsfg
import thinkstats2
import thinkplot
```

Importing data:
```
resp = nsfg.ReadFemResp()
```

Calculating the Actual PMF:
```
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
```

Plotting the actual PMF:
```
thinkplot.Pmfs([pmf])
thinkplot.Config(xlabel='Number of children under 18', ylabel='PMF')
```
![Actual PMF](https://github.com/joselom23/dsp/blob/master/statistics/ActualPmf31.png)

Creating the function BiasPmf:
```
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
```

Calculating the biased PMF:
```
biased_pmf = BiasPmf(pmf, label='observed')
```

Plotting two Pmfs:
```
biased_pmf = BiasPmf(pmf, label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Class size', ylabel='PMF')
```

![Actual vs Observed PMFs](https://github.com/joselom23/dsp/blob/master/statistics/Biasedpmf31.png)

Actual distribution Mean:
```
pmf.Mean()
```

Observed distribution Mean:
```
biased_pmf.Mean()
```
