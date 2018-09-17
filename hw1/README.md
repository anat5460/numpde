# hw1
Andrew Altomare

* I used polynomial interpolation to create FD operators D and D2
* Not only does interpolation allow for accurate differencing on non-uniform grids but it also yields accuracy on/near the boundary
* `diffmat` and `diff2mat` have a second argument `acc` so that the user can specify a desired order of accuracy (supported values 2,4,6,... and 1,3,5,..., respectively)
* Grid refinement equipped with the infinite norm demonstrates the convergence and order of accuracy for each operator with the caveat that the longer stencils for high-accuracy differences are unstable on very fine grids
* Fixing the length of the stencil (and thus the degree of the interpolant), D converges faster than D2 under grid refinement by a factor of h
    * We lose an order of accuracy by taking a second derivative
