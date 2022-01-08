# scipy_linear_sum_assignment_issue
`scipy.optimize.linear_sum_assignment` issue

I have a multivariate dataset `S` and a matrix `M` containing pairwise distances between elements of `S`. I wish to find a non-bipartite matching for `S` that minimises the sum of paired elements. 

The idea is to apply `scipy.optimizes.linear_sum_assignment` function to match elements of `S` with elements of `S`. To prevent trivial matchings (i.e., each element matching with itself), I replace the diagonal of `M` with a large value and apply `linear_sum_assignment` to `M`. 

If `S` is small, this gives the correct non-bipartite matching and I get matched pairs that are exhaustive. 

But for large `S`, I start to see some matched `n`-tuples (`n` > 2).
