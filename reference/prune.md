# Remove tree nodes by regular expression pattern matching.

`"prune"` takes an object of class `"dendrogram"` and removes all
branches whose branch labels match a given regular expression.

## Usage

``` r
prune(tree, pattern, keep = FALSE, ...)
```

## Arguments

- tree:

  an object of class `"dendrogram"`.

- pattern:

  a regular expression.

- keep:

  logical indicating whether the nodes whose labels match the regular
  expression provided in "pattern" should be kept and the remainder
  discarded. Defaults to FALSE. Note that nodes without "label"
  attributes are ignored.

- ...:

  further arguments to be passed to `grepl` and `gsub`.

## Value

Returns an object of class `"dendrogram"`.

## Details

This function recursively tests the "label" attribute of each dendrogram
node (including non-leaf inner nodes if applicable) for the specified
pattern, removing those that register a positive hit. Note that positive
matching inner nodes are removed along with all of their sub-nodes,
regardless of whether the "label" attributes of the sub-nodes match the
pattern.

## See also

The [`drop.tip`](https://rdrr.io/pkg/ape/man/drop.tip.html) function in
the [`ape`](https://rdrr.io/pkg/ape/man/ape-package.html) package
performs a similar operation for objects of class `"phylo"`. See
[`regex`](https://rdrr.io/r/base/regex.html) for help with compiling
regular expressions.

## Author

Shaun Wilkinson

## Examples

``` r
  x <- read.dendrogram(text = "(A:0.1,B:0.2,(C:0.3,D:0.4):0.5);")
  plot(x, horiz = TRUE)

  x <- prune(x, pattern = "^A$")
  plot(x, horiz = TRUE)
```
