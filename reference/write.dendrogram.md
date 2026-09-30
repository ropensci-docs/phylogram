# Write a dendrogram object to parenthetic text.

This function exports a dendrogram object as a Newick/New Hampshire text
string.

## Usage

``` r
write.dendrogram(x, file = "", append = FALSE, edges = TRUE, ...)
```

## Arguments

- x:

  an object of class `"dendrogram"`.

- file:

  a character string naming a file or connection to write the output to.
  If no file path is specified or `file = ""` the result is printed to
  the console.

- append:

  logical indicating whether the output should be appended to the file.
  If `append = FALSE` the contents of the file will be overwritten (the
  default setting).

- edges:

  logical indicating whether edge weights should be included in the
  output string.

- ...:

  further arguments to be passed to `format`. Used to specify the
  numbering style of the edge weights (if edges = TRUE).

## References

Felsenstein J (1986) The Newick tree format.
[http://evolution.genetics.washington.edu/phylip/newicktree.html](http://evolution.genetics.washington.edu/phylip/newicktree.md)

Olsen G (1990) Interpretation of the "Newick's 8:45" tree format
standard.
[http://evolution.genetics.washington.edu/phylip/newick_doc.html](http://evolution.genetics.washington.edu/phylip/newick_doc.md)

## See also

[`read.dendrogram`](https://docs.ropensci.org/phylogram/reference/read.dendrogram.md)
to parse a `"dendrogram"` object from a text file. The
[`write.tree`](https://rdrr.io/pkg/ape/man/write.tree.html) function in
the [`ape`](https://rdrr.io/pkg/ape/man/ape-package.html) package
performs a similar operation for `"phylo"` and `"multiPhylo"` objects.

## Examples

``` r
  newick <- "(A:0.1,B:0.2,(C:0.3,D:0.4):0.5);"
  x <- read.dendrogram(text = newick)
  write.dendrogram(x, edges = TRUE)
#> [1] "(A:0.1,B:0.2,(C:0.3,D:0.4):0.5);"
```
