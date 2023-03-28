Lab 10 - Grading the professor, Pt. 2
================
Lindsay Stall
3/28/2023

### Load packages and data

``` r
library(tidyverse) 
library(tidymodels)
library(openintro)
```

### Exercise 1

``` r
m_bty <- lm(score ~ bty_avg, data=evals)
summary(m_bty)
```

    ## 
    ## Call:
    ## lm(formula = score ~ bty_avg, data = evals)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -1.9246 -0.3690  0.1420  0.3977  0.9309 
    ## 
    ## Coefficients:
    ##             Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)  3.88034    0.07614   50.96  < 2e-16 ***
    ## bty_avg      0.06664    0.01629    4.09 5.08e-05 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.5348 on 461 degrees of freedom
    ## Multiple R-squared:  0.03502,    Adjusted R-squared:  0.03293 
    ## F-statistic: 16.73 on 1 and 461 DF,  p-value: 5.083e-05

y = 0.6664x + 3.88

R-squared: 0.03502 Adjusted R-squared: 0.03293

### Exercise 2

``` r
m_bty_gen <- lm(score ~ bty_avg + gender, data=evals)
```

``` r
summary(m_bty_gen)
```

    ## 
    ## Call:
    ## lm(formula = score ~ bty_avg + gender, data = evals)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -1.8305 -0.3625  0.1055  0.4213  0.9314 
    ## 
    ## Coefficients:
    ##             Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)  3.74734    0.08466  44.266  < 2e-16 ***
    ## bty_avg      0.07416    0.01625   4.563 6.48e-06 ***
    ## gendermale   0.17239    0.05022   3.433 0.000652 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.5287 on 460 degrees of freedom
    ## Multiple R-squared:  0.05912,    Adjusted R-squared:  0.05503 
    ## F-statistic: 14.45 on 2 and 460 DF,  p-value: 8.177e-07

y = 0.07416x + 0.17239z + 3.75

R-squared: 0.05912 Adjusted R-squared: 0.05503

### Exercise 3

Intercept = 3.7434, that would be the score if the beauty was 0 and the
gender was female .07416 is how much the score would go up for every 1
increase of beauty .17239 is the amount that male professors score
higher than females on average

### Exercise 4

The variability is 5.5503%

### Exercise 5

y= .07416x + (.17239 + 3.74734)

### Exercise 6

Males

### Exercise 7

Males will generally have higher scores

### Exercise 8

The adjusted r-squared for the equation with gender explains more
variance than without. In particular, adding it increases the variance
explained % by 22%.

### Exercise 9

Yeah, it raised by about .01

### Exercise 10

### Exercise 11

### Exercise 12

### Exercise 13

### Exercise 14

### Exercise 15

### Exercise 16

### Exercise 17

### Exercise 18
