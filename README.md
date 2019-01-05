# An Easy Way to Generate '3'                   
My little nephew asked me what 'three' is and why '3' can be '3'. Bewildering but interesting!                   
Before some valuable insights lying at my mind, a retrospection of a limitation containing the formula sqrt(6) gave me some candies.         
<a href="https://www.codecogs.com/eqnedit.php?latex=lim_{n\rightarrow&space;\infty&space;}\underset{n\;times\;of\;&space;iterations&space;}{\sqrt{...\sqrt{6&plus;\sqrt{6&plus;\sqrt{6&plus;\sqrt{6}}}}}}=3" target="_blank"><img src="https://latex.codecogs.com/gif.latex?lim_{n\rightarrow&space;\infty&space;}\underset{n\;times\;of\;&space;iterations&space;}{\sqrt{...\sqrt{6&plus;\sqrt{6&plus;\sqrt{6&plus;\sqrt{6}}}}}}=3" title="lim_{n\rightarrow \infty }\underset{n\;times\;of\; iterations }{\sqrt{...\sqrt{6+\sqrt{6+\sqrt{6+\sqrt{6}}}}}}=3" /></a>              
                  
                  
Firstly we just verify this result by using R, with **k = k1 = 3**.               
```r
iteration <- function(p)  sqrt(6+p)
k <- sqrt(6)
k1 <- sqrt(6)
n <- c(1:10000)
for(i in n) {
  k <- iteration(k)
}
n1 <- c(1:1000000)
for(j in n1) {
  k1 <- iteration(k1)
}
```
Then we can figure out this result more algebraically.             

