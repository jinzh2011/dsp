[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> First, create the pmf dictionary for the actual distribution of `numkdhh` variable.
>> ```
>> d_hist = thinkstats2.Hist(resp.numkdhh, label='numkdhh')
>> pmf = thinkstats2.Pmf(d_hist, label='correct')
>> ```
>> Then use bias function to create the biased pmf distribution if we survey the children
to get the number of children in households.
>> ```
>> def BiasPmf(pmf, label):
>>     new_pmf = pmf.Copy(label=label)
>>
>>     for x, p in pmf.Items():
>>         new_pmf.Mult(x, x)
>>        
>>     new_pmf.Normalize()
>>     return new_pmf
>> pmf_biased = BiasPmf(pmf, label= 'biased')
>> ```
>> Plot the graph of the two probability mass functions.

>> ![plot](https://github.com/jinzh2011/dsp/blob/master/statistics/chap03ex1.png)

>> ```
>> thinkplot.PrePlot(2)
>> thinkplot.Pmfs([pmf, pmf_biased])
>> thinkplot.Config(xlabel='Number of children', ylabel='PMF')
>> ```

>> The mean for actual distribution is 1.02, while the mean for biased distribution is 2.40.
>> ```
>> print(pmf.Mean())
>> print(pmf_biased.Mean())
>> ```
