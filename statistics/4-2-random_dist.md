[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

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
* **Generate 1000 random numbers and plot PMF and CDF**  
```python
nums = np.random.random(1000)
pmf = thinkstats2.Pmf(nums)
thinkplot.pmf(pmf)
thinkplot.config(xlabel='VALUE',ylabel='PMF')
```
![ex4.2a](https://raw.githubusercontent.com/sealoving/dsp/master/img/ex4_2a.png)

```python
cdf = thinkstats2.Cdf(nums)
fig = thinkplot.cdf(cdf)
thinkplot.config(xlabel='VALUE',ylabel='CDF')
```
![ex4.2b](https://raw.githubusercontent.com/sealoving/dsp/master/img/ex4_2b.png)

The PMF shows an even distribution (horizonal at the top), and the CDF shows close to a straight line between (0,0) and (1,1). Therefore the random numbers (uniform between 0,1) seem to be random enough!
