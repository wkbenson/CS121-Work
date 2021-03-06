Functions and Graphics
===========================================================

Functions
-------------------------------------------------
### Function countOdds

```r
countOdds <- function(n) {
    return(sum(n%%2))
}
```

#### Test countOdds

```r
countOdds(1:9)
```

```
## [1] 5
```

```r
countOdds(c(3, 5, 7))
```

```
## [1] 3
```

```r
countOdds(c(3, 5, 7, 6, 2, 0))
```

```
## [1] 3
```

### Function countEvens

```r
countEvens <- function(n) {
    x <- length(n)
    y <- sum(n%%2)
    return(x - y)
}
```

#### Test countEvens

```r
countEvens(c(1, 2, 3, 4, 5, 6, 7, 8))
```

```
## [1] 4
```

```r
countEvens(c(2, 2, 2, 2, 3, 3, 3, 3))
```

```
## [1] 4
```

```r
countEvens(c(1, 1, 1, 2, 4))
```

```
## [1] 2
```

### Function hypotenusLength

```r
hypotenusLength <- function(a, b) return(sqrt(a^2 + b^2))
```

#### Test hypotenusLength

```r
hypotenusLength(3, 4)
```

```
## [1] 5
```

```r
hypotenusLength(13, 84)
```

```
## [1] 85
```

### Function lawOfCosines

```r
lawOfCosines <- function(a, b, theta) {
    c <- sqrt(a^2 + b^2 - 2 * a * b * cos(theta))
    return(c)
}
```

#### Test lawOfCosines

```r
lawOfCosines(13, 84, pi/2)
```

```
## [1] 85
```

```r
lawOfCosines(13, 84, 0)
```

```
## [1] 71
```

```r
lawOfCosines(5, 5, pi/3)
```

```
## [1] 5
```

### Function thetaFromLengths

```r
thetaFromLengths <- function(a, b, c) {
    theta <- acos((c^2 - (a^2 + b^2))/-a * b)
    return(theta)
}
```

#### Test thetaFromLengths

```r
thetaFromLengths(3, 4, 5)
```

```
## [1] 1.571
```

### Function thetaFromLengthsTest

```r
thetaFromLengthsTest <- function(a, b, theta) {
    c <- lawOfCosines(a, b, theta)
    testTheta <- thetaFromLengths(a, b, c)
    return(theta - testTheta)
}
```

#### Test thetaFromLengthsTest

```r
thetaFromLengthsTest(3, 4, pi/2)
```

```
## [1] 0
```

Graphics
---------------------------------------------
### Canvas

```r
canvas <- function(x, y) plot(1, 1, type = "n", xlim = c(0, x), ylim = c(0, 
    y), asp = 1)
```

### Circles

```r
drawCircle <- function(x, y, r, c = NULL, d = NULL, b = NULL) {
    xPoint <- cos(seq(0, (2 * pi), by = 0.1))
    yPoint <- sin(seq(0, (2 * pi), by = 0.1))
    polygon(x + (r * xPoint), y + (r * yPoint), col = c, density = d, border = b)
}
canvas(50, 50)
drawCircle(25, 25, 10)
drawCircle(10, 25, 10, c = "dark blue")
```

![plot of chunk unnamed-chunk-14](figure/unnamed-chunk-14.png) 


### Olympic rings

```r
canvas(100, 100)
drawCircle(50, 60, 10, c = "black")
drawCircle(50, 60, 7, c = "white")
drawCircle(39, 50, 10, c = "yellow")
drawCircle(39, 50, 7, c = "white")
drawCircle(29, 60, 10, c = "blue")
drawCircle(29, 60, 7, c = "white")
drawCircle(61, 50, 10, c = "green")
drawCircle(61, 50, 7, c = "white")
drawCircle(71, 60, 10, c = "red")
drawCircle(71, 60, 7, c = "white")
```

![plot of chunk unnamed-chunk-15](figure/unnamed-chunk-15.png) 

```r

```


