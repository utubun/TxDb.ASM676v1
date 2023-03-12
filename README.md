
# TxDb.Paeruginosa.PAO1

<!-- badges: start -->
[![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

Annotation package for *Pseudomonas aeruginosa* str. PAO1. Data source: [NCBI](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/006/765/GCF_000006765.1_ASM676v1/).

## Installation

You can install the development version of TxDb.Paeruginosa.PAO1 like so:

``` r
devtools::install_github('utubun/TxDb.Paeruginosa.PAO1')
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(TxDb.Paeruginosa.PAO1)

pao1tx <- TxDb.Paeruginosa.PAO1

# show the information related to the build
pao1tx

# extract genes, as genomic ranges
gr <- GenomicFeatures::genes(pao1tx)

# show extracted ranges
gr

# convert gene ID into transcript names
head(
  (nm <- biomaRt::select(pao1tx, names(gr), 'TXNAME', 'GENEID'))
)
```

## More examples

``` r
methods(class = class(pao1tx))

help(package = 'GenomicFeatures')
```

