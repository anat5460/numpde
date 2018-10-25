# hw2
Andrew Altomare

### Part 1
* Solving the p-Laplacian with Picard linearization was a modest extension of 
  `nonlinear2d_div` and `solve_nonlinear`
* Computing full grad u at all four staggered points followed nicely from a
  9 point stencil; second order approximations to remaining partial derivatives 
  could be recovered by taking an average of u values and performing a centered difference.
* I included a switch for turning off the computation of J, thus making the
  iterations of newton-krylov solver less wasteful
* Convergence gets slower as p grows, p<2 has very fast convergence
### Part 2
* Matrix free jacobian approximation is efficient and reasonably accurate
* sp.linalg.factorized gives callable LU solve of Picard linearization, which is
  used as the preconditioner to GMRES
* Depending on epsilon and p, this method can stagnate in the beginning before
  achieving its quadratic convergence
* Generally much faster convergence than Picard solver, quadratic (in a neighborhood
  of the solution) vs linear convergence
### Part 3
* The Newton linearization is convoluted and cumbersome compared to the matrix-free
  Jacobian in part 2.
