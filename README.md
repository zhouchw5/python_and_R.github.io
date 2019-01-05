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
Then we can figure out this result more algebraically by using the middle school knowledge.                       
<a href="https://www.codecogs.com/eqnedit.php?latex=x_1&space;=&space;\sqrt{6}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_1&space;=&space;\sqrt{6}" title="x_1 = \sqrt{6}" /></a>, 
<a href="https://www.codecogs.com/eqnedit.php?latex=x_2&space;=&space;\sqrt{6&plus;\sqrt{6}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_2&space;=&space;\sqrt{6&plus;\sqrt{6}}" title="x_2 = \sqrt{6+\sqrt{6}}" /></a>, 
<a href="https://www.codecogs.com/eqnedit.php?latex=x_3&space;=&space;\sqrt{6&plus;\sqrt{6&plus;\sqrt{6}}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_3&space;=&space;\sqrt{6&plus;\sqrt{6&plus;\sqrt{6}}}" title="x_3 = \sqrt{6+\sqrt{6+\sqrt{6}}}" /></a>, 
...,  we can find the recurrence relation <a href="https://www.codecogs.com/eqnedit.php?latex=x_{n&plus;1}^2-x_{n}=6" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_{n&plus;1}^2-x_{n}=6" title="x_{n+1}^2-x_{n}=6" /></a>.        
We set 
<a href="https://www.codecogs.com/eqnedit.php?latex=x_{n}=k" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_{n}=k" title="x_{n}=k" /></a>, 
and 
<a href="https://www.codecogs.com/eqnedit.php?latex=x_{n&plus;1}=\sqrt{6&plus;k}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_{n&plus;1}=\sqrt{6&plus;k}" title="x_{n+1}=\sqrt{6+k}" /></a>, 
interested in the difference 
<a href="https://www.codecogs.com/eqnedit.php?latex=(6&plus;k-k^2)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?(6&plus;k-k^2)" title="(6+k-k^2)" /></a>.            
After solving the quadratic equation 
<a href="https://www.codecogs.com/eqnedit.php?latex=(k^2-k-6)=0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?(k^2-k-6)=0" title="(k^2-k-6)=0" /></a>, 
we can find that when 
<a href="https://www.codecogs.com/eqnedit.php?latex=k&space;\in&space;\left&space;(0,&space;3&space;\right&space;]" target="_blank"><img src="https://latex.codecogs.com/gif.latex?k&space;\in&space;\left&space;(0,&space;3&space;\right&space;]" title="k \in \left (0, 3 \right ]" /></a>, 
<a href="https://www.codecogs.com/eqnedit.php?latex=x_{n&plus;1}\geq&space;x_{n}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_{n&plus;1}\geq&space;x_{n}" title="x_{n+1}\geq x_{n}" /></a>; 
and 
<a href="https://www.codecogs.com/eqnedit.php?latex=k\in&space;\left&space;(&space;3,&space;&plus;\infty&space;\right&space;)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?k\in&space;\left&space;(&space;3,&space;&plus;\infty&space;\right&space;)" title="k\in \left ( 3, +\infty \right )" /></a>, 


