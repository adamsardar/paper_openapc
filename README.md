## About

The article is written in [R Markdown](http://rmarkdown.rstudio.com/).
This repository contains the dataset used as well as all analytical steps
involved. Also bibliography and latex styles are available.

Before generating the paper, make sure you have all R packages installed.

## Generate the paper

On the command line interface, execute the article file:

```
Rscript -e "rmarkdown::render('article.Rmd')"
```

HTMl version (available through the `gh-pages` branch):

```
Rscript -e "rmarkdown::render('article.Rmd', output_format = 'html_document', output_file = 'index.html')"
```

Read html version: <http://njahn82.github.io/paper_openapc/>

## Meta

Please note that this project is released with a [Contributor Code of Conduct](https://github.com/njahn82/paper_openapc/blob/master/CONDUCT.md). By participating in this project you agree to abide by its terms.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
