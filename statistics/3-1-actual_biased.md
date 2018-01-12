[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

## Solution

* **Import libraries and load data**  
(I use the same code block for all exercises)
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
* **Compute actual and biased pmf**  
Instead of using the given function in the book material, I wrote the computation of biased pmf step-by-step.
```python
pmf = thinkstats2.Pmf(resp.numkdhh,label='numkdhh')
pmfb = pmf.Copy()
for x,f in pmfb.Items():
    pmfb[x] = f*x
pmfb.Normalize()
pmf.label = 'actual'
pmfb.label = 'biased'
thinkplot.pmfs([pmf,pmfb])
thinkplot.config(xlabel='Number of children', ylabel='PMF')
```
The plot shows that biased pmf indicates 2 kids on average, versus 1 kid using the actual distribution.
![ex3.1](https://raw.githubusercontent.com/sealoving/dsp/master/img/ex3_1.png)
