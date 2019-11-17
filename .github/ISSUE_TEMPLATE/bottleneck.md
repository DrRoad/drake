---
name: Bottleneck
about: drake is too slow or consumes too many resources.
title: ''
labels: 'topic: performance'
assignees: wlandau

---

## Prework

- [ ] Read and abide by `drake`'s [code of conduct](https://github.com/ropensci/drake/blob/master/CODE_OF_CONDUCT.md).
- [ ] Search for duplicates among the [existing issues](https://github.com/ropensci/drake/issues), both open and closed.
- [ ] Advanced users: verify that the bottleneck still persists in the current development version (i.e. `remotes::install_github("ropensci/drake")`) and mention the [SHA-1 hash](https://git-scm.com/book/en/v1/Getting-Started-Git-Basics#Git-Has-Integrity) of the [Git commit you install](https://github.com/ropensci/drake/commits/master).

## Description

Describe the bottleneck clearly and concisely. 

## Reproducible example

Provide a minimal reproducible example with code and output that demonstrates the problem. The `reprex()` function from the [`reprex`](https://github.com/tidyverse/reprex) package is extremely helpful for this.

To help us read your code, please try to follow the [tidyverse style guide](https://style.tidyverse.org/). The `style_text()` and `style_file()` functions from the [`styler`](https://github.com/r-lib/styler) package make it easier.

## Benchmarks

How poorly does `drake` perform? Please share benchmarks: runtimes, memory consumption, [flame graphs](https://github.com/ropensci/drake/issues/647#issuecomment-451760866), etc. Tools to consider:

- In development `drake`, `make(console_log_file = "log.txt")` now prepends sub-second time stamps to each line of `log.txt`. It is a super convenient way to see how fast things are going.
-  [`Rprof()`](https://stat.ethz.ch/R-manual/R-devel/library/utils/html/Rprof.html), [`jointprof`](https://github.com/r-prof/jointprof), [`profile`](https://github.com/r-prof/profile), and [`pprof`](https://github.com/google/pprof). [Example here](https://github.com/wlandau/drake-examples/tree/master/overhead).
- [`profvis`](https://github.com/rstudio/profvis), though beware https://github.com/rstudio/profvis/issues/104.
- [`microbenchmark`](https://github.com/joshuaulrich/microbenchmark) and [`bench`](https://github.com/r-lib/bench).
