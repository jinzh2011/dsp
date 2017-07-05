[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> First, generate 1000 numbers from the function numpy.random.random
>> ```
>> sample = np.random.random(1000)
>> ```
>> Then, plot the pmf and cdf graphs.

>> ![pmf](https://github.com/jinzh2011/dsp/blob/master/statistics/chap04ex2_pmf.png)

>> ![cdf](https://github.com/jinzh2011/dsp/blob/master/statistics/chap04ex2_cdf.png)

>> ```
>> pmf = thinkstats2.Pmf(sample)
>> thinkplot.Pmf(pmf, linewidth=0.1)
>> thinkplot.Config(xlabel='Random numbers', ylabel='PMF')
>> plt.savefig('chap04ex2_pmf.png')
>>
>> cdf = thinkstats2.Cdf(sample)
>> thinkplot.Cdf(cdf)
>> thinkplot.Config(xlabel='Random numbers', ylabel='CDF')
>> plt.savefig('chap04ex2_cdf.png')
>> ```
