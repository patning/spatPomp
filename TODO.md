# spatPomp to-do list

23-03-10. Add params argument to spatPomp()

23-03-10. Issue with spatPomp_Csnippet: get const right for observations in rmeasure.

23-03-10. Write compartment models using mu[SE], dN[SE], etc.

22-12-06. rmeasure and dmeasure could be built using runit_measure and dunit_measure if those are supplied.

22-12-06. note that eunit_measure, vunit_measure and munit_measure calculate for all units and subset out the requested ones. this could lead to inefficient code when not used in a vectorized way.

22-12-06. dunit_measure and runit_measure could be vectorized to prevent the need for vec_dmeasure and vec_rmeasure.

22-10-05. Use spatPomp_Csnippet() where appropriate in the models.

22-09-02. add more unit tests (current coverage 83.1%)

22-09-02. add localization to enkf and ienkf

22-09-02. girf updates: looks for ways to get it working better on the measles example, for example Joonha Park's ideas:

1. Since the population dynamics show exponential growth or decay, the pseudo-simulations (obtained by adding suitable noises to a deterministic skeleton) can be made on the log scale.

2. The current bootstrap guide method scales the prediction variance linearly with the length of the prediction time interval for making pseudo-simulations.  However, this would not give accurate predictions when the size of the process noise varies over time.  A simple way to address this issue would be to make pseudo-prediction from time t_c to t in the following way:

pseudo-simulation at time t = (deterministic skeleton prediction at t) 
  + { (reference random prediction at time t)
     - (reference deterministic prediction at time t) }
  - { (reference random prediction at time t_c)
     - (reference deterministic prediction at time t_c) }

20-11-05. handle multivariate observations

20-11-05. output filter particles






