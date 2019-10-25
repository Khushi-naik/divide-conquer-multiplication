# divide-conquer-multiplication
multiplication of long numbers.

#Complexity of Karatsuba
To analyze the complexity of the Karatsuba algorithm, consider the number of multiplications the algorithm performs as a function of nn, M(n)M(n). Recall that the algorithm multiplies together two nn-bit numbers. If n=2^kn=2 
k
  for some kk, then the algorithm recurses three times on \frac{n}{2} 
2
n
​	
 -bit number. The recurrence for this is

M(n) = 3M\left(\frac{n}{2}\right).
M(n)=3M( 
2
n
​	
 ).
This takes care of the multiplications required for Karatsuba--now to consider the additions and subtractions. There are O(n)O(n) additions and subtractions required for the algorithm. Therefore, the overall recurrence for the Karatsuba algorithm is[2]

T(n) = 3T\left(\frac{n}{2}\right) + O(n).
T(n)=3T( 
2
n
​	
 )+O(n).

Using the master theorem on the above recurrence yields that the running time of the Karatsuba algorithm is \Theta\big(n^{\log_2 3}\big)\approx \Theta\big(n^{1.585}\big).Θ(n 
log 
2
​	
 3
 )≈Θ(n 
1.585
 ).

The Schönhage–Strassen algorithm and the Toom–Cook algorithm are other popular integer multiplication algorithms. The Toom-Cook algorithm is faster, more generalized version of the Karatsuba algorithm that runs in \Theta\left(n^{\frac{\log 5}{\log 3}}\right) \approx \Theta\big(n^{1.465}\big)Θ(n 
log3
log5
​	
 
 )≈Θ(n 
1.465
 ).[3] The Schönhage–Strassen algorithm is faster than both Karatsuba and Toom-Cook for very large nn \big((on the order of n > 2^{2^{15}}\big)n>2 
2 
15
 
 ) and runs in O(n \log n \log \log n)O(nlognloglogn).[4]

See Also