Title: Jitterplot
Slug: jitterplot
Summary: Jitterplot
Date: 2016-05-01 12:00
Category: R Stats
Tags: Data Visualization
Authors: Chris Albon

Want to learn more? I recommend working through: [R for Data Science](http://amzn.to/2myxnhi), [R Cookbook](http://amzn.to/2lF6hkb), and [R Graphics Cookbook](http://amzn.to/2m0fcPL).

```R
# load the ggplot2 library
library(ggplot2)

# set the seed so we can reproduce the results
set.seed(1410)
```


```R
# create a variable that is the first 100 rows of the diamonds dataset
dsmall <- diamonds[sample(nrow(diamonds), 100), ]
```


```R
# create a jitter plot that displays the price per carat varies with the colour of the diamond using jittering
qplot(color, price / carat, data = diamonds, geom = "jitter")
```









![png]({filename}/images/jitterplot_files/jitterplot_3_1.png)
