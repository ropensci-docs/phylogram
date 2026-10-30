# Reorder tree branches in ladderized pattern.

This function ladderizes the branches of a `dendrogram` object to aid in
visual interpretation.

## Usage

``` r
ladder(x, decreasing = FALSE)
```

## Arguments

- x:

  an object of class `"dendrogram"`.

- decreasing:

  logical indicating whether the tree should be ladderized upwards or
  downwards. Defaults to FALSE (downwards).

## Value

Returns an object of class `dendrogram`.

## Details

This function is the `dendrogram` analogue of the
[`ladderize`](https://rdrr.io/pkg/ape/man/ladderize.html) function in
the [`ape`](https://rdrr.io/pkg/ape/man/ape-package.html) package
(Paradis et al 2004, 2012).

## References

Paradis E, Claude J, Strimmer K, (2004) APE: analyses of phylogenetics
and evolution in R language. *Bioinformatics* **20**, 289-290.

Paradis E (2012) Analysis of Phylogenetics and Evolution with R (Second
Edition). Springer, New York.

## See also

The [`ladderize`](https://rdrr.io/pkg/ape/man/ladderize.html) function
in the [`ape`](https://rdrr.io/pkg/ape/man/ape-package.html) package
performs a similar operation for objects of class `"phylo"`.

## Author

Shaun Wilkinson

## Examples

``` r
  x <- read.dendrogram(text = "(A:0.1,B:0.2,(C:0.3,D:0.4):0.5);")
  plot(x, horiz = TRUE)

  x <- ladder(x, decreasing = TRUE)
  plot(x, horiz = TRUE)
```
