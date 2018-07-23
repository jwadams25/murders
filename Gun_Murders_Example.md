Gun Murders Example
================
John Adams
7/23/2018

R Markdown
==========

This is a sample R Markdown document generated while taking HarvardX: PH125.5x

Load Library and Dataset
========================

    ## ── Attaching packages ─────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
    ## ✔ tibble  1.4.2     ✔ dplyr   0.7.6
    ## ✔ tidyr   0.8.0     ✔ stringr 1.3.0
    ## ✔ readr   1.1.1     ✔ forcats 0.3.0

    ## Warning: package 'dplyr' was built under R version 3.4.4

    ## ── Conflicts ────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

Produce Visualizations
======================

### Visualization with code

This first example is one that produces the visualization with the code because it doesn't have echo=FALSE after murders.

``` r
murders %>% mutate(abb = reorder(abb,rate)) %>%
  ggplot(aes(abb, rate)) +
          geom_bar(width = 0.5, stat = "identity", color = "black") +
          coord_flip()
```

    ## Warning: package 'bindrcpp' was built under R version 3.4.4

![](Gun_Murders_Example_files/figure-markdown_github/murders%20plot%20no%20code-1.png)

### Visualization without code

The addition of echo = FALSE prevents code from showing up on the presentation. ![](Gun_Murders_Example_files/figure-markdown_github/pressure-1.png)
