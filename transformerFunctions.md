#Oct 1, 2013

## Reverser


```r
reverser <- function(x) {
    seperate = strsplit(as.character(x), split = character(0))
    seperate[[1]][nchar(x):1]
}
```

#test

```r
reverser("walter")
```

```
## [1] "r" "e" "t" "l" "a" "w"
```

```r
reverser("reverser")
```

```
## [1] "r" "e" "s" "r" "e" "v" "e" "r"
```



```r
scrambler <- function(x) {
    seperate = strsplit(as.character(x), split = character(0))
    randSeq = sample(1:nchar(x))
    seperate[[1]][randSeq[1:length(randSeq)]]
}
```

#test

```r
scrambler("walter")
```

```
## [1] "w" "r" "l" "a" "e" "t"
```

```r
scrambler("tomatoe")
```

```
## [1] "m" "t" "a" "e" "o" "o" "t"
```

