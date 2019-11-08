#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) 
Regardless of what n is, given that each step will increase by n^2 times, the code will loop through n time until it reaches n^3. So increase in n will increase the runtime linearly.

b) O(n log n)
The other loop loops through n times, and the inner loop will loop log2 n times, since the j doubles every step (n is divided by 2 each time).

c) O(n)
The function is called recursively until n is 0 and each time, n decrements by 1. 

## Exercise II

I would use binary search to solve this problem. 

def broken_egg(arr):       #arr of size n with Boolean values 
    if len(arr) == 0:
      return -1
    
    low = 0
    high = len(arr) - 1
    
    while high >= low:
        midpoint = (high + low) // 2
        
        if high == low:
            return high + 1              #arr value starts at 1

        if arr[midpoint]:                #if egg broke is true
            high = midpoint - 1
        else: 
            low = midpoint + 1

The complexity would be ~ O(log n) because the length of the array is divided by 2 each time.