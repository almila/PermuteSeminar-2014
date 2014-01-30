Borrelli Week 1 Notes
========================================================



```r
norm1 <- rnorm(100, 1, 3)
sampleMEAN <- mean(norm1)

boot <- matrix(nrow = 1000, ncol = 100)
for (i in 1:1000) {
    boot[i, ] <- sample(norm1, 100, replace = T)
}

meansBOOT <- rowMeans(boot)

hist(meansBOOT)
abline(v = sampleMEAN, col = "blue")
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 
