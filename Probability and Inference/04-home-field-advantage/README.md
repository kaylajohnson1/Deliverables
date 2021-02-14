Home Field Advantage
====================

**If home field advantage exists, how much of an impact does it have on winning the world series?**

In this assignment, I am tasked with answering probability and inference questions that relate to the World Series. I will use simulation and analytic probability calculations to answer the questions. 
I will take important data science concepts and will explain the questions and solutions in a way that is accessible to a general audience. I will be sure to mention any assumptions of my solution.

## Setup:

-   Suppose that the Braves and the Yankees are teams competing in the
    World Series.

-   The table below has the two possible schedules for each game of the
    series. (NYC = New York City, ATL = Atlanta)

| Overall advantage | Game 1 | Game 2 | Game 3 | Game 4 | Game 5 | Game 6 | Game 7 |
|:-----------------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
|       Braves      |   ATL  |   ATL  |   NYC  |   NYC  |   NYC  |   ATL  |   ATL  |
|      Yankees      |   NYC  |   NYC  |   ATL  |   ATL  |   ATL  |   NYC  |   NYC  |

-   Let *P*<sub>*B*</sub> be the probability that the Braves win a
    single head-to-head match-up with the Yankees, under the assumption
    that home field advantage doesn’t exist. Let
    *P*<sub>*B*</sub><sup>*H*</sup> denote the probability that the
    Braves win a single head-to-head match-up with the Yankees as the
    home team (H for home). Let *P*<sub>*B*</sub><sup>*A*</sup> denote
    the probability that the Braves win a single head-to-head match-up
    with the away team (A for away).

| Game location |    No advantage   | Advantage                                                            |
|:-------------:|:-----------------:|:---------------------------------------------------------------------|
|      ATL      | *P*<sub>*B*</sub> | *P*<sub>*B*</sub><sup>*H*</sup> = *P*<sub>*B*</sub> \* 1.1           |
|      NYC      | *P*<sub>*B*</sub> | *P*<sub>*B*</sub><sup>*A*</sup> = 1 − (1 − *P*<sub>*B*</sub>) \* 1.1 |

## Questions to answer:

1.  Compute analytically the probability that the Braves win the world
    series when the sequence of game locations is {NYC, NYC, ATL, ATL,
    ATL, NYC, NYC}. (The code below computes the probability for the
    alternative sequence of game locations. **Note:** The code uses
    `data.table` syntax, which may be new to you. This is intential, as
    a gentle way to introduce `data.table`.) Calculate the probability
    with and without home field advantage when *P*<sub>*B*</sub> = 0.55.
    What is the difference in probabilities?

2.  Calculate the same probabilities as the previous question by
    simulation.

3.  What is the absolute and relative error for your simulation in the
    previous question?
