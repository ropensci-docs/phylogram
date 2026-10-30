# Convert a "phylo" object to a dendrogram.

This function converts a "phylo" object (Paradis et al 2004) to a
dendrogram.

## Usage

``` r
# S3 method for class 'phylo'
as.dendrogram(object, ...)
```

## Arguments

- object:

  an object of class "phylo".

- ...:

  further arguments to be passed between methods.

## Value

an object of class "dendrogram".

## References

Paradis E, Claude J, Strimmer K, (2004) APE: analyses of phylogenetics
and evolution in R language. *Bioinformatics* **20**, 289-290.

Paradis E (2008) Definition of Formats for Coding Phylogenetic Trees in
R. <http://ape-package.ird.fr/misc/FormatTreeR_24Oct2012.pdf>

Paradis E (2012) Analysis of Phylogenetics and Evolution with R (Second
Edition). Springer, New York.

## Author

Shaun Wilkinson

## Examples

``` r
  newick <- "(A:0.1,B:0.2,(C:0.3,D:0.4):0.5);"
  x <- read.dendrogram(text = newick)
  y <- as.phylo(x)
  z <- as.dendrogram(y)
  identical(x, z)
#> [1] FALSE
```
