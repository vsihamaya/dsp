[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python
def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d
  
  
  CohenEffectSize(firsts.prglngth, others.prglngth)
```

Cohen effect size for the difference in pregnancy length for first babies and others:
0.028879044654449834

Cohen effect size to quantify the difference between the two groups in total weight:

```python
s = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
```

Cohen d: -0.08867292707260174

The effect size between the two groups in terms of weight is approx. four times stronger than 
compared to pregnancy length, but both effect sizes are considered very small and not significant.  