---
title: convertr tutorial
package_version: 0.1
---



An R package for converting things to other things.

The package contains one function which converts numerical vectors from one unit to another. Data on conversion factors comes from the [POSC Units of Measure Dictionary v2.2](http://w3.energistics.org/uom/poscUnits22.xml) and [Wikipedia](https://en.wikipedia.org/wiki/Conversion_of_units).


### Installation

Stable version from CRAN


```r
install.packages("convertr")
```


Development version from GitHub


```r
if (!require("devtools")) install.packages("devtools")
devtools::install_github("ropenscilabs/convertr")
```


```r
library("convertr")
```


### Usage


```r
convert(1:20, "kg", "g")
convert(1:20, "sq yd", "km2")

#This will produce an error:
convert(1:20, "kg", "km2)
```

Units are converted using a lookup table, based on the POSC dictionary. You can explore this table using the `explore_units()` function. This function launches a shiny app.

Figuring out which units can be converted to each other can be tricky, so convertr comes with an an shiny gadget to help you build valid `convert()` expressions. This can be accesed either by calliing `convert_gadget()` or through the addin menu. To access the addin make sure you are using a recent version of RStudio.

![Gadget Animation](/img/tutorial-images/convertr/convertr_gif.gif)

### Citing

> Gordon Shotwell (2016). convertr: Convert Between Units. R package version 0.1. https://github.com/ropenscilabs/convertr


### License and bugs

* License: [MIT](http://opensource.org/licenses/MIT)
* Report bugs at [our GitHub repo for convertr](https://github.com/ropenscilabs/convertr/issues?state=open)


[Back to top](#top)
