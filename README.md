
<!-- README.md is generated from README.Rmd. Please edit that file -->

# edm

<!-- badges: start -->

[![R build
status](https://github.com/tmsalab/edm/workflows/R-CMD-check/badge.svg)](https://github.com/tmsalab/edm)
[![Package-License](http://img.shields.io/badge/license-GPL%20(%3E=2)-brightgreen.svg?style=flat)](http://www.gnu.org/licenses/gpl-2.0.html)
<!-- badges: end -->

The goal of edm is to provide a modeling framework for exploratory
diagnostic models and classical diagnostic models.

## Installation

The `edm` package is currently only available via GitHub. To install
`edm`, your computer will need to have a compiler. The following guides
are avaliable:

-   [Windows:
    Rtools](http://thecoatlessprofessor.com/programming/installing-rtools-for-compiled-code-via-rcpp/)
-   [macOS:
    Rtools](http://thecoatlessprofessor.com/programming/r-compiler-tools-for-rcpp-on-macos/)

From there, please use `devtools` to retrieve the latest development
version.

``` r
if(!requireNamespace("remotes", quietly = TRUE)) install.packages("remotes")
remotes::install_github("tmsalab/edm")
```

## Usage

Load the `edm` package into *R*:

``` r
library(edm)
```

Exploratory CDM models can be estimated with:

``` r
edina_model = edina(<data>, <k>)
errum_model = errum(<data>, <k>, ... )
```

Classical CDMs can be estimated using:

``` r
dina_model = dina(<data>, <q>)
rrum_model = rrum(<data>, <q>)
```

## Details

The `edm` package is designed to act more as a “virtual” package. The
main functionalities of `edm` are split across multiple packages. The
rationale for this is many areas of psychometrics have overlap in terms
of computational code used. By dividing the underlying source of the
`edm` package, we are enabling fellow psychometricians to be able to
incorporate established routines into their own code. In addition, we
are lowering the amount of redundancies, or copy and pasted code, within
the CDM framework we are building.

Specifically, the `edm` package imports estimation routines from:

-   `dina`: Estimating the Deterministic Input, Noisy “And” Gate
    (‘DINA’) cognitive diagnostic model parameters using a Gibbs
    sampler.
-   `edina`: Estimating the Exploratory Deterministic Input, Noisy “And”
    Gate (‘EDINA’) cognitive diagnostic model parameters using a Gibbs
    sampler.
-   `rrum`: Estimating the reduced Reparametrized Unified Model (‘rRUM’)
    with a Gibbs sampler.
-   `errum`: Estimating the Exploratory reduced Reparametrized Unified
    Model (‘ErRUM’) with a Gibbs sampler.

Moreover, we have additional packages that are used within the modeling
process:

-   `rgen`: Simulate Multivariate Probability Distributions
-   `simcdm`: Simulate responses underneath a DINA or rRUM model.
-   `shinyedm`: User Interface for Modeling with Exploratory Models

Lastly, we have sampled data packages available here:

-   `edmdata`: Data package containing psychometric modeling data used
    in multiple packages.

## Authors

James Joseph Balamuta, Steven Andrew Culpepper, and Jeffrey A. Douglas

## Citing the `edm` package

To ensure future development of the package, please cite `edm` package
if used during an analysis or simulation studies. Citation information
for the package may be acquired by using in *R*:

``` r
citation("edm")
```

## License

GPL (&gt;= 2)
