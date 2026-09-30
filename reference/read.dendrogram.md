# Read a dendrogram from parenthetic text.

This function wraps the
[`read.tree`](https://rdrr.io/pkg/ape/man/read.tree.html) parser from
the [`ape`](https://rdrr.io/pkg/ape/man/ape-package.html) package to
read a phylogenetic tree from parenthetic text in the Newick/New
Hampshire format, and converts it to object of class "dendrogram".

## Usage

``` r
read.dendrogram(file = "", text = NULL, ...)
```

## Arguments

- file:

  character string giving a valid path to the file from which to read
  the data.

- text:

  optional character string in lieu of a "file" argument. If a text
  argument is provided instead of a file path, the data are read via a
  text connection.

- ...:

  further arguments to be passed to
  [`read.tree`](https://rdrr.io/pkg/ape/man/read.tree.html) (which may
  then be passed on to `scan`).

## Value

an object of class `"dendrogram"`.

## References

Felsenstein J (1986) The Newick tree format.
[http://evolution.genetics.washington.edu/phylip/newicktree.html](http://evolution.genetics.washington.edu/phylip/newicktree.md)

Olsen G (1990) Interpretation of the "Newick's 8:45" tree format
standard.
[http://evolution.genetics.washington.edu/phylip/newick_doc.html](http://evolution.genetics.washington.edu/phylip/newick_doc.md)

Paradis E, Claude J, Strimmer K, (2004) APE: analyses of phylogenetics
and evolution in R language. *Bioinformatics* **20**, 289-290.

Paradis E (2008) Definition of Formats for Coding Phylogenetic Trees in
R. <http://ape-package.ird.fr/misc/FormatTreeR_24Oct2012.pdf>

Paradis E (2012) Analysis of Phylogenetics and Evolution with R (Second
Edition). Springer, New York.

## See also

[`write.dendrogram`](https://docs.ropensci.org/phylogram/reference/write.dendrogram.md)
writes an object of class `"dendrogram"` to a Newick text string. The
[`read.tree`](https://rdrr.io/pkg/ape/man/read.tree.html) function in
the [`ape`](https://rdrr.io/pkg/ape/man/ape-package.html) package parses
objects of class `"phylo"` and `"multiPhylo"`.

## Author

Shaun Wilkinson

## Examples

``` r
  x <- read.dendrogram(text = "(A:0.1,B:0.2,(C:0.3,D:0.4):0.5);")
  plot(x, horiz = TRUE)
```
