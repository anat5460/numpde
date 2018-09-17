# hw1
Andrew Altomare

* I used polynomial interpolation to create FD operators $D$ and $D_2$
* Not only does interpolation allow for accurate differencing on non-uniform grids but it also yields accuracy on/near the boundary
* `diffmat` and `diff2mat` have a second argument `acc` so that the user can specify a desired order of accuracy (supported values 2,4,6,... and 1,3,5,..., respectively)
