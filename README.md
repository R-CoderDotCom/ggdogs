# ggdogs
The geom you always wished for adding dogs to ggplot2. This package is part of the memeverse.
The source code of this package is based on geom_image from ggimage.


<p align="center">
 <img src="https://user-images.githubusercontent.com/67192157/125283840-13c07680-e319-11eb-8344-389d6c45d4da.png">
</p>


+ Follow me on [Twitter](https://twitter.com/RCoderWeb)
+ Follow me on [Facebook](https://www.facebook.com/RCODERweb)
+ Visit my [R programming site](https://r-coder.com/)

## What is the memeverse?

A collection of funny packages which can be interesting to create plots to show on a first lesson to new R students in order to motivate them learning the language. The other package of the (small) memeverse are [ggcats](https://github.com/R-CoderDotCom/ggcats) and [ggbernie](https://github.com/R-CoderDotCom/ggbernie). Statistics and programming can be fun!

## Installation
```r
# install.packages("remotes")
remotes::install_github("R-CoderDotCom/ggdogs@main")
```


## Available dogs

There are 25 dogs available:

```r
"doge" (default) "doge_strong" "chihuahua" "eyes" "gabe" "glasses" "tail" "surprised"
"thisisfine" "hearing" "pug" "ears" "husky" "husky_2" "chilaquil"  "santa", "bryan",
"vinny" "jake" "lucy" "puppie" "goofy" "snoopy" "scooby" "suspicious"
```

## Some examples

```r
grid <- expand.grid(1:5, 3:1)

df <- data.frame(x = grid[, 1],
                 y = grid[, 2],
                 image = c("doge", "doge_strong", "chihuahua", "eyes", "gabe", "glasses", "tail", "surprised",
                           "thisisfine", "hearing", "pug", "ears", "husky", "husky_2", "chilaquil", "santa", "bryan", "vinny", "jake",
                           "lucy", "puppie", "goofy", "snoopy", "scooby", "suspicious"))
                           
library(ggplot2)
ggplot(df) +
 geom_dog(aes(x, y, dog = image), size = 5) +
 geom_label(aes(x, y - 0.25, label = image), size = 4) +
 xlim(c(0.25, 5.5)) + 
 ylim(c(0.25, 3.5))
```

<p align="center">
 <img src="https://user-images.githubusercontent.com/67192157/136852320-b2088483-a77b-45b8-855e-ec72e60b82c5.png">
</p>


```r
ggplot(mtcars) +
  geom_dog(aes(mpg, wt), dog = "doge_strong", size = 5)
```

<p align="center">
 <img src="https://user-images.githubusercontent.com/67192157/125281199-38671f00-e316-11eb-8dc3-48789ab1e511.png">
</p>


```r
ggplot(mtcars) +
  geom_dog(aes(mpg, wt, size = cyl), dog = "husky")
```

<p align="center">
 <img src="https://user-images.githubusercontent.com/67192157/125281261-4c128580-e316-11eb-9a2b-026545b0675f.png">
</p>




