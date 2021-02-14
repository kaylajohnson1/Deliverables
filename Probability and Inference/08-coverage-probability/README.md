Coverage probability
====================

**Coverage probability** is an important operating characteristic of methods
for constructing interval estimates (for example: confidence intervals).

**Definition:** For the purposes of this blog, I will define the _95%
confidence interval of the median_ to be the middle 95% of sampling
distribution of the median. Similarly, the 95% confidence interval of
the mean, standard deviation, etc. is the middle 95% of the respective
sampling distribution.

**Definition:** For the purposes of this blog, I will define the
_coverage probability_ as the long run proportion of intervals that
capture the population parameter of interest. 

**Conceptually, one can calculate the coverage probability with the following steps:**

1.  generate a sample of size *N* from a known distribution
2.  construct a confidence interval
3.  determine if the confidence captures the population parameter
4.  Repeat steps (1) - (3) many times. Estimate the coverage probability
    as the proportion of samples for which the confidence interval
    captured the population parameter.

Ideally, a 95% confidence interval will capture the population parameter
of interest in 95% of samples.

Assignment
----------

In this blog post, I will perform a simulation to calculate the
coverage probability of the 95% confidence interval of the median when
computed from *F̂*<sub>*X*</sub><sup>*m**l**e*</sup>. I will explain coverage probability 
and explain the simulation.

Suggested steps
---------------

**Step:** I will generate a single sample from a standard normal distribution
of size *N* = 201. I will explain to the reader how I use MLE to estimate the
distribution.

**Step:** I will show the reader how I approximate the sampling distribution
of the median, conditional on the estimate of the distribution in the
previous step.

**Step:** I will describe how I Calculate a 95% confidence interval from the
approximated sampling distribution.

**Step:** I will explain the concept of coverage probability. 

**Step:** I will perform the simulation and report the results.

**Step:** I will describe how I might change the simulation to learn more
about the operating characteristics of my chosen method for
constructing the 95% confidence interval.
