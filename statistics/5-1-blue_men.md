[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

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
* **Compute the probability between two heights using the CDF of a normal distribution**  
The normal continuous random variable "norm" in "scipy.stats" is imported:
```python
from scipy.stats import norm
```
The lower- and upper- bound of the range of height is converted to cm. Then the two values are used to find the percentage of the male population below each value, then the difference of the two is what we are looking for.
```python
h1 = (5+10/12)*0.3048*100 # lower-bound height in cm
h2 = (6+1/12)*0.3048*100 # higher-bound height in cm
mu = 178
sigma = 7.7
p = norm.cdf(h2,loc=mu, scale=sigma) - norm.cdf(h1,loc=mu, scale=sigma)
```
The result is: p = 0.34274683763147457  
The percentage of the U.S. male population is in the range of 5'8" (177.8cm) to 6'1" (185.4cm) is about 34.27%.
