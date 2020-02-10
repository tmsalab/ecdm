
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ecdm

<!-- badges: start -->

[![Travis-CI Build
Status](https://travis-ci.org/tmsalab/ecdm.svg?branch=master)](https://travis-ci.org/tmsalab/ecdm)
[![Package-License](http://img.shields.io/badge/license-GPL%20\(%3E=2\)-brightgreen.svg?style=flat)](http://www.gnu.org/licenses/gpl-2.0.html)
[![CRAN Version
Badge](http://www.r-pkg.org/badges/version/edina)](https://cran.r-project.org/package=edina)
[![CRAN
Status](https://cranchecks.info/badges/worst/edina)](https://cran.r-project.org/web/checks/check_results_edina.html)
[![RStudio CRAN Mirror’s Monthly
Downloads](http://cranlogs.r-pkg.org/badges/edina?color=brightgreen)](http://www.r-pkg.org/pkg/edina)
[![RStudio CRAN Mirror’s Total
Downloads](http://cranlogs.r-pkg.org/badges/grand-total/edina?color=brightgreen)](http://www.r-pkg.org/pkg/edina)
<!-- badges: end -->

The goal of ecdm is to provide a modeling framework for exploratory
cognitive diagnostic models and classical cognitive diagnostic models.

## Installation

The `ecdm` package is currently only available via GitHub. To install
`ecdm`, your computer will need to have a compiler. The following guides
are avaliable:

  - [Windows:
    Rtools](http://thecoatlessprofessor.com/programming/installing-rtools-for-compiled-code-via-rcpp/)
  - [macOS:
    Rtools](http://thecoatlessprofessor.com/programming/r-compiler-tools-for-rcpp-on-macos/)

From there, please use `devtools` to retrieve the latest development
version.

``` r
# install.packages("devtools")
devtools::install_github("tmsalab/ecdm")
```

## Usage

Load the `ecdm` package into *R*:

``` r
library(ecdm)
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

These classical CDMs are implemented in separate packages: `dina` and
`rrum`.

## Details

The `ecdm` package is designed to act more as a “virtual” package. The
main functionalities of `ecdm` are split across multiple packages. The
rationale for this is many areas of psychometrics have overlap in terms
of computational code used. By dividing the underlying source of the
`ecdm` package, we are enabling fellow psychometricians to be able to
incorporate established routines into their own code. In addition, we
are lowering the amount of redundancies, or copy and pasted code, within
the CDM framework we are building.

Specifically, the `ecdm` package imports:

  - `dina`: Estimating the Deterministic Input, Noisy “And” Gate
    (‘DINA’) cognitive diagnostic model parameters using a Gibbs
    sampler.
  - `rrum`: Estimating the reduced Reparametrized Unified Model (‘rRUM’)
    with a Gibbs sampler.
  - `shinyecdm`: User Interface for Modeling with Exploratory Models
  - `simcdm`: Simulate responses underneath a DINA or rRUM model.
  - `rgen`: Simulate Multivariate Probability Distributions
  - `ecdmdata`: Data package containing psychometric modeling data used
    in multiple packages.

# License

GPL (\>= 2)
