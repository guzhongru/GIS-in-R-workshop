# workflow
Xiao Feng  
October 12, 2016  

# Work with GIS data in R
## based on a workshop I tought in ? 


## 1. basic
Install and load libraries.


```r
# install.packages("rgdal") 
# install.packages("raster")
# install.packages("dismo")
library("rgdal") # this package is the basis of analyzing GIS data in R; for example, it handle basis coordinate systems, it defines a lot of spatial data types
library("raster")
library("dismo")
```

## 2. warm up 
R is pretty fun to use, let's plot some maps from one line of code

```r
require("XML")
# get a map of OK, you could type text that used to search on Google Maps
myMap <- gmap("oklahoma")
raster::plot(myMap)
```

![](report_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

```r
# try different text
plot(gmap("stillwater,OK")) # seems good
```

![](report_files/figure-html/unnamed-chunk-3-1.png)<!-- -->

```r
# get a snapshot of Walmart (satellite image)
plot(gmap("walmart,stillwater,OK",type = "satellite") )
```

![](report_files/figure-html/unnamed-chunk-4-1.png)<!-- -->

```r
# get a snapshot of Boomer Lake (satellite image)
plot(gmap("boomer lake,stillwater,OK",type = "satellite") )
```

![](report_files/figure-html/unnamed-chunk-5-1.png)<!-- -->


## references
1. Spatial data in R: Using R as a GIS <http://pakillo.github.io/R-GIS-tutorial/>
