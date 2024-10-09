# CI2024_lab1
The selected approach was **Simulated annealing**. Initially, the starting solution is *valid* (randomly generated). The **fitness** function returns a tuple with the validity of the solution and the cost. The **Tweak** function is a random multiple mutation tweak which takes as an input the strength in order to control the width of the step made with the tweak, increasing or decreasing with respect to the cost of the solution found (if the cost decreases, the strenght does so in order to make smaller steps, in the other case it's the opposite). As the Simulating annealing approach consists of, the *temperature* is a parameter that defines how likely we accept a worsening solution, and decreases each time we accept one until it falls below a treshold of 0.01 or the number of steps is reached.

| Universe size| Number of sets | Density | Validity | Cost
|----------|----------|----------|----------|----------|
| 100 | 10 | 0.2 |
| 1000 | 100 | 0.2 | True | 6444.29
| 10000 | 1000 | 0.2 | True | 128270.57
