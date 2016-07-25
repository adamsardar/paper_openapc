## About

The article is written in [R Markdown](http://rmarkdown.rstudio.com/). This
repository contains the datasets used as well as all data gathering methods and
analytical steps involved. Also bibliography and latex styles are shared.

Before generating the paper, make sure you have all R packages installed.

## Generate the paper

To replicate the analytical steps including tables and figures, execute the
article file via the command line interface:

```
Rscript -e "rmarkdown::render('article.Rmd')"
```

## Data collection methods used

### Open APC data-set

The script [R/aggregation.r](R/aggregation.r) contains the source code used
for enriching the original Open APC data.

The helper function [R/cr_parse](R/cr_parse.r) was used to parse the Crossref XML obtained with the great [rcrossref client](https://github.com/ropensci/rcrossref).

### Other cost data-sets

[data/cost_data_uk/README.md](data/cost_data_uk/README.md) tracks how we gathered the values for Table 2. Again, this notebook is written in R Markdown ([data/cost_data_uk/README.Rmd](data/cost_data_uk/README.Rmd))

## Meta

Please note that this project is released with a [Contributor Code of Conduct](https://github.com/njahn82/paper_openapc/blob/master/CONDUCT.md). By participating in this project you agree to abide by its terms.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
