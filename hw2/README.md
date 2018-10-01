# hw2
Andrew Altomare

* I used Chebyshev collocation to produce differential operators
    * Exploiting the linearity of the ODE made it easy to combine
      these operators to suit the BVP
* I was not able to solve the equation on the interval [0,1]. The solution 
worked well on [-1,1] but I couldn't figure out why the vander_chebyshev matrix
is so ill conditioned on different intervals.
* Achieved spectral convergence, as demonstrated with the method of
  manufactured solutions on hypterbolic tangent
* When a<<b, we recover a highly oscillatory u
    * This behavior follows intuition when observing the analytic solution of
      the ODE
