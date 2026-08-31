# Dendrograms for evolutionary analysis.

The **phylogram** R package is a tool for for developing phylogenetic
trees as deeply-nested lists known as "dendrogram" objects. It provides
functions for conversion between "dendrogram" and "phylo" class objects,
as well as several tools for command-line tree manipulation and
import/export via Newick parenthetic text. This improves accessibility
to the comprehensive range of object-specific analytical and
tree-visualization functions found across a wide array of bioinformatic
R packages.

## Functions

A brief description of the primary phylogram functions are provided with
links to their help pages below.

## File import/export

- [`read.dendrogram`](https://docs.ropensci.org/phylogram/reference/read.dendrogram.md)
  reads a Newick parenthetic text string from a file or text connection
  and creates an object of class `"dendrogram"`

- [`write.dendrogram`](https://docs.ropensci.org/phylogram/reference/write.dendrogram.md)
  outputs an object of class `"dendrogram"` to a text string or file in
  Newick format

## Object conversion

- [`as.phylo.dendrogram`](https://docs.ropensci.org/phylogram/reference/as.phylo.dendrogram.md)
  converts a dendrogram to an object of class "phylo" `"dendrogram"`

- [`as.dendrogram.phylo`](https://docs.ropensci.org/phylogram/reference/as.dendrogram.phylo.md)
  converts a "phylo" object to a dendrogram

## Tree editing and manipulation

- [`prune`](https://docs.ropensci.org/phylogram/reference/prune.md)
  remove branches from a `dendrogram` object based on regular expression
  pattern matching

- [`ladder`](https://docs.ropensci.org/phylogram/reference/ladder.md)
  reorders the branches of a `dendrogram` object to aid visualization

- [`remidpoint`](https://docs.ropensci.org/phylogram/reference/remidpoint.md)
  recursively sets "midpoint" and "members" attributes for a nested
  list/`dendrogram` object

- [`reposition`](https://docs.ropensci.org/phylogram/reference/reposition.md)
  shifts a `dendrogram` object up or down (or sideways if plotted
  horizontally)

- [`as.cladogram`](https://docs.ropensci.org/phylogram/reference/as.cladogram.md)
  modifies the "height" attributes of the nodes such that all leaves
  terminate at zero
