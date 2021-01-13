---
title: "R Bridge Week 1 Assignment"
author: "Jacob George"
date: "12/20/2020"
---






#### Question#1: Write a loop that calculates 12-factorial 
```
a = 1
b = 1
for(a in 1:12){
  b = b * a
}
b
```

#### Question#2: Show how to create a numeric vector that contains the sequence from 20 to 50 by 5.
```
print("Sequence from 20 to 50:")
print(seq(20,50, by = 5))
```


#### Question#3: Create the function “quadratic” that takes a trio of input numbers a, b, and c and solve the quadratic equation. The function should  print as output the two solutions.
```
quadratic <- function(a,b,c){
  pos <- (-b + sqrt(b^2 - 4*a*c))/(2*a)
  neg <- (-b - sqrt(b^2 - 4*a*c))/(2*a)
  print(pos)
  print(neg)
}
quadratic (1,5,3) #Test 
```
















