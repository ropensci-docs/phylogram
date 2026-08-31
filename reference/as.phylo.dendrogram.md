# Convert a dendrogram to a "phylo" object.

This function converts a dendrogram into an object of class "phylo" (see
Paradis et al 2004).

## Usage

``` r
# S3 method for class 'dendrogram'
as.phylo(x, ...)
```

## Arguments

- x:

  a dendrogram.

- ...:

  further arguments to be passed between methods.

## Value

an object of class "phylo".

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
```
