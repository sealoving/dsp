[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

## Solution

* **Import libraries and load in data**  
(I use the same block for all exercise)

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline
import nsfg
import thinkstats2
import thinkplot

preg = nsfg.ReadFemPreg()
resp = nsfg.ReadFemResp()
```
* **Compute the mean**
```python
firsts = preg[preg.birthord==1]
others = preg[preg.birthord>1]

mean1 = firsts.totalwgt_lb.mean()
mean2 = others.totalwgt_lb.mean()
print(mean1, mean2, mean1-mean2)
```
7.201094430437772 7.325855614973262 -0.12476118453549034  
  
The mean birth weight is about 7.20 lbs for first babies, and 7.33 lbs for other babies.  
First babies are on average 0.125 lbs lighter than other babies according to the sample, which is quite small.


* **Compute Cohen's d**
```python
var1 = firsts.totalwgt_lb.var()
var2 = others.totalwgt_lb.var()
pooled_var = (len(firsts)*var1 + len(others)*var2) / (len(firsts)+len(others))
cohen_d = (mean1-mean2) / np.sqrt(pooled_var)
print(cohen_d)
```
-0.0886729270726  
  
Cohen's d for birth weight is about -0.089, which is greater than the value for pregnancy length (0.029). But they both show that the difference in mean is very small in comparison to standard deviation.
