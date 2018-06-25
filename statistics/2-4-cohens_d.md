
[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

## Exercise 2.4  
Using the variable `totalwgt_lb`, investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

### Importing libraries to be used
```
import numpy as np
import first
import thinkstats2
```
### Reading al Preg data
```
preg = nsfg.ReadFemPreg()
```
### Only selecting data for live births
```
live = preg[preg.outcome == 1]
```
### Separating data into first and other children
```
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]
```
### Calculating and printing all the means
```
fm = firsts.totalwgt_lb.mean()
om = others.totalwgt_lb.mean()
md=fm-om

print (f'Firsts Weight Mean: {fm}')
print (f'Others Weight Mean: {om}')
print (f'Mean difference: {md}')
```
### Standard deviations
```
fs = firsts.totalwgt_lb.std()
os = others.totalwgt_lb.std()
```
### Computing pooled Standard deviation
```
var1 = firsts.totalwgt_lb.var()
var2 = others.totalwgt_lb.var()
n1, n2 = len(firsts.totalwgt_lb), len(others.totalwgt_lb)
pooled_std = ((n1 * var1 + n2 * var2) / (n1 + n2))**0.5
```
### Printing all STD
```
print (f'STD for firsts: {fs}')
print (f'STD for others: {os}')
print (f'Pooled STD: {pooled_std}')
```
### Cohen's d for total weight in lbs.
```
cohenswgt = (fm-om)/pooled_std
print(cohenswgt)
```
### Cohen's d for pregnancy length.
```
cohensprg = thinkstats2.CohenEffectSize(firsts.prglngth, others.prglngth)
print(cohensprg)
```
