# carnegiecolors
Contains code for R package with R color palettes inspired by Carnegie Mellon University.
Code adopted from the lovely `inauguration` R package by Cianna Bedford-Petersen, available [here](https://github.com/ciannabp/inauguration). 

# R package installation
Install the  `carnegiecolors` R package using the following code:
``` r
#install.packages("devtools")
devtools::install_github("kimhochstedler/carnegiecolors", ref="main")
library(carnegiecolors)
```

# Using the carnegiecolors package
Use the `names` function to view the available color palettes.
```r
names(carnegie_palettes)
#> [1] "classic"   "secondary" "accents"   "malott"    "brb" 
```

Call the palette using the `render_cornell_colors` function
```r
render_cornell_colors("classic")
```
![](classic.png)

View a subset of the secondary color scheme
```r
render_cornell_colors("secondary", 5)
```
![](secondary.png)

Use colors from `carnegie_palettes` in your graphs
```r
set.seed(1)
hist(rnorm(n = 100, mean = 0, sd = 1), col = carnegie_palettes[["campus"]][4])
```
![](carnegie_histogram.png)
