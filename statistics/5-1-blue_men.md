[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> First, create the normal distribution of men's height.
>> ```
>> mu = 178
>> sigma = 7.7
>> dist = scipy.stats.norm(loc=mu, scale=sigma)
>> ```
>> The percentage of men between between 5'10" (177.8cm) and 6'1" (185.4cm) is the difference of cdf of the two values, which is 34.2%.
>> ```
>> dist.cdf(185.42)-dist.cdf(177.8)
>> ```
