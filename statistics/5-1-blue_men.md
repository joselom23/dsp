[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)


### Exercise 5.1

In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters `μ = 178 cm` and `σ = 7.7 cm` for men, and `μ = 163 cm` and `σ = 7.3 cm` for women.  

In order to join Blue Man Group, you have to be male between `5’10”` and `6’1”` (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? `Hint: use scipy.stats.norm.cdf`.

#### Answer: 

Importing libraries:
```
import numpy as np
import scipy
```

Mean and STD from the BRFSS data:
```
mean = 178
std  = 7.7

# Values in CM

minval = 177.8 #5'10"
maxval = 185.42 #6'1"
```

Defining EvalNormalCdf to understand the Cdf of each value given the parameters:
```
def EvalNormalCdf(x, mu, sigma):
    return scipy.stats.norm.cdf(x, loc=mu, scale=sigma)
```

In order to calculate the probability of the range, we are going to calculate the difference of CDFs:
```
pbetween = EvalNormalCdf(maxval,mean,std) - EvalNormalCdf(minval,mean,std)
pb = round(pbetween*100,2)
print(f'The percentage of people that are between 5\'10\" and 6\'1\" is: {pb}%')
```
