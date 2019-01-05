# An Easy Way to Generate '3'                   
My little nephew asked me what 'three' is and why '3' can be '3'. Bewildering but interesting!                   
Before some valuable insights lying at my mind, a retrospection of a limitation containing the formula sqrt(6) gave me some candies.         
<a href="https://www.codecogs.com/eqnedit.php?latex=lim_{n\rightarrow&space;\infty&space;}\underset{n\;times\;of\;&space;iterations&space;}{\sqrt{...\sqrt{6&plus;\sqrt{6&plus;\sqrt{6&plus;\sqrt{6}}}}}}=3" target="_blank"><img src="https://latex.codecogs.com/gif.latex?lim_{n\rightarrow&space;\infty&space;}\underset{n\;times\;of\;&space;iterations&space;}{\sqrt{...\sqrt{6&plus;\sqrt{6&plus;\sqrt{6&plus;\sqrt{6}}}}}}=3" title="lim_{n\rightarrow \infty }\underset{n\;times\;of\; iterations }{\sqrt{...\sqrt{6+\sqrt{6+\sqrt{6+\sqrt{6}}}}}}=3" /></a>              
                  
                  
Firstly we just verify this result by using R, with **k = k1 = 3**. But we can witness some errors in the following code.                  
```r
iteration <- function(p)  sqrt(6+p)
k <- sqrt(6)
k1 <- sqrt(6)
n <- c(1:10000)
for(i in n) {
  k <- function(k)
}
n1 <- c(1:1000000)
for(j in n1) {
  k1 <- function(k1)
}
```
It would be diagnosed in the console that some errors happen with the unexpected "}" in the for loop. But if we make some revises without using the function, it would come up with the correct answer **k = k1 = 3**.     
```r
k <- sqrt(6)
k1 <- sqrt(6)
n <- c(1:10000)
for(i in n) {
  k <- sqrt(6+k)
}

n1 <- c(1:1000000)
for(j in n1) {
  k1 <- sqrt(6+k1)
}    
```
