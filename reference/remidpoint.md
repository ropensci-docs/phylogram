# Set dendrogram attributes for a nested list.

`remidpoint` is a helper function used for manually creating
`"dendrogram"` objects from nested lists. The function recursively
assigns the necessary 'midpoint', 'members', and 'leaf' attributes at
each node.

## Usage

``` r
remidpoint(x)
```

## Arguments

- x:

  a nested list, possibly of class `"dendrogram"`

## Value

returns a nested list, or an object of class `"dendrogram"` depending on
the class of the input object.

## Author

Shaun Wilkinson

## Examples

``` r
  ## manually create a small dendrogram with three members, A, B and C
  x <- list("A", list("B", "C"))
  attr(x[[1]], "leaf") <- TRUE
  attr(x[[2]][[1]], "leaf") <- TRUE
  attr(x[[2]][[2]], "leaf") <- TRUE
  attr(x[[1]], "label") <- "A"
  attr(x[[2]][[1]], "label") <- "B"
  attr(x[[2]][[2]], "label") <- "C"
  attr(x, "height") <- 1
  attr(x[[1]], "height") <- 0
  attr(x[[2]], "height") <- 0.5
  attr(x[[2]][[1]], "height") <- 0
  attr(x[[2]][[2]], "height") <- 0
  x <- remidpoint(x)
  class(x) <- "dendrogram"
  plot(x, horiz = TRUE)
```
