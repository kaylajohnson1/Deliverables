Modeling the unknown distribution with maximum likelihood and method of moments
===============================================================================

Maximum likelihood (MLE) and method of moments (MM) are two common
methods for constructing a model.

Assignment
----------

In this deliverable, I will write a tutorial in which I will explain 
how one might use MLE and MM to model (a) Glycohemoglobin
and (b) Height of adult females. The data will be from National Health
and Nutrition Examination Survey 2009-2010 (NHANES), available from the
Hmisc package. I will compare and contrast the two methods in addition
to comparing and contrasting the choice of underlying distribution.

## In the Deliverable I will:

1.  Show how I calculated estimates of parameters
2.  Provide visuals that show the estimated distribution compared to the
    empirical distribution ( I will comment on the quality of the fit)
    -   Overlay estimated pdf onto histogram
    -   Overlay estimated CDF onto eCDF
    -   QQ plot (sample vs estimated dist)
3.  Explain how I calculated the median from the estimated
    distribution
4.  Demonstrate how to generate the median sampling distribution
5.  Calculated the range of middle 95% of sampling distribution, and
    explain why such a quantity is important.

Data
----

This is the data that I will be using from National Health
and Nutrition Examination Survey 2009-2010 (NHANES). Since I am looking for (a) Glycohemoglobin
and (b) Height of adult females, I filtered the data to only show this information.

``` r
require(dplyr)
Hmisc::getHdata(nhgh)
d1 <- nhgh %>% 
  filter(sex == "female") %>% 
  filter(age >= 18) %>% 
  select(gh, ht) %>% 
  filter(1:n()<=1000)
```

Checklist
---------

I will do this for both MLE and MM.

|                                      | Normal | Gamma | Weibull |
|:-------------------------------------|:------:|:-----:|:-------:|
| Estimates of parameters              |        |       |         |
| Overlay estimated pdf onto histogram |        |       |         |
| Overlay estimated CDF onto eCDF      |        |       |         |
| QQ plot (sample vs estimated dist)   |        |       |         |
| Estimated Median                     |        |       |         |
| Median Samp Dist (hist)              |        |       |         |
| Range of middle 95% of Samp Dist     |        |       |         |


Other instructions
------------------

1.  The deliverable should be your own work. You may **discuss**
    concepts with classmates, but you may **not share** code or text.
