[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> First, I calculate the mean weight of the first babies versus other babies. The mean weight for first babies is 7.201 pounds, while the mean weight for other babies is 7.326 pounds.

>> ```
>> print(firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean())
>> ```

>> Then write the Cohen's D effect size function.
>> ```
>>    def CohenEffectSize(group1, group2):
>>    """Computes Cohen's effect size for two groups.   
>>    group1: Series or DataFrame
>>    group2: Series or DataFrame
>>    
>>    returns: float if the arguments are Series;
>>             Series if the arguments are DataFrames
>>    """
>>    diff = group1.mean() - group2.mean()
>>
>>    var1 = group1.var()
>>    var2 = group2.var()
>>    n1, n2 = len(group1), len(group2)
>>
>>    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
>>    d = diff / np.sqrt(pooled_var)
>>    return d
>> ```
>> Last, I calculate the effect size to quantify the difference between the two groups. The effect size is -0.089. The difference in means is about 0.09 standard deviations, this number is a bit larger than the effect size of pregnancy length, but still small. Assuming that the numbers are accurate, it is unlikely that there are significant differences between the two groups in weight.

>> ```
>> CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
>> ```
