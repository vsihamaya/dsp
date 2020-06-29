[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

Blue Man Group 
-----------
Height requirements between 5'10" and 6'1" 

```python
import scipy.stats
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
type(dist)
low = dist.cdf(177.8)   
high = dist.cdf(185.4)   
low, high, high-low
```
The percentage of the U.S. male population that is in this range is 0.34209468294595308 or 34%

