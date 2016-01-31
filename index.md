---
title       : Calculating Calories in Food
subtitle    : Using Carbs, Protein and Fat
author      : Kevin Lessard
job         : Data Scientist
framework   : io2012      # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Overview

Calculating calories in food can be a confusing experience.  Although food labels contain total calories of a "suggested serving", what if you wanted to know the calories of a different (and sometimes more realistic) serving size.  I have created an app that calculates the total energy in food.

This calculator uses the information about grams of Carbohydrates, Proteins and Fats that you enter (and assumingly want to eat) and provides a total calorie result using these rates of calories/gram...

1. Carborhydrates - 4 calories/gram
2. Protein - 4 calories/gram
3. Fat - 9 calories/gram

Although different foods from these groups can have different calories per gram, the average will provide a good estimate.

--- .class #id 


## Logic Example

Here is an example of how the logic in the application works.


```r
carbs <- 16
protein <- 7
fat <-9

carbsKcal <- carbs *4
protKcal <-  protein *4
fatKcal <-   fat *9
totalKcal <- sum(carbsKcal,protKcal,fatKcal) 
fatPercnt <- (ffatKcal/totalKcal)*100
```

```
## Error in eval(expr, envir, enclos): object 'ffatKcal' not found
```

---

## Results



```r
carbsKcal
## [1] 64
protKcal
## [1] 28
fatKcal
## [1] 81
totalKcal
## [1] 173
fatPercnt
## [1] 46.82081
```


---

## Applications

This application would be a great addition to a website about nutrition, a mobile app that people could take grocery shopping or eating out, or for use by business at web kiosks to help their customers understand more about the food they are buying.





