# pkgdown

[![Travis-CI Build Status](https://travis-ci.org/hadley/pkgdown.svg?branch=master)](https://travis-ci.org/hadley/pkgdown)
[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/pkgdown)](https://cran.r-project.org/package=pkgdown)

pkgdown is designed to make it quick and easy to build a website for your package. You can see pkgdown in action at <http://hadley.github.io/pkgdown/>: this is the output of pkgdown applied to the latest version of pkgdown. Learn more in `vignette("pkgdown")` or `?build_site`.

## Installation

pkgdown is not currently available from CRAN, but you can install the development version from github with:

```R
# install.packages("devtools")
devtools::install_github("hadley/pkgdown")
```

## Usage

Run pkgdown from the package directory each time you release your package:

```R
pkgdown::build_site()
```

This will generate a `docs/` directory. The home page will be generated from your package's `README.md`, and a function reference will be generated from the documentation in the `man/` directory. If you are using GitHub, the easiest way to make this your package website is to check into git, then go settings for your repo and make sure that the __GitHub pages__ source is set to "master branch /docs folder".

The package also includes an RStudio add-in which you can bind to a keyboard shortcut. I recommend `Cmd + Shift + W`: it uses Cmd + Shift, like all other package development worksheets, it replaces a rarely used command (close all tabs), and the W is mnemonic for website.
