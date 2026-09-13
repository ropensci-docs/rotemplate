# Build rOpenSci docs sites

Wrapper for
[pkgdown::build_site](https://pkgdown.r-lib.org/reference/build_site.html)
that we use to build the websites for `https://docs.ropensci.org`. Sets
a theme and logo, checks if mathjax is required, and injects a logo into
the readme if needed.

## Usage

``` r
build_ropensci_docs(
  path = ".",
  destination = NULL,
  install = FALSE,
  preview = interactive(),
  ...
)
```

## Arguments

- path:

  path to package source directory

- destination:

  path where to save the docs website

- install:

  passed to
  [pkgdown::build_site](https://pkgdown.r-lib.org/reference/build_site.html).
  Default is to *not* reinstall the package.

- preview:

  preview the website (servr will be used)

- ...:

  passed to
  [pkgdown::build_site](https://pkgdown.r-lib.org/reference/build_site.html)

## Details

Note the default behavior is to render the docs using the installed
package, i.e. not reinstall the package on the fly (which does not
always work well). In production, we manually install the package before
running `build_ro_site`.
