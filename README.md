# CI2024_lab1
The selected approach was **Simulated annealing**. Initially, the starting solution is *valid* (randomly generated). The **fitness** function returns a tuple with the validity of the solution and the cost. The **Tweak** function is a random multiple mutation tweak which takes as an input the strength in order to control the width of the step made with the tweak, increasing or decreasing with respect to the cost of the solution found (if the cost decreases, the strenght does so in order to make smaller steps, in the other case it's the opposite). As the Simulating annealing approach consists of, the *temperature* is a parameter that defines how likely we accept a worsening solution, and decreases each time we accept one until it falls below a treshold of 0.01 or the number of steps is reached. In the tests with *Universe size*= $10^5$ and *Number of sets*= $10^4$ the number of steps has been decreased in order to see the behaviour of the algorithm in an acceptable time (around 7 minutes). However, for the first instance there are not good results, because the tweak function also with low strength leads to big steps in the research, so basically modifies a lot a solution and the research acts quite like a random one.

| Instance | Universe size| Number of sets | Density | Validity | Cost | Number of steps
|----------|----------|----------|----------|----------|----------|----------|
| 1 | 100 | 10 | 0.2 | True | 289.98 | 10000
| 2 | 1000 | 100 | 0.2 | True | 6444.29 | 10000
| 3 | 10000 | 1000 | 0.2 | True | 128270.57 | 10000
| 4 | 100000 | 10000 | 0.1 | True | 1078.52* $10^5$ | 1000
| 5 | 100000 | 10000 | 0.2 | True | 2329.20* $10^5$ | 1000
| 6 | 100000 | 10000 | 0.3 | True | 3608.30* $10^5$ | 1000
